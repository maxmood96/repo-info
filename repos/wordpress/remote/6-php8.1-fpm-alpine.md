## `wordpress:6-php8.1-fpm-alpine`

```console
$ docker pull wordpress@sha256:731e5cf3e728cd853a1cf02a25442394e8d95af64d35ffdd8d1871d834d578da
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

### `wordpress:6-php8.1-fpm-alpine` - linux; amd64

```console
$ docker pull wordpress@sha256:571a2082322b5a93d64cfcfdda76a650f75a2e84f48dd9dafdcf73bd85c73ae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95163806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e0a9b9bfb8029c1fba8fea0f32240d2d779f0ff348d5e1490dc1a762d45b4b4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 23:41:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Dec 2025 23:41:21 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Dec 2025 23:41:21 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Dec 2025 23:41:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Dec 2025 23:41:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Dec 2025 23:41:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 23:41:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 23:41:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Dec 2025 23:41:21 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 19 Dec 2025 23:41:21 GMT
ENV PHP_VERSION=8.1.34
# Fri, 19 Dec 2025 23:41:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.34.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.34.tar.xz.asc
# Fri, 19 Dec 2025 23:41:21 GMT
ENV PHP_SHA256=ffa9e0982e82eeaea848f57687b425ed173aa278fe563001310ae2638db5c251
# Fri, 19 Dec 2025 23:41:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Dec 2025 23:41:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 23:44:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/a5df26691d1b1f71b964b869510473a5d5413999.patch?full_index=1' -o 19131.patch; 	echo 'c98c01c74d3a6da197116f8511b16fed361ca6bbb6a8af8df629a933f541c213 *19131.patch' | sha256sum -c -; 	patch --reverse -p1 < 19131.patch; 	rm 19131.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Dec 2025 23:44:05 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 23:44:05 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Dec 2025 23:44:06 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Dec 2025 23:44:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Dec 2025 23:44:06 GMT
WORKDIR /var/www/html
# Fri, 19 Dec 2025 23:44:06 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 19 Dec 2025 23:44:06 GMT
STOPSIGNAL SIGQUIT
# Fri, 19 Dec 2025 23:44:06 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 19 Dec 2025 23:44:06 GMT
CMD ["php-fpm"]
# Sat, 20 Dec 2025 00:07:12 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Sat, 20 Dec 2025 00:07:52 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Sat, 20 Dec 2025 00:07:52 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Sat, 20 Dec 2025 00:07:52 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Sat, 20 Dec 2025 00:07:54 GMT
RUN set -eux; 	version='6.9'; 	sha1='256dda5bb6a43aecd806b7a62528f442c06e6c25'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Sat, 20 Dec 2025 00:07:54 GMT
VOLUME [/var/www/html]
# Sat, 20 Dec 2025 00:07:54 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Sat, 20 Dec 2025 00:07:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 20 Dec 2025 00:07:54 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Sat, 20 Dec 2025 00:07:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 20 Dec 2025 00:07:54 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Sun, 07 Dec 2025 13:55:07 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5823d25b8955e44538154830ce6d55097606e79a2fe36b98e13c7264892e8d92`  
		Last Modified: Fri, 19 Dec 2025 23:44:20 GMT  
		Size: 3.4 MB (3367613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657eb7e9377fcdba324c8e5d43df8144f19ad2f647ae4562a21ededdc026360e`  
		Last Modified: Fri, 19 Dec 2025 23:44:20 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e2f214ed0fddbcd46ed372f3556bb0fa659a8978d1dfd7547bef1bd4d0b95b0`  
		Last Modified: Fri, 19 Dec 2025 23:44:20 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d74968981c27c48e1c996cec5f522fb6ed7bd64de1cb726b35690d329f75a4`  
		Last Modified: Fri, 19 Dec 2025 23:44:21 GMT  
		Size: 11.9 MB (11925150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bba1af80346106c5f13e1556f244a886bab6e5c20b5f78b28bbfecc51111a2`  
		Last Modified: Fri, 19 Dec 2025 23:44:20 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebfe12b6fda245f8de2e6cc37e7639385e9e896e4bb3357142a71be05c6de033`  
		Last Modified: Fri, 19 Dec 2025 23:44:21 GMT  
		Size: 12.7 MB (12744137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58ac6cf34be031b78628306028cb0395fedab066fa79ba9050a3fd1398190e5`  
		Last Modified: Fri, 19 Dec 2025 23:44:20 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a99cc297df1d51f3024e17a30d7e1fa12319db95364599c5bfb6635bfe0e5f0`  
		Last Modified: Fri, 19 Dec 2025 23:44:20 GMT  
		Size: 20.0 KB (19960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b0ee28409c950761b258d86823115ef911e4b33268717db12f3f4392f5ce1e`  
		Last Modified: Fri, 19 Dec 2025 23:44:20 GMT  
		Size: 20.0 KB (19956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f50fda9bccfe4017b13bbdf10e332e88ae1dc654a08d85faf2a56db4c6f77f18`  
		Last Modified: Fri, 19 Dec 2025 23:44:20 GMT  
		Size: 8.9 KB (8875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd69e2cf3be521ae7263c551f5cb12d9518be788e6b7c2e62b64d24b0748b45`  
		Last Modified: Sat, 20 Dec 2025 00:08:22 GMT  
		Size: 28.2 MB (28238138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd9a084a1a4e7bf8220effcfb1df3631b6d6eb70667cfc9e386f2c03f3fc0a6`  
		Last Modified: Sat, 20 Dec 2025 00:08:23 GMT  
		Size: 8.2 MB (8162964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8018ea7187d585bc450a10095b455926af940a55932cfd2648faf45c1bce3757`  
		Last Modified: Sat, 20 Dec 2025 00:08:21 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e6bfc966bdc838fabcfe75e82d504822ff5578fdfc7dd7a0815b816369d222`  
		Last Modified: Sat, 20 Dec 2025 00:08:21 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915b9f0ad1d4bb7e91ebb99eaa87569f64c7ceb78e5d15e5f13a1369352563fd`  
		Last Modified: Sat, 20 Dec 2025 00:08:24 GMT  
		Size: 27.0 MB (27025234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f990eb70730af8b7d0a2685bc6a957551cffd2e8ef8d18ba3de2ecc5350d1d`  
		Last Modified: Sat, 20 Dec 2025 00:08:21 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503ad25d3a03f11e9f3c82428a1402e7703afa81bf47f0d4505047b74adfe5a0`  
		Last Modified: Sat, 20 Dec 2025 00:08:21 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd6fa45a9a4d3b35ccc124e1841b2d3872663088077404c506fa3e991bd47e9`  
		Last Modified: Sat, 20 Dec 2025 00:08:21 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:f39446801286b2822204990e8f9b1938eb09f70229d0c4431bee234a50801a15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1128457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670ecd8699e6ec4249b508f2218134317598d72d57f84c07a29cef4ed3437387`

```dockerfile
```

-	Layers:
	-	`sha256:5cecdf4ec6fd8d24fc3ca4617f448339f131261f594fce19af9ffa5088a8d626`  
		Last Modified: Sat, 20 Dec 2025 02:14:22 GMT  
		Size: 1.1 MB (1076735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a69125e797414df9f1dcde9b199bb014453e68220aaf9467dfd58dbd790b1474`  
		Last Modified: Sat, 20 Dec 2025 02:14:23 GMT  
		Size: 51.7 KB (51722 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.1-fpm-alpine` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:d480fcdc1c4caa9005877e457e76a15da2d6ba96eef36ea52386fdcef29c9dcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88726123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:436745246eedceab979aeac03f488233623b6b4d0ea0e711b69cd07bca8c13e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 23:44:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Dec 2025 23:44:48 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Dec 2025 23:44:48 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Dec 2025 23:44:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Dec 2025 23:44:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Dec 2025 23:44:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 23:44:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 23:44:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Dec 2025 23:44:48 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 19 Dec 2025 23:44:48 GMT
ENV PHP_VERSION=8.1.34
# Fri, 19 Dec 2025 23:44:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.34.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.34.tar.xz.asc
# Fri, 19 Dec 2025 23:44:48 GMT
ENV PHP_SHA256=ffa9e0982e82eeaea848f57687b425ed173aa278fe563001310ae2638db5c251
# Fri, 19 Dec 2025 23:44:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Dec 2025 23:44:52 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 23:47:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/a5df26691d1b1f71b964b869510473a5d5413999.patch?full_index=1' -o 19131.patch; 	echo 'c98c01c74d3a6da197116f8511b16fed361ca6bbb6a8af8df629a933f541c213 *19131.patch' | sha256sum -c -; 	patch --reverse -p1 < 19131.patch; 	rm 19131.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Dec 2025 23:47:37 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 23:47:37 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Dec 2025 23:47:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Dec 2025 23:47:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Dec 2025 23:47:38 GMT
WORKDIR /var/www/html
# Fri, 19 Dec 2025 23:47:38 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 19 Dec 2025 23:47:38 GMT
STOPSIGNAL SIGQUIT
# Fri, 19 Dec 2025 23:47:38 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 19 Dec 2025 23:47:38 GMT
CMD ["php-fpm"]
# Sat, 20 Dec 2025 00:06:10 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Sat, 20 Dec 2025 00:07:06 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Sat, 20 Dec 2025 00:07:06 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Sat, 20 Dec 2025 00:07:06 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Sat, 20 Dec 2025 00:07:08 GMT
RUN set -eux; 	version='6.9'; 	sha1='256dda5bb6a43aecd806b7a62528f442c06e6c25'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Sat, 20 Dec 2025 00:07:08 GMT
VOLUME [/var/www/html]
# Sat, 20 Dec 2025 00:07:08 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Sat, 20 Dec 2025 00:07:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 20 Dec 2025 00:07:08 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Sat, 20 Dec 2025 00:07:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 20 Dec 2025 00:07:08 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f8b30cbd0fab9e5a803578a09c973d18d7450816d914e63e04e5c2edd79f8bee`  
		Last Modified: Mon, 08 Dec 2025 00:04:31 GMT  
		Size: 3.4 MB (3365468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b5e087361fff3c19271771ccb36f8b3a3c7c3a5e1904037c899cb9283d8702`  
		Last Modified: Fri, 19 Dec 2025 23:47:52 GMT  
		Size: 3.3 MB (3337565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:174a6fcd1af1ac4d91cefa1aab72dc2e035bc857b1d180638d196c1ede1a206a`  
		Last Modified: Fri, 19 Dec 2025 23:47:51 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069994c88742eab8797dac0226a0796dfe53cb498354b10211cd96380ce56c52`  
		Last Modified: Fri, 19 Dec 2025 23:47:51 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6dae8b281c78153c1ce3ba7b6443a5f68645ef823977adb394d9680605351d`  
		Last Modified: Fri, 19 Dec 2025 23:47:52 GMT  
		Size: 11.9 MB (11925156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd80c6d264c1e16016da32a732fd2b8a7d7a9a5630c1556faef792af25e4e0f3`  
		Last Modified: Fri, 19 Dec 2025 23:47:51 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2936d9d8fb91b6a42bef8dfc3a11c5a2f97b5582de972adec5af98eca58fff1b`  
		Last Modified: Fri, 19 Dec 2025 23:47:53 GMT  
		Size: 11.5 MB (11472277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0656fe02fae38a3de47551515def0402aa14f0222c788292260e922652d75783`  
		Last Modified: Fri, 19 Dec 2025 23:47:51 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f464c3110b3fd8fdbd275d0cdcda9526b8a2b530bcca1c2f097f4ed87c5d8bb6`  
		Last Modified: Fri, 19 Dec 2025 23:47:51 GMT  
		Size: 19.8 KB (19775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9ecc9aa7219d3154a7065b102eaebe23bf8483a801d3e590b9f025de60b310`  
		Last Modified: Fri, 19 Dec 2025 23:47:51 GMT  
		Size: 19.8 KB (19770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b00e037f8ad9efa480399438f91cb21681b71bc7f5cc5e10b26d43646310114c`  
		Last Modified: Fri, 19 Dec 2025 23:47:51 GMT  
		Size: 8.9 KB (8878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9604eb4d8515a55d526ab20dc0ca5fd75ec4140c7a2b3725d0f7a29173d44d12`  
		Last Modified: Sat, 20 Dec 2025 00:07:25 GMT  
		Size: 24.3 MB (24341871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadbbf12a37764051507c6a9cc898c8d8ed92c2690d5ce7eaef3ff4b9657afdd`  
		Last Modified: Sat, 20 Dec 2025 00:07:22 GMT  
		Size: 7.2 MB (7200914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d9f2f15cc73fcc271416f3bb13c1e55a06ff436a82ab782ab0bb7d190afde8`  
		Last Modified: Sat, 20 Dec 2025 00:07:22 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ed2b6150245cbefa49432b21d26a8ccc1b4c7444259517bc55eaf30a9262b5b`  
		Last Modified: Sat, 20 Dec 2025 00:07:22 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69cda9c575bc7d239ab04a618c963b9829bfd4a050032478269e9e220f8ce29`  
		Last Modified: Sat, 20 Dec 2025 00:07:24 GMT  
		Size: 27.0 MB (27025236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4baae3ffd557427a95517e242dd85434eb41472b95f7814fc7332bd5a95a3a1e`  
		Last Modified: Sat, 20 Dec 2025 00:07:22 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff2e4b439a1523a754506326cd2d893a9cde7c14dca05917a203fcdccfb41f76`  
		Last Modified: Sat, 20 Dec 2025 00:07:22 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e67597fee8a302260af5c79e2f7ada5d571505cbc9e9d7e4e59fb55f07678808`  
		Last Modified: Sat, 20 Dec 2025 00:07:23 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:5ce0eb6e2559ab220707cc75278e1d03a23203fe950aa5b92ef45c4d1f9dcaf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 KB (51652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:864686a7acb12a5aa9f7875a92273d245bd60f64ccb5cfa3d7665fde52a75550`

```dockerfile
```

-	Layers:
	-	`sha256:bc760b791073577b851702993b7b4ddb0590727421620fdb1280b0668ef9e2f5`  
		Last Modified: Sat, 20 Dec 2025 02:14:26 GMT  
		Size: 51.7 KB (51652 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.1-fpm-alpine` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:f61f7367a78da889aa3887b5525e2b471419c9ea08cec1d6dac5bcda427ce4d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.6 MB (87609697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae81f4e3c5aba5674609ba35616da4e7493903b222b50e7242c4e9b0288b0785`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 23:47:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Dec 2025 23:47:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Dec 2025 23:47:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Dec 2025 23:47:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Dec 2025 23:47:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Dec 2025 23:47:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 23:47:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 23:47:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Dec 2025 23:47:55 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 19 Dec 2025 23:47:55 GMT
ENV PHP_VERSION=8.1.34
# Fri, 19 Dec 2025 23:47:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.34.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.34.tar.xz.asc
# Fri, 19 Dec 2025 23:47:55 GMT
ENV PHP_SHA256=ffa9e0982e82eeaea848f57687b425ed173aa278fe563001310ae2638db5c251
# Fri, 19 Dec 2025 23:47:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Dec 2025 23:47:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 23:50:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/a5df26691d1b1f71b964b869510473a5d5413999.patch?full_index=1' -o 19131.patch; 	echo 'c98c01c74d3a6da197116f8511b16fed361ca6bbb6a8af8df629a933f541c213 *19131.patch' | sha256sum -c -; 	patch --reverse -p1 < 19131.patch; 	rm 19131.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Dec 2025 23:50:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 23:50:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Dec 2025 23:50:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Dec 2025 23:50:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Dec 2025 23:50:56 GMT
WORKDIR /var/www/html
# Fri, 19 Dec 2025 23:50:56 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 19 Dec 2025 23:50:56 GMT
STOPSIGNAL SIGQUIT
# Fri, 19 Dec 2025 23:50:56 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 19 Dec 2025 23:50:56 GMT
CMD ["php-fpm"]
# Sat, 20 Dec 2025 00:07:46 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Sat, 20 Dec 2025 00:08:46 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Sat, 20 Dec 2025 00:08:46 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Sat, 20 Dec 2025 00:08:46 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Sat, 20 Dec 2025 00:08:48 GMT
RUN set -eux; 	version='6.9'; 	sha1='256dda5bb6a43aecd806b7a62528f442c06e6c25'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Sat, 20 Dec 2025 00:08:48 GMT
VOLUME [/var/www/html]
# Sat, 20 Dec 2025 00:08:48 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Sat, 20 Dec 2025 00:08:48 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 20 Dec 2025 00:08:48 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Sat, 20 Dec 2025 00:08:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 20 Dec 2025 00:08:48 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:520d06ecc3ba4ec2920319fa6f2cc6bea9a9c1d5a43808c1d2388522c37d7b30`  
		Last Modified: Sun, 07 Dec 2025 17:58:54 GMT  
		Size: 3.1 MB (3098611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e2dc8efcbf2cedc6e1dcf552d4d9d66bd79b16963dbb1e0759f1b3d82870881`  
		Last Modified: Fri, 19 Dec 2025 23:51:10 GMT  
		Size: 3.1 MB (3143719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fd7773ca4b73c93012225538597894c202e9930a8547e3f9201155f562e51f`  
		Last Modified: Fri, 19 Dec 2025 23:51:10 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c51e40ff5c9debfa9d07fa9c857273eae3e0d968b6363eddd429ececbf7916d`  
		Last Modified: Fri, 19 Dec 2025 23:51:10 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d599ffa634bafe39f65c193c467745e7dca505eaacd8d6d80ecac6e58db6809b`  
		Last Modified: Fri, 19 Dec 2025 23:51:10 GMT  
		Size: 11.9 MB (11925153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef5feb9364f2f789c9f470526a3e27cf4ea543631165721486420d7b01827f83`  
		Last Modified: Fri, 19 Dec 2025 23:51:10 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:788da9ab81befb359fdb5303ab606b53547a0dfb46c04ad209134c273b418110`  
		Last Modified: Fri, 19 Dec 2025 23:51:11 GMT  
		Size: 10.8 MB (10806145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68d5359f184f14de3c361c0eeb5c0a3bc50e03de7b4bf2d86ec760111467965`  
		Last Modified: Fri, 19 Dec 2025 23:51:10 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5d84c42cfbd42661cc2745d5a9a9f0d627eec1765df0b0ba1b856e186600d6`  
		Last Modified: Fri, 19 Dec 2025 23:51:10 GMT  
		Size: 19.8 KB (19778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aac8f452dde0115d15d0463ed1c9f10a8cf565786c3944c9791fac79963b7238`  
		Last Modified: Fri, 19 Dec 2025 23:51:10 GMT  
		Size: 19.8 KB (19774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c1a6e7f640fc868029b18a323f860d4a573de06ae56045ca7197a300a4b52e`  
		Last Modified: Fri, 19 Dec 2025 23:51:10 GMT  
		Size: 8.9 KB (8875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da85becb693a0f42b4218fd30ca30b3b0e1e76fc0f16730443638abe225979c4`  
		Last Modified: Sat, 20 Dec 2025 00:09:07 GMT  
		Size: 23.1 MB (23119263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c26c23431451ee0b05e750f51e3e29d1051cc5450494eb9c7ade83bda395c0f`  
		Last Modified: Sat, 20 Dec 2025 00:09:06 GMT  
		Size: 8.4 MB (8433934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61bd75acb9415e3f6ed357f90d73e4012b2b803e809dd3665352863d08847520`  
		Last Modified: Sat, 20 Dec 2025 00:09:06 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b45c9598ad50fe96db5134a05db4003f3b9ffb15016bc31f20993a81e8bc040`  
		Last Modified: Sat, 20 Dec 2025 00:09:06 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34cfbf9d81a6bc860d9c1223bdb33cccc0eae3c7cc66c9b2c940d51556978890`  
		Last Modified: Sat, 20 Dec 2025 00:09:08 GMT  
		Size: 27.0 MB (27025230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0cc61d68f85c69a913e45484c569ee78096bfe10ed9de9377fcc46acee26df`  
		Last Modified: Sat, 20 Dec 2025 00:09:06 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9ac912e9ac87bffddc8ebd2e48dd1afb2fea7510f51f2e2ce8f647d98e524bf`  
		Last Modified: Sat, 20 Dec 2025 00:09:06 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2119b2fcb27f389fe20430853bb325112420813e8a786a65756a774ce609641d`  
		Last Modified: Sat, 20 Dec 2025 00:09:06 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:024926f310f7304e76110c5f1bdeb0bdeac3fdf88ef42593867ff0db72e81e6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1127395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b4291c3069870eb12003e48844724c54905dba30daaa38dcf4a9fff29ff604`

```dockerfile
```

-	Layers:
	-	`sha256:9e2e8173cb52d704f784897f85255420090a77b9b96e711de7b2b6f894bc989d`  
		Last Modified: Sat, 20 Dec 2025 02:14:34 GMT  
		Size: 1.1 MB (1075527 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ae3f2fa5dccfde9c208195af89cb4bf77a9f95429ec95266d1f7e008edbd431`  
		Last Modified: Sat, 20 Dec 2025 02:14:35 GMT  
		Size: 51.9 KB (51868 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.1-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:d39e56f238668c8b319b024a54bda3270b592950759cd5c55f66789ec148c03b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95868751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f58a714c117e3ab1e45d4620a77dd2305fdab5f5b65e410c8d3b338da2bf594d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 23:41:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Dec 2025 23:41:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Dec 2025 23:41:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Dec 2025 23:41:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Dec 2025 23:41:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Dec 2025 23:41:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 23:41:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 23:41:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Dec 2025 23:41:27 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 19 Dec 2025 23:41:27 GMT
ENV PHP_VERSION=8.1.34
# Fri, 19 Dec 2025 23:41:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.34.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.34.tar.xz.asc
# Fri, 19 Dec 2025 23:41:27 GMT
ENV PHP_SHA256=ffa9e0982e82eeaea848f57687b425ed173aa278fe563001310ae2638db5c251
# Fri, 19 Dec 2025 23:41:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Dec 2025 23:41:31 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 23:45:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/a5df26691d1b1f71b964b869510473a5d5413999.patch?full_index=1' -o 19131.patch; 	echo 'c98c01c74d3a6da197116f8511b16fed361ca6bbb6a8af8df629a933f541c213 *19131.patch' | sha256sum -c -; 	patch --reverse -p1 < 19131.patch; 	rm 19131.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Dec 2025 23:45:50 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 23:45:51 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Dec 2025 23:45:52 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Dec 2025 23:45:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Dec 2025 23:45:52 GMT
WORKDIR /var/www/html
# Fri, 19 Dec 2025 23:45:52 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 19 Dec 2025 23:45:52 GMT
STOPSIGNAL SIGQUIT
# Fri, 19 Dec 2025 23:45:52 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 19 Dec 2025 23:45:52 GMT
CMD ["php-fpm"]
# Sat, 20 Dec 2025 00:07:05 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Sat, 20 Dec 2025 00:07:58 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Sat, 20 Dec 2025 00:07:58 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Sat, 20 Dec 2025 00:07:58 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Sat, 20 Dec 2025 00:08:00 GMT
RUN set -eux; 	version='6.9'; 	sha1='256dda5bb6a43aecd806b7a62528f442c06e6c25'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Sat, 20 Dec 2025 00:08:00 GMT
VOLUME [/var/www/html]
# Sat, 20 Dec 2025 00:08:00 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Sat, 20 Dec 2025 00:08:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 20 Dec 2025 00:08:00 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Sat, 20 Dec 2025 00:08:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 20 Dec 2025 00:08:00 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Sun, 07 Dec 2025 17:54:48 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c38715603d8c09e111573f07db1db2a984d14e909fd6a5395455d477374459`  
		Last Modified: Fri, 19 Dec 2025 23:46:07 GMT  
		Size: 3.4 MB (3361731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1daf0b36a35d6057712a8fa9a8a55933916cd172b25c70b424866604d2b413e4`  
		Last Modified: Fri, 19 Dec 2025 23:46:07 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4978ba80c2ceab51b216a4a53086570011d301cb338aba4eef38f9f9fd7725`  
		Last Modified: Fri, 19 Dec 2025 23:46:07 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5207ad1f9fa7454bd87b6f0661c6ad934e748495e0539135db528b489f60ee61`  
		Last Modified: Fri, 19 Dec 2025 23:46:08 GMT  
		Size: 11.9 MB (11925164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1476ac8ae08f00f36a6a49c1145635d354431336857a7b58c01200ae4dac6ac8`  
		Last Modified: Fri, 19 Dec 2025 23:46:07 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083c66aedf88577840fa949b7facdbb52bf96bc84d1623adf8640545db223203`  
		Last Modified: Fri, 19 Dec 2025 23:46:08 GMT  
		Size: 12.7 MB (12731822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76f2e91111ac8ee89b63eb65da1a20ee01f276a93ef7e9b0b7adffc389737442`  
		Last Modified: Fri, 19 Dec 2025 23:46:07 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f7f781117608501bac0f1e2d2293dbf91d32abd730a15f72b0d55ce8b37b50`  
		Last Modified: Fri, 19 Dec 2025 23:46:07 GMT  
		Size: 19.8 KB (19779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4923d24532526b6ba91981f7fb1ffb5e3c483721121a5cbbe044c7e4c587f2cf`  
		Last Modified: Fri, 19 Dec 2025 23:46:07 GMT  
		Size: 19.8 KB (19778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db45ca96a1122b59767736d8b66fd0e97f05c261eed10907b7bdf2a97bf1281`  
		Last Modified: Fri, 19 Dec 2025 23:46:07 GMT  
		Size: 8.9 KB (8877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857d7b0964842fcc841ffb349da082bd452ff21339e0bb16fcf9c0a9216c3746`  
		Last Modified: Sat, 20 Dec 2025 00:08:19 GMT  
		Size: 28.1 MB (28057135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe626843bbf7bef4d05f905f2b739f4f3b1c0564bc38f80a156182eb6a0718a4`  
		Last Modified: Sat, 20 Dec 2025 00:08:18 GMT  
		Size: 8.7 MB (8717693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f54056e5da070593d820cae92009b53de306a135c1b32b63d18c2c1aa13268`  
		Last Modified: Sat, 20 Dec 2025 00:08:16 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25605837e1070b439f1c29ac2e7396daec42f98147ab0441ba3264f57bdf5b38`  
		Last Modified: Sat, 20 Dec 2025 00:08:18 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f76ccf59d8b0ec6ac0c34e75f1d5dbcb7b60b833d7f4e3da99102b08da2b574`  
		Last Modified: Sat, 20 Dec 2025 00:08:22 GMT  
		Size: 27.0 MB (27025210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2fa0227107de18b0b3a03533c591208208c08ab9776887c973a45f923deee6`  
		Last Modified: Sat, 20 Dec 2025 00:08:16 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e168d6e618f4eba06b6b0d83fda7735252fc2ef1414fe6492f7e79af226276`  
		Last Modified: Sat, 20 Dec 2025 00:08:16 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500929a954a79794afce2fd67bfdc809e5c616a31235c9a1fab485ed9132a7eb`  
		Last Modified: Sat, 20 Dec 2025 00:08:16 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:f03e8c59a7d287fe60dc7cef551ac2f360c0d7101e336d7fcae03823b50c2466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1127449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:950c27fa986b751136e7be8f186786e33534319659d65d5c412108df0f35126a`

```dockerfile
```

-	Layers:
	-	`sha256:86ce99f8ded6c56a99eff1c0207f246b4f041b5eba083744fdf48943937e497e`  
		Last Modified: Sat, 20 Dec 2025 02:14:41 GMT  
		Size: 1.1 MB (1075547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9884825eac5738c74312db6d1a86a977a0c18bca6884e621ccb14c7df5bf96ab`  
		Last Modified: Sat, 20 Dec 2025 02:14:41 GMT  
		Size: 51.9 KB (51902 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.1-fpm-alpine` - linux; 386

```console
$ docker pull wordpress@sha256:80d4bc7c50b39a1be78384eecbedc7ebc89daabc880451b021a49a3f528e64a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.4 MB (94424409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6371ff30e8204f8d2938363d0ec5d1db2516635565437a69cdffc5a6e0075412`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 23:44:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Dec 2025 23:44:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Dec 2025 23:44:51 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Dec 2025 23:44:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Dec 2025 23:44:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Dec 2025 23:44:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 23:44:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 23:44:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Dec 2025 23:44:51 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 19 Dec 2025 23:44:51 GMT
ENV PHP_VERSION=8.1.34
# Fri, 19 Dec 2025 23:44:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.34.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.34.tar.xz.asc
# Fri, 19 Dec 2025 23:44:51 GMT
ENV PHP_SHA256=ffa9e0982e82eeaea848f57687b425ed173aa278fe563001310ae2638db5c251
# Fri, 19 Dec 2025 23:44:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Dec 2025 23:44:54 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 23:48:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/a5df26691d1b1f71b964b869510473a5d5413999.patch?full_index=1' -o 19131.patch; 	echo 'c98c01c74d3a6da197116f8511b16fed361ca6bbb6a8af8df629a933f541c213 *19131.patch' | sha256sum -c -; 	patch --reverse -p1 < 19131.patch; 	rm 19131.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Dec 2025 23:48:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 23:48:25 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Dec 2025 23:48:26 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Dec 2025 23:48:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Dec 2025 23:48:26 GMT
WORKDIR /var/www/html
# Fri, 19 Dec 2025 23:48:26 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 19 Dec 2025 23:48:26 GMT
STOPSIGNAL SIGQUIT
# Fri, 19 Dec 2025 23:48:26 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 19 Dec 2025 23:48:26 GMT
CMD ["php-fpm"]
# Sat, 20 Dec 2025 00:07:47 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Sat, 20 Dec 2025 00:08:41 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Sat, 20 Dec 2025 00:08:41 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Sat, 20 Dec 2025 00:08:41 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Sat, 20 Dec 2025 00:08:42 GMT
RUN set -eux; 	version='6.9'; 	sha1='256dda5bb6a43aecd806b7a62528f442c06e6c25'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Sat, 20 Dec 2025 00:08:43 GMT
VOLUME [/var/www/html]
# Sat, 20 Dec 2025 00:08:43 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Sat, 20 Dec 2025 00:08:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 20 Dec 2025 00:08:43 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Sat, 20 Dec 2025 00:08:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 20 Dec 2025 00:08:43 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:bbedd1c05bb5090fc3fc2356be88d60b2a60937565b56e91fb4be42c5c73d485`  
		Last Modified: Sun, 07 Dec 2025 18:13:29 GMT  
		Size: 3.5 MB (3464704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc9c124fff6896921bff14f6a6c2a39d383c472b3e7eb987c62cf2d1721fc2b`  
		Last Modified: Fri, 19 Dec 2025 23:48:39 GMT  
		Size: 3.4 MB (3411348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c900988c7c1c5650d71a9b49769b4ea1baf08c1c66f7a6c1bf94fda0b75198f`  
		Last Modified: Fri, 19 Dec 2025 23:48:38 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c140cde6f36ccf3a48fe849f7d5c571f5344d18b3a6dcfd263531b3b892264`  
		Last Modified: Fri, 19 Dec 2025 23:48:38 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac86b8a23e3af0856a05020368d014496278981b416d11f2dbbc5b3aa3dc01c8`  
		Last Modified: Fri, 19 Dec 2025 23:48:40 GMT  
		Size: 11.9 MB (11925155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc07d320e819a6be8f6633edaa9abbd283eec709d98833c0f80ed6953e232584`  
		Last Modified: Fri, 19 Dec 2025 23:48:38 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2488b03654b87ee7dc0af1c9fee4d2ad18d8e0f6de20a7eb20a8e6bf45aacf9`  
		Last Modified: Fri, 19 Dec 2025 23:48:40 GMT  
		Size: 13.1 MB (13054701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4468c1bd60ccb8cf14eabd89ac3e0d8f043c2b5cd293278c2c9b1be7a3a50851`  
		Last Modified: Fri, 19 Dec 2025 23:48:38 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8264e5ca7d7e876aaad6f6231fd01a86753bc498a32b8e6bf81913dbb056fbc4`  
		Last Modified: Fri, 19 Dec 2025 23:48:38 GMT  
		Size: 20.0 KB (19965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb74f07ae6483850fc74519134f76d2ec37bf4f72d97a23db49a0a3c69d152c`  
		Last Modified: Fri, 19 Dec 2025 23:48:38 GMT  
		Size: 20.0 KB (19961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:742d1c70533b56f83426176a8d1bab7d1b395c8a69e0e0f5f47ea0fd8828d476`  
		Last Modified: Fri, 19 Dec 2025 23:48:38 GMT  
		Size: 8.9 KB (8879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0102e65308dff9ab0907a652c6429b7fd556b7248e9edfa59d9e86263d9702`  
		Last Modified: Sat, 20 Dec 2025 00:09:03 GMT  
		Size: 28.5 MB (28456950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea951a5d990ec03aa9d3242fde72a6d1b6be3abe6d9f74bb6ef5a57615c91110`  
		Last Modified: Sat, 20 Dec 2025 00:09:01 GMT  
		Size: 7.0 MB (7028308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61f8c73f595de4fae313e9661a308d8277caf064e53440141552cbbed35471d`  
		Last Modified: Sat, 20 Dec 2025 00:09:01 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebaafe82a89124383b66c3ee4f452a5238d93c61a215a6cd852e57551c57be2`  
		Last Modified: Sat, 20 Dec 2025 00:09:01 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1112fec8fac5954e1697f1eb3260412fe241d6e7e5894efb9f1e0cb53c7662`  
		Last Modified: Sat, 20 Dec 2025 00:09:05 GMT  
		Size: 27.0 MB (27025215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82467dbcb795ae029cbcb7f90dc5d63e0567c4031673cba02fdb692ac41b955d`  
		Last Modified: Sat, 20 Dec 2025 00:09:01 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6916bb6f2871313fb64f1f59ae2ba4e1548110e9052c470e77076dc698a66e`  
		Last Modified: Sat, 20 Dec 2025 00:09:01 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214fad0ab61f3422889ecd90f7315b38545258d979015670441868c7aeb4147d`  
		Last Modified: Sat, 20 Dec 2025 00:09:01 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:4d6ea3eb529d7753df2b222aabd54ba776e9280446cdd96df13a7f2885a68643
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1128391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acab79b40bf66fcfdde8597361220674966c59917931eb54cf366736c3df9c94`

```dockerfile
```

-	Layers:
	-	`sha256:dee0d42ba50324f8f327db1a7e3e5f3740b01fe3ce58bf9cb7c9a662d62bd7a8`  
		Last Modified: Sat, 20 Dec 2025 02:14:45 GMT  
		Size: 1.1 MB (1076710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea131786280a6fbbfdb416ef6bb5cff732863552520f5632ab7795c8422a11aa`  
		Last Modified: Sat, 20 Dec 2025 02:14:46 GMT  
		Size: 51.7 KB (51681 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.1-fpm-alpine` - linux; ppc64le

```console
$ docker pull wordpress@sha256:618dc172309f7da26c8f5ef6453cec51ecc84d841baaceefffd3e182760b7a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96255310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a7cd5c5b11b0ade0c18e96bd94f1ea8edd4ba8b3ca238467e9f9d1b7b378a9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-ppc64le.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Sat, 20 Dec 2025 00:04:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 20 Dec 2025 00:04:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 20 Dec 2025 00:04:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 20 Dec 2025 00:04:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 20 Dec 2025 00:04:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 20 Dec 2025 00:04:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 20 Dec 2025 00:04:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 20 Dec 2025 00:04:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 20 Dec 2025 00:04:07 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 20 Dec 2025 00:04:07 GMT
ENV PHP_VERSION=8.1.34
# Sat, 20 Dec 2025 00:04:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.34.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.34.tar.xz.asc
# Sat, 20 Dec 2025 00:04:07 GMT
ENV PHP_SHA256=ffa9e0982e82eeaea848f57687b425ed173aa278fe563001310ae2638db5c251
# Sat, 20 Dec 2025 00:04:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Sat, 20 Dec 2025 00:04:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 20 Dec 2025 00:12:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/a5df26691d1b1f71b964b869510473a5d5413999.patch?full_index=1' -o 19131.patch; 	echo 'c98c01c74d3a6da197116f8511b16fed361ca6bbb6a8af8df629a933f541c213 *19131.patch' | sha256sum -c -; 	patch --reverse -p1 < 19131.patch; 	rm 19131.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 20 Dec 2025 00:12:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 20 Dec 2025 00:12:42 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 20 Dec 2025 00:12:43 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 20 Dec 2025 00:12:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 20 Dec 2025 00:12:44 GMT
WORKDIR /var/www/html
# Sat, 20 Dec 2025 00:12:44 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 20 Dec 2025 00:12:44 GMT
STOPSIGNAL SIGQUIT
# Sat, 20 Dec 2025 00:12:44 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 20 Dec 2025 00:12:44 GMT
CMD ["php-fpm"]
# Sat, 20 Dec 2025 01:10:03 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Sat, 20 Dec 2025 01:11:17 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Sat, 20 Dec 2025 01:11:20 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Sat, 20 Dec 2025 01:11:21 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Sat, 20 Dec 2025 01:11:26 GMT
RUN set -eux; 	version='6.9'; 	sha1='256dda5bb6a43aecd806b7a62528f442c06e6c25'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Sat, 20 Dec 2025 01:11:27 GMT
VOLUME [/var/www/html]
# Sat, 20 Dec 2025 01:11:27 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Sat, 20 Dec 2025 01:11:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 20 Dec 2025 01:11:27 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Sat, 20 Dec 2025 01:11:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 20 Dec 2025 01:11:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:e99908f6ead74bb809123fe0d40505509ed6113949496be71629433c6ea3fa1a`  
		Last Modified: Sun, 07 Dec 2025 17:58:56 GMT  
		Size: 3.6 MB (3574075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8234c75cdf8473830bd6b3512561730e81ee79b867090fd2073159b1bddc031b`  
		Last Modified: Sat, 20 Dec 2025 00:08:31 GMT  
		Size: 3.5 MB (3514047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1956d0ce9ac6ee1796e3d5aedf7f8bddae2ad668111123c81bee12693cb3f98`  
		Last Modified: Sat, 20 Dec 2025 00:08:30 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe395c5bdd710299e5c2fc0c342d124306ed28c306010d563e5e04b3adb57f6`  
		Last Modified: Sat, 20 Dec 2025 00:08:31 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3e1037f14e3dd9036390ccf109a5f230ec1dafadd79f5d212965ea206135af`  
		Last Modified: Sat, 20 Dec 2025 00:08:32 GMT  
		Size: 11.9 MB (11925152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84aaa0283012556b1c167c4a608fb3d77cfaeaf3c608cb48768206b57c98c4bf`  
		Last Modified: Sat, 20 Dec 2025 00:08:30 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7914f5feaf525a8ac66afb3c90042180f407a3af43a43c5a2d8e2f249eb81eab`  
		Last Modified: Sat, 20 Dec 2025 00:13:14 GMT  
		Size: 13.1 MB (13148825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2aecc5405b0136dc3c299593a04aeccd0bded13581a594327e1d67261a7ada`  
		Last Modified: Sat, 20 Dec 2025 00:13:13 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734d1eaceb5f2c2074a27099290cf7b5ae542e2495e6cfa591eab8c25d3f8aab`  
		Last Modified: Sat, 20 Dec 2025 00:13:13 GMT  
		Size: 19.8 KB (19776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:728875e760a3092be11a5a00e7b543e86d93e18794c70a2b84a19434d3a34469`  
		Last Modified: Sat, 20 Dec 2025 00:13:13 GMT  
		Size: 19.8 KB (19772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b46bd198336616c8a7d78751970fe3cab3277b8be25e1523f3cb0739249caa`  
		Last Modified: Sat, 20 Dec 2025 00:13:14 GMT  
		Size: 8.9 KB (8881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bfc2fe44006fe923837d555f4ca07cff30e5b6751d9673dee9db4b3a7149393`  
		Last Modified: Sat, 20 Dec 2025 01:12:00 GMT  
		Size: 28.9 MB (28889330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d815641547760ef089eeb86d07246a5080f94e6b869341520a0d988d2ae9f09`  
		Last Modified: Sat, 20 Dec 2025 01:12:02 GMT  
		Size: 8.1 MB (8120987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c190216ef61685502ca42173ce590b4ef2fee60ac10d422e5a25f6720fdf164`  
		Last Modified: Sat, 20 Dec 2025 01:11:58 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006536dd25fbc373c7d4662f01aa74fa9d84b6a94c47de1211e5e85f01f16b39`  
		Last Modified: Sat, 20 Dec 2025 01:11:58 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a972559997d13faf24ada1b4050392a029b1e1c2600fda866ab3b1820fd06dc4`  
		Last Modified: Sat, 20 Dec 2025 01:12:01 GMT  
		Size: 27.0 MB (27025233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50b26d6d4b5efe4a201f6fddb0682a0fe1e8c9d03de35a28613cfe96de16427a`  
		Last Modified: Sat, 20 Dec 2025 01:11:57 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b861bd4d2981e0125dc44629f02a5bacbb4e7113ceb6e2975f38db67f0d093`  
		Last Modified: Sat, 20 Dec 2025 01:11:58 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bef09b261266d16cd52286dc6df9b8c19dc57d15ead78e70701201cac44bf84`  
		Last Modified: Sat, 20 Dec 2025 01:11:57 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:21bf917f050785f971cb9d7e4440d9c3b70c8b92a1da53858bc9b3357165639c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1125349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd686b2faba4932121bd2e2ecd2683a284427fffc59209f9b7d723e33651f642`

```dockerfile
```

-	Layers:
	-	`sha256:58ac92c4a918fc90328caed09b8756edc8d32d18edd1265439b1471bc4830e4c`  
		Last Modified: Sat, 20 Dec 2025 02:14:49 GMT  
		Size: 1.1 MB (1073574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3597915326f158d4afe7ceba83678f1772805400b9b2c8981fcf63c3a77a7cf`  
		Last Modified: Sat, 20 Dec 2025 02:14:50 GMT  
		Size: 51.8 KB (51775 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.1-fpm-alpine` - linux; riscv64

```console
$ docker pull wordpress@sha256:9be74b0cb971588ce69950dd19453a6a4bde34ec938354f517be69a699e994fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.4 MB (92432142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0fe5e2d676de7e8e00708b0652ddf9b217184862822b959b8a196364bc4090`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-riscv64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Mon, 22 Dec 2025 11:22:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Dec 2025 11:22:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 22 Dec 2025 11:22:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 22 Dec 2025 11:22:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Dec 2025 11:22:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 22 Dec 2025 11:22:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Dec 2025 11:22:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Dec 2025 11:22:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 22 Dec 2025 11:22:33 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Mon, 22 Dec 2025 11:22:33 GMT
ENV PHP_VERSION=8.1.34
# Mon, 22 Dec 2025 11:22:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.34.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.34.tar.xz.asc
# Mon, 22 Dec 2025 11:22:33 GMT
ENV PHP_SHA256=ffa9e0982e82eeaea848f57687b425ed173aa278fe563001310ae2638db5c251
# Mon, 22 Dec 2025 11:22:48 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Mon, 22 Dec 2025 11:22:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 22 Dec 2025 12:56:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/a5df26691d1b1f71b964b869510473a5d5413999.patch?full_index=1' -o 19131.patch; 	echo 'c98c01c74d3a6da197116f8511b16fed361ca6bbb6a8af8df629a933f541c213 *19131.patch' | sha256sum -c -; 	patch --reverse -p1 < 19131.patch; 	rm 19131.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 22 Dec 2025 12:56:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 22 Dec 2025 12:56:43 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 22 Dec 2025 12:56:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 22 Dec 2025 12:56:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 22 Dec 2025 12:56:49 GMT
WORKDIR /var/www/html
# Mon, 22 Dec 2025 12:56:49 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 22 Dec 2025 12:56:49 GMT
STOPSIGNAL SIGQUIT
# Mon, 22 Dec 2025 12:56:49 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 22 Dec 2025 12:56:49 GMT
CMD ["php-fpm"]
# Tue, 23 Dec 2025 11:47:52 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 23 Dec 2025 11:57:45 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 23 Dec 2025 11:57:45 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 23 Dec 2025 11:57:46 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 23 Dec 2025 11:57:55 GMT
RUN set -eux; 	version='6.9'; 	sha1='256dda5bb6a43aecd806b7a62528f442c06e6c25'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 23 Dec 2025 11:57:55 GMT
VOLUME [/var/www/html]
# Tue, 23 Dec 2025 11:57:55 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 23 Dec 2025 11:57:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Dec 2025 11:57:56 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 23 Dec 2025 11:57:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Dec 2025 11:57:56 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f874295bfcd01a87ee99265d45f0786d35242cd9d53bc2744cb330bf3be277f5`  
		Last Modified: Mon, 08 Dec 2025 00:04:31 GMT  
		Size: 3.4 MB (3351001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f41eecec29b983cc160ebd5420aeb9cbdc0bc7dada24be2ee2af08da7d6745`  
		Last Modified: Mon, 22 Dec 2025 12:10:02 GMT  
		Size: 3.5 MB (3492727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11dfb72afe5ade2a15528dfe0f5978060feb5b1c80a8c967d18994615a9b934d`  
		Last Modified: Mon, 22 Dec 2025 12:10:01 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f75a55b15ff95403dc014548b648585b407a9482e528203f5271e9fef2e8338`  
		Last Modified: Mon, 22 Dec 2025 12:10:01 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c1c015c37e8c080b2af75447028afd13d6d5c8589875da0fc0ab9267cb7da6`  
		Last Modified: Mon, 22 Dec 2025 12:10:03 GMT  
		Size: 11.9 MB (11925145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de661dc473b18d5e6daacbf4344c373cc5ba57f7d3808cec80042aecb3ee101a`  
		Last Modified: Mon, 22 Dec 2025 12:10:01 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baab38da285b45325b9ab76b4b667e76588c46a0bae471f0f27e357fce31a5ab`  
		Last Modified: Mon, 22 Dec 2025 12:57:46 GMT  
		Size: 12.0 MB (11993246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebd84d1fef2e050e05f3f9d0d68d679afc3d6256027793258aa518f975083dc`  
		Last Modified: Mon, 22 Dec 2025 12:57:45 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68d4b835bd93bce03e8144dc8940230fc6e31857bad0c4a840557abbef0833ca`  
		Last Modified: Mon, 22 Dec 2025 12:57:45 GMT  
		Size: 19.8 KB (19764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f328a0459c9c838b6dc358012f1d2d8731b64fc2d69023fceda6e134f9f50e48`  
		Last Modified: Mon, 22 Dec 2025 12:57:45 GMT  
		Size: 19.8 KB (19763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1598654857a7fa670baccaadd57aa7b72392eba17f166935c8a4aebb78a2857f`  
		Last Modified: Mon, 22 Dec 2025 12:57:45 GMT  
		Size: 8.9 KB (8881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176993adf56ec164c44aa03ddcd46dacb98218ee78bc62bf7e81e95829713f68`  
		Last Modified: Tue, 23 Dec 2025 11:59:48 GMT  
		Size: 28.0 MB (28049236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0fa6245f02881df27610eab96d31c9fa0d409c1f809f90dee0e61d3aa81eb70`  
		Last Modified: Tue, 23 Dec 2025 11:59:42 GMT  
		Size: 6.5 MB (6537912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6be0dc4d0300842a32e60157ee0e41fd7d0842901d6cb808173b51c0a7f4b3`  
		Last Modified: Tue, 23 Dec 2025 11:59:39 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45512f055fe23da26a86f1f5fb45d0b2b234a21e9e7dfff37a5df0ab278d1da`  
		Last Modified: Tue, 23 Dec 2025 11:59:39 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa69e30fe3ba52607c263c1c62fb25160cf40776d8472b93d72d998c24c7eefb`  
		Last Modified: Tue, 23 Dec 2025 11:59:48 GMT  
		Size: 27.0 MB (27025222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f51a10b2b46ec251fd60920bbdd45ee977c872e23fb084cb016a22f54816fb1`  
		Last Modified: Tue, 23 Dec 2025 11:59:41 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543ee78838d3e42b5c82ec6af34c3e258d5cd4f618fa0999f332694801e7316e`  
		Last Modified: Tue, 23 Dec 2025 11:59:43 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ae00e1839af70139158f1dd5dd53b447b8ea38e59d88351c3b627256c766f5`  
		Last Modified: Tue, 23 Dec 2025 11:59:43 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:c29207cad5b49f104b25eb73f00ebae8df8e79ac325fdd8997c7aa1bb49a166a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1125347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ec0e9cad694c33a98b1eb4d21f0c9c69568fc3992031c9e251757996a09210`

```dockerfile
```

-	Layers:
	-	`sha256:ecd7aa971a38f1db25076119281b16d38c210ecce2cc544d52b069047ff93b81`  
		Last Modified: Tue, 23 Dec 2025 14:13:05 GMT  
		Size: 1.1 MB (1073570 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0d2be3b530169464294ae9264d975d88385cdd7b9eff4fb78d8995cf3a92ec8`  
		Last Modified: Tue, 23 Dec 2025 14:13:06 GMT  
		Size: 51.8 KB (51777 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.1-fpm-alpine` - linux; s390x

```console
$ docker pull wordpress@sha256:4c2ca0d296e682d44937dc81646f1d17e3c47898b3d289cd86b2d233b6136c7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.2 MB (96194553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b519855374486cb8e7a65c57b6a818468dcdc58c95e3b54800ee2c72cf9e26d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-s390x.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Fri, 19 Dec 2025 23:48:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 19 Dec 2025 23:48:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 19 Dec 2025 23:48:16 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 19 Dec 2025 23:48:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Dec 2025 23:48:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Dec 2025 23:48:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 23:48:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 23:48:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Dec 2025 23:48:16 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 19 Dec 2025 23:48:16 GMT
ENV PHP_VERSION=8.1.34
# Fri, 19 Dec 2025 23:48:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.34.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.34.tar.xz.asc
# Fri, 19 Dec 2025 23:48:16 GMT
ENV PHP_SHA256=ffa9e0982e82eeaea848f57687b425ed173aa278fe563001310ae2638db5c251
# Fri, 19 Dec 2025 23:48:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 19 Dec 2025 23:48:23 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 23:55:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/a5df26691d1b1f71b964b869510473a5d5413999.patch?full_index=1' -o 19131.patch; 	echo 'c98c01c74d3a6da197116f8511b16fed361ca6bbb6a8af8df629a933f541c213 *19131.patch' | sha256sum -c -; 	patch --reverse -p1 < 19131.patch; 	rm 19131.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Dec 2025 23:55:51 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 23:55:52 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Dec 2025 23:55:53 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Dec 2025 23:55:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Dec 2025 23:55:53 GMT
WORKDIR /var/www/html
# Fri, 19 Dec 2025 23:55:53 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 19 Dec 2025 23:55:53 GMT
STOPSIGNAL SIGQUIT
# Fri, 19 Dec 2025 23:55:53 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 19 Dec 2025 23:55:53 GMT
CMD ["php-fpm"]
# Sat, 20 Dec 2025 00:05:17 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Sat, 20 Dec 2025 00:06:09 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Sat, 20 Dec 2025 00:06:09 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Sat, 20 Dec 2025 00:06:09 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Sat, 20 Dec 2025 00:06:11 GMT
RUN set -eux; 	version='6.9'; 	sha1='256dda5bb6a43aecd806b7a62528f442c06e6c25'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Sat, 20 Dec 2025 00:06:11 GMT
VOLUME [/var/www/html]
# Sat, 20 Dec 2025 00:06:11 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Sat, 20 Dec 2025 00:06:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 20 Dec 2025 00:06:11 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Sat, 20 Dec 2025 00:06:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 20 Dec 2025 00:06:11 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9f2ceebb28b6c8480d6ae26501eda06bf0b6029f7c797c80673b95a60276e050`  
		Last Modified: Sun, 07 Dec 2025 17:58:56 GMT  
		Size: 3.5 MB (3466434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c995452a6f3b5884334d0bcef1538883087a008b2c57c3c5066efa9f7e9aed2`  
		Last Modified: Fri, 19 Dec 2025 23:53:13 GMT  
		Size: 3.6 MB (3597069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b6b815032520b7639ad5f9b01780201cfeb726de5b05d9444613a4460256aff`  
		Last Modified: Fri, 19 Dec 2025 23:53:13 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ca55d47f504e81b31d97fea6b43923f5e06076344e5048d4f415b02454313d`  
		Last Modified: Fri, 19 Dec 2025 23:53:13 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:424c960a966b75d54654646d5203f5b09bf5849e50bf909ed80c112de2472195`  
		Last Modified: Fri, 19 Dec 2025 23:53:14 GMT  
		Size: 11.9 MB (11925152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3de39b51f0fea58170ede6781831ed5cdd8bbaa5e40f84d639714b038ac6aee`  
		Last Modified: Fri, 19 Dec 2025 23:53:13 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7e841382b05497566ed126e6bf3a41929650146e6584d93893fbac078466ef`  
		Last Modified: Fri, 19 Dec 2025 23:56:11 GMT  
		Size: 12.7 MB (12669166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c5f83f64701f9dd9793d28a79486295db9e4cbde3923cfc832d7f8373bb26c`  
		Last Modified: Fri, 19 Dec 2025 23:56:10 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb31b7df47d02e53be1ba16706581f6da60e809e688779f43d317e2ca2a01ee4`  
		Last Modified: Fri, 19 Dec 2025 23:56:10 GMT  
		Size: 19.8 KB (19777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5064ded3b4d1f4c53b197d83fa8b28af0ac86deb811d24c6e8bf07b5b8198d6`  
		Last Modified: Fri, 19 Dec 2025 23:56:10 GMT  
		Size: 19.8 KB (19772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19e4e04418fb3e42999885193d5a2f11bd3d6a3368a8e02f4942f1b66a9ee7d0`  
		Last Modified: Fri, 19 Dec 2025 23:56:10 GMT  
		Size: 8.9 KB (8878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3ad5f04e7696b66835d1068428a7abf1f53d4c604f25979eacfaa05b14cea8`  
		Last Modified: Sat, 20 Dec 2025 00:06:37 GMT  
		Size: 29.2 MB (29223622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b476becbe63681706f1579201918a69dbc3e283cf0ea96d58552ffbf3bcf51b`  
		Last Modified: Sat, 20 Dec 2025 00:06:34 GMT  
		Size: 8.2 MB (8230231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56fcfaaaf9d3347fbce6bcf2f737127d3aeed61f1c9ef184700aee6b01eec5fe`  
		Last Modified: Sat, 20 Dec 2025 00:06:33 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7a43e2e2d332633fdfa1d636916bc3ac5e4773f6a6953f6fa7320e5e6cc7ccd`  
		Last Modified: Sat, 20 Dec 2025 00:06:35 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d743bc3094ef6efe8a4dd7e0ff77d2b07d90eefb6fbcdc73a1786b2efbc029a9`  
		Last Modified: Sat, 20 Dec 2025 00:06:35 GMT  
		Size: 27.0 MB (27025232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6170ac8d1a3c549f3500a16ee1578a7f7a7ac1eb5e9152ff3160591e3ea65a46`  
		Last Modified: Sat, 20 Dec 2025 00:06:33 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673bc58d631cb14b908a7602b9725b8c763d0ac649a2a0cd50fe21e3a6f64365`  
		Last Modified: Sat, 20 Dec 2025 00:06:33 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9179501460f40bbdbb99b52b474aac607c3ac55a05b911a7befa520d61997b70`  
		Last Modified: Sat, 20 Dec 2025 00:06:33 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:49030afd0b8fd6823c8f34ca21811a815e76dc4c50da7dcfa1c04a2e07435ec4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1125263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5319bb0f3226ca62cde6e0d6d0cd6172d04db828feb6cae0641ef88748c30741`

```dockerfile
```

-	Layers:
	-	`sha256:151458117603a612eea97ae9f872b5c0714ce7751cdfdfd4307a143a47a67676`  
		Last Modified: Sat, 20 Dec 2025 02:14:57 GMT  
		Size: 1.1 MB (1073540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74f69e7638197398d31c0bd165c73675cb00663e54476e57737acb4d321ec151`  
		Last Modified: Sat, 20 Dec 2025 02:14:58 GMT  
		Size: 51.7 KB (51723 bytes)  
		MIME: application/vnd.in-toto+json
