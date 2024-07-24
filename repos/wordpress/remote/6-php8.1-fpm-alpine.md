## `wordpress:6-php8.1-fpm-alpine`

```console
$ docker pull wordpress@sha256:3a3f98792f220493926cfc36c06774aa9601c8197a6ee26e20061ee45cfd3b61
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
$ docker pull wordpress@sha256:a30caf942723e27d390afb9f3ba4e72f89ee83383f4df0fb64b67045e3edc81b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.3 MB (87346803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffd466417d0e93885a3d840fa272c76e38dbcfa3bef39e7ed8e401a20c64add7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:43 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Mon, 22 Jul 2024 22:26:43 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 01:21:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 23 Jul 2024 01:21:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 23 Jul 2024 01:21:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 23 Jul 2024 01:21:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 23 Jul 2024 01:21:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 23 Jul 2024 01:21:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 Jul 2024 01:21:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 Jul 2024 01:21:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 Jul 2024 03:28:00 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 23 Jul 2024 03:28:00 GMT
ENV PHP_VERSION=8.1.29
# Tue, 23 Jul 2024 03:28:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Tue, 23 Jul 2024 03:28:00 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Tue, 23 Jul 2024 03:28:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 23 Jul 2024 03:28:05 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 23 Jul 2024 03:35:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 23 Jul 2024 03:36:00 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 23 Jul 2024 03:36:01 GMT
RUN docker-php-ext-enable sodium
# Tue, 23 Jul 2024 03:36:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 23 Jul 2024 03:36:01 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 03:36:02 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Tue, 23 Jul 2024 03:36:02 GMT
STOPSIGNAL SIGQUIT
# Tue, 23 Jul 2024 03:36:02 GMT
EXPOSE 9000
# Tue, 23 Jul 2024 03:36:02 GMT
CMD ["php-fpm"]
# Tue, 23 Jul 2024 19:30:08 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
RUN set -eux; 	version='6.6.1'; 	sha1='cd5544c85824e3cd8105018c63ccdba31883d881'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
VOLUME [/var/www/html]
# Tue, 23 Jul 2024 19:30:08 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jul 2024 19:30:08 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae0d9dfc4dada15e6a030ba7b9c9a3b16f9f5a7597a4d46ff24226e91b91db7`  
		Last Modified: Tue, 23 Jul 2024 03:55:04 GMT  
		Size: 3.3 MB (3272601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce295ca8623e5dc914104e970c5496db996db5f2abb336389bcbadd10465d21d`  
		Last Modified: Tue, 23 Jul 2024 03:55:03 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d3eb99f3c122bc8d6c22107602ed9c22fce771289b54bb2598142d1626f693`  
		Last Modified: Tue, 23 Jul 2024 03:55:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a72fb3364c73fdcb13e5b695da1fb0dd61d2a964437dca870d61ef6838a6b8`  
		Last Modified: Tue, 23 Jul 2024 04:03:47 GMT  
		Size: 11.8 MB (11847387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f903a35577bead659b898979c823c5131262b09508248b5f96ff93c78ef8b6a9`  
		Last Modified: Tue, 23 Jul 2024 04:03:46 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea1017fadda431a7920bdc852dd88a2274c9fdf960adba7334510669c44eb85`  
		Last Modified: Tue, 23 Jul 2024 04:04:09 GMT  
		Size: 12.6 MB (12612031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d5203ef29582462ba7cd947845705116fa0892c917ecc8fb3a8571018ce659`  
		Last Modified: Tue, 23 Jul 2024 04:04:07 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6f3b18a5996d0f826fc80b0f7e259c8049f3b9a4de9bdc8ba397ad509f8b43`  
		Last Modified: Tue, 23 Jul 2024 04:04:07 GMT  
		Size: 19.7 KB (19697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1faccbbd188bccd0d4caf71ac1cf1cb4d0c6ea00792d19d0b49c5db2f822466`  
		Last Modified: Tue, 23 Jul 2024 04:04:07 GMT  
		Size: 8.9 KB (8875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54fb88679bd8f0626218cd6fd3e27124046497aad7ad37b8eda717ebb7dc22d`  
		Last Modified: Wed, 24 Jul 2024 01:10:04 GMT  
		Size: 27.7 MB (27706951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:705918bccaf8d84c743a5e0816114bf35ee3889b71ff91cd7e5dceb35e10f2d5`  
		Last Modified: Wed, 24 Jul 2024 01:10:04 GMT  
		Size: 3.7 MB (3725011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec46bf250ea889e6ca8900c12a0ca970f8b443719383f88c4996a803d008d73f`  
		Last Modified: Wed, 24 Jul 2024 01:10:03 GMT  
		Size: 59.9 KB (59937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c57e43eb91331b073eb1f0713f2a8c93443fc12ea12fcf7b3bd15281fd30f0a`  
		Last Modified: Wed, 24 Jul 2024 01:10:03 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb1525c28a28cc6e31886269ef6c0641a187dadeae9c0409db1cd401f36a9d2`  
		Last Modified: Wed, 24 Jul 2024 01:10:05 GMT  
		Size: 24.5 MB (24462845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0b36d5af4dacbb503fe09e794b5d4fb0a671c7da8cc2356aed3f8d3cb880561`  
		Last Modified: Wed, 24 Jul 2024 01:10:04 GMT  
		Size: 2.3 KB (2349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd59b75378c58acdfff9c59e576d30aed1c2df96f6b1b02435a290ba0592dc1`  
		Last Modified: Wed, 24 Jul 2024 01:10:05 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:d657bcc54af750d9f8a8a1545bba4ec1835cd6e05a6dc24fa53a00ff1bdfb1a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1078360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5477f703b3a4dfbfbd754756da67c983cea9d1ee9b091b3b8c5b105cbcc8d70f`

```dockerfile
```

-	Layers:
	-	`sha256:099a5b124182404576f28c4553823eae534528d2e01978b6f639a7825db75d1c`  
		Last Modified: Wed, 24 Jul 2024 01:10:03 GMT  
		Size: 1.0 MB (1031606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:248425d410c728e1add42632921bba3dc031685ff4d6c8e2b88cc3586d040663`  
		Last Modified: Wed, 24 Jul 2024 01:10:03 GMT  
		Size: 46.8 KB (46754 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.1-fpm-alpine` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:4f56160480fd48ab888d4df6d28d612d1aa7949f088d8c2e58be44363d11f7b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82853610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a9e1a7c2609d6b5752fad382a743c2fe1fdb168cb29a774619c270038840cdd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 22 Jul 2024 21:49:18 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Mon, 22 Jul 2024 21:49:19 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 22:16:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jul 2024 22:16:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 22 Jul 2024 22:16:44 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 22 Jul 2024 22:16:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jul 2024 22:16:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 22 Jul 2024 22:16:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:16:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 22:16:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 Jul 2024 00:30:38 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 23 Jul 2024 00:30:38 GMT
ENV PHP_VERSION=8.1.29
# Tue, 23 Jul 2024 00:30:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Tue, 23 Jul 2024 00:30:39 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Tue, 23 Jul 2024 00:30:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 23 Jul 2024 00:30:46 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 23 Jul 2024 00:39:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 23 Jul 2024 00:39:06 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 23 Jul 2024 00:39:07 GMT
RUN docker-php-ext-enable sodium
# Tue, 23 Jul 2024 00:39:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 23 Jul 2024 00:39:08 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 00:39:09 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Tue, 23 Jul 2024 00:39:09 GMT
STOPSIGNAL SIGQUIT
# Tue, 23 Jul 2024 00:39:09 GMT
EXPOSE 9000
# Tue, 23 Jul 2024 00:39:10 GMT
CMD ["php-fpm"]
# Tue, 23 Jul 2024 19:30:08 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
RUN set -eux; 	version='6.6.1'; 	sha1='cd5544c85824e3cd8105018c63ccdba31883d881'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
VOLUME [/var/www/html]
# Tue, 23 Jul 2024 19:30:08 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jul 2024 19:30:08 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b041a1a670328abed5fe2b73e068aba477e969ddbfe65c606c8054a4c36067b2`  
		Last Modified: Tue, 23 Jul 2024 01:00:35 GMT  
		Size: 3.3 MB (3263638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51daa6109cd19af541c6fc2600ad5a2f2382e50d3938e2b51f30d24df583fee`  
		Last Modified: Tue, 23 Jul 2024 01:00:33 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b57c8706e4f06f42a10294d5c9eef985613e48298dedb390c6e6816b60a8f78`  
		Last Modified: Tue, 23 Jul 2024 01:00:33 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf93de61e35babe0a6323ab894a6c16bb734d7526a4350782d7f0566838fb1b`  
		Last Modified: Tue, 23 Jul 2024 01:09:18 GMT  
		Size: 11.8 MB (11847377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cace6bb4c1462e21f963a1bbc551e2ea3fa87903b850a5fc7a4159e2548291e`  
		Last Modified: Tue, 23 Jul 2024 01:09:17 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7597437bf208ecf10c9c19f280251f02e164d617a408f6fd93debc1808804b6d`  
		Last Modified: Tue, 23 Jul 2024 01:09:44 GMT  
		Size: 11.4 MB (11437266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e8e9229bf40bffd22d16366806c7adc0ff84234aec7ed6f96e20d07d34c54d`  
		Last Modified: Tue, 23 Jul 2024 01:09:41 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0883622889dd1eaaf5d640ce80897009de07037975e969ad645b353099a19208`  
		Last Modified: Tue, 23 Jul 2024 01:09:41 GMT  
		Size: 19.5 KB (19492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fecaa3cc6ee14eebadd2646f6c193b81773f915aabfadd3e8327887dca767d4c`  
		Last Modified: Tue, 23 Jul 2024 01:09:41 GMT  
		Size: 8.9 KB (8878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9a6fe715eee911e5917ddb496a81fe0546ec231e3c188842961f4eb8cbc7052`  
		Last Modified: Tue, 23 Jul 2024 12:28:00 GMT  
		Size: 24.0 MB (23953222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8f28117ea27cf84f1c4ae037271b58b3b51b5a0cc7518006dbcf53c512c706`  
		Last Modified: Tue, 23 Jul 2024 12:28:00 GMT  
		Size: 4.4 MB (4427208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c59f2e92357241bf1d473c4b5293f2da5f08728370ba5a599ad10e2b946a55a`  
		Last Modified: Tue, 23 Jul 2024 12:28:00 GMT  
		Size: 59.9 KB (59915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7cd9061cf2a1a0be038fc62ed003ebd881f568199902f34cdef6e15ccc0f3b3`  
		Last Modified: Tue, 23 Jul 2024 12:28:00 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5d20298320fddf55f97d95d811ab31efba7dd819e2487712444b89811cf00c`  
		Last Modified: Wed, 24 Jul 2024 01:12:43 GMT  
		Size: 24.5 MB (24462849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb244f29c15d1c605cfa006ce5715c912fda485c16faacf0d356087094eb525`  
		Last Modified: Wed, 24 Jul 2024 01:12:42 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e0f64ff322f048251ff788ce41a79c2ed7521ed95a0ff2894356d2de710277`  
		Last Modified: Wed, 24 Jul 2024 01:12:42 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:63f44759d08735928b9c2675a20bc924da632a5df776b427a3512685c500f38f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 KB (46657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c41571b8a873d28b02bfc7635e9c9215364d209864dec18b94598501b981210f`

```dockerfile
```

-	Layers:
	-	`sha256:ffc1b0f4cb5a4982d137d5485023a8c8ddd88d8b1dbd2160252c3b21b10ebaff`  
		Last Modified: Wed, 24 Jul 2024 01:12:41 GMT  
		Size: 46.7 KB (46657 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.1-fpm-alpine` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:4977316e331a89e6f29a175c0e4a996a1db9cc3f5d796c5108e19d40f08cbac8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83169683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aca6169f88954526ba18a7e7709145737ec7b2c28201f11280bba4bf61b2411`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:28 GMT
ADD file:4d58f44e3cedeba6fad741c79bc5acab1a9f2a2f597c854dc3bb8b8595ebf3e1 in / 
# Thu, 20 Jun 2024 18:00:28 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 18:17:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 18:17:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 18:17:29 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 18:17:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 18:17:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 18:17:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 18:17:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 18:17:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 19:32:12 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 20 Jun 2024 19:32:13 GMT
ENV PHP_VERSION=8.1.29
# Thu, 20 Jun 2024 19:32:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Thu, 20 Jun 2024 19:32:13 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Thu, 20 Jun 2024 19:32:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 19:32:21 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 19:43:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 19:43:09 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 20 Jun 2024 19:43:11 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 19:43:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 19:43:12 GMT
WORKDIR /var/www/html
# Thu, 20 Jun 2024 19:43:14 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 20 Jun 2024 19:43:14 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Jun 2024 19:43:15 GMT
EXPOSE 9000
# Thu, 20 Jun 2024 19:43:15 GMT
CMD ["php-fpm"]
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -eux; 	version='6.6'; 	sha1='6bdc580973c6c5e44c0c6164c348217152874817'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
VOLUME [/var/www/html]
# Tue, 16 Jul 2024 19:06:40 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jul 2024 19:06:40 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3fb467f9cb36e54d3cb8806db734a6c640048f3dc270b506ec1f111640905b79`  
		Last Modified: Thu, 20 Jun 2024 18:00:55 GMT  
		Size: 3.1 MB (3094856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b938a00e90a786cd6136482ec16d36fde70734970bf1a3417ac3a7bc1ae3db78`  
		Last Modified: Thu, 20 Jun 2024 20:08:04 GMT  
		Size: 3.1 MB (3069230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eff9bafae6056d786c9d80432f880c7019dc7cbabf4b4422e3722984e47fc241`  
		Last Modified: Thu, 20 Jun 2024 20:08:02 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93bf863a52c49447e08f0ca17d6916598399d3a5919085117aee7b8825dff07e`  
		Last Modified: Thu, 20 Jun 2024 20:08:02 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701b2d09d1b7236090c36184c7aced5a8993737350f2c5c55e71af94c994d972`  
		Last Modified: Thu, 20 Jun 2024 20:12:42 GMT  
		Size: 11.8 MB (11847387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:136a145a33aa3979e9c41d180b717263418df9404459264755b43bfca7db1e1b`  
		Last Modified: Thu, 20 Jun 2024 20:12:40 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6119489c7d3ba12f1c2f21b58c5ece68b52d851aae0098036fd10b46c60e8a`  
		Last Modified: Thu, 20 Jun 2024 20:13:08 GMT  
		Size: 10.7 MB (10722807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a40d14159110f10ceff9697413206a692867e61d6694c598969d8e67afae001`  
		Last Modified: Thu, 20 Jun 2024 20:13:05 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ac217d369744ca65552a004dc4534d19ad92799485a0ea8bf3261a53b6f692d`  
		Last Modified: Thu, 20 Jun 2024 20:13:05 GMT  
		Size: 19.5 KB (19484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b83b326e1c2e762247c61592988400e4fce1c02f9b9090f96a1b8711cc1096`  
		Last Modified: Thu, 20 Jun 2024 20:13:05 GMT  
		Size: 8.9 KB (8879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8096c24b4a2f5d1e475e9a41cf4275eb6bf537cc3ae7b41ed1eaa0b1bf60dcf`  
		Last Modified: Wed, 03 Jul 2024 19:51:04 GMT  
		Size: 26.3 MB (26288361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57ad5600071675c89c67390b0b8b642c36271a342114dc0b0a16b1b23b3a43a6`  
		Last Modified: Wed, 03 Jul 2024 19:51:04 GMT  
		Size: 3.6 MB (3590004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf14701b01397f028515f42e8748437f61b12ca32db0dadf606b59dd00224dd0`  
		Last Modified: Wed, 03 Jul 2024 19:51:04 GMT  
		Size: 59.7 KB (59723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850d8a10ab4d9920a8782eaf0b9d50613ba2225580b51a2d8479e17d9be3b0ae`  
		Last Modified: Wed, 03 Jul 2024 19:51:04 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e4a468e0dc10a78f98797ae6ad32903bfad3619d2d091354e0271c9ef634a9`  
		Last Modified: Tue, 16 Jul 2024 22:58:53 GMT  
		Size: 24.5 MB (24460367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddddada21d9019c28a7712ec519421ea9dc7ecbe05f18c17c0c8e22eb7635e95`  
		Last Modified: Tue, 16 Jul 2024 22:58:52 GMT  
		Size: 2.4 KB (2352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813bbe96f2763272d5a9b131b8ca81e60573cb0fdf4516c02b8bfce428eb390d`  
		Last Modified: Tue, 16 Jul 2024 22:58:52 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:7ff0465635c45b1b0420c3c35b0a858eb5bdb172ea42546d2b20c015ec5dcc89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1075744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:183f607f1912cb48f5dd7000e7172b956a4f46fe331222c07a4a428ee6edcc05`

```dockerfile
```

-	Layers:
	-	`sha256:423e8cb79497a5e5b3f9b3f0c3b0d67066060d42064ffb7b29d5b6c710aa2621`  
		Last Modified: Tue, 16 Jul 2024 22:58:52 GMT  
		Size: 1.0 MB (1028874 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd372a1bc08397308d25fe2e54bb4a1217a66146f12a5dd26aaed8a297f934ab`  
		Last Modified: Tue, 16 Jul 2024 22:58:51 GMT  
		Size: 46.9 KB (46870 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.1-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:b91e2d13fcbb934faed9e893443e1d054c1b58ec6285a180ea87327b25b91eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88656377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fc6189eccc195777c45e260c69cd4cd7eb735527e0a37e75d9f629a370a5933`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 22:37:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 22:37:26 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 22:37:26 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 22:37:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 22:37:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 22:37:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 22:37:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 22:37:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 23:30:44 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 20 Jun 2024 23:30:44 GMT
ENV PHP_VERSION=8.1.29
# Thu, 20 Jun 2024 23:30:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Thu, 20 Jun 2024 23:30:45 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Thu, 20 Jun 2024 23:30:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 23:30:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 23:38:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 23:38:51 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 20 Jun 2024 23:38:52 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 23:38:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 23:38:53 GMT
WORKDIR /var/www/html
# Thu, 20 Jun 2024 23:38:53 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 20 Jun 2024 23:38:53 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Jun 2024 23:38:53 GMT
EXPOSE 9000
# Thu, 20 Jun 2024 23:38:53 GMT
CMD ["php-fpm"]
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -eux; 	version='6.6'; 	sha1='6bdc580973c6c5e44c0c6164c348217152874817'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
VOLUME [/var/www/html]
# Tue, 16 Jul 2024 19:06:40 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jul 2024 19:06:40 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7259c6ecde9ace3d2e6f16129e48d1f2a4617a863b50141060d68dff3bca6be4`  
		Last Modified: Thu, 20 Jun 2024 23:57:33 GMT  
		Size: 3.3 MB (3321315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cba877fe96736ac16322578eac8e248770148b6e42b5f6059172ee20a2285ebf`  
		Last Modified: Thu, 20 Jun 2024 23:57:32 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8737749d8335aefd2aa7a5ecff2afc3bd5458f2f463a8dd634f9e53e953f7fa`  
		Last Modified: Thu, 20 Jun 2024 23:57:32 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3b7520703454786c6fc4ed5b0de4a3bbc1558de709ed7edaa08fb282ff78c8f`  
		Last Modified: Fri, 21 Jun 2024 00:01:35 GMT  
		Size: 11.8 MB (11847373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f181573376dc8f044ea139f81c00cc0151725c49de52abc3062ffb027670fd3d`  
		Last Modified: Fri, 21 Jun 2024 00:01:34 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c600a5cdfb8129cfa31d8df180fb6d80c3a28fc4d76f2a78456b6c399c5d2f`  
		Last Modified: Fri, 21 Jun 2024 00:01:57 GMT  
		Size: 12.7 MB (12662404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db297191a7640db15c048b1b4d146c8689cf0ecc7f0c00f652588b01b629a799`  
		Last Modified: Fri, 21 Jun 2024 00:01:55 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d21fa5789aa174f90f0f87e478b0fcb37c21b7f328c7d7842b886c8012eff76`  
		Last Modified: Fri, 21 Jun 2024 00:01:55 GMT  
		Size: 19.5 KB (19475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b230f032eaf15f0fed9c09f772660b251abfeeb87438c3ff7fce8833a4a05026`  
		Last Modified: Fri, 21 Jun 2024 00:01:55 GMT  
		Size: 8.9 KB (8878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c04a62fd3c97c4f17657885e655a42c225254d29fcdc070adc20f8816f7fcd`  
		Last Modified: Wed, 03 Jul 2024 19:11:42 GMT  
		Size: 28.4 MB (28412219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8f2043e6db0370dd5bff13681921e5063a9926cad09189475359ee6c722ce16`  
		Last Modified: Wed, 03 Jul 2024 19:11:42 GMT  
		Size: 3.8 MB (3767310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28d6330523f7f305ee3e4fa0fbe345fcf80200ec6c8a444b859f9c6b54aac9c`  
		Last Modified: Wed, 03 Jul 2024 19:11:41 GMT  
		Size: 59.7 KB (59652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e959eba9cb1e1b04471eb0c588d70964b3fec309fdacdef932fd0e264e5f74`  
		Last Modified: Wed, 03 Jul 2024 19:11:41 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923401e8951c8ac9d6ebf91b680f70e990136c41f0dea1e3cd1585d73490a0c3`  
		Last Modified: Tue, 16 Jul 2024 22:58:00 GMT  
		Size: 24.5 MB (24460370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60f5dfd0f6bf66ce19fcd2f819724f9711de1f802ddd1fd4324fcdebc6ffb8f5`  
		Last Modified: Tue, 16 Jul 2024 22:57:59 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9c07cdb7a88fb05de6bbc07d02c6177a47bcecede3633b99269b78e0802201`  
		Last Modified: Tue, 16 Jul 2024 22:57:59 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:8c52db54699cb54a4ebf8a476607ed81eb4a4597f0f301a324ddf9ad853acdfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1075949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ddd7d5c7708fb54b941386a373342aafb8e352adef569f09168cc2ac9195e0`

```dockerfile
```

-	Layers:
	-	`sha256:c87a82026bf172aa34a48c26a8bcb2ad20d05899506493865d0d918bd9b8b583`  
		Last Modified: Tue, 16 Jul 2024 22:57:59 GMT  
		Size: 1.0 MB (1028894 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8dd85dbfa8fdcad4a320aba28da348b4ada49828de56d79f06e7b93802d6df98`  
		Last Modified: Tue, 16 Jul 2024 22:57:59 GMT  
		Size: 47.1 KB (47055 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.1-fpm-alpine` - linux; 386

```console
$ docker pull wordpress@sha256:5e62c6ec45e2aee57b96db418e69fad588806a6494fb8e1c074fb289d62bf441
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.0 MB (87987319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:911710c3505c8f814e77bf5f726cc4215461db153c88c250a1154c716e74418d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 22 Jul 2024 21:38:29 GMT
ADD file:e5b77b9337c5f89df9a65f8c439736a6d79e68274100ab1a1d7d61359a9abf5d in / 
# Mon, 22 Jul 2024 21:38:30 GMT
CMD ["/bin/sh"]
# Mon, 22 Jul 2024 21:58:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 22 Jul 2024 21:58:53 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Mon, 22 Jul 2024 21:58:53 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 22 Jul 2024 21:58:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 22 Jul 2024 21:58:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Mon, 22 Jul 2024 21:58:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 21:58:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 22 Jul 2024 21:58:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 Jul 2024 01:31:14 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 23 Jul 2024 01:31:14 GMT
ENV PHP_VERSION=8.1.29
# Tue, 23 Jul 2024 01:31:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Tue, 23 Jul 2024 01:31:14 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Tue, 23 Jul 2024 01:31:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 23 Jul 2024 01:31:19 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 23 Jul 2024 01:44:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 23 Jul 2024 01:44:34 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 23 Jul 2024 01:44:36 GMT
RUN docker-php-ext-enable sodium
# Tue, 23 Jul 2024 01:44:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 23 Jul 2024 01:44:36 GMT
WORKDIR /var/www/html
# Tue, 23 Jul 2024 01:44:36 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Tue, 23 Jul 2024 01:44:37 GMT
STOPSIGNAL SIGQUIT
# Tue, 23 Jul 2024 01:44:37 GMT
EXPOSE 9000
# Tue, 23 Jul 2024 01:44:37 GMT
CMD ["php-fpm"]
# Tue, 23 Jul 2024 19:30:08 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
RUN set -eux; 	version='6.6.1'; 	sha1='cd5544c85824e3cd8105018c63ccdba31883d881'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
VOLUME [/var/www/html]
# Tue, 23 Jul 2024 19:30:08 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 23 Jul 2024 19:30:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 23 Jul 2024 19:30:08 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2585500d54afa42a6b579f9ed6f62b49c5fb21c2653f79194342804bde8770fe`  
		Last Modified: Mon, 22 Jul 2024 21:38:55 GMT  
		Size: 3.5 MB (3468071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3702ede31b739c37f265c096aaa90041a249a222cf13f8141408974d1da345`  
		Last Modified: Tue, 23 Jul 2024 02:14:27 GMT  
		Size: 3.3 MB (3322587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd32fd053b31656313ffe5c4d6a711c2bdfbac32689ec3ed4eb1993c89d7c5cf`  
		Last Modified: Tue, 23 Jul 2024 02:14:26 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c734d1f76ba06cf1de68095cf88223f8aecf6242e60ae0985e4b555bd937308d`  
		Last Modified: Tue, 23 Jul 2024 02:14:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35ac3c7a6049cbb2c43c3cee3a082c78b920ba2c95a857eec5ddce781382071`  
		Last Modified: Tue, 23 Jul 2024 02:23:56 GMT  
		Size: 11.8 MB (11847383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3699cf6a7dea95ba3951a43f9fc20dd776ad2e27cd5b3879cd0f404e2521b03e`  
		Last Modified: Tue, 23 Jul 2024 02:23:55 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b7df077f9c1a5f393603f12aa08121ada8fc2f47f31800f0b61cbe2d4cd456`  
		Last Modified: Tue, 23 Jul 2024 02:24:21 GMT  
		Size: 12.9 MB (12939651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f9284b854b7ba651e4776ad2f7c9a68a1007a43cac9453f0ca79e276b0e326`  
		Last Modified: Tue, 23 Jul 2024 02:24:18 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473ae4ce44e894cd868035147f2bafc9fe93aa11bcab02f3e0b695b2e053e19f`  
		Last Modified: Tue, 23 Jul 2024 02:24:18 GMT  
		Size: 19.7 KB (19699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47f470755c2dd792049ebfbec5841c7d5438911e66c43d8e506c067c9fe0c42`  
		Last Modified: Tue, 23 Jul 2024 02:24:18 GMT  
		Size: 8.9 KB (8880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eca1db88dd410bec1b9816b6dbee9e3435677fe8cb7621e30a64b7f34ec62c0`  
		Last Modified: Wed, 24 Jul 2024 01:10:18 GMT  
		Size: 28.0 MB (27962922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e766c39113c7ab2e9306b48bb1a8de9b9deec97355f81708221753a004b5d6d`  
		Last Modified: Wed, 24 Jul 2024 01:10:17 GMT  
		Size: 3.9 MB (3886832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c9ace200f3bba70f4c63126a1da1d575ec1d99c70b3c2312c228f2f9bb11de`  
		Last Modified: Wed, 24 Jul 2024 01:10:17 GMT  
		Size: 59.9 KB (59917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da940baa914ebf49cd7123667ccf949f245ac4c34a03faf48da606ecda9e904`  
		Last Modified: Wed, 24 Jul 2024 01:10:16 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1847a400c9cd61dc5d96899aced774cc1851da805427f1839a0de9bee06eb26`  
		Last Modified: Wed, 24 Jul 2024 01:10:19 GMT  
		Size: 24.5 MB (24462806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2128f3d7001d8b26a441f87d7492c466e5dec3d294f15285c59916343dad1ff`  
		Last Modified: Wed, 24 Jul 2024 01:10:17 GMT  
		Size: 2.3 KB (2345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a8a53c5f2e82c01a3667dc7d22a86644f1e40d8935cab93af0257176b8acdc0`  
		Last Modified: Wed, 24 Jul 2024 01:10:18 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:60324c4422e48a762ba7b8b68c7b3b951a66a3046f412b70c6caaa9d0d42ab09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1078298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4cf65fa5dfdfc0f7f6c99c636b95c6552b0b51eb99dad53b7413b625f5c17d6`

```dockerfile
```

-	Layers:
	-	`sha256:7246eeb9dac73411212cfa14b99159dc5d77acfd3f6793d9b0b3e56f7c79b265`  
		Last Modified: Wed, 24 Jul 2024 01:10:17 GMT  
		Size: 1.0 MB (1031581 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47d5a10bf3b7227881fb587a3c8da9d63e65f966527edd492f48a9591805e0ab`  
		Last Modified: Wed, 24 Jul 2024 01:10:16 GMT  
		Size: 46.7 KB (46717 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.1-fpm-alpine` - linux; ppc64le

```console
$ docker pull wordpress@sha256:d3cc592e6c46d2fd0565763780db0db0b74bba741a7019f007562d8128593f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.3 MB (89286805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9bc1993393e799cedaf373ecc08beaeb1f681390a95842d805a452d40fe591d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:21 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Thu, 20 Jun 2024 18:18:22 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 18:43:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 18:43:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 18:43:14 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 18:43:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 18:43:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 18:43:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 18:43:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 18:43:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 19:18:36 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 20 Jun 2024 19:18:36 GMT
ENV PHP_VERSION=8.1.29
# Thu, 20 Jun 2024 19:18:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Thu, 20 Jun 2024 19:18:37 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Thu, 20 Jun 2024 19:20:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 20 Jun 2024 19:20:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 19:25:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 19:25:58 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 20 Jun 2024 19:26:00 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 19:26:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 19:26:00 GMT
WORKDIR /var/www/html
# Thu, 20 Jun 2024 19:26:02 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 20 Jun 2024 19:26:02 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Jun 2024 19:26:02 GMT
EXPOSE 9000
# Thu, 20 Jun 2024 19:26:02 GMT
CMD ["php-fpm"]
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -eux; 	version='6.6'; 	sha1='6bdc580973c6c5e44c0c6164c348217152874817'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
VOLUME [/var/www/html]
# Tue, 16 Jul 2024 19:06:40 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jul 2024 19:06:40 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6a26704de1bf6248f6df44727e1e01ae48fec7917e229bc3e343c672804b51`  
		Last Modified: Thu, 20 Jun 2024 19:38:43 GMT  
		Size: 3.4 MB (3395236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ee9c5937bf5aa444d1623e38c7154bb2971a8bd3cbd2f3b736c22ed6c73927`  
		Last Modified: Thu, 20 Jun 2024 19:38:41 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84c1b8ee2969afc28f29a4447dc6ee6dbe5a916abb033890d01ce72b9e98d79`  
		Last Modified: Thu, 20 Jun 2024 19:38:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6786cdf2ba2e763d7f565ac08054ef090fad8282fbd84e0ee79a540b97c1ad10`  
		Last Modified: Thu, 20 Jun 2024 19:42:49 GMT  
		Size: 11.8 MB (11847387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2116f97c8303d9103f65f33c9b8abb47d99118cfbe66b98fbdfc0162291f6d15`  
		Last Modified: Thu, 20 Jun 2024 19:42:48 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d936d4daca873b501c2a9accc5119a661c7f9c3797c2a58f1e8e2eb0c1f0a0d1`  
		Last Modified: Thu, 20 Jun 2024 19:43:14 GMT  
		Size: 13.1 MB (13055958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8e3fe7448a5983d1f14bc11b0a79c38a96111c25d73114cb76c6e893d29a43`  
		Last Modified: Thu, 20 Jun 2024 19:43:12 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373a6eba41633add7fb208c0cefcb8ea0ed19b27dee965706d0f9cbf5c8558fa`  
		Last Modified: Thu, 20 Jun 2024 19:43:12 GMT  
		Size: 19.5 KB (19477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56528d0b1572c17e90b62e84891146b83cb292e2efb45c1d5b4b64254fb44e9b`  
		Last Modified: Thu, 20 Jun 2024 19:43:11 GMT  
		Size: 8.9 KB (8877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e5244a6f29f35cf82acfc7dfa46127d70a5678304d94280f87929d0d211733`  
		Last Modified: Wed, 03 Jul 2024 23:08:01 GMT  
		Size: 29.0 MB (28979086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41acc6cc5d77cc28545898898d8331f9c7b67ea66a162bccd7e889f3ec9d5d9`  
		Last Modified: Wed, 03 Jul 2024 23:08:01 GMT  
		Size: 3.9 MB (3880452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abdfadf283a4c7f4d84eab898823184b0e2c3b4168247f0962d7c2575fb973e`  
		Last Modified: Wed, 03 Jul 2024 23:08:00 GMT  
		Size: 59.7 KB (59679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f939ed12860df2ba65dfe8607fd802249be0e49cef3bad399f5fcc77a8e7e3e8`  
		Last Modified: Wed, 03 Jul 2024 23:08:00 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8becefbcd2216146b4b71802c3e590da8eb7efd1ed47613d218036910c94f6`  
		Last Modified: Tue, 16 Jul 2024 22:59:06 GMT  
		Size: 24.5 MB (24460366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed65cc37f6add42afd399257f74e76fecd375275535cf76d7394bae133e5b6fa`  
		Last Modified: Tue, 16 Jul 2024 22:59:05 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2bf16d18a219f9fee3335b88802e457f6cd7d63b37f162e18cfdb3b95d0574`  
		Last Modified: Tue, 16 Jul 2024 22:59:05 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:c6bd18c304926ade0daacd7804c18dcb44412e856b1de5d992e8b269a5584177
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1073712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:035b7c8a82e2fee81c604c32a13abc257ffc0c0cab64fc172a119a1fa33a90b4`

```dockerfile
```

-	Layers:
	-	`sha256:f7076f93a6fd8031748ee6331f1647d1fe29f97936db409a7787beae97625a00`  
		Last Modified: Tue, 16 Jul 2024 22:59:05 GMT  
		Size: 1.0 MB (1026918 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:834fb14fecf0090441a5610b77c4fd6c4c138e655d76496e7436e113863268d5`  
		Last Modified: Tue, 16 Jul 2024 22:59:04 GMT  
		Size: 46.8 KB (46794 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.1-fpm-alpine` - linux; riscv64

```console
$ docker pull wordpress@sha256:5e73ec8aba67a6a6941626886f1b48563e696809078ba2e04b9d8384446c5e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.2 MB (87203774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:536ab667fe353b5d22666e88553f0289c5352a0a6f10afe066924bd47ab48115`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:03 GMT
ADD file:851dbd05bad08468ee2a960e5f9f0aa9b19f1114ec52c39d1a28cd427344d0ef in / 
# Thu, 20 Jun 2024 18:18:04 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 20:56:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 20:56:07 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 20:56:10 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 20:56:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 20:56:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 20:56:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 20:56:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 20:56:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 21 Jun 2024 01:24:52 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 21 Jun 2024 01:24:52 GMT
ENV PHP_VERSION=8.1.29
# Fri, 21 Jun 2024 01:24:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Fri, 21 Jun 2024 01:24:53 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Fri, 21 Jun 2024 01:25:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 21 Jun 2024 01:25:10 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 21 Jun 2024 02:46:29 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 21 Jun 2024 02:46:31 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 21 Jun 2024 02:46:38 GMT
RUN docker-php-ext-enable sodium
# Fri, 21 Jun 2024 02:46:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 21 Jun 2024 02:46:39 GMT
WORKDIR /var/www/html
# Fri, 21 Jun 2024 02:46:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 21 Jun 2024 02:46:42 GMT
STOPSIGNAL SIGQUIT
# Fri, 21 Jun 2024 02:46:43 GMT
EXPOSE 9000
# Fri, 21 Jun 2024 02:46:43 GMT
CMD ["php-fpm"]
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -eux; 	version='6.6'; 	sha1='6bdc580973c6c5e44c0c6164c348217152874817'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
VOLUME [/var/www/html]
# Tue, 16 Jul 2024 19:06:40 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jul 2024 19:06:40 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d4714cc4c8bb5ceda619fceb44b088091082a8d2407d2008123fe93478722d1a`  
		Last Modified: Thu, 20 Jun 2024 18:18:22 GMT  
		Size: 3.4 MB (3371037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75477805297b2e5d3e45445d2b14ef5781642095163a9180372584156228308d`  
		Last Modified: Fri, 21 Jun 2024 03:29:15 GMT  
		Size: 3.4 MB (3390439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f052e2934ece7510f678f44b5c8af4ca01c8c831d77f69244bf017c94d869629`  
		Last Modified: Fri, 21 Jun 2024 03:29:11 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb6c1f73b878cfca599e88261cc519ca171226efafcdd1238320261b2c41459`  
		Last Modified: Fri, 21 Jun 2024 03:29:11 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa464477aba35b821c25284a6a518cb006d747f7c2f935d5f5c36b915cce826`  
		Last Modified: Fri, 21 Jun 2024 03:33:24 GMT  
		Size: 11.8 MB (11847383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc2f56c0fe0b766abf63d507297d2668abfb4e9c6be97250d432e32b09129aa`  
		Last Modified: Fri, 21 Jun 2024 03:33:18 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ef66de0df6b25e3577ec99fd6b2a5ee224f526235ead3ace3eea5ae0286a77`  
		Last Modified: Fri, 21 Jun 2024 03:34:11 GMT  
		Size: 11.9 MB (11934213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7589d3d83dfa2cddd6e573a0002c7826ea8175d4d54ecee587568ccbf1cc8b50`  
		Last Modified: Fri, 21 Jun 2024 03:33:59 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0905a075f3e04940d0b8bc263f8f24809c98969ce03307eba7701f321d68c6d0`  
		Last Modified: Fri, 21 Jun 2024 03:33:59 GMT  
		Size: 19.5 KB (19482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ca8de1443a079c1ecc1921c1cfbd1283e6ee7f2ae5f4c2aabafe8492b63f62`  
		Last Modified: Fri, 21 Jun 2024 03:33:59 GMT  
		Size: 8.9 KB (8883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002c75e8f3b39c50b188733defe19c1e6d5af63e10b1a7f2a9c4c725a2774b7f`  
		Last Modified: Thu, 04 Jul 2024 01:54:20 GMT  
		Size: 28.4 MB (28353840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b43f5de46397b68afc970b7d08325c25e6dec681e7c9854a992fa9bf067a5f`  
		Last Modified: Thu, 04 Jul 2024 01:54:16 GMT  
		Size: 3.7 MB (3749849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c03c4c90e406c180ea242750664ecdd37ce81299d9a640965af9cbb68596287`  
		Last Modified: Thu, 04 Jul 2024 01:54:16 GMT  
		Size: 59.7 KB (59696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2aac1fd45768ee6f5f31a4ab075adc34abc9d8378168be21c91d7e0ce0536a`  
		Last Modified: Thu, 04 Jul 2024 01:54:16 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b99a04d4531ff247d95fa23bf98561727ae58709e048d864f0dc8add71dac98`  
		Last Modified: Tue, 16 Jul 2024 22:58:30 GMT  
		Size: 24.5 MB (24460366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a73f6d127cad688483b2869982a067a4ce04cef12486be33b5361380f4ffd6d`  
		Last Modified: Tue, 16 Jul 2024 22:58:26 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f781c6b672376964e12b36cf2b160711cdfeab6f034c92daba2185f3b1aeb664`  
		Last Modified: Tue, 16 Jul 2024 22:58:26 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:4b1d294808d9c6bd7141c96ab9771e0bb8bb2f097978ece398e88cbc1fa79961
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1073708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be4da8194b5832fba1ee1a2ffb47233607bfe9c6b76112fab03cf01b9df49162`

```dockerfile
```

-	Layers:
	-	`sha256:9d3cc74fb12748b233841d34bacf918776a08848c6e9cff1144796375b0c660a`  
		Last Modified: Tue, 16 Jul 2024 22:58:26 GMT  
		Size: 1.0 MB (1026914 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89145f81672beee26210d2852d60cbdf6cc47fdc47a281ecab40a67d1da43a04`  
		Last Modified: Tue, 16 Jul 2024 22:58:25 GMT  
		Size: 46.8 KB (46794 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.1-fpm-alpine` - linux; s390x

```console
$ docker pull wordpress@sha256:2ac94a226fbcff7edbc4b4822d565875ee793e1e6b46107507a64d000147a23d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.0 MB (88969109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10ed21f2bab6f32aee335b613aa7a813dc27a579e298e3c5bbe817c8a6f7d99b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:02 GMT
ADD file:23eeda2aa519e3b51e03f1ce8faeb8c4b597b4b31ec175cb09306147000967fc in / 
# Thu, 20 Jun 2024 17:42:03 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 00:27:39 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 21 Jun 2024 00:27:42 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 21 Jun 2024 00:27:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 21 Jun 2024 00:27:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 21 Jun 2024 00:27:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 21 Jun 2024 00:27:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 21 Jun 2024 00:27:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 21 Jun 2024 00:27:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 21 Jun 2024 01:40:33 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 21 Jun 2024 01:40:33 GMT
ENV PHP_VERSION=8.1.29
# Fri, 21 Jun 2024 01:40:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Fri, 21 Jun 2024 01:40:33 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Fri, 21 Jun 2024 01:40:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 21 Jun 2024 01:40:38 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 21 Jun 2024 01:46:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 21 Jun 2024 01:46:36 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 21 Jun 2024 01:46:37 GMT
RUN docker-php-ext-enable sodium
# Fri, 21 Jun 2024 01:46:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 21 Jun 2024 01:46:37 GMT
WORKDIR /var/www/html
# Fri, 21 Jun 2024 01:46:37 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 21 Jun 2024 01:46:37 GMT
STOPSIGNAL SIGQUIT
# Fri, 21 Jun 2024 01:46:38 GMT
EXPOSE 9000
# Fri, 21 Jun 2024 01:46:38 GMT
CMD ["php-fpm"]
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
RUN set -eux; 	version='6.6'; 	sha1='6bdc580973c6c5e44c0c6164c348217152874817'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
VOLUME [/var/www/html]
# Tue, 16 Jul 2024 19:06:40 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 16 Jul 2024 19:06:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 16 Jul 2024 19:06:40 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f9a77bce0ddc1b9251f410e8c69566b002f4e557ee68895b558671311b17fd91`  
		Last Modified: Thu, 20 Jun 2024 17:43:02 GMT  
		Size: 3.5 MB (3461856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3e83a7b4cb32d011e679386186946d82818581def86d57f1b8c9ca8c934c1c`  
		Last Modified: Fri, 21 Jun 2024 02:02:33 GMT  
		Size: 3.5 MB (3462701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1864acc991a0f2fd74bdcd479ec121dcab7cd543eb1e6666fac2260843f34bbd`  
		Last Modified: Fri, 21 Jun 2024 02:02:32 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed80ee1d18ee2422d537f9fbb168383860d34cfce3c9b043a35b6d86b38f2da6`  
		Last Modified: Fri, 21 Jun 2024 02:02:32 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd20f8dac69a34fa2ccc8de7657c74cb8dd1a00808264b9d47f71cc87066397`  
		Last Modified: Fri, 21 Jun 2024 02:06:02 GMT  
		Size: 11.8 MB (11847379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b6e40b7c310931b373cb2eedef3e019fc20397eb566d27cd6ef4724596474b`  
		Last Modified: Fri, 21 Jun 2024 02:06:01 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b908e19ff274e57b1f10dc89b395c30ffa37042e91746db50d70b7119e6cea2`  
		Last Modified: Fri, 21 Jun 2024 02:06:20 GMT  
		Size: 12.5 MB (12547524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6017ab45bdeb94cfbec1bd8171d1cc99824cc3608a86f1b694b22c14e1065f`  
		Last Modified: Fri, 21 Jun 2024 02:06:18 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4b5a9d1b908d1652daf05b6071c11009f46c9b4ddd0021393992d21cd94845`  
		Last Modified: Fri, 21 Jun 2024 02:06:18 GMT  
		Size: 19.5 KB (19477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e40ba870cf6ddba89dc8a8ea7cf9d8eff1cfbe99425a129fb0b246828bf7e9`  
		Last Modified: Fri, 21 Jun 2024 02:06:18 GMT  
		Size: 8.9 KB (8878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ffa4843f5593cb53be63ff6b977b86a981494864fdb27dbb892aacb26e5739`  
		Last Modified: Wed, 03 Jul 2024 22:23:41 GMT  
		Size: 29.2 MB (29237277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2fc0294f9449beddf4a7bde369629996120b4a68c7c9cce36a18c605238c6ef`  
		Last Modified: Wed, 03 Jul 2024 22:23:40 GMT  
		Size: 3.9 MB (3855385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b05ac2c7c6a07568648a7793e79746c8ec528abaad5a47d04f951dddab5dea8`  
		Last Modified: Wed, 03 Jul 2024 22:23:40 GMT  
		Size: 59.7 KB (59697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396a515582a7e5319e190ca61dc1b44a47ee85b38b76843f496cd1218524e0b7`  
		Last Modified: Wed, 03 Jul 2024 22:23:40 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c22214e805e6b62b8dbb64f02ee460fd771af7f13cf69abd2afe92dc01b396`  
		Last Modified: Tue, 16 Jul 2024 22:58:23 GMT  
		Size: 24.5 MB (24460354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae5726776f3cd78341855fbe277efe77fe1b0623533b248560c18f00505d55b`  
		Last Modified: Tue, 16 Jul 2024 22:58:21 GMT  
		Size: 2.4 KB (2352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78fbc6927eeabbc3382a3d9243190222f06c54f895350a3238f8cb083b71c92`  
		Last Modified: Tue, 16 Jul 2024 22:58:22 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:c9c7bb9a1ec78433aae99919c580112da02a1b55ebeaf30415e6557be980fc61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1073631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dca2a10a75a122879722058b42d8b6dcd98218f7440ec548818e7618a63fc108`

```dockerfile
```

-	Layers:
	-	`sha256:fb6680df149d4fb04113e07fac84cb356bf5ebd08ba82ca3a4e8b01896dfa9b1`  
		Last Modified: Tue, 16 Jul 2024 22:58:21 GMT  
		Size: 1.0 MB (1026884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99861359ef0adc969d6d3b8f1de4f970ae49283e026afe4705dbfb789d5a8970`  
		Last Modified: Tue, 16 Jul 2024 22:58:21 GMT  
		Size: 46.7 KB (46747 bytes)  
		MIME: application/vnd.in-toto+json
