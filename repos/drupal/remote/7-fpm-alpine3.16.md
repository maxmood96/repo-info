## `drupal:7-fpm-alpine3.16`

```console
$ docker pull drupal@sha256:ae77a5c2ef86de691766d6db5afe0f15b22be97fdbd5be4eb41eae7b4d4f8f29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `drupal:7-fpm-alpine3.16` - linux; amd64

```console
$ docker pull drupal@sha256:3888192d0c925100228b352a33ec92bce87063c44dea5fb7f05a0708703c05df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.5 MB (35490847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7be47673a3f1a9b494615c33f9a5ce68493883e7840cafb56a4087181d3e875a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:28 GMT
ADD file:970e6b2578ef73457ffed1189e8ba128b0211cabd3174b8c7d3afd8fb58ad614 in / 
# Wed, 29 Mar 2023 18:19:28 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 22:51:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 29 Mar 2023 22:51:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 29 Mar 2023 22:51:59 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 29 Mar 2023 22:51:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 29 Mar 2023 22:51:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 29 Mar 2023 22:51:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 Mar 2023 22:51:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 Mar 2023 22:51:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 29 Mar 2023 23:28:19 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Fri, 09 Jun 2023 02:25:34 GMT
ENV PHP_VERSION=8.0.29
# Fri, 09 Jun 2023 02:25:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.29.tar.xz.asc
# Fri, 09 Jun 2023 02:25:34 GMT
ENV PHP_SHA256=14db2fbf26c07d0eb2c9fab25dbde7e27726a3e88452cca671f0896bbb683ca9
# Fri, 09 Jun 2023 02:25:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 09 Jun 2023 02:25:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 09 Jun 2023 02:33:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 09 Jun 2023 02:33:25 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 09 Jun 2023 02:33:26 GMT
RUN docker-php-ext-enable sodium
# Fri, 09 Jun 2023 02:33:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jun 2023 02:33:26 GMT
WORKDIR /var/www/html
# Fri, 09 Jun 2023 02:33:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 09 Jun 2023 02:33:27 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Jun 2023 02:33:27 GMT
EXPOSE 9000
# Fri, 09 Jun 2023 02:33:27 GMT
CMD ["php-fpm"]
# Fri, 09 Jun 2023 03:36:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Fri, 09 Jun 2023 03:36:40 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 09 Jun 2023 03:40:04 GMT
ENV DRUPAL_VERSION=7.98
# Fri, 09 Jun 2023 03:40:04 GMT
ENV DRUPAL_MD5=4139f0feecb44a53645242194809b73a
# Fri, 09 Jun 2023 03:40:05 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes
```

-	Layers:
	-	`sha256:91d30c5bc19582de1415b18f1ec5bcbf52a558b62cf6cc201c9669df9f748c22`  
		Last Modified: Wed, 29 Mar 2023 18:20:09 GMT  
		Size: 2.8 MB (2807803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f977684c5326656755ba69adab7c1989451954daad61e400152c14db3b58191`  
		Last Modified: Wed, 29 Mar 2023 23:42:40 GMT  
		Size: 1.7 MB (1721496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f96bd6a4095a15cb294111d5e4b59369b0f8a7bfaf385564da3c3e38c3c2335`  
		Last Modified: Wed, 29 Mar 2023 23:42:39 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b846eb5992b401350c0a6de95336db96189d8d64ffaaad47d983c487ea3ebdf`  
		Last Modified: Wed, 29 Mar 2023 23:42:39 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5b348997471ffe1db9657d50e3484f6ce9d40e1835e363e75bfa1b693d6859`  
		Last Modified: Fri, 09 Jun 2023 02:55:12 GMT  
		Size: 10.8 MB (10823746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb7f43eb815f968f06031ab48735c3c51a3ffa0a6e937aba4cb58b37f0e804b`  
		Last Modified: Fri, 09 Jun 2023 02:55:11 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a3c2fd4cf23d48aac0276b85170efa9ecaf292641626d05c4fff8f1b97c125`  
		Last Modified: Fri, 09 Jun 2023 02:55:37 GMT  
		Size: 14.3 MB (14348714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b501b980ea245d13a017e51d52fa8c9bfd897a333dd61b8d708378c16b62b20d`  
		Last Modified: Fri, 09 Jun 2023 02:55:34 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5092502ef145e0db8c444dd38f3f54cfaf3ab45f6a80ff6f979e4d960f8b05ac`  
		Last Modified: Fri, 09 Jun 2023 02:55:34 GMT  
		Size: 18.8 KB (18797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb233535ce8da5c495f3fe139574295b53699b2e17b1ae1a3384543a2e63f59`  
		Last Modified: Fri, 09 Jun 2023 02:55:34 GMT  
		Size: 8.7 KB (8713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ad165f5715c10508546550b3b5043b7c3d1faaa634747e63be56b89f996ab0`  
		Last Modified: Fri, 09 Jun 2023 03:53:39 GMT  
		Size: 2.3 MB (2345650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0ed6a7dd20b402bedc11a531f7cd97d43996d9abe25aa5eeded067266bb470`  
		Last Modified: Fri, 09 Jun 2023 03:53:38 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d992f819843f70d497613e3ef05f6ecece94f680c8553ca0fb4529e3de6fdda`  
		Last Modified: Fri, 09 Jun 2023 03:59:02 GMT  
		Size: 3.4 MB (3411147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:7-fpm-alpine3.16` - linux; arm variant v6

```console
$ docker pull drupal@sha256:0131d0ee987400397d0f264773413a457887e5307a59bec4de06d41b0902af39
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.1 MB (32072680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01dfd99fd27b1f4bbbd90658ee745dc25c1869f4e370c371d29bfe6744d9a61e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:11 GMT
ADD file:c5e68ad58a515830d33f20488adffa6af47be2e332543c747b8931cab7444e59 in / 
# Wed, 29 Mar 2023 18:01:11 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 21:22:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 29 Mar 2023 21:22:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 29 Mar 2023 21:22:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 29 Mar 2023 21:22:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 29 Mar 2023 21:22:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 29 Mar 2023 21:22:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 Mar 2023 21:22:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 Mar 2023 21:22:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 29 Mar 2023 21:22:07 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Fri, 09 Jun 2023 01:19:55 GMT
ENV PHP_VERSION=8.0.29
# Fri, 09 Jun 2023 01:19:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.29.tar.xz.asc
# Fri, 09 Jun 2023 01:19:55 GMT
ENV PHP_SHA256=14db2fbf26c07d0eb2c9fab25dbde7e27726a3e88452cca671f0896bbb683ca9
# Fri, 09 Jun 2023 01:20:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 09 Jun 2023 01:20:02 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:27:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 09 Jun 2023 01:27:51 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:27:53 GMT
RUN docker-php-ext-enable sodium
# Fri, 09 Jun 2023 01:27:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jun 2023 01:27:53 GMT
WORKDIR /var/www/html
# Fri, 09 Jun 2023 01:27:53 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 09 Jun 2023 01:27:54 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Jun 2023 01:27:54 GMT
EXPOSE 9000
# Fri, 09 Jun 2023 01:27:54 GMT
CMD ["php-fpm"]
# Fri, 09 Jun 2023 02:04:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Fri, 09 Jun 2023 02:04:45 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 09 Jun 2023 02:06:15 GMT
ENV DRUPAL_VERSION=7.98
# Fri, 09 Jun 2023 02:06:15 GMT
ENV DRUPAL_MD5=4139f0feecb44a53645242194809b73a
# Fri, 09 Jun 2023 02:06:17 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes
```

-	Layers:
	-	`sha256:c4ddbcc13e08e4ef30f810d8afad41fd6994bd8af7d37746d0ea33d8813968fc`  
		Last Modified: Wed, 29 Mar 2023 18:02:04 GMT  
		Size: 2.6 MB (2616846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f445ee3888b2a7a18fe767d16071cfdea3155d0932b5e99bf409ec4e9a5dbafd`  
		Last Modified: Tue, 04 Apr 2023 00:27:31 GMT  
		Size: 1.7 MB (1708402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:054954c7f81b0b78f5476d73502ad54e34473893b5ee827ef57ba5cf938cad32`  
		Last Modified: Tue, 04 Apr 2023 00:27:31 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a032fb52ae7cff625afd1f9ab9219ec4a06bda54cbd7c4ca26ca4458adc73c1`  
		Last Modified: Tue, 04 Apr 2023 00:27:31 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9888ec55572644cbaf2f4b38b85c9919988a1acfda46b9471d9610d549dafb8f`  
		Last Modified: Fri, 09 Jun 2023 01:38:50 GMT  
		Size: 10.8 MB (10823740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6bee3a6434b3faae0801283c062522ad05bf874a5cf8a633bf76631ffa7c2b`  
		Last Modified: Fri, 09 Jun 2023 01:38:48 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16814266d7b30829fc705af04c54a99a84ab6d3a3c3d58906ac1cdeee75086ae`  
		Last Modified: Fri, 09 Jun 2023 01:39:17 GMT  
		Size: 11.7 MB (11653012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c3bf347b550350f5202cd1aee6b20f7afb511a7c35837994c33dcfced727ddb`  
		Last Modified: Fri, 09 Jun 2023 01:39:14 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54df09cd5ea9e96fe36abce3610b070698ad846eb5a256f89f1d06a726e56d37`  
		Last Modified: Fri, 09 Jun 2023 01:39:14 GMT  
		Size: 18.7 KB (18744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0741fcacba9f1a7812931d98d560b209151a8ecf7256bf2938ae97b81d5a6cc8`  
		Last Modified: Fri, 09 Jun 2023 01:39:14 GMT  
		Size: 8.7 KB (8715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441c0cc69f6e81f5fb5f4c363cecef8c9a769ad073415e19f69229c384c47a7b`  
		Last Modified: Fri, 09 Jun 2023 02:10:10 GMT  
		Size: 1.8 MB (1827280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1b1da8439188899e4a17026a514d7c82c91881a8c4b0cd286bb0d1f82e78059`  
		Last Modified: Fri, 09 Jun 2023 02:10:10 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea929411be409bffe9a91dc2349e4fcbc4418134d34b98b1dc0d6cf12967fa4`  
		Last Modified: Fri, 09 Jun 2023 02:11:35 GMT  
		Size: 3.4 MB (3411150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:7-fpm-alpine3.16` - linux; arm variant v7

```console
$ docker pull drupal@sha256:e4cfa2f8b7a708971be725955773eac22b814ae33766e21aafbe7861a3e88277
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.3 MB (30257588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ffa267dca05dda30d601f59fb8ad5aff24852e0a9ee382e9f8ece42d7dc9c8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 29 Mar 2023 18:04:21 GMT
ADD file:68992157dbe7c3a454c26656c7bcb497794c1008ead5e078b2928ce165cd65cd in / 
# Wed, 29 Mar 2023 18:04:21 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 23:07:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 29 Mar 2023 23:07:42 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 29 Mar 2023 23:07:42 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 29 Mar 2023 23:07:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 29 Mar 2023 23:07:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 29 Mar 2023 23:07:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 Mar 2023 23:07:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 Mar 2023 23:07:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 29 Mar 2023 23:55:53 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Wed, 29 Mar 2023 23:55:54 GMT
ENV PHP_VERSION=8.0.28
# Wed, 29 Mar 2023 23:55:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.28.tar.xz.asc
# Wed, 29 Mar 2023 23:55:54 GMT
ENV PHP_SHA256=5e07278a1f315a67d36a676c01343ca2d4da5ec5bdb15d018e4248b3012bc0cd
# Wed, 29 Mar 2023 23:56:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 29 Mar 2023 23:56:01 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 30 Mar 2023 00:01:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 30 Mar 2023 00:01:32 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 30 Mar 2023 00:01:33 GMT
RUN docker-php-ext-enable sodium
# Thu, 30 Mar 2023 00:01:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 30 Mar 2023 00:01:33 GMT
WORKDIR /var/www/html
# Thu, 30 Mar 2023 00:01:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 30 Mar 2023 00:01:34 GMT
STOPSIGNAL SIGQUIT
# Thu, 30 Mar 2023 00:01:34 GMT
EXPOSE 9000
# Thu, 30 Mar 2023 00:01:34 GMT
CMD ["php-fpm"]
# Fri, 31 Mar 2023 23:36:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Fri, 31 Mar 2023 23:36:29 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 21 Apr 2023 20:50:59 GMT
ENV DRUPAL_VERSION=7.97
# Fri, 21 Apr 2023 20:51:00 GMT
ENV DRUPAL_MD5=37b63299e115a9e8863f564780a026e9
# Fri, 21 Apr 2023 20:51:01 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes
```

-	Layers:
	-	`sha256:d378ffb313542b797defad9ec843de710c353f40e17e124e74f7e874971429ee`  
		Last Modified: Wed, 29 Mar 2023 18:07:08 GMT  
		Size: 2.4 MB (2420546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86d13d590903b10a3f8afa44f0996831af1c87877a282d4f5693f411c1936c2`  
		Last Modified: Fri, 31 Mar 2023 23:10:36 GMT  
		Size: 1.6 MB (1575757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f246394a2a9a0a02da9af8d29d2d625795b7ef20518c632577b83a33b0ed950`  
		Last Modified: Fri, 31 Mar 2023 23:10:36 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:776b670052ddf86d4fc58a1b78dd450b39c5fe07107d1fe6c15dae8fe238b719`  
		Last Modified: Fri, 31 Mar 2023 23:10:36 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a89b2c5c4a4bd367f10b4e98739df08fc67a93051d54904361392267e6c03493`  
		Last Modified: Fri, 31 Mar 2023 23:13:08 GMT  
		Size: 10.8 MB (10821683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:357b8eec6255ece63a9ade824098da1c6bfd35ad9995d092404c7012ffbbdf6e`  
		Last Modified: Fri, 31 Mar 2023 23:13:07 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86956f09a3631f49f092f1baec7b45ca3a4bf6473af8ed3bd18d8ec92cf315de`  
		Last Modified: Fri, 31 Mar 2023 23:13:31 GMT  
		Size: 10.3 MB (10332275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:135ae6f621c763d86136452db5024fa1e23732469f38cd7f0fa8cd00a94c2441`  
		Last Modified: Fri, 31 Mar 2023 23:13:29 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c7a5e1c2cd722e5d0cdbe9ec9136e6a244641765bf16a367319923024fca681`  
		Last Modified: Fri, 31 Mar 2023 23:13:29 GMT  
		Size: 18.6 KB (18642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7abee795f9728dd2fd05e26117e66f9c315a556fa02c162da402996fd1145c85`  
		Last Modified: Fri, 31 Mar 2023 23:13:29 GMT  
		Size: 8.7 KB (8709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465a69874946e78a17d6db84bc4dac6dbb9d399b17eccb8659ea9cb3f9c63e84`  
		Last Modified: Fri, 31 Mar 2023 23:43:05 GMT  
		Size: 1.7 MB (1671365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7446fe53fb19007b9727768a772326e6e2279c31647aaff96c047dc52b5a8d7f`  
		Last Modified: Fri, 31 Mar 2023 23:43:04 GMT  
		Size: 308.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e37b7ebb7da08813346917dcbf3e8d12cfc33b9005864ac83a953764d05a6d4`  
		Last Modified: Fri, 21 Apr 2023 20:55:04 GMT  
		Size: 3.4 MB (3403834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:7-fpm-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:2b6cb1a1eb32254a580ba2c8154157190e6e7a9b8a6d2f9fa43515229fe65207
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.2 MB (32196138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1457e91203187130d31fa1b05b14230175ea80affb0485407dabe0b2df16fc2b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:20 GMT
ADD file:a6a2f69b60d7d27bc6e2b9b7e9910dabdc3f5e3702c2345d26a7dc8c603ae595 in / 
# Wed, 29 Mar 2023 17:39:20 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 21:38:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 29 Mar 2023 21:38:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 29 Mar 2023 21:38:10 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 29 Mar 2023 21:38:10 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 29 Mar 2023 21:38:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 29 Mar 2023 21:38:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 Mar 2023 21:38:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 Mar 2023 21:38:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 29 Mar 2023 22:15:32 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Wed, 29 Mar 2023 22:15:32 GMT
ENV PHP_VERSION=8.0.28
# Wed, 29 Mar 2023 22:15:32 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.28.tar.xz.asc
# Wed, 29 Mar 2023 22:15:32 GMT
ENV PHP_SHA256=5e07278a1f315a67d36a676c01343ca2d4da5ec5bdb15d018e4248b3012bc0cd
# Wed, 29 Mar 2023 22:15:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 29 Mar 2023 22:15:39 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 29 Mar 2023 22:21:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 29 Mar 2023 22:21:10 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 29 Mar 2023 22:21:11 GMT
RUN docker-php-ext-enable sodium
# Wed, 29 Mar 2023 22:21:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 29 Mar 2023 22:21:11 GMT
WORKDIR /var/www/html
# Wed, 29 Mar 2023 22:21:12 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 29 Mar 2023 22:21:12 GMT
STOPSIGNAL SIGQUIT
# Wed, 29 Mar 2023 22:21:12 GMT
EXPOSE 9000
# Wed, 29 Mar 2023 22:21:12 GMT
CMD ["php-fpm"]
# Thu, 30 Mar 2023 06:32:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Thu, 30 Mar 2023 06:32:23 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 21 Apr 2023 20:10:23 GMT
ENV DRUPAL_VERSION=7.97
# Fri, 21 Apr 2023 20:10:23 GMT
ENV DRUPAL_MD5=37b63299e115a9e8863f564780a026e9
# Fri, 21 Apr 2023 20:10:24 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes
```

-	Layers:
	-	`sha256:547446be3368f442c50ff95e2a2a9c85110b6b41bbb3c75b7e5ebb115f478b57`  
		Last Modified: Wed, 29 Mar 2023 17:39:56 GMT  
		Size: 2.7 MB (2709344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273930647520993753dd5a2df61373dddd6a462c42c49b7ac22b4e352bd92a59`  
		Last Modified: Wed, 29 Mar 2023 22:27:00 GMT  
		Size: 1.7 MB (1715649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ce6df451b8065d3d6a91a2b460b90d6b595752b01602dbf0fb3e61594e7c14`  
		Last Modified: Wed, 29 Mar 2023 22:26:59 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35120381a81b24152df5ec5250dc2172b8766280cbdd3f50633dcac37ddfcbb9`  
		Last Modified: Wed, 29 Mar 2023 22:26:59 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d256bafa6746361e758806706e5baac0a23dc47dceb6190cd17ef1f91f2f22`  
		Last Modified: Wed, 29 Mar 2023 22:29:26 GMT  
		Size: 10.8 MB (10821697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97eb0527d2f361ac72aefb52a228e1d89df43bed0eede4870a3eaf803913f3e8`  
		Last Modified: Wed, 29 Mar 2023 22:29:25 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a7a4887c4cfaaf4988aac3826e37122d5e0deedcc78418aa226440d84cfa98`  
		Last Modified: Wed, 29 Mar 2023 22:29:49 GMT  
		Size: 11.6 MB (11554264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457131b4099aa9d91da077b02fcd99d05d9d82deebd931d0e2f70417b7c1d35d`  
		Last Modified: Wed, 29 Mar 2023 22:29:47 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a283290cc8885706514e5a3dd100d8440f9a9fc16e4e120435fd725d2b6c11`  
		Last Modified: Wed, 29 Mar 2023 22:29:47 GMT  
		Size: 18.7 KB (18663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e96e204211e381cc00a66223feee45794f8bcbd1baa55c7a7970455df995b98`  
		Last Modified: Wed, 29 Mar 2023 22:29:47 GMT  
		Size: 8.7 KB (8712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa26e0ba3817d890d8d54fe9320c87e86f1fa7b53d6efbd88e0b753f42d9ba69`  
		Last Modified: Thu, 30 Mar 2023 06:38:19 GMT  
		Size: 2.0 MB (1959204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652c31d8194d96557d4207a1c3d8671cfec8fd23859e3c711a2990a38a63089e`  
		Last Modified: Thu, 30 Mar 2023 06:38:18 GMT  
		Size: 314.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82bae9223634d542f4e411ad45501c795a5d77e92ae180a08f1e29b3b7d92b1c`  
		Last Modified: Fri, 21 Apr 2023 20:14:34 GMT  
		Size: 3.4 MB (3403820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:7-fpm-alpine3.16` - linux; 386

```console
$ docker pull drupal@sha256:92b7f88b20f23eb17062bbebb971d537e13063869e2c6300ce25f7631a265d3c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.6 MB (33645628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28101c24f6cc58705c360d599002b088e878bb644689ee972c672f7f574b0f82`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 29 Mar 2023 17:38:33 GMT
ADD file:c9d37b1a7eee54b1a8c1ebde284829510ec289f7b7db2c16059b26f01b416fe0 in / 
# Wed, 29 Mar 2023 17:38:33 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 20:21:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 29 Mar 2023 20:21:15 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 29 Mar 2023 20:21:16 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 29 Mar 2023 20:21:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 29 Mar 2023 20:21:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 29 Mar 2023 20:21:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 Mar 2023 20:21:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 Mar 2023 20:21:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 29 Mar 2023 21:25:56 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Wed, 29 Mar 2023 21:25:56 GMT
ENV PHP_VERSION=8.0.28
# Wed, 29 Mar 2023 21:25:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.28.tar.xz.asc
# Wed, 29 Mar 2023 21:25:56 GMT
ENV PHP_SHA256=5e07278a1f315a67d36a676c01343ca2d4da5ec5bdb15d018e4248b3012bc0cd
# Wed, 29 Mar 2023 21:26:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 29 Mar 2023 21:26:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 29 Mar 2023 21:40:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 29 Mar 2023 21:40:11 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 29 Mar 2023 21:40:12 GMT
RUN docker-php-ext-enable sodium
# Wed, 29 Mar 2023 21:40:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 29 Mar 2023 21:40:13 GMT
WORKDIR /var/www/html
# Wed, 29 Mar 2023 21:40:13 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 29 Mar 2023 21:40:13 GMT
STOPSIGNAL SIGQUIT
# Wed, 29 Mar 2023 21:40:13 GMT
EXPOSE 9000
# Wed, 29 Mar 2023 21:40:13 GMT
CMD ["php-fpm"]
# Thu, 30 Mar 2023 02:34:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Thu, 30 Mar 2023 02:34:15 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 21 Apr 2023 20:46:08 GMT
ENV DRUPAL_VERSION=7.97
# Fri, 21 Apr 2023 20:46:08 GMT
ENV DRUPAL_MD5=37b63299e115a9e8863f564780a026e9
# Fri, 21 Apr 2023 20:46:10 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes
```

-	Layers:
	-	`sha256:dea45757091f21722aec41fb20845e57a04f4bb8c199531491f1dc070480a574`  
		Last Modified: Wed, 29 Mar 2023 17:39:11 GMT  
		Size: 2.8 MB (2810814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a567b52fdc1cd3a2bee7bd070b7d0877448ee524cefbaac1482d5c97c5716724`  
		Last Modified: Wed, 29 Mar 2023 21:50:31 GMT  
		Size: 1.8 MB (1821100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2535a6171e7e823a72acfb0de9dc421fc1cf370ecb4806c2af8929c2f47c1dd4`  
		Last Modified: Wed, 29 Mar 2023 21:50:30 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848901e0fbf7732b01a4127a50e731b858148a525e80e34dfe3ad3c91a5a2ba7`  
		Last Modified: Wed, 29 Mar 2023 21:50:30 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec740a7f969ba9465ee96edd1b3b1b93caa6254134d5390581455b25479aa50a`  
		Last Modified: Wed, 29 Mar 2023 21:53:19 GMT  
		Size: 10.8 MB (10821686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2baec074b41a86cb41c2a162f3a18736ca26826943954b508b3fc6de80181dd`  
		Last Modified: Wed, 29 Mar 2023 21:53:18 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c05a7932c8df9d5a2bdb761d88fa11e0b9bc44d352fe3b3191a69f2e0a16894f`  
		Last Modified: Wed, 29 Mar 2023 21:53:44 GMT  
		Size: 12.3 MB (12341544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04015af42dc90125640d882f9845cf8a892c5d2e14386235021be449f163118f`  
		Last Modified: Wed, 29 Mar 2023 21:53:41 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b26adf16a2bcd6f29e10cca36e0de2998c203776b206b8d81042506782f55a9`  
		Last Modified: Wed, 29 Mar 2023 21:53:41 GMT  
		Size: 18.6 KB (18643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d05f3900b6816d0969acf799734a43a8a2d1ed8ef32beb5a88b78e742cd532d8`  
		Last Modified: Wed, 29 Mar 2023 21:53:41 GMT  
		Size: 8.7 KB (8714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdbe61cde8488f8e4ff574aa4287811a3c25567aa7e39de3c868a028b8295ee`  
		Last Modified: Thu, 30 Mar 2023 02:41:08 GMT  
		Size: 2.4 MB (2414505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bbfeab8fdeb3f08646cebe13c2a301d0653b501ae6491273fa3c0b7cd8208d0`  
		Last Modified: Thu, 30 Mar 2023 02:41:07 GMT  
		Size: 312.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a34cbd798ea6a279f86b5b31ed59468cb47d6a819aa356f0122beb8dbb9c7f`  
		Last Modified: Fri, 21 Apr 2023 20:50:23 GMT  
		Size: 3.4 MB (3403834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:7-fpm-alpine3.16` - linux; ppc64le

```console
$ docker pull drupal@sha256:bb94a6c876cc0a7b086d0211709c54a0a38073b67ad08fad7e5d35bf3aebcd57
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35715149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ada0c7d8a005a41c3e91920b8f70f58d5b86131f3f7c1cd87cae29bc8a89a8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 29 Mar 2023 18:16:34 GMT
ADD file:00a20a25a46ff8ebd9bc78b5b8c6fc5b1dc8ae73d5a42048fa5769a2b2e717c7 in / 
# Wed, 29 Mar 2023 18:16:34 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 22:50:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 29 Mar 2023 22:50:33 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 29 Mar 2023 22:50:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 29 Mar 2023 22:50:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 29 Mar 2023 22:50:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 29 Mar 2023 22:50:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 Mar 2023 22:50:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 Mar 2023 22:50:36 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 29 Mar 2023 23:36:54 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Fri, 09 Jun 2023 02:02:54 GMT
ENV PHP_VERSION=8.0.29
# Fri, 09 Jun 2023 02:02:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.29.tar.xz.asc
# Fri, 09 Jun 2023 02:02:54 GMT
ENV PHP_SHA256=14db2fbf26c07d0eb2c9fab25dbde7e27726a3e88452cca671f0896bbb683ca9
# Fri, 09 Jun 2023 02:03:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 09 Jun 2023 02:03:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 09 Jun 2023 02:13:16 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 09 Jun 2023 02:13:17 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 09 Jun 2023 02:13:19 GMT
RUN docker-php-ext-enable sodium
# Fri, 09 Jun 2023 02:13:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jun 2023 02:13:19 GMT
WORKDIR /var/www/html
# Fri, 09 Jun 2023 02:13:20 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 09 Jun 2023 02:13:21 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Jun 2023 02:13:21 GMT
EXPOSE 9000
# Fri, 09 Jun 2023 02:13:21 GMT
CMD ["php-fpm"]
# Fri, 09 Jun 2023 03:11:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Fri, 09 Jun 2023 03:11:37 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 09 Jun 2023 03:16:22 GMT
ENV DRUPAL_VERSION=7.98
# Fri, 09 Jun 2023 03:16:22 GMT
ENV DRUPAL_MD5=4139f0feecb44a53645242194809b73a
# Fri, 09 Jun 2023 03:16:24 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes
```

-	Layers:
	-	`sha256:d80736dee7a63492583c90bab1ab07f987ed5e10dfb16fd3f025df3a2d65f1c6`  
		Last Modified: Wed, 29 Mar 2023 18:17:28 GMT  
		Size: 2.8 MB (2804670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567564086a1fc2e55fb79fcb242e4b796529924c25db656182d23db312756d02`  
		Last Modified: Wed, 29 Mar 2023 23:56:08 GMT  
		Size: 1.8 MB (1772659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01e9b4703132e5b7a3a83e7d2f4e1c7e304482d157213265354960d321599e2`  
		Last Modified: Wed, 29 Mar 2023 23:56:08 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d860562bbe27579611e6e8b1892c914da934d9681f142a3fc9de640ab8c0515f`  
		Last Modified: Wed, 29 Mar 2023 23:56:08 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d47e2ee52c4e0847ddf9ddcb231d5f6d0236cf35aedd58c16fa701159284ecc`  
		Last Modified: Fri, 09 Jun 2023 02:35:28 GMT  
		Size: 10.8 MB (10823752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:434c372d006505e832cc4bec73d73314f37ffd8eab8ff7a6d9699ba99be77169`  
		Last Modified: Fri, 09 Jun 2023 02:35:27 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6d7ecb35832a2e00b255ec197394284f5bcf03f5340361f39db13525a5fb8c`  
		Last Modified: Fri, 09 Jun 2023 02:35:59 GMT  
		Size: 14.8 MB (14751422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c779b97aaa9494f6a77cdd83a002731e74d7d6945f20d6fa23376872775c2cb6`  
		Last Modified: Fri, 09 Jun 2023 02:35:55 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f898ea0ee8cd9b67c8e2d37388f71717976fd7e76bc024f6526f9fd1dd659965`  
		Last Modified: Fri, 09 Jun 2023 02:35:55 GMT  
		Size: 18.8 KB (18790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04632f0d7ffd56de1b101d8160ed9fd9678e55b117211a3c5bfbeee44d92cbc9`  
		Last Modified: Fri, 09 Jun 2023 02:35:55 GMT  
		Size: 8.7 KB (8717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007c1ca90d2cc46c7684903fc5cd6ccf788d637ace5772378a1d569c288bc468`  
		Last Modified: Fri, 09 Jun 2023 03:31:18 GMT  
		Size: 2.1 MB (2119198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6558ff3213e94e30c252e46f1d15330e2c44b66417a9a4ad086fff519aebd2de`  
		Last Modified: Fri, 09 Jun 2023 03:31:18 GMT  
		Size: 313.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0f017b93f09784d5c6d8e5f1cbcbdbbe2fe1904d283aab18d84ea3f7c6b5f3`  
		Last Modified: Fri, 09 Jun 2023 03:38:26 GMT  
		Size: 3.4 MB (3411152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:7-fpm-alpine3.16` - linux; s390x

```console
$ docker pull drupal@sha256:17f0758d55b79999abd80fa4a7dc0d1063c32956d8eb5685096a8505f7492db3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.0 MB (33989586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42644b79fa1c2e91b7c291dfd80acce8bab3579254c42c2471a3f6750e0b17c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 29 Mar 2023 17:42:02 GMT
ADD file:6c3b2d8f192a3a12e6df8bc7130bbc723b1a39aa71809d23b15cf80bc5135096 in / 
# Wed, 29 Mar 2023 17:42:02 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:12:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 29 Mar 2023 19:12:31 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 29 Mar 2023 19:12:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 29 Mar 2023 19:12:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 29 Mar 2023 19:12:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 29 Mar 2023 19:12:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 Mar 2023 19:12:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 Mar 2023 19:12:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 29 Apr 2023 02:57:22 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4
# Fri, 09 Jun 2023 01:22:44 GMT
ENV PHP_VERSION=8.0.29
# Fri, 09 Jun 2023 01:22:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.29.tar.xz.asc
# Fri, 09 Jun 2023 01:22:44 GMT
ENV PHP_SHA256=14db2fbf26c07d0eb2c9fab25dbde7e27726a3e88452cca671f0896bbb683ca9
# Fri, 09 Jun 2023 01:22:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 09 Jun 2023 01:22:48 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:29:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 09 Jun 2023 01:29:02 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:29:03 GMT
RUN docker-php-ext-enable sodium
# Fri, 09 Jun 2023 01:29:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jun 2023 01:29:03 GMT
WORKDIR /var/www/html
# Fri, 09 Jun 2023 01:29:04 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 09 Jun 2023 01:29:04 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Jun 2023 01:29:04 GMT
EXPOSE 9000
# Fri, 09 Jun 2023 01:29:04 GMT
CMD ["php-fpm"]
# Fri, 09 Jun 2023 02:09:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Fri, 09 Jun 2023 02:09:21 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 09 Jun 2023 02:12:35 GMT
ENV DRUPAL_VERSION=7.98
# Fri, 09 Jun 2023 02:12:35 GMT
ENV DRUPAL_MD5=4139f0feecb44a53645242194809b73a
# Fri, 09 Jun 2023 02:12:36 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes
```

-	Layers:
	-	`sha256:95cbbfdf0c760cbcde91603c8eee15ec60d4aa5f874b4a538babcd2df1709174`  
		Last Modified: Wed, 29 Mar 2023 17:42:37 GMT  
		Size: 2.6 MB (2593389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fdfd2f8b8531d48e4c87d755c1944888d5da7015dd1f593536327ea037d1bdd`  
		Last Modified: Wed, 29 Mar 2023 19:54:00 GMT  
		Size: 1.8 MB (1776265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962fb7fb76af91375d30ce593445bc5d72cab123d7ff4de2d98d2ee034c2336a`  
		Last Modified: Wed, 29 Mar 2023 19:53:59 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ba68e13725670de4293f877cea92aa9b673ddb664615bb005c6d0b5c9ee879`  
		Last Modified: Wed, 29 Mar 2023 19:53:59 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3831bc537a53c5236508b96be93b6fe0246affb620ad4252f6c3b59dd39f45`  
		Last Modified: Fri, 09 Jun 2023 01:41:24 GMT  
		Size: 10.8 MB (10823756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61fc27bd6398fd7794e86367be7e4de5fe2b958ea80f49a840f1d33975d4d60`  
		Last Modified: Fri, 09 Jun 2023 01:41:24 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f159530b0ba7ec0f4c9048e22e89ffb4ccdf54262c6b0d7bb179ce7b9ab18bca`  
		Last Modified: Fri, 09 Jun 2023 01:41:40 GMT  
		Size: 13.4 MB (13363970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cea639a7ef5e542eca9b4288a41303558aa2c40ae0e796658aa3fdaeff1a764`  
		Last Modified: Fri, 09 Jun 2023 01:41:38 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a60c69d51080b9578dc4553cd1125e02c70f079d278e05f3dda6ddb54d9b45`  
		Last Modified: Fri, 09 Jun 2023 01:41:38 GMT  
		Size: 18.8 KB (18809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57a35fd5bbbd015699048bd7fff48ad45fa7bf861965b2593a4f60560cb008c3`  
		Last Modified: Fri, 09 Jun 2023 01:41:39 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd44f9a5832b867820e74e415b206a7e05a1a65c369f117c33fd3fdf4b9dc022`  
		Last Modified: Fri, 09 Jun 2023 02:19:15 GMT  
		Size: 2.0 MB (1988750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55dc056432364cfb701174e57deff28a6bb1234c76ccfe3d434550e1e0703091`  
		Last Modified: Fri, 09 Jun 2023 02:19:14 GMT  
		Size: 309.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16fd5cff502f8a48d0d90309e2765ea406eff01c103d4012cb00674a76c07bd5`  
		Last Modified: Fri, 09 Jun 2023 02:21:34 GMT  
		Size: 3.4 MB (3411150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
