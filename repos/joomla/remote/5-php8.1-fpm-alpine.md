## `joomla:5-php8.1-fpm-alpine`

```console
$ docker pull joomla@sha256:f6036f473b149c7368d8935557556611938423dc80094dbc1040842265bec824
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

### `joomla:5-php8.1-fpm-alpine` - linux; amd64

```console
$ docker pull joomla@sha256:2a2db80bb47e0ea927045e32f45da03083b120b155db4cdb102fc648b70f248f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.9 MB (88906898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:caa91e2ac9a785a62d8ac86b888495da611f8eca6543115c1e5a34c7a5d1420a`
-	Entrypoint: `["\/entrypoint.sh"]`
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
# Tue, 12 Dec 2023 22:31:11 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 28 Dec 2023 00:47:07 GMT
ENV PHP_VERSION=8.1.27
# Thu, 28 Dec 2023 00:47:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Thu, 28 Dec 2023 00:47:07 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Thu, 28 Dec 2023 00:47:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 28 Dec 2023 00:47:14 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 28 Dec 2023 00:55:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 28 Dec 2023 00:55:09 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 28 Dec 2023 00:55:10 GMT
RUN docker-php-ext-enable sodium
# Thu, 28 Dec 2023 00:55:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Dec 2023 00:55:11 GMT
WORKDIR /var/www/html
# Thu, 28 Dec 2023 00:55:11 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 28 Dec 2023 00:55:11 GMT
STOPSIGNAL SIGQUIT
# Thu, 28 Dec 2023 00:55:11 GMT
EXPOSE 9000
# Thu, 28 Dec 2023 00:55:11 GMT
CMD ["php-fpm"]
# Thu, 28 Dec 2023 02:07:47 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Thu, 28 Dec 2023 02:07:47 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Thu, 28 Dec 2023 02:07:50 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 		zstd 	;
# Thu, 28 Dec 2023 02:10:05 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.7.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Thu, 28 Dec 2023 02:10:06 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 28 Dec 2023 02:10:07 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 28 Dec 2023 02:10:07 GMT
VOLUME [/var/www/html]
# Tue, 09 Jan 2024 19:43:53 GMT
ENV JOOMLA_VERSION=5.0.2
# Tue, 09 Jan 2024 19:43:53 GMT
ENV JOOMLA_SHA512=e7bc9ecab410217fdf91a87f9461ff18dab311af56c61156fb7cf076b2fdf270b003ffddf131386ef35c94cb9f4ada39f8a69712c07664147108268ab5cc85a3
# Tue, 09 Jan 2024 19:43:57 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.0.2/Joomla_5.0.2-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla
# Mon, 22 Jan 2024 22:46:34 GMT
COPY file:6dcb949f1bfc58f87c0887173eb61a91c7f9c1290655683ed002e25b7aeb694a in /entrypoint.sh 
# Mon, 22 Jan 2024 22:46:34 GMT
COPY file:4365854cfba2f0673f4930c9c90629a51419815bb2048df2d1803bf1a9d79fd6 in /makedb.php 
# Mon, 22 Jan 2024 22:46:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jan 2024 22:46:34 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc99979baa6760dc40a927f812328a1431e3870d0f166b035365166ef2cf8d4`  
		Last Modified: Tue, 12 Dec 2023 23:24:24 GMT  
		Size: 2.8 MB (2755737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47536423e0797b82f7a737a4efeb29297c96a33e8662ddcd121d728a01eac477`  
		Last Modified: Tue, 12 Dec 2023 23:24:23 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be6d4fc569fcdbdb835c5ee3607367e6ba4779809c0fad97de75045144220f8`  
		Last Modified: Tue, 12 Dec 2023 23:24:23 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427b4c7058bd11824fd178a84765ae46f8986757d5fdecf603573e9a5adcf595`  
		Last Modified: Thu, 28 Dec 2023 01:25:35 GMT  
		Size: 11.9 MB (11935901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f3ca02654c8ed90874067782c187f5ed63b8574ed212f60e705ca4bce8a798f`  
		Last Modified: Thu, 28 Dec 2023 01:25:34 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe80a6acaf0f3b606bdbeaa3f7fc40fc52c4b194fad35a8d608583139e1378d`  
		Last Modified: Thu, 28 Dec 2023 01:26:00 GMT  
		Size: 12.6 MB (12599198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f662d6528eebdaaaca76b70ccd5ef3dc755f0861ff1fe3b07bbe6d34b12631b5`  
		Last Modified: Thu, 28 Dec 2023 01:25:58 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f2738c7fe0ccbc5ab9b8a43e704f0e2ad165445069156b957e682a70b26c22`  
		Last Modified: Thu, 28 Dec 2023 01:25:58 GMT  
		Size: 19.3 KB (19290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074b70018705fd505fbd643a105a3814057a41e671dcae44be1eaa117d11d717`  
		Last Modified: Thu, 28 Dec 2023 01:25:58 GMT  
		Size: 8.9 KB (8879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da312cd7880b286de21aeed37e1f4b46ee6e51c7f610cdd6d312914bb260b272`  
		Last Modified: Thu, 28 Dec 2023 02:40:48 GMT  
		Size: 28.7 MB (28747290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e31752a310e5c4648b3b9d772a92921615ac797ad35794b9a80ad205f0a265`  
		Last Modified: Thu, 28 Dec 2023 02:40:45 GMT  
		Size: 6.9 MB (6915574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4540b8706102dce5dce30f822abf122f1fcb1792938aff89e84f29b0b1e771d`  
		Last Modified: Thu, 28 Dec 2023 02:40:42 GMT  
		Size: 61.3 KB (61343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880feb752878f3e5eb7deda49fe7565f5dc76adfd94f385fe6e496b14c72b118`  
		Last Modified: Thu, 28 Dec 2023 02:40:42 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54669fffaff3356ebbd94844ba85e332cc48f40013c4fcc657d7dc1a26268ef0`  
		Last Modified: Tue, 09 Jan 2024 19:46:44 GMT  
		Size: 22.4 MB (22446543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0bf418d2a2efeb2f3a145580c510f0a90459dae74791d952e2b08c98c7177ae`  
		Last Modified: Mon, 22 Jan 2024 22:48:17 GMT  
		Size: 2.7 KB (2737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83c23d94f571bfb7e70471032ecfbca2b13296b86ae88eb7b57d70d27121d6a`  
		Last Modified: Mon, 22 Jan 2024 22:48:17 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:5-php8.1-fpm-alpine` - linux; arm variant v6

```console
$ docker pull joomla@sha256:7e8fe5446c7185e3331af612ff99acc376fb08aa9007de60cab8a9b6f2987009
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.7 MB (86713805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f6b6328a8ca4240e8f2871731ad15a46b65386c9bdd0bfd59e33bc244947980`
-	Entrypoint: `["\/entrypoint.sh"]`
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
# Tue, 12 Dec 2023 21:30:34 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 28 Dec 2023 03:20:51 GMT
ENV PHP_VERSION=8.1.27
# Thu, 28 Dec 2023 03:20:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Thu, 28 Dec 2023 03:20:51 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Thu, 28 Dec 2023 03:20:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 28 Dec 2023 03:20:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 28 Dec 2023 03:26:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 28 Dec 2023 03:26:24 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 28 Dec 2023 03:26:25 GMT
RUN docker-php-ext-enable sodium
# Thu, 28 Dec 2023 03:26:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Dec 2023 03:26:26 GMT
WORKDIR /var/www/html
# Thu, 28 Dec 2023 03:26:26 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 28 Dec 2023 03:26:26 GMT
STOPSIGNAL SIGQUIT
# Thu, 28 Dec 2023 03:26:26 GMT
EXPOSE 9000
# Thu, 28 Dec 2023 03:26:27 GMT
CMD ["php-fpm"]
# Thu, 28 Dec 2023 07:24:14 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Thu, 28 Dec 2023 07:24:14 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Thu, 28 Dec 2023 07:24:20 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 		zstd 	;
# Thu, 28 Dec 2023 07:26:37 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.7.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Thu, 28 Dec 2023 07:26:38 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 28 Dec 2023 07:26:39 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 28 Dec 2023 07:26:39 GMT
VOLUME [/var/www/html]
# Tue, 09 Jan 2024 21:38:21 GMT
ENV JOOMLA_VERSION=5.0.2
# Tue, 09 Jan 2024 21:38:21 GMT
ENV JOOMLA_SHA512=e7bc9ecab410217fdf91a87f9461ff18dab311af56c61156fb7cf076b2fdf270b003ffddf131386ef35c94cb9f4ada39f8a69712c07664147108268ab5cc85a3
# Tue, 09 Jan 2024 21:38:26 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.0.2/Joomla_5.0.2-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla
# Tue, 09 Jan 2024 21:38:27 GMT
COPY file:75d4151822bf32487f27c3996faec3e2842350001f3cabdee80506df7825dc96 in /entrypoint.sh 
# Tue, 09 Jan 2024 21:38:27 GMT
COPY file:4365854cfba2f0673f4930c9c90629a51419815bb2048df2d1803bf1a9d79fd6 in /makedb.php 
# Tue, 09 Jan 2024 21:38:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 09 Jan 2024 21:38:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6157a5053a6ba5646a1361153760014335e77813c8792b60d226dedefbb229`  
		Last Modified: Tue, 12 Dec 2023 22:10:24 GMT  
		Size: 2.8 MB (2761045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2682a06d9f91bef66466bcb1b37715dc344282ac9f062ffff8405cf448d71f51`  
		Last Modified: Tue, 12 Dec 2023 22:10:23 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982a61382f7fcec3d428935d516ac99bf603d105e72ebe0c2952b860f329675f`  
		Last Modified: Tue, 12 Dec 2023 22:10:22 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18067ddb037748f68a4543bdc439b3ccc530fe154d4c4e55e40744bdb2fdf4a1`  
		Last Modified: Thu, 28 Dec 2023 03:42:56 GMT  
		Size: 11.9 MB (11935921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:018ebffeb0402b70011a338481119981065e34683facc4ae094f102d8c8d5081`  
		Last Modified: Thu, 28 Dec 2023 03:42:55 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffe2394fba4399c5dadf63ff268f7eae748c00c8e90d999bfc56b8c8618aed1`  
		Last Modified: Thu, 28 Dec 2023 03:43:22 GMT  
		Size: 11.4 MB (11427155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324eae947d17053bfd692c3b7d5bc8c8f4c639dc4ad5394f1edc7a3466ebc133`  
		Last Modified: Thu, 28 Dec 2023 03:43:20 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b953584b6199d8b64c4cbd6d66907bb96d753779ddadc2a2f2ddcc702c8f5e`  
		Last Modified: Thu, 28 Dec 2023 03:43:20 GMT  
		Size: 19.1 KB (19124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113f154202f8872a7b8cf1930264ca911e7fcd4ef5a3f27b116653c025aef525`  
		Last Modified: Thu, 28 Dec 2023 03:43:20 GMT  
		Size: 8.9 KB (8877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d0f826e2d1c08251ac80732831b9d508100d978e7a9c78175bfee828a3bcbbb`  
		Last Modified: Thu, 28 Dec 2023 07:36:30 GMT  
		Size: 28.3 MB (28279035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86dccca4736bc7d63f6c9cec9c6dcd7be2d9119d78d4dc139af09cb708c84141`  
		Last Modified: Thu, 28 Dec 2023 07:36:26 GMT  
		Size: 6.6 MB (6601062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f91da89a6b48141ae7f14d6e476a4a62ed24714e0dc6c2c200768b2df7cb2813`  
		Last Modified: Thu, 28 Dec 2023 07:36:23 GMT  
		Size: 61.4 KB (61355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b154573a5c564c4b45f5449da4bdf4171373674e635de94c9cdc1af9ac91e5`  
		Last Modified: Thu, 28 Dec 2023 07:36:23 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65481e2a2cf2f8650b7989b9ae7eaa01a90eba78160d3807e0646a9d3b93d141`  
		Last Modified: Tue, 09 Jan 2024 21:39:20 GMT  
		Size: 22.4 MB (22446547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7c83655f190451c48d8a7f3897896d9fff0ba91ae096a3651f03362606606e8`  
		Last Modified: Tue, 09 Jan 2024 21:39:15 GMT  
		Size: 2.6 KB (2619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80deb34ddce8cbd1127223bc52cc585bc044ab095b44c465a8b547f58185dcf5`  
		Last Modified: Tue, 09 Jan 2024 21:39:15 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:5-php8.1-fpm-alpine` - linux; arm variant v7

```console
$ docker pull joomla@sha256:7ee4b4be1223286180d14713ae9506e6463fe03c8617ece2485bf780d8a5fcf3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.0 MB (84003179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7a2d07322a76b7cf5e716b2cdf621dae782aadde6e0d2f358d9817c79f9539`
-	Entrypoint: `["\/entrypoint.sh"]`
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
# Tue, 12 Dec 2023 21:55:39 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 28 Dec 2023 02:16:29 GMT
ENV PHP_VERSION=8.1.27
# Thu, 28 Dec 2023 02:16:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Thu, 28 Dec 2023 02:16:30 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Thu, 28 Dec 2023 02:16:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 28 Dec 2023 02:16:40 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 28 Dec 2023 02:29:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 28 Dec 2023 02:29:10 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 28 Dec 2023 02:29:12 GMT
RUN docker-php-ext-enable sodium
# Thu, 28 Dec 2023 02:29:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Dec 2023 02:29:13 GMT
WORKDIR /var/www/html
# Thu, 28 Dec 2023 02:29:14 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 28 Dec 2023 02:29:15 GMT
STOPSIGNAL SIGQUIT
# Thu, 28 Dec 2023 02:29:15 GMT
EXPOSE 9000
# Thu, 28 Dec 2023 02:29:15 GMT
CMD ["php-fpm"]
# Thu, 28 Dec 2023 05:52:03 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Thu, 28 Dec 2023 05:52:04 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Thu, 28 Dec 2023 05:52:10 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 		zstd 	;
# Thu, 28 Dec 2023 05:57:15 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.7.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Thu, 28 Dec 2023 05:57:18 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 28 Dec 2023 05:57:19 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 28 Dec 2023 05:57:20 GMT
VOLUME [/var/www/html]
# Tue, 09 Jan 2024 19:22:34 GMT
ENV JOOMLA_VERSION=5.0.2
# Tue, 09 Jan 2024 19:22:34 GMT
ENV JOOMLA_SHA512=e7bc9ecab410217fdf91a87f9461ff18dab311af56c61156fb7cf076b2fdf270b003ffddf131386ef35c94cb9f4ada39f8a69712c07664147108268ab5cc85a3
# Tue, 09 Jan 2024 19:22:45 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.0.2/Joomla_5.0.2-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla
# Mon, 22 Jan 2024 23:57:03 GMT
COPY file:6dcb949f1bfc58f87c0887173eb61a91c7f9c1290655683ed002e25b7aeb694a in /entrypoint.sh 
# Mon, 22 Jan 2024 23:57:04 GMT
COPY file:4365854cfba2f0673f4930c9c90629a51419815bb2048df2d1803bf1a9d79fd6 in /makedb.php 
# Mon, 22 Jan 2024 23:57:04 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jan 2024 23:57:04 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:1086c24c41097f090ce847d192c11307e1715eeb563a2cf4f410b2a199ae1942`  
		Last Modified: Fri, 08 Dec 2023 01:57:36 GMT  
		Size: 2.9 MB (2918701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00fcdc554dd7b708317247ba5731b0d76bc06dc68a48af57f662820d33c665cc`  
		Last Modified: Tue, 12 Dec 2023 22:36:17 GMT  
		Size: 2.6 MB (2608664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4717604343f2899832c4417228ef3cdb02080f72378a4152eb72083f09c96e`  
		Last Modified: Tue, 12 Dec 2023 22:36:15 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe0a6a05c32e2329e654bc633b417da36b7c74ed6bf626231bf0e900f912838e`  
		Last Modified: Tue, 12 Dec 2023 22:36:15 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc25cc92d8b722de9b1ef9fc1eab62df0a78ff5b659834107c07eee26732829`  
		Last Modified: Thu, 28 Dec 2023 02:58:00 GMT  
		Size: 11.9 MB (11935914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d2a8ed9e221b97461198f46e07c5d74d35e5e3f8aeb0802de6756c89eca40a7`  
		Last Modified: Thu, 28 Dec 2023 02:57:59 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d7a306819a10563c795bcc17b49b9eb3b6f2536fbc1e4ef192b9b1d0c5ff41`  
		Last Modified: Thu, 28 Dec 2023 02:58:27 GMT  
		Size: 10.7 MB (10715745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760c91d98d487c56f96c3670c9fe7090bbc359d8928d8cf2c0a1640e4ee9df75`  
		Last Modified: Thu, 28 Dec 2023 02:58:25 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a678b267f2b1da2a3cf6bc729a781be82a0df3eb3600f8b336b6d5a5e02edb`  
		Last Modified: Thu, 28 Dec 2023 02:58:24 GMT  
		Size: 19.1 KB (19109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45c48b983968efc94de759469e07cc58afe98911572f010cd0f5d6719ed42cb`  
		Last Modified: Thu, 28 Dec 2023 02:58:25 GMT  
		Size: 8.9 KB (8878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc1c7087bf091163c36e0aaaec899159872435ee1b1c488bc28be43186d08df9`  
		Last Modified: Thu, 28 Dec 2023 06:54:14 GMT  
		Size: 26.7 MB (26711424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6dd08bb75ab4391c86b9fc8c61a301d6eb5bc90f143e6eb2746efd12b470fe5`  
		Last Modified: Thu, 28 Dec 2023 06:54:11 GMT  
		Size: 6.6 MB (6568195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bf57d573bbe6b65161934913b42ce5739002c3aca5ca8f2a80fadff41942a8f`  
		Last Modified: Thu, 28 Dec 2023 06:54:08 GMT  
		Size: 61.3 KB (61325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed45cbaf93ac05b0e73fb238013159bfeeb888ad72f0c40622d14e5c8b8f8d9`  
		Last Modified: Thu, 28 Dec 2023 06:54:08 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aaff9805b58d6eeaa102b3a8784e7dae28df958538aa30635647816a47212e1`  
		Last Modified: Tue, 09 Jan 2024 19:28:10 GMT  
		Size: 22.4 MB (22446561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddc4272f13b1d31521bd0b3ab5173139657bc4161fcbcdc711ac8b829d97eaf`  
		Last Modified: Mon, 22 Jan 2024 23:59:34 GMT  
		Size: 2.7 KB (2737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0840dcd30a42a45a484889704f7ea83d6bd0a7cbce0538bb63ef76ff4e66284`  
		Last Modified: Mon, 22 Jan 2024 23:59:34 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:5-php8.1-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull joomla@sha256:da98cc43caf2d5af2d47c7be3a633ddd73087798ca34afc70ea4ea13df652ca7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.1 MB (89086318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac1869b257f65bf7dcd50d3ad2bf2dd372a3c422eff5b9329109cc885646f81c`
-	Entrypoint: `["\/entrypoint.sh"]`
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
# Tue, 12 Dec 2023 22:05:06 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 28 Dec 2023 00:03:39 GMT
ENV PHP_VERSION=8.1.27
# Thu, 28 Dec 2023 00:03:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Thu, 28 Dec 2023 00:03:39 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Thu, 28 Dec 2023 00:03:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 28 Dec 2023 00:03:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 28 Dec 2023 00:11:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 28 Dec 2023 00:11:44 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 28 Dec 2023 00:11:45 GMT
RUN docker-php-ext-enable sodium
# Thu, 28 Dec 2023 00:11:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Dec 2023 00:11:45 GMT
WORKDIR /var/www/html
# Thu, 28 Dec 2023 00:11:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 28 Dec 2023 00:11:45 GMT
STOPSIGNAL SIGQUIT
# Thu, 28 Dec 2023 00:11:46 GMT
EXPOSE 9000
# Thu, 28 Dec 2023 00:11:46 GMT
CMD ["php-fpm"]
# Thu, 28 Dec 2023 01:32:44 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Thu, 28 Dec 2023 01:32:44 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Thu, 28 Dec 2023 01:32:47 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 		zstd 	;
# Thu, 28 Dec 2023 01:34:41 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.7.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Thu, 28 Dec 2023 01:34:42 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 28 Dec 2023 01:34:42 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 28 Dec 2023 01:34:43 GMT
VOLUME [/var/www/html]
# Tue, 09 Jan 2024 19:43:14 GMT
ENV JOOMLA_VERSION=5.0.2
# Tue, 09 Jan 2024 19:43:14 GMT
ENV JOOMLA_SHA512=e7bc9ecab410217fdf91a87f9461ff18dab311af56c61156fb7cf076b2fdf270b003ffddf131386ef35c94cb9f4ada39f8a69712c07664147108268ab5cc85a3
# Tue, 09 Jan 2024 19:43:17 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.0.2/Joomla_5.0.2-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla
# Mon, 22 Jan 2024 23:26:59 GMT
COPY file:6dcb949f1bfc58f87c0887173eb61a91c7f9c1290655683ed002e25b7aeb694a in /entrypoint.sh 
# Mon, 22 Jan 2024 23:26:59 GMT
COPY file:4365854cfba2f0673f4930c9c90629a51419815bb2048df2d1803bf1a9d79fd6 in /makedb.php 
# Mon, 22 Jan 2024 23:26:59 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jan 2024 23:26:59 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a19b0853c69aaf4e0a33f42601f1bddea728304bef39e2fc08f66f3d518576`  
		Last Modified: Tue, 12 Dec 2023 23:00:29 GMT  
		Size: 2.8 MB (2810204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:872ba87116831a71587816ab8564d1a2b7137e1163524eb7e5abf40966e6882c`  
		Last Modified: Tue, 12 Dec 2023 23:00:28 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a9508fcdd73dc8c678f841adc3269e9919da38f14917ddaa2162b636d4661c`  
		Last Modified: Tue, 12 Dec 2023 23:00:28 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e3817fbec1f47fc54089a02e7f760bf0bbb9eb9c1af6953cfc99be2e7bd858`  
		Last Modified: Thu, 28 Dec 2023 00:41:20 GMT  
		Size: 11.9 MB (11935913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65cf5238cc447cb27f7bc8a847a8ddd60a04cd1e69d3376cdfe220462051fa70`  
		Last Modified: Thu, 28 Dec 2023 00:41:19 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3fbefb84faf5c65fad9a664a3f5f9d6fbf88ef236eed824cb7aebe6a0dfa7b8`  
		Last Modified: Thu, 28 Dec 2023 00:41:44 GMT  
		Size: 12.6 MB (12647692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72ae9b8315787d3979f28df922725ace807859150d551b24d48b3f3089b0faa8`  
		Last Modified: Thu, 28 Dec 2023 00:41:42 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:926f777588cff8a9d96bbfe230a728b6dc9b8181d3d8421dcef37ca034aa00cd`  
		Last Modified: Thu, 28 Dec 2023 00:41:42 GMT  
		Size: 19.1 KB (19086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a3aee1165dbbdca0ee13af2ba7457cf8f0fbec0aede3cdf5a840cf361d3915`  
		Last Modified: Thu, 28 Dec 2023 00:41:43 GMT  
		Size: 8.9 KB (8877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eedd1b154fd6a2fe96f4403c9c657f03faa8d1aa0a32ebddd031d6d4babe75f`  
		Last Modified: Thu, 28 Dec 2023 02:00:31 GMT  
		Size: 28.9 MB (28882629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0273655b93957ad5be4132d57779e66242f59469cf80cba9cb5e10a8353a518`  
		Last Modified: Thu, 28 Dec 2023 02:00:29 GMT  
		Size: 6.9 MB (6917583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d33b17de8960885d1fc221e826a44e7d98dcce9d571132f4e6b0a609aadb18`  
		Last Modified: Thu, 28 Dec 2023 02:00:26 GMT  
		Size: 61.3 KB (61308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5937d2a04a1e2f92d51bf02ed43f70aeee92f51128e5aac3be6681439227ed56`  
		Last Modified: Thu, 28 Dec 2023 02:00:26 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffac57071aea71f25188dc0a1ce4808e019fd82b997e57ec8b563a2df896e7eb`  
		Last Modified: Tue, 09 Jan 2024 19:45:36 GMT  
		Size: 22.4 MB (22446563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b732c720ef2b4e5527f1ce4dd3931978ee3e730baf5f75fc91606f4a39b8efb3`  
		Last Modified: Mon, 22 Jan 2024 23:28:29 GMT  
		Size: 2.7 KB (2738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e55ab3d70809d8e838e075803d0c7c8a1894ffb4cbb51f1af12ff948c233e5`  
		Last Modified: Mon, 22 Jan 2024 23:28:29 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:5-php8.1-fpm-alpine` - linux; 386

```console
$ docker pull joomla@sha256:62f1cbdf2c8c533b230b08ac68bf96d89a941d45f4ecaeb67d2d378ad72063ac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89474909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb64dff414b83ac5b0ad945f2c4bfd543f8fc9a66cbcb94e2478af86ec769d2`
-	Entrypoint: `["\/entrypoint.sh"]`
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
# Tue, 12 Dec 2023 23:05:55 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 28 Dec 2023 01:29:44 GMT
ENV PHP_VERSION=8.1.27
# Thu, 28 Dec 2023 01:29:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Thu, 28 Dec 2023 01:29:44 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Thu, 28 Dec 2023 01:29:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 28 Dec 2023 01:29:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 28 Dec 2023 01:43:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 28 Dec 2023 01:43:09 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 28 Dec 2023 01:43:10 GMT
RUN docker-php-ext-enable sodium
# Thu, 28 Dec 2023 01:43:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Dec 2023 01:43:10 GMT
WORKDIR /var/www/html
# Thu, 28 Dec 2023 01:43:11 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 28 Dec 2023 01:43:11 GMT
STOPSIGNAL SIGQUIT
# Thu, 28 Dec 2023 01:43:11 GMT
EXPOSE 9000
# Thu, 28 Dec 2023 01:43:11 GMT
CMD ["php-fpm"]
# Thu, 28 Dec 2023 04:12:11 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Thu, 28 Dec 2023 04:12:11 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Thu, 28 Dec 2023 04:12:16 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 		zstd 	;
# Thu, 28 Dec 2023 04:15:15 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.7.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Thu, 28 Dec 2023 04:15:17 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 28 Dec 2023 04:15:17 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 28 Dec 2023 04:15:17 GMT
VOLUME [/var/www/html]
# Tue, 09 Jan 2024 19:38:33 GMT
ENV JOOMLA_VERSION=5.0.2
# Tue, 09 Jan 2024 19:38:33 GMT
ENV JOOMLA_SHA512=e7bc9ecab410217fdf91a87f9461ff18dab311af56c61156fb7cf076b2fdf270b003ffddf131386ef35c94cb9f4ada39f8a69712c07664147108268ab5cc85a3
# Tue, 09 Jan 2024 19:38:39 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.0.2/Joomla_5.0.2-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla
# Mon, 22 Jan 2024 23:13:17 GMT
COPY file:6dcb949f1bfc58f87c0887173eb61a91c7f9c1290655683ed002e25b7aeb694a in /entrypoint.sh 
# Mon, 22 Jan 2024 23:13:17 GMT
COPY file:4365854cfba2f0673f4930c9c90629a51419815bb2048df2d1803bf1a9d79fd6 in /makedb.php 
# Mon, 22 Jan 2024 23:13:17 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jan 2024 23:13:17 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9acd8b4c9d4385585f74dabb4bc6b3351888710ae37ec5dbd9ea950281b8f9bb`  
		Last Modified: Fri, 08 Dec 2023 01:38:43 GMT  
		Size: 3.2 MB (3244115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35c853c51aa63c9f21d6c91fa6948b8160ed6a90764a48e7b1891c38e016590`  
		Last Modified: Wed, 13 Dec 2023 00:34:22 GMT  
		Size: 2.8 MB (2820917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6af7fb9ea0ea850c653027fa7b1b18f1d4c405aade35df3c3ec2151bb8251f`  
		Last Modified: Wed, 13 Dec 2023 00:34:21 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9233674231d3f63e2099e1d4253bf67fd488ef3d4fcd72e3e741ffb7a41f385e`  
		Last Modified: Wed, 13 Dec 2023 00:34:20 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39660522076cdd34d1b9b00834848c5682a2f2311b1cc3284dc058ee930c6d7d`  
		Last Modified: Thu, 28 Dec 2023 02:26:29 GMT  
		Size: 11.9 MB (11935912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e0d65d2ac1e6517a815b50880a249dac19879ca94cdc0e7319464e41b3d7a4b`  
		Last Modified: Thu, 28 Dec 2023 02:26:28 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8975975d5ccf88169cb01c9ed68259e1b3064741f97a5f88a6eefa93a99f2032`  
		Last Modified: Thu, 28 Dec 2023 02:26:59 GMT  
		Size: 12.9 MB (12925760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ed54df2401e513ff8645bc6d26e7a605d1bb2c359e850995197075b1f2469e`  
		Last Modified: Thu, 28 Dec 2023 02:26:55 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213db9b9303d420e4c3f07574b153a083b374b791e2ad9f5d22458d234c7737a`  
		Last Modified: Thu, 28 Dec 2023 02:26:55 GMT  
		Size: 19.3 KB (19290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ca0539b2ac5c20ae078f743d3fd58e4cbd1b2574220896efcd7fdc09f1574c`  
		Last Modified: Thu, 28 Dec 2023 02:26:55 GMT  
		Size: 8.9 KB (8876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0604e4bf590f2d8b37a0e108547372116d909c5d21b4e95225d301713fcfa3c8`  
		Last Modified: Thu, 28 Dec 2023 04:54:21 GMT  
		Size: 29.0 MB (28996610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bcb7475329b8f60b04fd97760ea07a9ba2505b0d8ff31f125c0cbb703942b79`  
		Last Modified: Thu, 28 Dec 2023 04:54:16 GMT  
		Size: 7.0 MB (7006892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe5d9ad07a971d00d21535524379132aae536546c776e74760e005284506536e`  
		Last Modified: Thu, 28 Dec 2023 04:54:11 GMT  
		Size: 61.3 KB (61329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e1dbff73ba357244f2cd4de4658c04fc1b1b0f14fc44367272e73f0425b5a61`  
		Last Modified: Thu, 28 Dec 2023 04:54:11 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6917237061b418a94dabcbd2fb15495975ed4704fb9b0496bb7b5e8e2c700b4f`  
		Last Modified: Tue, 09 Jan 2024 19:41:46 GMT  
		Size: 22.4 MB (22446537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3934e431cd0b12f487d9e33471c1920387b35f413ef837fa730b6b40a429e0fc`  
		Last Modified: Mon, 22 Jan 2024 23:14:52 GMT  
		Size: 2.7 KB (2738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e07e019e5a02139d4eac8561ab0f18710974dad6439e27336de34c8b7e4640f`  
		Last Modified: Mon, 22 Jan 2024 23:14:52 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:5-php8.1-fpm-alpine` - linux; ppc64le

```console
$ docker pull joomla@sha256:0dc438f7824675d869e822dbaa3a42ddabee58f68fec2afe02228239d6ab8c1e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90232553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deca360e703610aae04a3841ddba7f5b1d91aee25fa2e9ab3ef879df34950914`
-	Entrypoint: `["\/entrypoint.sh"]`
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
# Tue, 12 Dec 2023 22:00:30 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 28 Dec 2023 00:37:41 GMT
ENV PHP_VERSION=8.1.27
# Thu, 28 Dec 2023 00:37:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Thu, 28 Dec 2023 00:37:42 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Thu, 28 Dec 2023 00:37:50 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 28 Dec 2023 00:37:50 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 28 Dec 2023 00:43:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 28 Dec 2023 00:43:08 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 28 Dec 2023 00:43:09 GMT
RUN docker-php-ext-enable sodium
# Thu, 28 Dec 2023 00:43:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 28 Dec 2023 00:43:09 GMT
WORKDIR /var/www/html
# Thu, 28 Dec 2023 00:43:10 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 28 Dec 2023 00:43:11 GMT
STOPSIGNAL SIGQUIT
# Thu, 28 Dec 2023 00:43:11 GMT
EXPOSE 9000
# Thu, 28 Dec 2023 00:43:11 GMT
CMD ["php-fpm"]
# Thu, 28 Dec 2023 01:35:14 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Thu, 28 Dec 2023 01:35:14 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Thu, 28 Dec 2023 01:35:22 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 		zstd 	;
# Thu, 28 Dec 2023 01:37:57 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.7.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Thu, 28 Dec 2023 01:37:58 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 28 Dec 2023 01:37:59 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 28 Dec 2023 01:37:59 GMT
VOLUME [/var/www/html]
# Tue, 09 Jan 2024 19:30:21 GMT
ENV JOOMLA_VERSION=5.0.2
# Tue, 09 Jan 2024 19:30:22 GMT
ENV JOOMLA_SHA512=e7bc9ecab410217fdf91a87f9461ff18dab311af56c61156fb7cf076b2fdf270b003ffddf131386ef35c94cb9f4ada39f8a69712c07664147108268ab5cc85a3
# Tue, 09 Jan 2024 19:30:32 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.0.2/Joomla_5.0.2-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla
# Mon, 22 Jan 2024 23:31:25 GMT
COPY file:6dcb949f1bfc58f87c0887173eb61a91c7f9c1290655683ed002e25b7aeb694a in /entrypoint.sh 
# Mon, 22 Jan 2024 23:31:25 GMT
COPY file:4365854cfba2f0673f4930c9c90629a51419815bb2048df2d1803bf1a9d79fd6 in /makedb.php 
# Mon, 22 Jan 2024 23:31:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jan 2024 23:31:26 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:243ac51c334a47917a84be93e972ee6378987e9b3b917a5a8df29025e161c1f3`  
		Last Modified: Fri, 08 Dec 2023 01:23:14 GMT  
		Size: 3.4 MB (3358233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89935d2f947cbd3585545f82639d347027ef82fbbf413f8684101953ea74bd6`  
		Last Modified: Tue, 12 Dec 2023 22:41:51 GMT  
		Size: 2.8 MB (2838539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b208bea042d5cdcbe6436f88d2f7ea51b03a91df91ae099118f57b644b87bdb2`  
		Last Modified: Tue, 12 Dec 2023 22:41:50 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dcb83a14858379fd485cb474c02417cd209b148b775365e9bae3ab90f5fe798`  
		Last Modified: Tue, 12 Dec 2023 22:41:50 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d5fd7610f006231467afb3e1bf1a78ae58009a26ff5bcbf66c29d704bbff6d`  
		Last Modified: Thu, 28 Dec 2023 01:10:05 GMT  
		Size: 11.9 MB (11935915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea24fce3c40554523cd23d89ce7029b4ea53b50be91051f4b01e8931eda3594f`  
		Last Modified: Thu, 28 Dec 2023 01:10:04 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55765a2471cd90d2a9f5ec9f53def7b5f5b41b233c07194244dfc6533739444`  
		Last Modified: Thu, 28 Dec 2023 01:10:36 GMT  
		Size: 13.0 MB (13039504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4328bb4adb18737305288c0e2f3186e11cfc4eeb8f179a0be5c2979aacbaf419`  
		Last Modified: Thu, 28 Dec 2023 01:10:33 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652c9c18dbe0975c3f9d844cf42ee54033184a129f0c9d5c7b3916b978acce96`  
		Last Modified: Thu, 28 Dec 2023 01:10:33 GMT  
		Size: 19.1 KB (19103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e477145b95f710ced9c0821a433efade91a54f69834318d2079a62764658edb`  
		Last Modified: Thu, 28 Dec 2023 01:10:33 GMT  
		Size: 8.9 KB (8876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db9732bd6fa7dd4b8c81b4093c7c100b0516ac8e7120dcaee7da52d4244dac66`  
		Last Modified: Thu, 28 Dec 2023 02:24:37 GMT  
		Size: 29.5 MB (29495465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5274a688abda62286748093f25410f055529163d9223d1f2bd2ba47ba2126a17`  
		Last Modified: Thu, 28 Dec 2023 02:24:33 GMT  
		Size: 7.0 MB (7020355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2e3eef6f239b117118000c77570d7a474924417abd7194e26f9b7a43e200a0`  
		Last Modified: Thu, 28 Dec 2023 02:24:30 GMT  
		Size: 61.4 KB (61354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ae0b34624b557bffa51239115673f17c523550e31120b7b803581e42c35cdf`  
		Last Modified: Thu, 28 Dec 2023 02:24:30 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19287a79c12118da836f985b00d232889ba5e8148d5cbc0fdad37d4125652b49`  
		Last Modified: Tue, 09 Jan 2024 19:37:04 GMT  
		Size: 22.4 MB (22446543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33ccab861e424a6d9c42b0241bd766a6fcf0073c5270d26e2d20d02f2194d7c9`  
		Last Modified: Mon, 22 Jan 2024 23:33:46 GMT  
		Size: 2.7 KB (2738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba0261f9451ae972f69a877f0ea85f128a4ba3aa742e7d7f76038a52b6dff51`  
		Last Modified: Mon, 22 Jan 2024 23:33:46 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:5-php8.1-fpm-alpine` - linux; s390x

```console
$ docker pull joomla@sha256:e005ffc39b203060bd3ca0e555a76e4d0a4e957c738f6a60f7a7f06c03fa9d83
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.8 MB (89752748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2556b14d3e9924c4871ae0596e7d21d64de5b06a9db2f3f71ed0967255207cd5`
-	Entrypoint: `["\/entrypoint.sh"]`
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
# Tue, 12 Dec 2023 21:24:49 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 27 Dec 2023 23:19:52 GMT
ENV PHP_VERSION=8.1.27
# Wed, 27 Dec 2023 23:19:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Wed, 27 Dec 2023 23:19:53 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Wed, 27 Dec 2023 23:19:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 27 Dec 2023 23:20:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 27 Dec 2023 23:25:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 27 Dec 2023 23:25:22 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 27 Dec 2023 23:25:23 GMT
RUN docker-php-ext-enable sodium
# Wed, 27 Dec 2023 23:25:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 27 Dec 2023 23:25:23 GMT
WORKDIR /var/www/html
# Wed, 27 Dec 2023 23:25:23 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 27 Dec 2023 23:25:23 GMT
STOPSIGNAL SIGQUIT
# Wed, 27 Dec 2023 23:25:23 GMT
EXPOSE 9000
# Wed, 27 Dec 2023 23:25:24 GMT
CMD ["php-fpm"]
# Thu, 28 Dec 2023 00:25:53 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Thu, 28 Dec 2023 00:25:53 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Thu, 28 Dec 2023 00:25:57 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 		zstd 	;
# Thu, 28 Dec 2023 00:27:40 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.7.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Thu, 28 Dec 2023 00:27:41 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 28 Dec 2023 00:27:41 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 28 Dec 2023 00:27:42 GMT
VOLUME [/var/www/html]
# Tue, 09 Jan 2024 19:42:40 GMT
ENV JOOMLA_VERSION=5.0.2
# Tue, 09 Jan 2024 19:42:40 GMT
ENV JOOMLA_SHA512=e7bc9ecab410217fdf91a87f9461ff18dab311af56c61156fb7cf076b2fdf270b003ffddf131386ef35c94cb9f4ada39f8a69712c07664147108268ab5cc85a3
# Tue, 09 Jan 2024 19:42:46 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.0.2/Joomla_5.0.2-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla
# Mon, 22 Jan 2024 23:49:26 GMT
COPY file:6dcb949f1bfc58f87c0887173eb61a91c7f9c1290655683ed002e25b7aeb694a in /entrypoint.sh 
# Mon, 22 Jan 2024 23:49:26 GMT
COPY file:4365854cfba2f0673f4930c9c90629a51419815bb2048df2d1803bf1a9d79fd6 in /makedb.php 
# Mon, 22 Jan 2024 23:49:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 22 Jan 2024 23:49:28 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e0180a7268e169fa6dd82fc04f9270dbd4fe716cf09b03fc82f84618025bad4`  
		Last Modified: Tue, 12 Dec 2023 22:07:16 GMT  
		Size: 2.9 MB (2937974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ecaefbf268f4b1e4d9f16c5d67523f3b76e72db0c3fc7a2f3fb6fd7fbdec547`  
		Last Modified: Tue, 12 Dec 2023 22:07:16 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f0d18e8f1067fcb105dea2ad180f140d138c6d99310025696d1aaa322017db`  
		Last Modified: Tue, 12 Dec 2023 22:07:16 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f97b96ef70a38faba8ef4787e09f02b7ca659119df67786f4f85fb197ea5de`  
		Last Modified: Wed, 27 Dec 2023 23:47:27 GMT  
		Size: 11.9 MB (11935924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37eef94665682c7d2f0bc56dff833d9f4302466b7ac0bfe3816cc1516d15cf90`  
		Last Modified: Wed, 27 Dec 2023 23:47:26 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe5148de5018eb87456d35ea1a8c601840767d9f54c3fd7056c56892e06270fe`  
		Last Modified: Wed, 27 Dec 2023 23:47:43 GMT  
		Size: 12.3 MB (12322549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11246d162a55292fc1f0406e68fa903dbb3e2106a67a6e3db76634d67aaa5810`  
		Last Modified: Wed, 27 Dec 2023 23:47:41 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84e2d095d04d08e98b8022eeafee1be3bb36cebfe2497baf5ffe11f60871cac9`  
		Last Modified: Wed, 27 Dec 2023 23:47:41 GMT  
		Size: 19.1 KB (19105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63d322b4dbc1888cb502178f5a3b9627add0711cfbac07ce86d154ee067771f`  
		Last Modified: Wed, 27 Dec 2023 23:47:41 GMT  
		Size: 8.9 KB (8876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437621bdeb492496ff2b0fdb9ed1a5c8a4342b4775aef087d252c2ca841748e4`  
		Last Modified: Thu, 28 Dec 2023 00:53:54 GMT  
		Size: 29.7 MB (29734266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:558facd0a383a2391d04d8b23e4feabdd6a523c1d7923586f592e289639f0a72`  
		Last Modified: Thu, 28 Dec 2023 00:53:50 GMT  
		Size: 7.0 MB (7035151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5f8f1ce44d4fca038c394f8dabd34aff579fbaafaa3052aeb6e64c259b8c40`  
		Last Modified: Thu, 28 Dec 2023 00:53:48 GMT  
		Size: 61.4 KB (61366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc54eca7243f5b5b1c0c73ad190709d27c3f431353e0243221bb6f317955fb1`  
		Last Modified: Thu, 28 Dec 2023 00:53:48 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3dbacda7eb7082fc5b047074ba0d835eb5ed46b57f9e76f86ab4ad73efde6a3`  
		Last Modified: Tue, 09 Jan 2024 19:47:30 GMT  
		Size: 22.4 MB (22446541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296db3515bb968afbaf055fef16f1be7ab686501cb4e7f9ac2b37c5bc7b69834`  
		Last Modified: Tue, 23 Jan 2024 00:12:32 GMT  
		Size: 2.7 KB (2738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1993c6ac5bab38a27f300ae8932ad1652981744e5fbf34a0a5cac46c28a913e1`  
		Last Modified: Tue, 23 Jan 2024 00:12:32 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
