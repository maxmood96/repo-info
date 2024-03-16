## `wordpress:beta-php8.1-fpm-alpine`

```console
$ docker pull wordpress@sha256:e92b35ee5efd80f68f921ac77b87e65892ead06817f7282d95cab524f360cd1b
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

### `wordpress:beta-php8.1-fpm-alpine` - linux; amd64

```console
$ docker pull wordpress@sha256:00070a851813a8498b5be083e12a0e4879de6a781d6dd906ec12c60c7b529b7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.7 MB (87687561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad2e030340ac416d2d685ad9a4b6d17b26028b0c561a545375840234dddbd585`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 12 Mar 2024 19:03:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 12 Mar 2024 19:03:10 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 12 Mar 2024 19:03:10 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 12 Mar 2024 19:03:10 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Mar 2024 19:03:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Mar 2024 19:03:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 19:03:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 19:03:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Mar 2024 19:03:10 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 12 Mar 2024 19:03:10 GMT
ENV PHP_VERSION=8.1.27
# Tue, 12 Mar 2024 19:03:10 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Tue, 12 Mar 2024 19:03:10 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Tue, 12 Mar 2024 19:03:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 12 Mar 2024 19:03:10 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 12 Mar 2024 19:03:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 12 Mar 2024 19:03:10 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 12 Mar 2024 19:03:10 GMT
RUN docker-php-ext-enable sodium
# Tue, 12 Mar 2024 19:03:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 12 Mar 2024 19:03:10 GMT
WORKDIR /var/www/html
# Tue, 12 Mar 2024 19:03:10 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Tue, 12 Mar 2024 19:03:10 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Mar 2024 19:03:10 GMT
EXPOSE 9000
# Tue, 12 Mar 2024 19:03:10 GMT
CMD ["php-fpm"]
# Tue, 12 Mar 2024 19:03:10 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
RUN set -eux; 	version='6.5-RC2'; 	sha1='3c09b4f3da34b0e5e8914f0b491081d42782ee63'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
VOLUME [/var/www/html]
# Tue, 12 Mar 2024 19:03:10 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Mar 2024 19:03:10 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b99432ace8a7bcff6a457c1ea616c20b241e4012ebc18ff9b4b9a7ca571de2d`  
		Last Modified: Sat, 16 Mar 2024 02:36:07 GMT  
		Size: 2.8 MB (2761513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a73aae1c86e8e06844a0d6ff516b8d12cc95d745da7005aea6ff3ec71c90ef`  
		Last Modified: Sat, 16 Mar 2024 02:36:07 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9294d9185d898643d89218d8a670313cd2bb59107bf32cb6ac92e7f46839bbc8`  
		Last Modified: Sat, 16 Mar 2024 02:36:07 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a850bb625daccc97170bf7027bf7c134b5bc5742d9d64996e3d2fb4fc2c1938b`  
		Last Modified: Sat, 16 Mar 2024 02:42:26 GMT  
		Size: 11.9 MB (11935901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558e09d774beadd062d44d2de9140cb978094afcd17aecd767be914f7b253003`  
		Last Modified: Sat, 16 Mar 2024 02:42:25 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e6cdf957b36b0ed4003d02d20aea4ba2526c54dc32cb1ed6093f4418609130`  
		Last Modified: Sat, 16 Mar 2024 02:42:50 GMT  
		Size: 12.6 MB (12599519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fe63adf5c332b26bf65997acaf6c3daf8a3a1f10a4dfd89cff6e594576f3af`  
		Last Modified: Sat, 16 Mar 2024 02:42:48 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ec781635263e72fa078959b98a4eff7cd223040e12042750127d67de92fa936`  
		Last Modified: Sat, 16 Mar 2024 02:42:48 GMT  
		Size: 19.3 KB (19291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0914106f7a54342e00f3bd3f940e080220940ccd913ed92d4f6068fbcdab8f`  
		Last Modified: Sat, 16 Mar 2024 02:42:48 GMT  
		Size: 8.9 KB (8882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0897b7ef2ed15b7a52010c01ebecf94b577ec2c187f61372f41833e2a1ea51a1`  
		Last Modified: Sat, 16 Mar 2024 02:52:17 GMT  
		Size: 28.6 MB (28637221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:611d4b7b82da0667b8f5fbaf4a5cef2d12a6a379e7d9bd301f6e76c4842c0323`  
		Last Modified: Sat, 16 Mar 2024 02:52:15 GMT  
		Size: 3.7 MB (3725642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b0876328da0477a654db43d36c2c63c4173e6169f4fe2a98b691e5bb83f3391`  
		Last Modified: Sat, 16 Mar 2024 02:52:14 GMT  
		Size: 59.4 KB (59389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1953ce42733dd6b40555c04b0f7437c0d726b10f91fb512a577b162e31031bab`  
		Last Modified: Sat, 16 Mar 2024 02:52:14 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c95c9179a9cd78259b61e6d1873a5e8a589a9881b9ebecfec401e6102e478d`  
		Last Modified: Sat, 16 Mar 2024 02:52:16 GMT  
		Size: 24.5 MB (24522548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5d9a37283c23c61a3660ed40f57e24803b4b806472fd5ac97f6311630a3767`  
		Last Modified: Sat, 16 Mar 2024 02:52:15 GMT  
		Size: 2.3 KB (2341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb4feadc58d57ef34550b9d0b2bdb38e88a31983ec382192f6476ffe033165e`  
		Last Modified: Sat, 16 Mar 2024 02:52:16 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:c1f33c8331fcb4b516c2a7a052d6985664b2fbcb649aa8cc6f16867c591a4123
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1059677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4fa7ca7608638f0fdaaf0b186e7f25a5db7b3645c324c49bff54912ccaa4589`

```dockerfile
```

-	Layers:
	-	`sha256:52412fbe3301ec8909941695e6c828875032e13a725cc0d773e29f3cc32f4110`  
		Last Modified: Sat, 16 Mar 2024 02:52:14 GMT  
		Size: 1.0 MB (1011303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f9328b57f666c390b3b3f1ed4a940db103451bdab968a9b316cc0bb7b5c5965`  
		Last Modified: Sat, 16 Mar 2024 02:52:14 GMT  
		Size: 48.4 KB (48374 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.1-fpm-alpine` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:65ded8d95184890f77839da5830e6156f09ea564ede332c858f74320af0d2bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85624695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef2f0cb4510a87adb249f2f695aa4042db1f4d2fe396d707c1148bc169c7b2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 05:22:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 27 Jan 2024 05:22:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 27 Jan 2024 05:22:19 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 27 Jan 2024 05:22:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 27 Jan 2024 05:22:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 27 Jan 2024 05:22:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 05:22:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 05:22:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 27 Jan 2024 06:23:28 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 27 Jan 2024 06:23:29 GMT
ENV PHP_VERSION=8.1.27
# Sat, 27 Jan 2024 06:23:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Sat, 27 Jan 2024 06:23:29 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Sat, 27 Jan 2024 06:23:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 27 Jan 2024 06:23:39 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 27 Jan 2024 06:31:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 27 Jan 2024 06:31:26 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 27 Jan 2024 06:31:27 GMT
RUN docker-php-ext-enable sodium
# Sat, 27 Jan 2024 06:31:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 27 Jan 2024 06:31:27 GMT
WORKDIR /var/www/html
# Sat, 27 Jan 2024 06:31:27 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 27 Jan 2024 06:31:27 GMT
STOPSIGNAL SIGQUIT
# Sat, 27 Jan 2024 06:31:28 GMT
EXPOSE 9000
# Sat, 27 Jan 2024 06:31:28 GMT
CMD ["php-fpm"]
# Tue, 12 Mar 2024 19:03:10 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
RUN set -eux; 	version='6.5-RC2'; 	sha1='3c09b4f3da34b0e5e8914f0b491081d42782ee63'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
VOLUME [/var/www/html]
# Tue, 12 Mar 2024 19:03:10 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Mar 2024 19:03:10 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6147d01edb253ab7eff347bb08482a430759361f869152a4c0a0ecdd946e0d17`  
		Last Modified: Sat, 27 Jan 2024 06:44:23 GMT  
		Size: 2.8 MB (2764487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b42f6e9b3a3a721beed37ea494f71a49e981f945e849780a3cc6a57bf1c0ed9`  
		Last Modified: Sat, 27 Jan 2024 06:44:22 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7136267c1932cb42af7ae697ecc07c459f4c5a75f3adf037cdfff9774f183ff3`  
		Last Modified: Sat, 27 Jan 2024 06:44:22 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d40f548d68eacfeafc3ba888cef9b1832cfc39a4ee37dbc85f9408ea4dc0e4`  
		Last Modified: Sat, 27 Jan 2024 06:48:26 GMT  
		Size: 11.9 MB (11935923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4770e2fa5de99531c2d9a6435f5560398c3f6bac82197a6e7cf03c561112ad3`  
		Last Modified: Sat, 27 Jan 2024 06:48:25 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1da5ab6a26b1dcf1bab3bad51178a41122cd50ad00e8f72bbc497d1f0700f79`  
		Last Modified: Sat, 27 Jan 2024 06:48:53 GMT  
		Size: 11.4 MB (11427002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73681126150f7eb5fa75d0114a0d45fdb62edfee32ce56cd907f09f4e843822f`  
		Last Modified: Sat, 27 Jan 2024 06:48:50 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d01ed697273c81440082629134b8742ddbebcfb55125799bfca3f7c7ac5e09`  
		Last Modified: Sat, 27 Jan 2024 06:48:50 GMT  
		Size: 19.1 KB (19131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1d4d2d4d9959b46b726ab6705197bd0ae1aa2acca8582a6f241e46b41d4c5a`  
		Last Modified: Sat, 27 Jan 2024 06:48:50 GMT  
		Size: 8.9 KB (8879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9977ea81643361729d09d27b6e00a394c5fac806c25cf602a7c0c81117bf6eb3`  
		Last Modified: Tue, 12 Mar 2024 23:58:27 GMT  
		Size: 28.2 MB (28163522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbec4aecf7f132155d226dc8d8f1703d3af66a4a60238b244bdd918427958329`  
		Last Modified: Tue, 12 Mar 2024 23:58:27 GMT  
		Size: 3.5 MB (3549440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6140c5cc72c77813739a0122b4b4c4503b59a2a26a4581ba34f7b379e6a6e77f`  
		Last Modified: Tue, 12 Mar 2024 23:58:26 GMT  
		Size: 59.4 KB (59421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5fd6917c9fd1a78c6a318d6ec28f4246fc5ec9a4b1d10b828523ca9608d119`  
		Last Modified: Tue, 12 Mar 2024 23:58:27 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266f957e9786194c0a6321841d0612c1abc0910a90b746891dd0132478ee441c`  
		Last Modified: Tue, 12 Mar 2024 23:58:29 GMT  
		Size: 24.5 MB (24522551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41204f191d4a24b7e8fe62933c2b532ff5bdfc4da0157cf5b2f6d140e573116`  
		Last Modified: Tue, 12 Mar 2024 23:58:28 GMT  
		Size: 2.3 KB (2347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0edc6930772f3828bfd5da6d9ab88f270a9d263cb42f742958251280cafc4f`  
		Last Modified: Tue, 12 Mar 2024 23:58:28 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:a582f1852274b6c4faf2abb5daf0a4e1fe65b12373c0f73b669650498c766b3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 KB (46655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d5fe42aa689015ad1326d9b61cca415201e8842b00c3c94e92a35998cb22af`

```dockerfile
```

-	Layers:
	-	`sha256:c9f1633eb0760d47043e89ee5cdb76615ba29b70d4a65b4ceaead3e179af0304`  
		Last Modified: Tue, 12 Mar 2024 23:58:26 GMT  
		Size: 46.7 KB (46655 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.1-fpm-alpine` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:3d8dcfde4a07f8ae81cd73134e2cace589977d1038ad7f94004f67c71c1d9ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.0 MB (82989154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4ef5747cd2f130a71c9f6606f4e6e25305fd583a7cae559cc0384a5cbe576c2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 06:34:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 27 Jan 2024 06:34:53 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 27 Jan 2024 06:34:54 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 27 Jan 2024 06:34:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 27 Jan 2024 06:34:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 27 Jan 2024 06:34:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 06:34:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 06:34:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 27 Jan 2024 07:14:08 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 27 Jan 2024 07:14:08 GMT
ENV PHP_VERSION=8.1.27
# Sat, 27 Jan 2024 07:14:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Sat, 27 Jan 2024 07:14:08 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Sat, 27 Jan 2024 07:14:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 27 Jan 2024 07:14:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 27 Jan 2024 07:19:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 27 Jan 2024 07:19:32 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 27 Jan 2024 07:19:33 GMT
RUN docker-php-ext-enable sodium
# Sat, 27 Jan 2024 07:19:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 27 Jan 2024 07:19:33 GMT
WORKDIR /var/www/html
# Sat, 27 Jan 2024 07:19:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 27 Jan 2024 07:19:34 GMT
STOPSIGNAL SIGQUIT
# Sat, 27 Jan 2024 07:19:34 GMT
EXPOSE 9000
# Sat, 27 Jan 2024 07:19:34 GMT
CMD ["php-fpm"]
# Tue, 12 Mar 2024 19:03:10 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
RUN set -eux; 	version='6.5-RC2'; 	sha1='3c09b4f3da34b0e5e8914f0b491081d42782ee63'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
VOLUME [/var/www/html]
# Tue, 12 Mar 2024 19:03:10 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Mar 2024 19:03:10 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fad4c06f9510d8c219b7fe261aa66aed178abd7a1c84deb7c27194f902386d7`  
		Last Modified: Sat, 27 Jan 2024 07:33:08 GMT  
		Size: 2.6 MB (2612619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b84d0418e4ec14c0677d1849ef32a6fc29b8ff5271474a5fc99e97086db728`  
		Last Modified: Sat, 27 Jan 2024 07:33:07 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae368cea0e62724a4b01ec73e9ff3a02291ca0fd945c2ae68057812a20aaa69`  
		Last Modified: Sat, 27 Jan 2024 07:33:07 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58e0fce7384e01214cbe65e5edd12b8431b7cba305a2095437d473453265ad29`  
		Last Modified: Sat, 27 Jan 2024 07:37:15 GMT  
		Size: 11.9 MB (11935916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c6ee5e18bf753b71408d09a8891243a50ce9ee787dda581cb2c830f9888bca6`  
		Last Modified: Sat, 27 Jan 2024 07:37:14 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dff34a65ac75057c6b60e075980704c6ad331616183dde1ae8be4764fdd25eb`  
		Last Modified: Sat, 27 Jan 2024 07:37:39 GMT  
		Size: 10.7 MB (10715789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b69fd5f798bdf8f1a35dac496ba78ea15db1c134322533c18c3ab817fb2aa5`  
		Last Modified: Sat, 27 Jan 2024 07:37:37 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35b78846be7b7f8d8b8ee1c7aa7228b1097a1c2216c5676ced59aab2c615199`  
		Last Modified: Sat, 27 Jan 2024 07:37:37 GMT  
		Size: 19.1 KB (19106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38daadf7cbf584ef5d0b2ed818ee671254a42c226c250dd30757d2ca2afc393f`  
		Last Modified: Sat, 27 Jan 2024 07:37:37 GMT  
		Size: 8.9 KB (8879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe09cbed1db21498928676afb9034e56f7366b9a9bc7d6174b0ffcf6fd7452b`  
		Last Modified: Fri, 02 Feb 2024 13:36:47 GMT  
		Size: 26.6 MB (26597398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2284cf7ff36390050b33da166b95b25834760e6c50a3aeffedabb8cfe22f53b2`  
		Last Modified: Tue, 12 Mar 2024 00:56:29 GMT  
		Size: 3.6 MB (3589671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab8d28ee5694f71591db9a33706ca469a5778f2c59f6d08231f748bc4a373dd5`  
		Last Modified: Tue, 12 Mar 2024 00:56:28 GMT  
		Size: 59.4 KB (59370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f019466b69d7ba64693aee054a027b45343ae99b977983b6444c7e04a738bc9`  
		Last Modified: Tue, 12 Mar 2024 00:56:28 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6762a049bd6b875c4756e1476d0feacb52ae264a05c9a8e67b03d2da44d2a4b`  
		Last Modified: Wed, 13 Mar 2024 10:39:29 GMT  
		Size: 24.5 MB (24522562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29dd55d6e0920c63a1822115a26ed398b04fe40869e2da59d27ddbcbfd8ad79`  
		Last Modified: Wed, 13 Mar 2024 10:39:27 GMT  
		Size: 2.4 KB (2353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a46ffe7ebd0e274ca9455f6f68b57933edb9de288df8b40c6e849c6c90a5575`  
		Last Modified: Wed, 13 Mar 2024 10:39:27 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:e73f1ceca8f3a14243b130e5477862999388c740451a33b4714d2a5becccc900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1058210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:824722bc97e06f9d66b3169b174b5c935b53e26cd49b6540005643a92d62ad99`

```dockerfile
```

-	Layers:
	-	`sha256:54ec7069661890b08989b67d711511f6aae2a553bb0e868ac9443a32dad4b896`  
		Last Modified: Wed, 13 Mar 2024 10:39:27 GMT  
		Size: 1.0 MB (1011340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f9b34faf6415f542f6d2582b9465caafcf1f34cc94cd52281ab71e3eeb4b889`  
		Last Modified: Wed, 13 Mar 2024 10:39:27 GMT  
		Size: 46.9 KB (46870 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.1-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:27b90d6f57e401c2ec024e9a206444f44ca9d1754692c660b5323befd9883203
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.9 MB (87903983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59deacdc42609934112ab8b54dae0a56cdf51719957587cd37e7b4c025be07d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 07:28:53 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 27 Jan 2024 07:28:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 27 Jan 2024 07:28:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 27 Jan 2024 07:28:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 27 Jan 2024 07:28:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 27 Jan 2024 07:28:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 07:28:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 07:28:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 27 Jan 2024 08:16:12 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 27 Jan 2024 08:16:12 GMT
ENV PHP_VERSION=8.1.27
# Sat, 27 Jan 2024 08:16:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Sat, 27 Jan 2024 08:16:12 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Sat, 27 Jan 2024 08:16:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 27 Jan 2024 08:16:19 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 27 Jan 2024 08:23:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 27 Jan 2024 08:23:46 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 27 Jan 2024 08:23:47 GMT
RUN docker-php-ext-enable sodium
# Sat, 27 Jan 2024 08:23:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 27 Jan 2024 08:23:48 GMT
WORKDIR /var/www/html
# Sat, 27 Jan 2024 08:23:48 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 27 Jan 2024 08:23:48 GMT
STOPSIGNAL SIGQUIT
# Sat, 27 Jan 2024 08:23:48 GMT
EXPOSE 9000
# Sat, 27 Jan 2024 08:23:48 GMT
CMD ["php-fpm"]
# Tue, 12 Mar 2024 19:03:10 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
RUN set -eux; 	version='6.5-RC2'; 	sha1='3c09b4f3da34b0e5e8914f0b491081d42782ee63'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
VOLUME [/var/www/html]
# Tue, 12 Mar 2024 19:03:10 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Mar 2024 19:03:10 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f072bab4d3b766550992c322a39fcd900b329ffbe17cdcb1a7d74010688b23ec`  
		Last Modified: Sat, 27 Jan 2024 08:40:23 GMT  
		Size: 2.8 MB (2815760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537d23c253bc777c8630b1470aee1d7857122cbdf09144b5cb061bde634e0fbd`  
		Last Modified: Sat, 27 Jan 2024 08:40:22 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65cde09541f81b6406c9aa0f33cd98ae9716bc8c625290248755e374475bda3`  
		Last Modified: Sat, 27 Jan 2024 08:40:22 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7d5020f694220fc1797edee3319eee3b01603df0ef569f1a395ba38a916fd4`  
		Last Modified: Sat, 27 Jan 2024 08:44:22 GMT  
		Size: 11.9 MB (11935916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a44c371136b1f7805552fa358092b935b8921c3ebe60c922a16ae23bfb2b0d`  
		Last Modified: Sat, 27 Jan 2024 08:44:21 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d0d9688c570ce8ce642c189dfc216084ed44c385a70285e38a034abc1f0d58`  
		Last Modified: Sat, 27 Jan 2024 08:44:44 GMT  
		Size: 12.6 MB (12647468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1145011450e85d373be896096bbfe1fe91b4c921566a0fc0a008238036bc54`  
		Last Modified: Sat, 27 Jan 2024 08:44:42 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff668bd8399ecb1c209fd3dc10f9c605a008e011df7b109dbfdd2be08ccf089`  
		Last Modified: Sat, 27 Jan 2024 08:44:42 GMT  
		Size: 19.1 KB (19087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f681dc3e8a7d16b88de580063a919552fb36158f8a8fb5c4a113009af73d5ff`  
		Last Modified: Sat, 27 Jan 2024 08:44:42 GMT  
		Size: 8.9 KB (8877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6690304e96070a2d2ac751d5df5603bd69f011dee555a385598ae0e2800dcdf5`  
		Last Modified: Wed, 06 Mar 2024 01:58:07 GMT  
		Size: 28.8 MB (28770683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ac908fd7c05f40910aa7b7ecd3cac383ba3e1b8a32e3df491d12da78a34ac5`  
		Last Modified: Wed, 13 Mar 2024 06:36:08 GMT  
		Size: 3.8 MB (3767624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00be37cfc6c2b5cd3fa53ad28c3f711ce1295eabde6b790e53da1b15c78e239c`  
		Last Modified: Wed, 13 Mar 2024 06:36:07 GMT  
		Size: 59.4 KB (59361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9088b60fd376d7608da930ab60c2f1324344e431160e860d4736abdf489a9d3e`  
		Last Modified: Wed, 13 Mar 2024 06:36:07 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59426acaefda316fc400020d9478f26d871cacd70aefed52adc1902c74844c68`  
		Last Modified: Wed, 13 Mar 2024 08:35:56 GMT  
		Size: 24.5 MB (24522559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4b7c65735558e22ecbfd951ac8ae6725a0f0c3acdeff18a42c322402c2e684`  
		Last Modified: Wed, 13 Mar 2024 08:35:56 GMT  
		Size: 2.4 KB (2350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68a51f4087a6907950e632719642466d75a01025e2f6f6b42794b93adf90f69`  
		Last Modified: Wed, 13 Mar 2024 08:35:56 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:7c685f7b97cfde2ecafb883fbb4934f2f73ffa6be3544d206622d8e783024b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1058073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:863b5536d25a595c28a8d48f2f9065e457dc4e68b43a61280d19fd08318cf115`

```dockerfile
```

-	Layers:
	-	`sha256:0aa4c11cc2742a85a03ab3eb103445e2e6d719c2cd19149d7046470a0f31c9c4`  
		Last Modified: Wed, 13 Mar 2024 08:35:55 GMT  
		Size: 1.0 MB (1011314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c42782a1673e984096268ad9c8966ec598ca8896d3ac0aad93bcfa629350a48b`  
		Last Modified: Wed, 13 Mar 2024 08:35:55 GMT  
		Size: 46.8 KB (46759 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.1-fpm-alpine` - linux; 386

```console
$ docker pull wordpress@sha256:31d7f110066e3984fb35e31910ee399ee5b37115931abdc29230083e9f46867e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.3 MB (88314381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:987a25d6b90d7b3e2bd1205d4eb328897a404027546d417c5bbf25cb9f120bb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Tue, 12 Mar 2024 19:03:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 12 Mar 2024 19:03:10 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 12 Mar 2024 19:03:10 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 12 Mar 2024 19:03:10 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 12 Mar 2024 19:03:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 12 Mar 2024 19:03:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 19:03:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 12 Mar 2024 19:03:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 12 Mar 2024 19:03:10 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 12 Mar 2024 19:03:10 GMT
ENV PHP_VERSION=8.1.27
# Tue, 12 Mar 2024 19:03:10 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Tue, 12 Mar 2024 19:03:10 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Tue, 12 Mar 2024 19:03:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 12 Mar 2024 19:03:10 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 12 Mar 2024 19:03:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 12 Mar 2024 19:03:10 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 12 Mar 2024 19:03:10 GMT
RUN docker-php-ext-enable sodium
# Tue, 12 Mar 2024 19:03:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 12 Mar 2024 19:03:10 GMT
WORKDIR /var/www/html
# Tue, 12 Mar 2024 19:03:10 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Tue, 12 Mar 2024 19:03:10 GMT
STOPSIGNAL SIGQUIT
# Tue, 12 Mar 2024 19:03:10 GMT
EXPOSE 9000
# Tue, 12 Mar 2024 19:03:10 GMT
CMD ["php-fpm"]
# Tue, 12 Mar 2024 19:03:10 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
RUN set -eux; 	version='6.5-RC2'; 	sha1='3c09b4f3da34b0e5e8914f0b491081d42782ee63'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
VOLUME [/var/www/html]
# Tue, 12 Mar 2024 19:03:10 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Mar 2024 19:03:10 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a52b85e4d8e4d0e4048cab06c149fd0b6d64c5a5f04ec3a3f7c0ab4d4a3d8e6`  
		Last Modified: Sat, 16 Mar 2024 04:58:57 GMT  
		Size: 2.8 MB (2825337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d00dcc91f58845575e9487816e58609662888d41b2facfcf6128056ee483579`  
		Last Modified: Sat, 16 Mar 2024 04:58:56 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3264601b4fa42c37a2b6f6e47b5c8cb1c963b67ee7e15c2c18d17f2fd035a3fa`  
		Last Modified: Sat, 16 Mar 2024 04:58:56 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:affca4caf2ab4701295808e9bb7a85c8d018538ef50bf32a8e23401fbc280d0c`  
		Last Modified: Sat, 16 Mar 2024 05:06:09 GMT  
		Size: 11.9 MB (11935924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c639082e4e2e1abb77890fb882ef4d4b6d75dd1dfb531b7f23662a4a104c56c6`  
		Last Modified: Sat, 16 Mar 2024 05:06:08 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85c06c1c7efb48c22cefc7a6cd94f417c129954c2c02bd78aecdbcf6a1ed512`  
		Last Modified: Sat, 16 Mar 2024 05:06:38 GMT  
		Size: 12.9 MB (12926049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b72ed62fb5204ede3ff5bfb02cd6d48ec05638ae963fedcb35245788bfc03f1`  
		Last Modified: Sat, 16 Mar 2024 05:06:34 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb58a46af5e8b5e3a1d118db27878b29b49c02c682323d73ac4078b2808cb6b9`  
		Last Modified: Sat, 16 Mar 2024 05:06:34 GMT  
		Size: 19.3 KB (19304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2dca242e310d2d374cdd86a96b668ddc2bccdafb8a685c6ff80f18e3c2b19d`  
		Last Modified: Sat, 16 Mar 2024 05:06:34 GMT  
		Size: 8.9 KB (8876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb2d4d110190a85a0c0392c2f48e6c5aa013905dda748b1d37eefe98e8fc88e2`  
		Last Modified: Sat, 16 Mar 2024 05:52:54 GMT  
		Size: 28.9 MB (28877628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1741f174fcd99da6136a00b819c92a9ce1e583d5a855c67d1ca37272ad4e0568`  
		Last Modified: Sat, 16 Mar 2024 05:52:53 GMT  
		Size: 3.9 MB (3886300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770241d0bc9543d644d672f548a4c1f4c57cd16725f48b5f002db1d02640a613`  
		Last Modified: Sat, 16 Mar 2024 05:52:53 GMT  
		Size: 59.4 KB (59390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40ccaa2f2df0b88b8f162ce6800b0690dae749ff8109c45a4ad7f78d3c9732bf`  
		Last Modified: Sat, 16 Mar 2024 05:52:53 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23be45c56a408626bf128c24973cb577aa71b0ccb00cb6d7edac213018afb50`  
		Last Modified: Sat, 16 Mar 2024 05:52:55 GMT  
		Size: 24.5 MB (24522556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6042ea8f8e2c5a7e4f478eacf71ae4f3d928d1e6ebe12e2370d19c587d16f5fa`  
		Last Modified: Sat, 16 Mar 2024 05:52:54 GMT  
		Size: 2.3 KB (2347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670bfc6e14206ce530441995866ab87a0ba410fa15273b7875574c0de28d4a6a`  
		Last Modified: Sat, 16 Mar 2024 05:52:54 GMT  
		Size: 1.7 KB (1722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:d231679bbcf5f7ce1e6663a66dc5c193ff31ddafc7a0a363dd7c50c7619eae68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1059615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:425575cd8d9144902a4d0f74f946cc216a016fbf00566a228115ac587681b968`

```dockerfile
```

-	Layers:
	-	`sha256:e6ce9c76bd533914748a2fd6af8b4f1eab5fdd9b01960cf56cab8648a561418f`  
		Last Modified: Sat, 16 Mar 2024 05:52:53 GMT  
		Size: 1.0 MB (1011278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78a91386d18d2f58654b9eb6a655637982a40b248ea567bc79e24e6f5f64a0a8`  
		Last Modified: Sat, 16 Mar 2024 05:52:53 GMT  
		Size: 48.3 KB (48337 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.1-fpm-alpine` - linux; ppc64le

```console
$ docker pull wordpress@sha256:4090b50cfc98ec2a18b8042a8fd4af2e6c784091e741e7439e7ce4365115609f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.1 MB (89055029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49aa052387fcd2d0905d27da2b67c6c7e3126a5663c6fed20d80e7c5cb7864b9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:26:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 27 Jan 2024 03:26:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 27 Jan 2024 03:26:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 27 Jan 2024 03:26:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 27 Jan 2024 03:26:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 27 Jan 2024 03:26:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 03:26:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 03:26:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 27 Jan 2024 04:02:02 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 27 Jan 2024 04:02:02 GMT
ENV PHP_VERSION=8.1.27
# Sat, 27 Jan 2024 04:02:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Sat, 27 Jan 2024 04:02:03 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Sat, 27 Jan 2024 04:02:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 27 Jan 2024 04:02:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 27 Jan 2024 04:07:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 27 Jan 2024 04:07:29 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 27 Jan 2024 04:07:31 GMT
RUN docker-php-ext-enable sodium
# Sat, 27 Jan 2024 04:07:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 27 Jan 2024 04:07:32 GMT
WORKDIR /var/www/html
# Sat, 27 Jan 2024 04:07:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 27 Jan 2024 04:07:34 GMT
STOPSIGNAL SIGQUIT
# Sat, 27 Jan 2024 04:07:35 GMT
EXPOSE 9000
# Sat, 27 Jan 2024 04:07:36 GMT
CMD ["php-fpm"]
# Tue, 12 Mar 2024 19:03:10 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
RUN set -eux; 	version='6.5-RC2'; 	sha1='3c09b4f3da34b0e5e8914f0b491081d42782ee63'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
VOLUME [/var/www/html]
# Tue, 12 Mar 2024 19:03:10 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Mar 2024 19:03:10 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8953adc2ed89719cf332d6841a33f5396f09790ebe287db3934fd2327d14b7`  
		Last Modified: Sat, 27 Jan 2024 04:21:21 GMT  
		Size: 2.8 MB (2842838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a412c6f832e805dac7f8f5eb85b03e9340bde010929c469a7aa203611edf867d`  
		Last Modified: Sat, 27 Jan 2024 04:21:21 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ad5c29bf6c410c283dc6e7c4619fb7570382a7860ef5d8b6a00e3228ea8a03`  
		Last Modified: Sat, 27 Jan 2024 04:21:21 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c05c363edc61cae391bcd1d44d0206df4a4c43a91a5ea476ffbcfb9d3fde440`  
		Last Modified: Sat, 27 Jan 2024 04:26:16 GMT  
		Size: 11.9 MB (11935917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f641efd1d5b4974ea31091b37a60a3bc3e477ce8d38d2a417bb5bbbf17f46bbc`  
		Last Modified: Sat, 27 Jan 2024 04:26:15 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a882990e960c0e76f57e3a20a028367068f75e34cd244e18c7e4d60e1d430d3b`  
		Last Modified: Sat, 27 Jan 2024 04:26:44 GMT  
		Size: 13.0 MB (13039496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6585c5db41e56c22c3a2209dfe4f0baa5aaab6b6c3b792b2272b1b2c6ac8d0d5`  
		Last Modified: Sat, 27 Jan 2024 04:26:42 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6e3e491ff1ae26b6d3ccd9e40d153bdd3962252339384b166f4a8aa9dad32a`  
		Last Modified: Sat, 27 Jan 2024 04:26:42 GMT  
		Size: 19.1 KB (19107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e3ca200b8cd98674da2dffe015f36fb443735acb520db1d761541a5e0a7b92d`  
		Last Modified: Sat, 27 Jan 2024 04:26:42 GMT  
		Size: 8.9 KB (8879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b096342245c3eece98841a75402318b4591f51bcb50e7ba7b42750b0058c3c7f`  
		Last Modified: Wed, 06 Mar 2024 09:36:00 GMT  
		Size: 29.4 MB (29378912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbbc371244fde7e2a8d828847bba0709c9c2a24e9d9b0279225eabd5c6aa00f`  
		Last Modified: Tue, 12 Mar 2024 19:19:32 GMT  
		Size: 3.9 MB (3880619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6258e6fb155e71fee05259366d825daa9868543dd37ca9511df30ee326df2e8b`  
		Last Modified: Tue, 12 Mar 2024 19:19:32 GMT  
		Size: 59.4 KB (59402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534713ab73b6d7e090bfa2937d49f69a6183f2b641827fa4195d0be41804d344`  
		Last Modified: Tue, 12 Mar 2024 19:19:32 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dcb3b27eb58c08c2ba7fb2cabcba1b1dc4a49ff07a7524b069c3dc42354861d`  
		Last Modified: Wed, 13 Mar 2024 09:49:48 GMT  
		Size: 24.5 MB (24522559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c45b6d237b1300a4098732b275b823bd3f71a54290b1deff373cdbba7d7674`  
		Last Modified: Wed, 13 Mar 2024 09:49:47 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b49bc990b556b2bd7977d64cabdf7b22bcadb568f1ccad1482d63ba20e8688e`  
		Last Modified: Wed, 13 Mar 2024 09:49:47 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:daf06d435be0f4bcc7b8e83662e8e2f78fc437793b4b8ff4b1d691cd0c9377f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1056178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f2a0296bef35f684ca588e422558aee0dd32b6d7914b56f4d7ce2c0d6561d02`

```dockerfile
```

-	Layers:
	-	`sha256:867127968fb2d212209dd5e035231285bffb9142ea6de879143768b450c7c7e2`  
		Last Modified: Wed, 13 Mar 2024 09:49:47 GMT  
		Size: 1.0 MB (1009383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff20b96bf5c427b11b50c15c0bdad1cc58ff52c88e50247a78ced4f9f50ef589`  
		Last Modified: Wed, 13 Mar 2024 09:49:47 GMT  
		Size: 46.8 KB (46795 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.1-fpm-alpine` - linux; s390x

```console
$ docker pull wordpress@sha256:04fc21dfbd8b22c94a0db76511ed6c5493d2dd41144d77fae5e386ce706c2a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88540485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0fb3581a168d325b8f02f0fe2cdb2a8fe2189ba328c71b772a84f07942575a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 10:55:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 27 Jan 2024 10:55:04 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 27 Jan 2024 10:55:05 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 27 Jan 2024 10:55:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 27 Jan 2024 10:55:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 27 Jan 2024 10:55:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 10:55:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 10:55:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 27 Jan 2024 12:17:19 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Sat, 27 Jan 2024 12:17:19 GMT
ENV PHP_VERSION=8.1.27
# Sat, 27 Jan 2024 12:17:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.27.tar.xz.asc
# Sat, 27 Jan 2024 12:17:20 GMT
ENV PHP_SHA256=479e65c3f05714d4aace1370e617d78e49e996ec7a7579a5be47535be61f0658
# Sat, 27 Jan 2024 12:17:27 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 27 Jan 2024 12:17:28 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 27 Jan 2024 12:29:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 27 Jan 2024 12:29:21 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 27 Jan 2024 12:29:23 GMT
RUN docker-php-ext-enable sodium
# Sat, 27 Jan 2024 12:29:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 27 Jan 2024 12:29:24 GMT
WORKDIR /var/www/html
# Sat, 27 Jan 2024 12:29:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 27 Jan 2024 12:29:26 GMT
STOPSIGNAL SIGQUIT
# Sat, 27 Jan 2024 12:29:26 GMT
EXPOSE 9000
# Sat, 27 Jan 2024 12:29:27 GMT
CMD ["php-fpm"]
# Tue, 12 Mar 2024 19:03:10 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
RUN set -eux; 	version='6.5-RC2'; 	sha1='3c09b4f3da34b0e5e8914f0b491081d42782ee63'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
VOLUME [/var/www/html]
# Tue, 12 Mar 2024 19:03:10 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 12 Mar 2024 19:03:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 12 Mar 2024 19:03:10 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6de5ae65e656b2b4fa74ec7767361eaadc5cd5fe084c14430793caa205b914`  
		Last Modified: Sat, 27 Jan 2024 13:01:18 GMT  
		Size: 2.9 MB (2940559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ae336f1db4cf8874ad7a1c11fdd671f8cfec2f2870323c9d69be5c95f4dc84`  
		Last Modified: Sat, 27 Jan 2024 13:01:17 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641172590360f4af57f25f7e5069c42671cce55bb70bee9d82d9b5fb865e3edb`  
		Last Modified: Sat, 27 Jan 2024 13:01:17 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c3765b447ec133ce7763aca834eda384b680d8afa3e50d4f6630a9e804ee16`  
		Last Modified: Sat, 27 Jan 2024 13:05:20 GMT  
		Size: 11.9 MB (11935919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36da090e29aa88b19bedc5171a49f5ceba71b96844beb62e80d8b9965ac0e41`  
		Last Modified: Sat, 27 Jan 2024 13:05:21 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d6ac1b2214639dcd8d2dcd8199a89dc33ab4fa888ba0a5edcd907d42bebfe6`  
		Last Modified: Sat, 27 Jan 2024 13:05:40 GMT  
		Size: 12.3 MB (12322454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb7cb4e799ed75a01a6ce920c86773b9e933c1dde20c09f8fb38cfd5328fda4`  
		Last Modified: Sat, 27 Jan 2024 13:05:36 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcec871bf5e855681a924c193a58aba764519c9894021ab056f3d1d216bf3c6c`  
		Last Modified: Sat, 27 Jan 2024 13:05:37 GMT  
		Size: 19.1 KB (19102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00136ec500399e3f6efa4819ecfda9b7df706c2def27973b8c14804523464fe`  
		Last Modified: Sat, 27 Jan 2024 13:05:37 GMT  
		Size: 8.9 KB (8879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d6bf5a1259f0be27749956ad6c0396678ea395abacea86d65596c8ba79b104`  
		Last Modified: Wed, 06 Mar 2024 03:18:40 GMT  
		Size: 29.6 MB (29624636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a726571ba5bff59c168ef4502568c513d1da160159f7376265f5ea818838941`  
		Last Modified: Thu, 14 Mar 2024 08:58:37 GMT  
		Size: 3.9 MB (3855380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:999e489604d24dfdddaf4730d5e91902b5805f18bfa0a8a2513b2393a5bd83cb`  
		Last Modified: Thu, 14 Mar 2024 08:58:36 GMT  
		Size: 59.4 KB (59418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc0a93ed36d846c901f7d84070635051a1bfaf0c4cecb578df7833ecd32a35c`  
		Last Modified: Thu, 14 Mar 2024 08:58:37 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd5947166129319114babddbe7a038ed5ec4d76feb8dcb392c4f224d487d1425`  
		Last Modified: Thu, 14 Mar 2024 18:18:08 GMT  
		Size: 24.5 MB (24522547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0c1a7debfdf614a378d45f6165256fc443b5557c065c4232ea58fec910551a`  
		Last Modified: Thu, 14 Mar 2024 18:18:07 GMT  
		Size: 2.4 KB (2353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894be16a7b7fd13cb508de8b64710850af7d8037afb626500e4129cc95f1a54a`  
		Last Modified: Thu, 14 Mar 2024 18:18:08 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:538c10c676fc098177b0f9ab2b3994f18fd5dce32f93e9dcbcd005a2bc98edfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1056098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7259e17a0d0e946c70b8683384714bbf968c2150485325ac0dcf422db4a76f5e`

```dockerfile
```

-	Layers:
	-	`sha256:4491eb3ba497c0e15d546ca7b09f044281ec635864d615877c6e10fa79e95b5c`  
		Last Modified: Thu, 14 Mar 2024 18:18:07 GMT  
		Size: 1.0 MB (1009349 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06c7690f03e8cbe72cc25350f283f55e8eedb4c864fdcdae245752fa583540ac`  
		Last Modified: Thu, 14 Mar 2024 18:18:07 GMT  
		Size: 46.7 KB (46749 bytes)  
		MIME: application/vnd.in-toto+json
