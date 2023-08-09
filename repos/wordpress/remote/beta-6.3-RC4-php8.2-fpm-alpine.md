## `wordpress:beta-6.3-RC4-php8.2-fpm-alpine`

```console
$ docker pull wordpress@sha256:20e84f0518c0e617b99bcc2dbc752adf3e8b5264dbf4a72079b1729969433b78
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

### `wordpress:beta-6.3-RC4-php8.2-fpm-alpine` - linux; amd64

```console
$ docker pull wordpress@sha256:c753e03dbe4995d9c5d75687c3f5bb517304257f2e7fa93b89f6ce38cc201a4d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103608256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecfbdfbd15c1e7c27a04d967d64767253f43ffdb586d366b93879848ce0af3ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 14 Jun 2023 20:41:58 GMT
ADD file:1da756d12551a0e3e793e02ef87432d69d4968937bd11bed0af215db19dd94cd in / 
# Wed, 14 Jun 2023 20:41:59 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 00:31:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Jun 2023 00:31:26 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 15 Jun 2023 00:31:26 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 15 Jun 2023 00:31:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Jun 2023 00:31:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 15 Jun 2023 00:31:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jun 2023 00:31:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jun 2023 00:31:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Jun 2023 00:54:34 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Mon, 10 Jul 2023 22:18:20 GMT
ENV PHP_VERSION=8.2.8
# Mon, 10 Jul 2023 22:18:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.8.tar.xz.asc
# Mon, 10 Jul 2023 22:18:20 GMT
ENV PHP_SHA256=cfe1055fbcd486de7d3312da6146949aae577365808790af6018205567609801
# Mon, 10 Jul 2023 22:18:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Mon, 10 Jul 2023 22:18:27 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 10 Jul 2023 22:25:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 10 Jul 2023 22:25:25 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Mon, 10 Jul 2023 22:25:26 GMT
RUN docker-php-ext-enable sodium
# Mon, 10 Jul 2023 22:25:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 10 Jul 2023 22:25:27 GMT
WORKDIR /var/www/html
# Mon, 10 Jul 2023 22:25:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Mon, 10 Jul 2023 22:25:27 GMT
STOPSIGNAL SIGQUIT
# Mon, 10 Jul 2023 22:25:27 GMT
EXPOSE 9000
# Mon, 10 Jul 2023 22:25:27 GMT
CMD ["php-fpm"]
# Tue, 11 Jul 2023 03:53:33 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	;
# Tue, 11 Jul 2023 03:54:25 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Tue, 11 Jul 2023 03:54:27 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 11 Jul 2023 03:54:27 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Tue, 08 Aug 2023 00:26:09 GMT
RUN set -eux; 	version='6.3-RC4'; 	sha1='f714ca262c5566a0893ac4c5a42ce11b023695df'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content
# Tue, 08 Aug 2023 00:26:10 GMT
VOLUME [/var/www/html]
# Tue, 08 Aug 2023 00:26:10 GMT
COPY --chown=www-data:www-datafile:d38fd3c0db552e13465e83c5d7bbd85c7c3d036bf1285495988cc4ab2ffaf7f5 in /usr/src/wordpress/ 
# Tue, 08 Aug 2023 00:26:10 GMT
COPY file:5be6bcc31206cb827f037769d89fd092037ed61a1e10d6cae7939a37055beb4c in /usr/local/bin/ 
# Tue, 08 Aug 2023 00:26:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 00:26:10 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:31e352740f534f9ad170f75378a84fe453d6156e40700b882d737a8f4a6988a3`  
		Last Modified: Wed, 14 Jun 2023 20:42:26 GMT  
		Size: 3.4 MB (3397879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f034080c2b5d3afb2ec354e2b425f48df6326f28bcf3d2cee4ed50b9721ba482`  
		Last Modified: Thu, 15 Jun 2023 02:07:05 GMT  
		Size: 2.7 MB (2659635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b8701d6f7d5844dd4fa64c17ce3e1999f152f0dbfa3ea704bf38e8617e6b4d5`  
		Last Modified: Thu, 15 Jun 2023 02:07:05 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:259e9197ff8b826653ac60962d424d223ae725c1368f3fbd6efe6853200e945c`  
		Last Modified: Thu, 15 Jun 2023 02:07:04 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2392abb1ba7637b75a33ff6d92da9b21e06ad93e287aa70395423e70ab9cb71`  
		Last Modified: Mon, 10 Jul 2023 23:52:53 GMT  
		Size: 12.1 MB (12055821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d702db174c5d175eb9525ed88eece39997c57f2f6bc82af1ba9ae7f458ad04b0`  
		Last Modified: Mon, 10 Jul 2023 23:52:53 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50fcfcb8d4453617dcb0b8f904811afc7b24768c83c27b4f65bd8c172fd0e855`  
		Last Modified: Mon, 10 Jul 2023 23:53:36 GMT  
		Size: 12.7 MB (12700194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c47b10976e6437f5106ea36b9a59333e3c2876fd6e2d2440215030f7dfd18b`  
		Last Modified: Mon, 10 Jul 2023 23:53:34 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecd554125af07ddd61bef388e9945d8990c750dc0110d7a7506b5ff38234f8f2`  
		Last Modified: Mon, 10 Jul 2023 23:53:34 GMT  
		Size: 18.9 KB (18938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bcb66c14b0abcd802e3a2eee30d1aa7bdbba6e565a9496dcaa4adfd2f3bacb4`  
		Last Modified: Mon, 10 Jul 2023 23:53:34 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:871689940eed38546bc8ff4b361f787f09147b7d72d8fc2742adf8a4869023f0`  
		Last Modified: Tue, 11 Jul 2023 04:01:27 GMT  
		Size: 45.1 MB (45062396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf6d1ced3c791be98dcb4dc7fc5d0d4e728392087ee8810ba841824181db35d`  
		Last Modified: Tue, 11 Jul 2023 04:01:21 GMT  
		Size: 4.4 MB (4355069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e06d69b601f06bd4a9dcb339b4822c5403d4fa7788f3d8d1c95514fe4cb37f7`  
		Last Modified: Tue, 11 Jul 2023 04:01:18 GMT  
		Size: 66.4 KB (66366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2575dd96758d28e0969749cd174aaaa2def743f8bdae64389403951adb8ce5`  
		Last Modified: Tue, 11 Jul 2023 04:01:18 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9b47ad54dd17c1cb50bcd4d7c4e63208fc7771d9b858157bfbcf967e0ae962`  
		Last Modified: Tue, 08 Aug 2023 00:31:54 GMT  
		Size: 23.3 MB (23273830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee38fc52b0c6b332800c1f910c35257d5a9e26e58209d1be920be9cd33c97691`  
		Last Modified: Tue, 08 Aug 2023 00:31:50 GMT  
		Size: 2.3 KB (2349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9603d1e803aeb61d11f182dbafed81ad744c96af85ce5ad13f64c0babdf56547`  
		Last Modified: Tue, 08 Aug 2023 00:31:50 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:beta-6.3-RC4-php8.2-fpm-alpine` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:059a4799fdc5c40d0cd0acdd90bc1607581712b5ddeda3f2800c2910f8e120ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.0 MB (98013384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79743b32fbc11622925c6114311bca2d748582e9d21d7c9f57383660ae7dc071`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 00:06:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 09 Aug 2023 00:06:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 09 Aug 2023 00:06:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 09 Aug 2023 00:06:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 09 Aug 2023 00:06:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 09 Aug 2023 00:06:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 09 Aug 2023 00:06:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 09 Aug 2023 00:06:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 09 Aug 2023 00:24:44 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 09 Aug 2023 00:42:48 GMT
ENV PHP_VERSION=8.2.8
# Wed, 09 Aug 2023 00:42:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.8.tar.xz.asc
# Wed, 09 Aug 2023 00:42:48 GMT
ENV PHP_SHA256=cfe1055fbcd486de7d3312da6146949aae577365808790af6018205567609801
# Wed, 09 Aug 2023 00:42:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 09 Aug 2023 00:42:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 09 Aug 2023 00:48:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 09 Aug 2023 00:48:28 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 09 Aug 2023 00:48:29 GMT
RUN docker-php-ext-enable sodium
# Wed, 09 Aug 2023 00:48:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 09 Aug 2023 00:48:30 GMT
WORKDIR /var/www/html
# Wed, 09 Aug 2023 00:48:30 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 09 Aug 2023 00:48:30 GMT
STOPSIGNAL SIGQUIT
# Wed, 09 Aug 2023 00:48:30 GMT
EXPOSE 9000
# Wed, 09 Aug 2023 00:48:30 GMT
CMD ["php-fpm"]
# Wed, 09 Aug 2023 04:28:40 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	;
# Wed, 09 Aug 2023 04:29:34 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Wed, 09 Aug 2023 04:29:35 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Wed, 09 Aug 2023 04:29:35 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Wed, 09 Aug 2023 04:33:29 GMT
RUN set -eux; 	version='6.3-RC4'; 	sha1='f714ca262c5566a0893ac4c5a42ce11b023695df'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content
# Wed, 09 Aug 2023 04:33:29 GMT
VOLUME [/var/www/html]
# Wed, 09 Aug 2023 04:33:29 GMT
COPY --chown=www-data:www-datafile:d38fd3c0db552e13465e83c5d7bbd85c7c3d036bf1285495988cc4ab2ffaf7f5 in /usr/src/wordpress/ 
# Wed, 09 Aug 2023 04:33:29 GMT
COPY file:5be6bcc31206cb827f037769d89fd092037ed61a1e10d6cae7939a37055beb4c in /usr/local/bin/ 
# Wed, 09 Aug 2023 04:33:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Aug 2023 04:33:29 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c86f23b6f54d6e2a8ad7bd169a67e8c3b546cb7f2a7f2a6a59b252b11a54fd64`  
		Last Modified: Wed, 09 Aug 2023 01:35:32 GMT  
		Size: 2.7 MB (2666341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5831210199409c627f51822ba56a05e076469f5375f7841904326dd9ae6c8c3e`  
		Last Modified: Wed, 09 Aug 2023 01:35:31 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b818ba6e6fe1abab346c1e22bac5a61390d2b9d0909558a79ce40dac5f44e82e`  
		Last Modified: Wed, 09 Aug 2023 01:35:31 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1cfd8dbf828bbe0ed959fcb7ea32087fb564911e8d09d14d86b334584cae463`  
		Last Modified: Wed, 09 Aug 2023 01:38:43 GMT  
		Size: 12.1 MB (12055820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc68d84957095e9edd32c73299dff4a5a6fc7e8af477d38a77c6b283a96c98aa`  
		Last Modified: Wed, 09 Aug 2023 01:38:42 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c0fe5b0c7773934a65994dbc995465367ddbc5525ef3a80584e7713055b6842`  
		Last Modified: Wed, 09 Aug 2023 01:39:27 GMT  
		Size: 11.6 MB (11609871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfabf6f0ab1b8ef4be85c871db07c75ed67df8aef6b96c9a0005a6cea71248c8`  
		Last Modified: Wed, 09 Aug 2023 01:39:25 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03971a9b2441826bfc37ae6009766bda552611d7d321b4eca4271b31bc944f04`  
		Last Modified: Wed, 09 Aug 2023 01:39:25 GMT  
		Size: 18.7 KB (18743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51538831974f48091b6b70e0cbd9b13f8e5ed0f8220ac849f61871038513c22a`  
		Last Modified: Wed, 09 Aug 2023 01:39:25 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2280946a5f7fbf701eccfca4e12897376b7f479b1c6f8d24c9f305c9c4bcd6`  
		Last Modified: Wed, 09 Aug 2023 04:35:00 GMT  
		Size: 41.0 MB (40994296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b65b8c4857652bc1721e4c18f2ec3178043756579c16702c04f4ae7298cf5ea4`  
		Last Modified: Wed, 09 Aug 2023 04:34:54 GMT  
		Size: 4.2 MB (4165170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995acfd85228be4427066961507d64a3d538460afa34880277f97b21d7eaf3d5`  
		Last Modified: Wed, 09 Aug 2023 04:34:51 GMT  
		Size: 66.4 KB (66387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:546809fdc62c918073e1704a659f24e6e28c7f1ea761d17fe274d8177381a457`  
		Last Modified: Wed, 09 Aug 2023 04:34:51 GMT  
		Size: 388.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8ebbd967d57d5920bb275adc177c3fd9811e8dd4ac68d72124772690fe28436`  
		Last Modified: Wed, 09 Aug 2023 04:37:11 GMT  
		Size: 23.3 MB (23273827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8557a08801fe0a8cea43da4109bf9355aaf3b1c16b7f1c1e4ab0a9a385aede1`  
		Last Modified: Wed, 09 Aug 2023 04:37:07 GMT  
		Size: 2.3 KB (2347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996503483dda4b68ed91461d59710e501f0b7a612922f4209ae788c31483ffe7`  
		Last Modified: Wed, 09 Aug 2023 04:37:07 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:beta-6.3-RC4-php8.2-fpm-alpine` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:1cb7387fdc371f59873972ee71b6c6cce6dcfb8d303698fd09797aee067deaca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94698514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7a875e19fd4edc48aa21dc8b95f9f74a691028caff6bf3223e96103890ca783`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:25 GMT
ADD file:e3f56488d3d3bb67729714db13ddadf6652e7efb5281cfc7010d3e71f9d6607f in / 
# Mon, 07 Aug 2023 19:57:25 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 23:45:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 07 Aug 2023 23:45:02 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Mon, 07 Aug 2023 23:45:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 07 Aug 2023 23:45:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 07 Aug 2023 23:45:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 07 Aug 2023 23:45:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Aug 2023 23:45:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 07 Aug 2023 23:45:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 08 Aug 2023 00:01:01 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 08 Aug 2023 00:16:46 GMT
ENV PHP_VERSION=8.2.8
# Tue, 08 Aug 2023 00:16:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.8.tar.xz.asc
# Tue, 08 Aug 2023 00:16:46 GMT
ENV PHP_SHA256=cfe1055fbcd486de7d3312da6146949aae577365808790af6018205567609801
# Tue, 08 Aug 2023 00:16:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 08 Aug 2023 00:16:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 08 Aug 2023 00:21:44 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 08 Aug 2023 00:21:45 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 08 Aug 2023 00:21:46 GMT
RUN docker-php-ext-enable sodium
# Tue, 08 Aug 2023 00:21:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 08 Aug 2023 00:21:46 GMT
WORKDIR /var/www/html
# Tue, 08 Aug 2023 00:21:46 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Tue, 08 Aug 2023 00:21:47 GMT
STOPSIGNAL SIGQUIT
# Tue, 08 Aug 2023 00:21:47 GMT
EXPOSE 9000
# Tue, 08 Aug 2023 00:21:47 GMT
CMD ["php-fpm"]
# Tue, 08 Aug 2023 05:50:54 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	;
# Tue, 08 Aug 2023 05:51:45 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Tue, 08 Aug 2023 05:51:46 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 08 Aug 2023 05:51:47 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Tue, 08 Aug 2023 05:56:14 GMT
RUN set -eux; 	version='6.3-RC4'; 	sha1='f714ca262c5566a0893ac4c5a42ce11b023695df'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content
# Tue, 08 Aug 2023 05:56:14 GMT
VOLUME [/var/www/html]
# Tue, 08 Aug 2023 05:56:14 GMT
COPY --chown=www-data:www-datafile:d38fd3c0db552e13465e83c5d7bbd85c7c3d036bf1285495988cc4ab2ffaf7f5 in /usr/src/wordpress/ 
# Tue, 08 Aug 2023 05:56:14 GMT
COPY file:5be6bcc31206cb827f037769d89fd092037ed61a1e10d6cae7939a37055beb4c in /usr/local/bin/ 
# Tue, 08 Aug 2023 05:56:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 05:56:15 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f8dec92eec42224ef9e6ca9c6207ea6b9195dcf93d06bd5ceff0f814b62bf064`  
		Last Modified: Mon, 07 Aug 2023 19:57:55 GMT  
		Size: 2.9 MB (2899480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c53730165c5dd25f49dfa5e188b41f8d9be86e5e86adf6c765ceb1120853f36`  
		Last Modified: Tue, 08 Aug 2023 01:08:04 GMT  
		Size: 2.5 MB (2506232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10cb15fb50aac58af758965db75571d10382d95341fb109bee5260d370560772`  
		Last Modified: Tue, 08 Aug 2023 01:08:02 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe5f5b7d39cd3a05f25820f07393ecbd138724348b5cf7a7be272495f109290`  
		Last Modified: Tue, 08 Aug 2023 01:08:03 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ee51d65203f67afa9d2a8782fcb8a8b22452578a619b7e273af6e9fc70c39f`  
		Last Modified: Tue, 08 Aug 2023 01:12:03 GMT  
		Size: 12.1 MB (12055827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948a61c923c1739cea9e60cff8f3b52e1c1478581776ccb8e8bac0ef1b286eee`  
		Last Modified: Tue, 08 Aug 2023 01:12:02 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a33627aa3662355e9ce72ea1543b5bf6db661af4dcc2abfab3356a21d0caa5d9`  
		Last Modified: Tue, 08 Aug 2023 01:12:47 GMT  
		Size: 10.9 MB (10853713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9ccce5f89b46208fada43227c9faa6d5bc539aca495a71261d9416a4e89b65`  
		Last Modified: Tue, 08 Aug 2023 01:12:45 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565d7e26d0f2f898d9816149a1e871b854594ce2e789e21953a12c7ff76b69d5`  
		Last Modified: Tue, 08 Aug 2023 01:12:45 GMT  
		Size: 18.8 KB (18754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77dd0bbed9abfb59883d08eb6194538a1521f018539f643cbd0ec8e0fab9e203`  
		Last Modified: Tue, 08 Aug 2023 01:12:45 GMT  
		Size: 9.2 KB (9175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea753c12bd73dbcb09cd8a85aebcfdde754e46515ac0a48505c9f4d4504fa0a`  
		Last Modified: Tue, 08 Aug 2023 05:58:58 GMT  
		Size: 38.8 MB (38798655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85698a85efbbfc6cf9c3a44db06f0e10b4cdd7f05f9fa275ecee8e6145885e1d`  
		Last Modified: Tue, 08 Aug 2023 05:58:53 GMT  
		Size: 4.2 MB (4207529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d5ea156f3c822d146ea095355e757ecc42b198d49f10316a5d3512844a14bdb`  
		Last Modified: Tue, 08 Aug 2023 05:58:50 GMT  
		Size: 66.4 KB (66382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc45af27ab65e067216c8751f6cea67c40c3ee8afb087d5cbc9085cbcf854e0`  
		Last Modified: Tue, 08 Aug 2023 05:58:50 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa34501ee04587e8ee16b09fc6c6db82fc544cdb9a0dab3ecc52bc881ec04b76`  
		Last Modified: Tue, 08 Aug 2023 06:04:46 GMT  
		Size: 23.3 MB (23273830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb8a5c371ee96c291c29f58e1267cc3d55509c9f8ecc3002d7bde1c81369dd1d`  
		Last Modified: Tue, 08 Aug 2023 06:04:42 GMT  
		Size: 2.3 KB (2346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de2b5c4fdc7c85a66688d14f2a2c1c55c5ccde5cae31bd1c3cbeeaef088c376`  
		Last Modified: Tue, 08 Aug 2023 06:04:42 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:beta-6.3-RC4-php8.2-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:d3eb9b9c6df64e5eed6d91cfdcac12faeb44ca146484788f05dad421e70746d8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102861168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987d32e3d666f59919ea572ae6af7a8e99b717c928124980c6bfa9d33f03d1b0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 14 Jun 2023 20:48:58 GMT
ADD file:289c2fac17119508ced527225d445747cd177111b4a0018a6b04948ecb3b5e29 in / 
# Wed, 14 Jun 2023 20:48:58 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 03:05:37 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Jun 2023 03:05:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 15 Jun 2023 03:05:39 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 15 Jun 2023 03:05:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Jun 2023 03:05:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 15 Jun 2023 03:05:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jun 2023 03:05:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jun 2023 03:05:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Jun 2023 03:30:20 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Mon, 10 Jul 2023 23:02:37 GMT
ENV PHP_VERSION=8.2.8
# Mon, 10 Jul 2023 23:02:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.8.tar.xz.asc
# Mon, 10 Jul 2023 23:02:37 GMT
ENV PHP_SHA256=cfe1055fbcd486de7d3312da6146949aae577365808790af6018205567609801
# Mon, 10 Jul 2023 23:02:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Mon, 10 Jul 2023 23:02:44 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 10 Jul 2023 23:09:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 10 Jul 2023 23:09:39 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Mon, 10 Jul 2023 23:09:40 GMT
RUN docker-php-ext-enable sodium
# Mon, 10 Jul 2023 23:09:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 10 Jul 2023 23:09:40 GMT
WORKDIR /var/www/html
# Mon, 10 Jul 2023 23:09:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Mon, 10 Jul 2023 23:09:40 GMT
STOPSIGNAL SIGQUIT
# Mon, 10 Jul 2023 23:09:40 GMT
EXPOSE 9000
# Mon, 10 Jul 2023 23:09:41 GMT
CMD ["php-fpm"]
# Tue, 11 Jul 2023 04:18:42 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	;
# Tue, 11 Jul 2023 04:19:31 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Tue, 11 Jul 2023 04:19:32 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 11 Jul 2023 04:19:33 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Tue, 08 Aug 2023 00:07:56 GMT
RUN set -eux; 	version='6.3-RC4'; 	sha1='f714ca262c5566a0893ac4c5a42ce11b023695df'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content
# Tue, 08 Aug 2023 00:07:56 GMT
VOLUME [/var/www/html]
# Tue, 08 Aug 2023 00:07:57 GMT
COPY --chown=www-data:www-datafile:d38fd3c0db552e13465e83c5d7bbd85c7c3d036bf1285495988cc4ab2ffaf7f5 in /usr/src/wordpress/ 
# Tue, 08 Aug 2023 00:07:57 GMT
COPY file:5be6bcc31206cb827f037769d89fd092037ed61a1e10d6cae7939a37055beb4c in /usr/local/bin/ 
# Tue, 08 Aug 2023 00:07:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 00:07:57 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8c6d1654570f041603f4cef49c320c8f6f3e401324913009d92a19132cbf1ac0`  
		Last Modified: Wed, 14 Jun 2023 20:49:23 GMT  
		Size: 3.3 MB (3329251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68cbf4f33af4ff20fa90638cea5f48dda44f171afe80c0ca68a40b5c67ee1102`  
		Last Modified: Thu, 15 Jun 2023 04:39:12 GMT  
		Size: 2.7 MB (2696456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0262450c79d37bc5398bf1154c4bb2681100ef9caf7e008c5d0bd06c3d840a7`  
		Last Modified: Thu, 15 Jun 2023 04:39:11 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ca0f0b2514d4e2b8323c60eece66557c89959c380362deb6862fe5ffe3ad14`  
		Last Modified: Thu, 15 Jun 2023 04:39:11 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc9f367bc792d1e117225a211e2e4ae1221cc48c2a09615e05b0f75b630daff`  
		Last Modified: Tue, 11 Jul 2023 00:34:42 GMT  
		Size: 12.1 MB (12055813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e16d2a5e0aa3b2bb7f74ad466170e87dd144390e777cae42042bb91586e7e6`  
		Last Modified: Tue, 11 Jul 2023 00:34:41 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b65f2858856ac1a11d1f8cbfc9c040cd05d5f87e93e9203f964adbab55283f`  
		Last Modified: Tue, 11 Jul 2023 00:35:22 GMT  
		Size: 12.8 MB (12776345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c2ec79043bca7daf3545c835ffec84f78488080fbecf338067dd16f16c0f4d`  
		Last Modified: Tue, 11 Jul 2023 00:35:21 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea2a0ccf10156df06163ec516cc305621e515210b4c53e1685969337c29cd29`  
		Last Modified: Tue, 11 Jul 2023 00:35:21 GMT  
		Size: 18.7 KB (18707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e1b69f1a71736a433a47df7fb3cd181918d835df3766398e052b524644b010`  
		Last Modified: Tue, 11 Jul 2023 00:35:21 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a165f11217d7b6a6250f203057ddda7f97585c0e1af8c75d31ce3e983dfc01ed`  
		Last Modified: Tue, 11 Jul 2023 04:25:49 GMT  
		Size: 44.2 MB (44246734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:720c33b6692574194d1525a0b6a262458746b44250bc92bca3867b5c0037e85c`  
		Last Modified: Tue, 11 Jul 2023 04:25:45 GMT  
		Size: 4.4 MB (4379581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07ce44f697d5a7b7b3bff47065b4032630466ad3003fcbd6536be3f985b4d1e`  
		Last Modified: Tue, 11 Jul 2023 04:25:43 GMT  
		Size: 66.3 KB (66337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9560eda727c3643def96da41e38fdf3dab6015706fcebf3e292d796833aaa086`  
		Last Modified: Tue, 11 Jul 2023 04:25:42 GMT  
		Size: 391.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d2942b31c891abbed6a20104756f87b845986a5c6ebf0332024fc575de149b`  
		Last Modified: Tue, 08 Aug 2023 00:13:41 GMT  
		Size: 23.3 MB (23273821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5ccf6b5fc87f8a9957ded325eb11ba0f9e2e82feb413fe4e0d1f32002d01ce0`  
		Last Modified: Tue, 08 Aug 2023 00:13:38 GMT  
		Size: 2.4 KB (2350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383e753a4899aab46e4587d6eb2c58e040135b173196fa03693e0a5575005aac`  
		Last Modified: Tue, 08 Aug 2023 00:13:38 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:beta-6.3-RC4-php8.2-fpm-alpine` - linux; 386

```console
$ docker pull wordpress@sha256:56621088216d3bc9ba2af7754386769d752f273ba66780de806e4a709f2c52ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100714783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ffdb521fb633f3a0781e701d825034f1a4c479f23828390c1c4b90d8bbfed91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 07 Aug 2023 19:38:26 GMT
ADD file:4b33c52e11b19fde30197c62ead0b77bde28d34edaa08346a5302cd892d3cebe in / 
# Mon, 07 Aug 2023 19:38:27 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:13:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 08 Aug 2023 23:13:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Tue, 08 Aug 2023 23:13:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 08 Aug 2023 23:13:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 08 Aug 2023 23:13:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 08 Aug 2023 23:13:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 08 Aug 2023 23:13:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 08 Aug 2023 23:13:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 08 Aug 2023 23:51:54 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 09 Aug 2023 00:29:56 GMT
ENV PHP_VERSION=8.2.8
# Wed, 09 Aug 2023 00:29:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.8.tar.xz.asc
# Wed, 09 Aug 2023 00:29:56 GMT
ENV PHP_SHA256=cfe1055fbcd486de7d3312da6146949aae577365808790af6018205567609801
# Wed, 09 Aug 2023 00:30:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 09 Aug 2023 00:30:04 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 09 Aug 2023 00:42:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 09 Aug 2023 00:42:25 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 09 Aug 2023 00:42:26 GMT
RUN docker-php-ext-enable sodium
# Wed, 09 Aug 2023 00:42:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 09 Aug 2023 00:42:26 GMT
WORKDIR /var/www/html
# Wed, 09 Aug 2023 00:42:26 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 09 Aug 2023 00:42:27 GMT
STOPSIGNAL SIGQUIT
# Wed, 09 Aug 2023 00:42:27 GMT
EXPOSE 9000
# Wed, 09 Aug 2023 00:42:27 GMT
CMD ["php-fpm"]
# Wed, 09 Aug 2023 08:40:19 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	;
# Wed, 09 Aug 2023 08:41:25 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Wed, 09 Aug 2023 08:41:27 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Wed, 09 Aug 2023 08:41:27 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Wed, 09 Aug 2023 08:46:23 GMT
RUN set -eux; 	version='6.3-RC4'; 	sha1='f714ca262c5566a0893ac4c5a42ce11b023695df'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content
# Wed, 09 Aug 2023 08:46:24 GMT
VOLUME [/var/www/html]
# Wed, 09 Aug 2023 08:46:24 GMT
COPY --chown=www-data:www-datafile:d38fd3c0db552e13465e83c5d7bbd85c7c3d036bf1285495988cc4ab2ffaf7f5 in /usr/src/wordpress/ 
# Wed, 09 Aug 2023 08:46:24 GMT
COPY file:5be6bcc31206cb827f037769d89fd092037ed61a1e10d6cae7939a37055beb4c in /usr/local/bin/ 
# Wed, 09 Aug 2023 08:46:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Aug 2023 08:46:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:95dc695758361a4038a2d9026959d72e1f531114edb0341be7ce47d912ef069e`  
		Last Modified: Mon, 07 Aug 2023 19:38:56 GMT  
		Size: 3.2 MB (3235144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7b2187279b62839adee215aff0a17bafb09ccd31d0570c33d4e98042a183874`  
		Last Modified: Wed, 09 Aug 2023 03:11:03 GMT  
		Size: 2.7 MB (2702127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5141c6405baaddb270a3c61e413a7537d8dbc121079b59d34890bcc5924823d3`  
		Last Modified: Wed, 09 Aug 2023 03:11:02 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b100920b232fdc449e8cff1b9c496bf2866fe12c32e7153b97d586e7d2d609`  
		Last Modified: Wed, 09 Aug 2023 03:11:02 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8550b67f90ac511f8a355c4b4df40f82b531cf31dbd46b99819ebcdd24918734`  
		Last Modified: Wed, 09 Aug 2023 03:15:07 GMT  
		Size: 12.1 MB (12055824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675d3f72d1dda6333a7a4e70fa582f988dc2f9ef49cae942cc111b998a6f7d26`  
		Last Modified: Wed, 09 Aug 2023 03:15:06 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf4fce7701cbeda414e1afac15c6062f58fd642b74d862362131cc4c411bd5c`  
		Last Modified: Wed, 09 Aug 2023 03:15:53 GMT  
		Size: 12.9 MB (12898483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13bdc53b23156309973608d4269cda577ce8a0ba85a52e70fd19da3b81a61da9`  
		Last Modified: Wed, 09 Aug 2023 03:15:49 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864779f7eed15992c9477e53811029171167c7911c605ed4f90f44decf5477a6`  
		Last Modified: Wed, 09 Aug 2023 03:15:49 GMT  
		Size: 18.9 KB (18924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564816d26b6fbd4f2ddfa80488af2e319f5bcf130b3c2d2281355657e3e2e2c4`  
		Last Modified: Wed, 09 Aug 2023 03:15:49 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe548e5bf8de8a843e9ec83538773f1dd45c98fbdad9addf44ac46280fb9ea1`  
		Last Modified: Wed, 09 Aug 2023 08:50:29 GMT  
		Size: 42.0 MB (41956726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165faefb36cbdf06384928d534ae31e30ef8231cfd0d2b521b9e4d23f0d4eb43`  
		Last Modified: Wed, 09 Aug 2023 08:50:22 GMT  
		Size: 4.5 MB (4489246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e601f443dac91edc70d354bdaba56dfc18f9996cec85e9f7f8d70e99112eee86`  
		Last Modified: Wed, 09 Aug 2023 08:50:18 GMT  
		Size: 66.4 KB (66361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ab3c30913405ed55b5b69f2e925dd08728bd5d51a37bcc80a1015adee8820c`  
		Last Modified: Wed, 09 Aug 2023 08:50:18 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:323eb5e8323a513dc5b98280a6bf33fdbea2d2fdda40b0fb814f229c5d7b023b`  
		Last Modified: Wed, 09 Aug 2023 08:54:34 GMT  
		Size: 23.3 MB (23273819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894f2d20434fd976a40d1f68965c562e12164f692f90cc93e7c5c01dfbe5a34d`  
		Last Modified: Wed, 09 Aug 2023 08:54:29 GMT  
		Size: 2.3 KB (2348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f6eedb533c99c7e6ed54e50928a013dd4b786e4f4fc0ba7c9c007f8cd7a17b`  
		Last Modified: Wed, 09 Aug 2023 08:54:29 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:beta-6.3-RC4-php8.2-fpm-alpine` - linux; ppc64le

```console
$ docker pull wordpress@sha256:d803d02a7b8790b8236d161ca71cfc3bd4f01cfbf64954c54ed694e4959d742f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.1 MB (109100863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f81794e352c879983371495d44f719e4a620e411bb9f7250033461ce5af2553`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 15 Jun 2023 00:39:49 GMT
ADD file:694c636c0dd19fd01accbc189e4c1dc4d063952692c6e7eb26dce02a7adba833 in / 
# Thu, 15 Jun 2023 00:39:49 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 02:20:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Jun 2023 02:20:19 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 15 Jun 2023 02:20:20 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 15 Jun 2023 02:20:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Jun 2023 02:20:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 15 Jun 2023 02:20:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jun 2023 02:20:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jun 2023 02:20:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Jun 2023 02:46:03 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Mon, 10 Jul 2023 23:35:05 GMT
ENV PHP_VERSION=8.2.8
# Mon, 10 Jul 2023 23:35:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.8.tar.xz.asc
# Mon, 10 Jul 2023 23:35:06 GMT
ENV PHP_SHA256=cfe1055fbcd486de7d3312da6146949aae577365808790af6018205567609801
# Mon, 10 Jul 2023 23:35:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Mon, 10 Jul 2023 23:35:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 10 Jul 2023 23:43:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 10 Jul 2023 23:43:52 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Mon, 10 Jul 2023 23:43:56 GMT
RUN docker-php-ext-enable sodium
# Mon, 10 Jul 2023 23:43:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 10 Jul 2023 23:43:57 GMT
WORKDIR /var/www/html
# Mon, 10 Jul 2023 23:43:59 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Mon, 10 Jul 2023 23:43:59 GMT
STOPSIGNAL SIGQUIT
# Mon, 10 Jul 2023 23:43:59 GMT
EXPOSE 9000
# Mon, 10 Jul 2023 23:44:00 GMT
CMD ["php-fpm"]
# Tue, 11 Jul 2023 07:17:48 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	;
# Tue, 11 Jul 2023 07:19:37 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Tue, 11 Jul 2023 07:19:39 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 11 Jul 2023 07:19:40 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Tue, 08 Aug 2023 01:43:24 GMT
RUN set -eux; 	version='6.3-RC4'; 	sha1='f714ca262c5566a0893ac4c5a42ce11b023695df'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content
# Tue, 08 Aug 2023 01:43:27 GMT
VOLUME [/var/www/html]
# Tue, 08 Aug 2023 01:43:28 GMT
COPY --chown=www-data:www-datafile:d38fd3c0db552e13465e83c5d7bbd85c7c3d036bf1285495988cc4ab2ffaf7f5 in /usr/src/wordpress/ 
# Tue, 08 Aug 2023 01:43:28 GMT
COPY file:5be6bcc31206cb827f037769d89fd092037ed61a1e10d6cae7939a37055beb4c in /usr/local/bin/ 
# Tue, 08 Aug 2023 01:43:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 01:43:30 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ffa4a466dbb8eebd7e7f25590a9df12390de9016abf82279c29c9a64aa76491a`  
		Last Modified: Thu, 15 Jun 2023 00:40:26 GMT  
		Size: 3.3 MB (3344781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a82af153dde64aaecebbaa654ef25fe458cadc53b82b53ef2709b36ee12472`  
		Last Modified: Thu, 15 Jun 2023 04:11:27 GMT  
		Size: 2.7 MB (2743785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:513a439724cb0dce6489fcef92ec4c613854488cc971907f16b38f06ff6e8a14`  
		Last Modified: Thu, 15 Jun 2023 04:11:26 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60c5f3fdb07b83b724766e77b9ffeaaa86c0112dc077280c28d8ab36d1b52955`  
		Last Modified: Thu, 15 Jun 2023 04:11:26 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2f8de8efb5e3f0eacdfc5c9ee5c77495033c64695cf8b1bc4f82538d7d9f3d`  
		Last Modified: Tue, 11 Jul 2023 01:39:22 GMT  
		Size: 12.1 MB (12055817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd4ea97683ddbf39a918a6653c39e5671799725b6c63944d07ac43dd81e82303`  
		Last Modified: Tue, 11 Jul 2023 01:39:21 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:192834a44bde505d9fdb03302197a462f0793ae1888ed23ad196a6e04d0c5a95`  
		Last Modified: Tue, 11 Jul 2023 01:40:31 GMT  
		Size: 13.1 MB (13114643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3481e347725092d91dd7f24f84ac75bdec037802c60c4325628b89a78d8ba779`  
		Last Modified: Tue, 11 Jul 2023 01:40:28 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a49f59f655c90a428bfba7ddae16d6fca3210b609e01d9ecce32df27e46604`  
		Last Modified: Tue, 11 Jul 2023 01:40:28 GMT  
		Size: 18.7 KB (18727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226454baa51f25d9195c9aafa634f79add1cdf9877de03863895154f0731871b`  
		Last Modified: Tue, 11 Jul 2023 01:40:28 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcbf681c20cd6a433a993099b07ae2085bc0c3e03d570a08ee5e5c9cfa2d33fd`  
		Last Modified: Tue, 11 Jul 2023 07:32:02 GMT  
		Size: 49.9 MB (49934634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61354eca9c4dc74a5b2839ed2d2f4d166758d47241bbd67579087e05445ce89`  
		Last Modified: Tue, 11 Jul 2023 07:31:51 GMT  
		Size: 4.5 MB (4530156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82929ed520ed85df42116ec04a846a55f279f5060a8bd5bbb0caae2f91b9e758`  
		Last Modified: Tue, 11 Jul 2023 07:31:47 GMT  
		Size: 66.4 KB (66355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e5499443238dfaf1062d5c42544d4926a2cdb6d351a369ad7acad6b256a964`  
		Last Modified: Tue, 11 Jul 2023 07:31:47 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd79d68bab02e9be3eb7e0d411fbdae8f43eb46ff4108bf0582769f8a1cefb39`  
		Last Modified: Tue, 08 Aug 2023 01:53:17 GMT  
		Size: 23.3 MB (23273834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9862550168fd8241a7d5b87e06742ceaa14604564123ed0ae9aea01e847ab93d`  
		Last Modified: Tue, 08 Aug 2023 01:53:12 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e68d95e7446143d1b2bc4a1d9f6e3cc0ce462947a8fc06ee22a6d0aba154d9`  
		Last Modified: Tue, 08 Aug 2023 01:53:12 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:beta-6.3-RC4-php8.2-fpm-alpine` - linux; s390x

```console
$ docker pull wordpress@sha256:8684806ec163bd13815f66d3681d87db609f0536b8e862d2dcd343667b62b6fb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102523998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a51a02f4a96fe7da027f5598be3820c5cdcda0ef35c8572bcf3c57fba81b870`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 15 Jun 2023 05:18:38 GMT
ADD file:a59beca78118ebf4f86cc1685237dc3a29a519401a70668da520beaa3d29eb7a in / 
# Thu, 15 Jun 2023 05:18:38 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 18:32:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 15 Jun 2023 18:32:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Thu, 15 Jun 2023 18:32:20 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 15 Jun 2023 18:32:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 15 Jun 2023 18:32:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 15 Jun 2023 18:32:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jun 2023 18:32:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 15 Jun 2023 18:32:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 15 Jun 2023 19:09:45 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 11 Jul 2023 04:24:54 GMT
ENV PHP_VERSION=8.2.8
# Tue, 11 Jul 2023 04:24:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.8.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.8.tar.xz.asc
# Tue, 11 Jul 2023 04:24:55 GMT
ENV PHP_SHA256=cfe1055fbcd486de7d3312da6146949aae577365808790af6018205567609801
# Tue, 11 Jul 2023 04:24:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 11 Jul 2023 04:25:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 11 Jul 2023 04:31:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 11 Jul 2023 04:31:49 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 11 Jul 2023 04:31:50 GMT
RUN docker-php-ext-enable sodium
# Tue, 11 Jul 2023 04:31:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 11 Jul 2023 04:31:50 GMT
WORKDIR /var/www/html
# Tue, 11 Jul 2023 04:31:50 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Tue, 11 Jul 2023 04:31:50 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 Jul 2023 04:31:50 GMT
EXPOSE 9000
# Tue, 11 Jul 2023 04:31:51 GMT
CMD ["php-fpm"]
# Tue, 11 Jul 2023 07:42:33 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	;
# Tue, 11 Jul 2023 07:43:20 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Tue, 11 Jul 2023 07:43:21 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 11 Jul 2023 07:43:21 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Tue, 08 Aug 2023 05:57:06 GMT
RUN set -eux; 	version='6.3-RC4'; 	sha1='f714ca262c5566a0893ac4c5a42ce11b023695df'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content
# Tue, 08 Aug 2023 05:57:08 GMT
VOLUME [/var/www/html]
# Tue, 08 Aug 2023 05:57:08 GMT
COPY --chown=www-data:www-datafile:d38fd3c0db552e13465e83c5d7bbd85c7c3d036bf1285495988cc4ab2ffaf7f5 in /usr/src/wordpress/ 
# Tue, 08 Aug 2023 05:57:08 GMT
COPY file:5be6bcc31206cb827f037769d89fd092037ed61a1e10d6cae7939a37055beb4c in /usr/local/bin/ 
# Tue, 08 Aug 2023 05:57:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 05:57:08 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:998cc98447b44e5f0fe799dce691412796ba586ab22eb7c99aebf9d45f34833b`  
		Last Modified: Thu, 15 Jun 2023 05:29:38 GMT  
		Size: 3.2 MB (3213497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9863b5dcc3e5885fe5ff8335b86d4287dfd59b451fe22e94b79f83b396c3776d`  
		Last Modified: Thu, 15 Jun 2023 21:54:07 GMT  
		Size: 2.8 MB (2766871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f159305449b6c309659dadfedb968259be79e6f5b9f552d97134f0a94490ae8`  
		Last Modified: Thu, 15 Jun 2023 21:54:07 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e5f78cdbb2bcfe6b24c6cc002d51d1551a0fbabd06fa3baaee2be566d6d55f`  
		Last Modified: Thu, 15 Jun 2023 21:54:07 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db651d70c1113ea67c57f04de6578937a1822d540ea190adb9b62b74c523f671`  
		Last Modified: Tue, 11 Jul 2023 05:40:13 GMT  
		Size: 12.1 MB (12055817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d0fcf43facc9ad25e15871e8a258d7f3294f702dc8444ab7a1f9d25cf8fa7f`  
		Last Modified: Tue, 11 Jul 2023 05:40:12 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e26acc5519ff9a9e1fc7d193d951f53492d466e64789675f4d9ebf1e47a03d`  
		Last Modified: Tue, 11 Jul 2023 05:40:39 GMT  
		Size: 11.9 MB (11859192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e056fdfeb3b2acccdab7cd7babd09d90c23c21bfce505cf809b66708b28c4b21`  
		Last Modified: Tue, 11 Jul 2023 05:40:37 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddb21b31515b037f99c0a8d964321a389cea0310755e0fe81bca9f916e60b6fb`  
		Last Modified: Tue, 11 Jul 2023 05:40:37 GMT  
		Size: 18.8 KB (18755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40a685e272409810914224b8b0a6aac843e3271f790ec89b7a24ac6c039bf3d`  
		Last Modified: Tue, 11 Jul 2023 05:40:37 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed22155ac335b258eba15a14cf585cf0ee63108af7e8a3254742930d400cd00`  
		Last Modified: Tue, 11 Jul 2023 07:50:48 GMT  
		Size: 44.8 MB (44784373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9408583f22cec2a6eeef7759812ad3a86d6ad70cf6b69cf21b81e527976ac9c3`  
		Last Modified: Tue, 11 Jul 2023 07:50:42 GMT  
		Size: 4.5 MB (4467607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c650f08145decdf570a42328fdceeee318a387a30b4df1b1d8b9bfad956b0564`  
		Last Modified: Tue, 11 Jul 2023 07:50:41 GMT  
		Size: 65.9 KB (65919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b8f02734ddeeaba30a57f7b41ae8feff51b5d2914ca0c12e8f7c7a9b4b2efc`  
		Last Modified: Tue, 11 Jul 2023 07:50:41 GMT  
		Size: 390.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a374c23c7865b8f42c31e8736bc4eae0b577b65155ee7872ddd52360fc87a0aa`  
		Last Modified: Tue, 08 Aug 2023 06:02:21 GMT  
		Size: 23.3 MB (23273844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:884f42a74319a1bc0e31e91fc8f3d4cc017c39abbdba770046820747a41af5c2`  
		Last Modified: Tue, 08 Aug 2023 06:02:17 GMT  
		Size: 2.4 KB (2352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de698b8e5664abc5dd5b0fb97c3e845a873cdb382dbfbf6e80a2dbeb4475d9e0`  
		Last Modified: Tue, 08 Aug 2023 06:02:17 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
