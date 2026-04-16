## `wordpress:6-fpm-alpine`

```console
$ docker pull wordpress@sha256:810b49e12ec0b072b4d9235d5699949cd5a273e69518c13ed11bafdc88697dac
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

### `wordpress:6-fpm-alpine` - linux; amd64

```console
$ docker pull wordpress@sha256:215144f586821d7655d5695b88b21bb6fc4443aa2072a599c27d464d58ea8f03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102765985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfea0abdbbdcdf2670f3b6863f56b3a58f08d6e765187f545758486e351e835b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:19:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:19:00 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:19:00 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:19:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:19:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:19:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:19:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:19:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:19:00 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 15 Apr 2026 20:19:00 GMT
ENV PHP_VERSION=8.3.30
# Wed, 15 Apr 2026 20:19:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Wed, 15 Apr 2026 20:19:00 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Wed, 15 Apr 2026 20:19:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:19:04 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:21:36 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:37 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 15 Apr 2026 20:21:37 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:21:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:21:38 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 20:21:38 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 15 Apr 2026 20:21:38 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:21:38 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 15 Apr 2026 20:21:38 GMT
CMD ["php-fpm"]
# Wed, 15 Apr 2026 21:19:23 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 15 Apr 2026 21:20:10 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 15 Apr 2026 21:20:11 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Wed, 15 Apr 2026 21:20:11 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 15 Apr 2026 21:20:12 GMT
RUN set -eux; 	version='6.9.4'; 	sha1='018542f4c3e15db0d8e38aaf0fcf1b5dc56dbb79'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 15 Apr 2026 21:20:12 GMT
VOLUME [/var/www/html]
# Wed, 15 Apr 2026 21:20:12 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 15 Apr 2026 21:20:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:20:13 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Wed, 15 Apr 2026 21:20:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:20:13 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d93a9d7176b338a20c469f6f0fa5e3d2b377eeee003d8c35b3e7e41ee9244b`  
		Last Modified: Wed, 15 Apr 2026 20:21:44 GMT  
		Size: 3.6 MB (3587445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c03d96be3df4a72326d745bddd56dd30d134b53b286e8fb3da7a4b95cdf2ec`  
		Last Modified: Wed, 15 Apr 2026 20:21:44 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d80a2f3a95c23359dc591ecf663cfeefd60cacd18bd9fb521968459d87e384`  
		Last Modified: Wed, 15 Apr 2026 20:21:44 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e094f665cd2138ea3f93f30d4f7333b1777b17f62fce6e9030dbc4de2e5181`  
		Last Modified: Wed, 15 Apr 2026 20:21:45 GMT  
		Size: 12.6 MB (12632562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12dade307f00cf42585ff55fc8f7c4ea135310998cda773fe5d50a2d143ac85`  
		Last Modified: Wed, 15 Apr 2026 20:21:45 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ac6e4456a3500a3474d4cb03e57705870c49670569b3539006ead2e400ef78`  
		Last Modified: Wed, 15 Apr 2026 20:21:46 GMT  
		Size: 13.4 MB (13371308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1cf03c449ef791d3dd35877a0240a63378d54ebd24ceac423d34c6341cea896`  
		Last Modified: Wed, 15 Apr 2026 20:21:46 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:265f286c149bbcf9ce87fcd1f9db26ea0bdeecc70b74d5ed102323785b832e9e`  
		Last Modified: Wed, 15 Apr 2026 20:21:46 GMT  
		Size: 23.4 KB (23402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c10a67ff35410659bc946556f1deb3b29cf61bb5546ffe709533e40ada92b6`  
		Last Modified: Wed, 15 Apr 2026 20:21:46 GMT  
		Size: 23.4 KB (23412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b2dd7809f857006c91e59a93ac81c89977dd008ef256ec8790338bf71e586f`  
		Last Modified: Wed, 15 Apr 2026 20:21:47 GMT  
		Size: 9.3 KB (9251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f8c8a0b957cc0d1551d457ed0b79f552760e4af0f4fb10777d9b3351fc7565`  
		Last Modified: Wed, 15 Apr 2026 21:20:25 GMT  
		Size: 32.8 MB (32839364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ffc622fe69fbcf0f8732b5829797320da5fd9d6fa2d687e3f6162b68e72713`  
		Last Modified: Wed, 15 Apr 2026 21:20:24 GMT  
		Size: 9.4 MB (9373856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd2e8d94d4cc6244935d4630f5b935d5612cf97640a9bfe87d047daa5a2677b`  
		Last Modified: Wed, 15 Apr 2026 21:20:24 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed70efccb7e30086e79ddac8026e0ef3b98c8c0064abab7e1dc78028fcb56365`  
		Last Modified: Wed, 15 Apr 2026 21:20:24 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c4ba44be1cf34f9ce6c68e794d2c874d208ccc87400fa6abb5a3433a49cf40`  
		Last Modified: Wed, 15 Apr 2026 21:20:26 GMT  
		Size: 27.0 MB (27031984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fedeacf771c6a507c809f6b71614e365b85d94727d52afafd48f23f9f8945027`  
		Last Modified: Wed, 15 Apr 2026 21:20:25 GMT  
		Size: 2.4 KB (2433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af0bcca37fe5acde44d3d537d0916750053b7dd7f05772b8c2c15f7486794b67`  
		Last Modified: Wed, 15 Apr 2026 21:20:26 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7934d1243dff33762d0a96f771c1dd0a442db32ce3d296cd8557d02d50a48e3c`  
		Last Modified: Wed, 15 Apr 2026 21:20:26 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:eff27786716b2b78f4d6947e693e66f15fd9db7d59bb1d85f05726f56ea37eef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1175576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5e81f31a47605d916bc67095e8064bc18efe02ba29d7969ff6d6cffb28bd6e`

```dockerfile
```

-	Layers:
	-	`sha256:82d179c3158e5cb3a7428840b08276fb89294cffbf8080b115d7746f09d90ac8`  
		Last Modified: Wed, 15 Apr 2026 21:20:24 GMT  
		Size: 1.1 MB (1122579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b75c9f776684f7accc23c0492566f79ec18eae90d1a8523021be08e31e275bd`  
		Last Modified: Wed, 15 Apr 2026 21:20:24 GMT  
		Size: 53.0 KB (52997 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-fpm-alpine` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:1548fc590343919f924f30f42218210f33c73185d5ef1f35c5b1b7aefd2e11eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.2 MB (95176219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3562d8299cbd17596a99c488974f506516008e9b055385717b45d34ab4deee73`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:22:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:22:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:22:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:22:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:22:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:22:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:22:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:22:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:22:49 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 15 Apr 2026 20:22:49 GMT
ENV PHP_VERSION=8.3.30
# Wed, 15 Apr 2026 20:22:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Wed, 15 Apr 2026 20:22:49 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Wed, 15 Apr 2026 20:22:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:22:53 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:25:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:25:34 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:25:36 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 15 Apr 2026 20:25:36 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:25:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:25:36 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 20:25:36 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 15 Apr 2026 20:25:36 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:25:36 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 15 Apr 2026 20:25:36 GMT
CMD ["php-fpm"]
# Wed, 15 Apr 2026 21:19:16 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 15 Apr 2026 21:20:25 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 15 Apr 2026 21:20:25 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Wed, 15 Apr 2026 21:20:25 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 15 Apr 2026 21:20:27 GMT
RUN set -eux; 	version='6.9.4'; 	sha1='018542f4c3e15db0d8e38aaf0fcf1b5dc56dbb79'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 15 Apr 2026 21:20:27 GMT
VOLUME [/var/www/html]
# Wed, 15 Apr 2026 21:20:27 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 15 Apr 2026 21:20:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:20:27 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Wed, 15 Apr 2026 21:20:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:20:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacf06c3f6eb1e545915a818177412e7f205ceda11a0d937da6e335e77e42b36`  
		Last Modified: Wed, 15 Apr 2026 20:25:42 GMT  
		Size: 3.5 MB (3543069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe21005c3f37b43e108acd2c035565c1e30c16cc783f258c2b6d0ad7d30a9fb3`  
		Last Modified: Wed, 15 Apr 2026 20:25:42 GMT  
		Size: 928.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752daeb76b3aa09bdab60762e9fc29224e27a3745231d971af6c33d8f06417f1`  
		Last Modified: Wed, 15 Apr 2026 20:25:42 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443a3430ac334ee79e452ef7b1189be12347e5f15c633432e2a82082cbc5d13f`  
		Last Modified: Wed, 15 Apr 2026 20:25:42 GMT  
		Size: 12.6 MB (12632565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d17ab241e03b56ec0c5eaecd00bf0e00cf7421e6121d47db115dedd13ea7a6`  
		Last Modified: Wed, 15 Apr 2026 20:25:43 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a0cec3e3ef23a4ddcd7b570f1cc2720d4297de8455a463df5afb222e6ae45b`  
		Last Modified: Wed, 15 Apr 2026 20:25:44 GMT  
		Size: 12.1 MB (12098858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:752f3cf692f43cbc1b568c6f0fd6f9a7a952c3260806e9ac8a8922a79f082f4e`  
		Last Modified: Wed, 15 Apr 2026 20:25:44 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:535a8050479928c09f0c4fc005ca20d3f8751545582fcad4ebc282d690032427`  
		Last Modified: Wed, 15 Apr 2026 20:25:44 GMT  
		Size: 23.2 KB (23208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0896113dc7b1eb8fd820084a781ccd8937c71b741fb525a4cb7b845036746f39`  
		Last Modified: Wed, 15 Apr 2026 20:25:44 GMT  
		Size: 23.2 KB (23222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a1048bda68a5b0ffb172bd57b8268824ef7cf3009612d7d58718c1598c11f3`  
		Last Modified: Wed, 15 Apr 2026 20:25:45 GMT  
		Size: 9.2 KB (9247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4896848b80d4f3d0fa2512fc866cf7285fd84935ac53c3cdf524c78c0bc73320`  
		Last Modified: Wed, 15 Apr 2026 21:20:35 GMT  
		Size: 28.6 MB (28550482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:216e8a43272db7667ce7a39f8417c41d7f0fb7e2c7921a6ad45098f043f93781`  
		Last Modified: Wed, 15 Apr 2026 21:20:34 GMT  
		Size: 7.7 MB (7682482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466815ba678dfe98fd3168ba31b0128df9399a3073a8437aad81872b6442aea7`  
		Last Modified: Wed, 15 Apr 2026 21:20:34 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47294cd599073a3ee55a6150d4fe7ae4a94a90b07b48e0aa98dea4d2d95006d2`  
		Last Modified: Wed, 15 Apr 2026 21:20:34 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a36ed3368e893297a446aba6edfe50d78a8a4d2fe436fe331b07848092760b9a`  
		Last Modified: Wed, 15 Apr 2026 21:20:36 GMT  
		Size: 27.0 MB (27032015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17da1d5dd82854781d29a56a183bbf5f994710a1826c9a48190456660bcafec6`  
		Last Modified: Wed, 15 Apr 2026 21:20:35 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d57a0644607cacf11c769c7439427e872180e30a987966d5604cb5bb67b3e4b`  
		Last Modified: Wed, 15 Apr 2026 21:20:36 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd519373710aba5a44432ff8b7642780e6a2f3f10c9e602af2ae41111d8ca128`  
		Last Modified: Wed, 15 Apr 2026 21:20:36 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:f5491d8719590dee3052071d8f6cca46e51165f6cf31c71807d2047d119d08a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 KB (52959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d969dd5c2a8c9b2da2fc4e2a10f022af75f063ad0897e77e87cbf5903773dc3`

```dockerfile
```

-	Layers:
	-	`sha256:7e82425aa97fcf80805ce8f344200e60446eec16febbf86a2aab3804cf7262a2`  
		Last Modified: Wed, 15 Apr 2026 21:20:33 GMT  
		Size: 53.0 KB (52959 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-fpm-alpine` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:679322b55ad716b394b6e37e2bec9f8410751ac585a001757da79e49d1691960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.4 MB (93350725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d9bb4a173cf0e4c57d5a8bacb8c378b4a2f0ace0a9086495b6c63956cc8b8f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:22:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:22:45 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:22:45 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:22:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:22:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:22:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:22:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:22:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:22:45 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 15 Apr 2026 20:22:45 GMT
ENV PHP_VERSION=8.3.30
# Wed, 15 Apr 2026 20:22:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Wed, 15 Apr 2026 20:22:45 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Wed, 15 Apr 2026 20:22:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:22:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:25:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:25:36 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:25:37 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 15 Apr 2026 20:25:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:25:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:25:38 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 20:25:38 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 15 Apr 2026 20:25:38 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:25:38 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 15 Apr 2026 20:25:38 GMT
CMD ["php-fpm"]
# Wed, 15 Apr 2026 21:28:03 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 15 Apr 2026 21:29:12 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 15 Apr 2026 21:29:12 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Wed, 15 Apr 2026 21:29:12 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 15 Apr 2026 21:29:14 GMT
RUN set -eux; 	version='6.9.4'; 	sha1='018542f4c3e15db0d8e38aaf0fcf1b5dc56dbb79'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 15 Apr 2026 21:29:14 GMT
VOLUME [/var/www/html]
# Wed, 15 Apr 2026 21:29:14 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 15 Apr 2026 21:29:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:29:14 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Wed, 15 Apr 2026 21:29:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:29:14 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff111b433c9694192115eb5216d3617b860a0b85c339a15fc5d2321e74ce02a`  
		Last Modified: Wed, 15 Apr 2026 20:25:44 GMT  
		Size: 3.3 MB (3343342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d91a5d31fd71f882a991a643e5be4dafc13975058b291344fea553808f43934`  
		Last Modified: Wed, 15 Apr 2026 20:25:44 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccd8babc39733495d5507af135d29d9baccf1802474c90127e30bd42eeb53ae1`  
		Last Modified: Wed, 15 Apr 2026 20:25:44 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea5ff3a45f40fcb58246fed8c2fb8578bd1a288506e19dea4a1c674aa222905`  
		Last Modified: Wed, 15 Apr 2026 20:25:44 GMT  
		Size: 12.6 MB (12632573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab40f3b11f106a3c9f9f2e12c8d9cddd022328d4b3882ca9403f3551077b4a1`  
		Last Modified: Wed, 15 Apr 2026 20:25:45 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5c8650af8727fa8bbc0ec352af4a92add8ae16a0ad5678dbf7074459cc9ca6`  
		Last Modified: Wed, 15 Apr 2026 20:25:45 GMT  
		Size: 11.4 MB (11399475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4972584d3665ef2cb976059056d9e5660d2c029fc7d877219ed3b6621d1acad`  
		Last Modified: Wed, 15 Apr 2026 20:25:45 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b81e6318ba30a1553a9befb47f69067b1a4a8ce45d975d03cff8622226e6cc57`  
		Last Modified: Wed, 15 Apr 2026 20:25:46 GMT  
		Size: 23.2 KB (23216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50aa8e4c765b6787bfdb0aa5d586ee20468be9ffedc56bce948b170023e7cd1b`  
		Last Modified: Wed, 15 Apr 2026 20:25:46 GMT  
		Size: 23.2 KB (23237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80074198273294c391b38133ec9055b9f5fdb79ddbdc0ca110918256b4bcaaea`  
		Last Modified: Wed, 15 Apr 2026 20:25:46 GMT  
		Size: 9.2 KB (9250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb1cfc17e813e0cc4f5a01e36f2bd543b96844281fbb6af98dcbe10d037317b3`  
		Last Modified: Wed, 15 Apr 2026 21:29:24 GMT  
		Size: 26.9 MB (26900929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af57daa59e32c3b8ec4476f1577438bed5a5b47584e17ea5d11a52765937a8f4`  
		Last Modified: Wed, 15 Apr 2026 21:29:23 GMT  
		Size: 8.7 MB (8694344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec3dd97ee3e27d0216c8d9c5d84a3f61d7ef6f8a6ed7845c03d286a8bf39de8f`  
		Last Modified: Wed, 15 Apr 2026 21:29:23 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1dcc63c0df08083bb8b5ec06d91a081c49281ac75dceece96a85c1f17358f7`  
		Last Modified: Wed, 15 Apr 2026 21:29:23 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a39e7688e5bc526a5940c1b0b916258e5e6d47dfaf28af1e7ead874bb5a032a`  
		Last Modified: Wed, 15 Apr 2026 21:29:25 GMT  
		Size: 27.0 MB (27032019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040fe65b4d788e589be562cfb1b174cf6846cf4473819383896f71f0ff3cc5da`  
		Last Modified: Wed, 15 Apr 2026 21:29:24 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61af44da098dd4b54d87e5009dceafe5fbc2edb417c875d14cd127edcde24566`  
		Last Modified: Wed, 15 Apr 2026 21:29:25 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340b2208a509082b9a1fea6071d2aa78564c5ae1b120a305274a08fbc578a6a5`  
		Last Modified: Wed, 15 Apr 2026 21:29:25 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:4ddc10eecef1e1ffdc50789d4e8599d058fe57611d9162fef7b62da33211db14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1173927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bc1e01313e1cee4d598ca627de02a322b757367940466ac44f56a142def073f`

```dockerfile
```

-	Layers:
	-	`sha256:fbf8aa4053df251e4dc16dccec626b50613108ad1cd6090ec124215ff38a7154`  
		Last Modified: Wed, 15 Apr 2026 21:29:23 GMT  
		Size: 1.1 MB (1120753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2b833f0d19c70fecf9ba2f3e33e6eb0d47c992100dc56d77f9aedff21ab01790`  
		Last Modified: Wed, 15 Apr 2026 21:29:23 GMT  
		Size: 53.2 KB (53174 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:0cfa0fa2d1eaa90b3c2f9846887a62020b61cf31660105c1411159fee3e16ee1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.4 MB (102353280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b89bace93640bd499b84e257aaa9ef21e4d945bf8141b2b6c1461f69fd7b263e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:17:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:17:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:17:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:17:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:17:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:17:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:17:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:17:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 15 Apr 2026 20:17:09 GMT
ENV PHP_VERSION=8.3.30
# Wed, 15 Apr 2026 20:17:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Wed, 15 Apr 2026 20:17:09 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Wed, 15 Apr 2026 20:17:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:17:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:21:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:39 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 15 Apr 2026 20:21:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:21:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:21:40 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 20:21:40 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 15 Apr 2026 20:21:40 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:21:40 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 15 Apr 2026 20:21:40 GMT
CMD ["php-fpm"]
# Wed, 15 Apr 2026 21:35:53 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 15 Apr 2026 21:36:50 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 15 Apr 2026 21:36:50 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Wed, 15 Apr 2026 21:36:50 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 15 Apr 2026 21:36:52 GMT
RUN set -eux; 	version='6.9.4'; 	sha1='018542f4c3e15db0d8e38aaf0fcf1b5dc56dbb79'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 15 Apr 2026 21:36:52 GMT
VOLUME [/var/www/html]
# Wed, 15 Apr 2026 21:36:52 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 15 Apr 2026 21:36:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:36:52 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Wed, 15 Apr 2026 21:36:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:36:52 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f087e2713a9916b20b8838a7655f1cdf3cdebb4e28b94456d05f716a45ced1da`  
		Last Modified: Wed, 15 Apr 2026 20:21:47 GMT  
		Size: 3.6 MB (3596149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7222f28085b850c7507a00c688f290dbf8410b92b32ce5fcd0af1f7ca6c7d0b1`  
		Last Modified: Wed, 15 Apr 2026 20:21:47 GMT  
		Size: 929.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d5fdf753459617bad921f3f3513304fbb60de9290ff35e13c2c282c4a69410d`  
		Last Modified: Wed, 15 Apr 2026 20:21:47 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67c54993f97c039e21a49021345ccbee34608c85b59674afa15987843eb9910`  
		Last Modified: Wed, 15 Apr 2026 20:21:47 GMT  
		Size: 12.6 MB (12632556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42da022847f8f41319a51a34bd056c96729e3229f4f6c6d981508fd4d21df0d0`  
		Last Modified: Wed, 15 Apr 2026 20:21:48 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb25c3c7f8d2477479cedfda983112623bdc7b007e87925eb703098fac15653c`  
		Last Modified: Wed, 15 Apr 2026 20:21:48 GMT  
		Size: 13.3 MB (13262525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085fde6ab5c88eee108fa68ee0653b25dbc3bb89d44d0025fd078fd5c207a224`  
		Last Modified: Wed, 15 Apr 2026 20:21:48 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce041495507e681ef5c16481181b06e7626f1f6c948d2eb1b891df61a3082cd1`  
		Last Modified: Wed, 15 Apr 2026 20:21:49 GMT  
		Size: 23.2 KB (23214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240fb24b9d93cd5d1382f3fe92bdd3905c814f153619ec752fc5a859e9ea7a3c`  
		Last Modified: Wed, 15 Apr 2026 20:21:49 GMT  
		Size: 23.2 KB (23232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b36262d145da712344cf2145c66295d2cd6bfe53cfd781cd11b869ea71b965`  
		Last Modified: Wed, 15 Apr 2026 20:21:49 GMT  
		Size: 9.2 KB (9249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051ebe2c35582c9599016e45d8bdc934078ce3e498e375f3e6b03207b891d7d0`  
		Last Modified: Wed, 15 Apr 2026 21:37:17 GMT  
		Size: 32.5 MB (32480066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b67ab4bca00501c1309c0fb9df2eca81a4a494e59fc4be07989b1f7993bbff7`  
		Last Modified: Wed, 15 Apr 2026 21:37:14 GMT  
		Size: 9.1 MB (9085196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78239aa722be5077f4e17483b78c56ba93ee8a59cfa0c4f6aadde3319e4c3e43`  
		Last Modified: Wed, 15 Apr 2026 21:37:05 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8340a3f97dcd774baef8f0281d94db3e2b36c0d148741b40d6e8491ce64295`  
		Last Modified: Wed, 15 Apr 2026 21:37:05 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8f36f67db46ee91453c377641e6d395c23fd3f3288aefc4bd5d9489e9b84bf`  
		Last Modified: Wed, 15 Apr 2026 21:37:17 GMT  
		Size: 27.0 MB (27032018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21a41571969c8a6cfc8deeb2d23b2c38a12ff564209dce41db8437d11405abf`  
		Last Modified: Wed, 15 Apr 2026 21:37:12 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd56e4cb3496b96b39a43cbf2d724c2fe2e0d540be86c7195096f346af114d06`  
		Last Modified: Wed, 15 Apr 2026 21:37:14 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4afe6f1566fb5d8080c9df2f9b70f489945a7756cefe6662ceabe9957ffacac0`  
		Last Modified: Wed, 15 Apr 2026 21:37:16 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:f35b2742094a84d4303ae0e7c6ea0c9e074ea15cea659dd25cf411a4c832cbba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1174013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b80a882d634130420c8857d449b3a1ed82d3256ba1d6955068a2900e999b21`

```dockerfile
```

-	Layers:
	-	`sha256:614496e9bbae7015bff6ac6b009595e3e0e9c6834e489b3c5db4f9e3a4bc1325`  
		Last Modified: Wed, 15 Apr 2026 21:37:04 GMT  
		Size: 1.1 MB (1120789 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d82f71463779b6d1386ac083218023083817d7d854bc71c21f0b5fab0acdc36b`  
		Last Modified: Wed, 15 Apr 2026 21:37:04 GMT  
		Size: 53.2 KB (53224 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-fpm-alpine` - linux; 386

```console
$ docker pull wordpress@sha256:423bae23041cd0d388aad2d27e34d8659d8daf09642953e11f35ca7d6ffa521f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.2 MB (102247358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33511503ebc40fea10faa11014ef80ed5ee726bf82df101298434992147b209d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Fri, 30 Jan 2026 01:19:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 30 Jan 2026 01:19:07 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 30 Jan 2026 01:19:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 30 Jan 2026 01:19:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 30 Jan 2026 01:19:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 30 Jan 2026 01:19:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 30 Jan 2026 01:19:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 30 Jan 2026 01:19:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 30 Jan 2026 01:19:07 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 30 Jan 2026 01:19:07 GMT
ENV PHP_VERSION=8.3.30
# Fri, 30 Jan 2026 01:19:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Fri, 30 Jan 2026 01:19:07 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Fri, 30 Jan 2026 01:23:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 30 Jan 2026 01:23:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 30 Jan 2026 01:26:21 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 30 Jan 2026 01:26:21 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 30 Jan 2026 01:26:21 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 30 Jan 2026 01:26:22 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 30 Jan 2026 01:26:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Jan 2026 01:26:22 GMT
WORKDIR /var/www/html
# Fri, 30 Jan 2026 01:26:22 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 30 Jan 2026 01:26:22 GMT
STOPSIGNAL SIGQUIT
# Fri, 30 Jan 2026 01:26:22 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 30 Jan 2026 01:26:22 GMT
CMD ["php-fpm"]
# Wed, 11 Mar 2026 20:37:53 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 11 Mar 2026 20:38:45 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 11 Mar 2026 20:38:45 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Wed, 11 Mar 2026 20:38:46 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 11 Mar 2026 20:38:47 GMT
RUN set -eux; 	version='6.9.4'; 	sha1='018542f4c3e15db0d8e38aaf0fcf1b5dc56dbb79'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 11 Mar 2026 20:38:47 GMT
VOLUME [/var/www/html]
# Wed, 11 Mar 2026 20:38:47 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 11 Mar 2026 20:38:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 11 Mar 2026 20:38:48 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Wed, 11 Mar 2026 20:38:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2026 20:38:48 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2937fa672ad33a0e99a83e5ed108c8cb1ba4208c3af3d80d9ca95c5366de636c`  
		Last Modified: Fri, 30 Jan 2026 01:22:50 GMT  
		Size: 3.6 MB (3629393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544c44246f2a933b8be60151492b88da5a99d2d30f2f22180c69991ec8a59284`  
		Last Modified: Fri, 30 Jan 2026 01:22:50 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32dba4931e0952d271ff7d2af4d794bb70466ead84a218ca3618953b8619314`  
		Last Modified: Fri, 30 Jan 2026 01:22:10 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b9be542d2081782578c54ceba92ac4c6335f1241b047ed944b6b13ec54d9fa`  
		Last Modified: Fri, 30 Jan 2026 01:26:30 GMT  
		Size: 12.6 MB (12632634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ebea7bf763ebc16c8b83324438e9563ce711d0e993ba4d48eafab41c0dabec`  
		Last Modified: Fri, 30 Jan 2026 01:26:29 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03e3ade1f446b49c654c1ae63d9b17547ef52e4fbebdc65c6cfde17ce91f81ee`  
		Last Modified: Fri, 30 Jan 2026 01:26:30 GMT  
		Size: 13.6 MB (13625366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bde399b513380837f8c3635e31b44397194f4240f750b46d6948e87ac9bad4`  
		Last Modified: Fri, 30 Jan 2026 01:26:29 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f3d6a47ad5f8db91dc55e686bafc509f4ae7e7dc6199a65e5794a6444e26aa`  
		Last Modified: Fri, 30 Jan 2026 01:26:30 GMT  
		Size: 23.5 KB (23513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfba059c14b518794c21795ec480d6478025e9138dab05c793b79ae20b6c8a92`  
		Last Modified: Fri, 30 Jan 2026 01:26:31 GMT  
		Size: 23.5 KB (23537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9cfa6c81ecf7e2804884e8910e985cd1e1ca68c49ae2b849650ac0333646f98`  
		Last Modified: Fri, 30 Jan 2026 01:26:31 GMT  
		Size: 9.2 KB (9249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93c534a0524e0926a0eda5daa1fa1e1594f43b1bd8a668d1a8c732b0cd47c70`  
		Last Modified: Wed, 11 Mar 2026 20:38:59 GMT  
		Size: 33.3 MB (33301562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f837f5efe8962f593ea8de7a6a35ed82a536c244e749e7e79ea785d918c32a23`  
		Last Modified: Wed, 11 Mar 2026 20:38:58 GMT  
		Size: 8.3 MB (8273858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898667ff8e80b0585e92dd6e5b6140e422b836e80b33ac900715e74327065834`  
		Last Modified: Wed, 11 Mar 2026 20:38:58 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f9fca02834c8340508a760fe0cf60b0c3cea9532f6bf072cfa259ba1f5f7b1c`  
		Last Modified: Wed, 11 Mar 2026 20:38:58 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd493674d38a86589ffb07539727f3cf495d88e175d990de38cfda4f20acbacd`  
		Last Modified: Wed, 11 Mar 2026 20:39:00 GMT  
		Size: 27.0 MB (27032026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c0675917a2c296566856882280ad8d64876977b635c0381dc56e67c1770420a`  
		Last Modified: Wed, 11 Mar 2026 20:38:59 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6adf369ee0b7169d406bf51f9ff353551fc1ff074a0fd56dc01c3cec7ad34dc1`  
		Last Modified: Wed, 11 Mar 2026 20:38:59 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146850ea74496bb26dd98447e65ea782a10f3e037756e18f68c505a0acb7ffd0`  
		Last Modified: Wed, 11 Mar 2026 20:39:00 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:131223d32a7d28888ac3840cd0d01f6b4e1158978f9078933f8ef7c2a5bbf662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1177423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d1f1d64d87e13e46df6c8a67ca833def7cfc099b9b5ebd02d1d15c549e9d9f8`

```dockerfile
```

-	Layers:
	-	`sha256:6c39711d593c0c18c00777e644cd30326b42fea66499704b71942a65ea73ad21`  
		Last Modified: Wed, 11 Mar 2026 20:38:58 GMT  
		Size: 1.1 MB (1124489 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85099bbb67b2d25bd8187771a6ad77901230bb9f2a23d709c75507e1178a9640`  
		Last Modified: Wed, 11 Mar 2026 20:38:57 GMT  
		Size: 52.9 KB (52934 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-fpm-alpine` - linux; ppc64le

```console
$ docker pull wordpress@sha256:9ddaae9fc6f5d55a721f0c87048eba83a144ecfcd0887be6f2140906342c127d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104295455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d99c7af89ac0612ed1b9fd1bc862c92f209dee4030b836a5587241cf0f18168`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:38:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 28 Jan 2026 02:38:57 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 28 Jan 2026 02:38:57 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 28 Jan 2026 02:38:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 28 Jan 2026 02:38:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 28 Jan 2026 02:38:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:38:57 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:38:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 28 Jan 2026 02:38:57 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 28 Jan 2026 02:38:57 GMT
ENV PHP_VERSION=8.3.30
# Wed, 28 Jan 2026 02:38:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Wed, 28 Jan 2026 02:38:57 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Wed, 28 Jan 2026 03:08:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 28 Jan 2026 03:08:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:11:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 28 Jan 2026 03:11:59 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 28 Jan 2026 03:12:01 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 28 Jan 2026 03:12:03 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 28 Jan 2026 03:12:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 28 Jan 2026 03:12:03 GMT
WORKDIR /var/www/html
# Fri, 30 Jan 2026 02:17:45 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 30 Jan 2026 02:17:45 GMT
STOPSIGNAL SIGQUIT
# Fri, 30 Jan 2026 02:17:45 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 30 Jan 2026 02:17:45 GMT
CMD ["php-fpm"]
# Thu, 05 Mar 2026 22:03:40 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Thu, 05 Mar 2026 22:05:21 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 05 Mar 2026 22:05:23 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Thu, 05 Mar 2026 22:05:23 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 11 Mar 2026 20:37:42 GMT
RUN set -eux; 	version='6.9.4'; 	sha1='018542f4c3e15db0d8e38aaf0fcf1b5dc56dbb79'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 11 Mar 2026 20:37:43 GMT
VOLUME [/var/www/html]
# Wed, 11 Mar 2026 20:37:43 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 11 Mar 2026 20:37:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 11 Mar 2026 20:37:44 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Wed, 11 Mar 2026 20:37:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2026 20:37:44 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7dd774a9daa9cc5f74d16d61155e614ceedece1fd19c05044ba6ace37dd4c6`  
		Last Modified: Wed, 28 Jan 2026 02:43:14 GMT  
		Size: 3.8 MB (3768852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59a002cadcf53d322e552c6a02f973915d8017427dfda71de122592386df6743`  
		Last Modified: Wed, 28 Jan 2026 02:43:14 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210b05b21b742c21780f39ad80c5babf4b1d13a4f41a2726c561bfb0fcc954e0`  
		Last Modified: Wed, 28 Jan 2026 02:43:14 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e03da60cfd062e9d2407439f9f381cf1c6d89cca0e136aeadf49145ea41c5b`  
		Last Modified: Wed, 28 Jan 2026 03:11:16 GMT  
		Size: 12.6 MB (12632661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16fda7b707b3d7ab8d64e7437640ea493ae868b9f36cc987d07851c8ad9433f8`  
		Last Modified: Wed, 28 Jan 2026 03:11:15 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a4c564dfa02aae4e4f3ba0ebcfe4e29cd57f9657ce67718bbbd6ce4b40d495`  
		Last Modified: Wed, 28 Jan 2026 03:12:21 GMT  
		Size: 13.9 MB (13932975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9230d7e674e8394708f8764fd0b66bba15aa33e2272dc53280af0afdbfc29e3c`  
		Last Modified: Wed, 28 Jan 2026 03:12:21 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6096db7953945b8f862eecaefffb45215192bae27d4183852a99ccd1e865ac0`  
		Last Modified: Wed, 28 Jan 2026 03:12:21 GMT  
		Size: 23.3 KB (23341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:192c784d907527db6b1cf64575617c97220dbe278b92cb695dfa8feeca8279f4`  
		Last Modified: Wed, 28 Jan 2026 03:12:21 GMT  
		Size: 23.4 KB (23362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650b43c66d2ed301e0ae4eececba02150c9798c35a31878a4b703a22f0722337`  
		Last Modified: Fri, 30 Jan 2026 02:17:55 GMT  
		Size: 9.3 KB (9262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c8d8cdb742cce730b44860b076437b06cf1c3b2a17e9372a48243757b14775`  
		Last Modified: Thu, 05 Mar 2026 22:05:59 GMT  
		Size: 34.1 MB (34069325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:287c39ce95e5daace341232b829f68488028a792983a551180cbfbcd893ea76e`  
		Last Modified: Thu, 05 Mar 2026 22:05:58 GMT  
		Size: 9.0 MB (8964730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12404df2feaa933f3d5e8808a0c42251c21169d80a98975ab235e245082e9d6`  
		Last Modified: Thu, 05 Mar 2026 22:05:58 GMT  
		Size: 318.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db128bd7dfe1bfa8528246a1ed61cdb5c5002a09bf70c90a6a0afe81e936590`  
		Last Modified: Thu, 05 Mar 2026 22:05:58 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:083189140c11d1450531dfb3a9b6781de7f72b71f1d2970a26219f60d83715f3`  
		Last Modified: Wed, 11 Mar 2026 20:38:06 GMT  
		Size: 27.0 MB (27032054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e881aa0f84e351bdfb9b332ae0b8e20897eb5300b5028ce6a3969e55e6024a23`  
		Last Modified: Wed, 11 Mar 2026 20:38:06 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58dc1d0c811076bbca8215aae639e4539cb10405a524de765f27b245e5d512f9`  
		Last Modified: Wed, 11 Mar 2026 20:38:06 GMT  
		Size: 1.8 KB (1771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e7052ff2ab339ca5db6ad181c8b56027a2dc320fdbf505b1f96d57aed222dc5`  
		Last Modified: Wed, 11 Mar 2026 20:38:06 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:bc058e483f80d35fbf49bb4ec0876d68e251db4e144e89b61f855be6c718ca16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1175772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4060ef378cbce86ef2a4d8b6d91c8bd3dd048fa30f911edb7da864f1b8d31f`

```dockerfile
```

-	Layers:
	-	`sha256:06782317455a33b17f469ff51945649f8fbdfa46766435524232577f495b6674`  
		Last Modified: Wed, 11 Mar 2026 20:38:05 GMT  
		Size: 1.1 MB (1122697 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a48e80d5f04da7c3c7a5c388817b4402e3521703addd9a08fc6e474a59159d87`  
		Last Modified: Wed, 11 Mar 2026 20:38:05 GMT  
		Size: 53.1 KB (53075 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-fpm-alpine` - linux; riscv64

```console
$ docker pull wordpress@sha256:cd473654cd45231f28a92754d91813cad18b35b8e62d3ab06f165977eee67075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.5 MB (99522560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b92d88ffa3a760b5ab93885d3585e94ac2e10ef1cf318a647e9f9e52b53125c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 09:13:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 28 Jan 2026 09:13:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 28 Jan 2026 09:13:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 28 Jan 2026 09:13:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 28 Jan 2026 09:13:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 28 Jan 2026 09:13:07 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_VERSION=8.3.30
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Wed, 28 Jan 2026 23:24:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 28 Jan 2026 23:24:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 01:13:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 29 Jan 2026 01:13:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 29 Jan 2026 01:13:25 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 29 Jan 2026 01:13:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 29 Jan 2026 01:13:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 29 Jan 2026 01:13:30 GMT
WORKDIR /var/www/html
# Sat, 31 Jan 2026 22:21:20 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 31 Jan 2026 22:21:20 GMT
STOPSIGNAL SIGQUIT
# Sat, 31 Jan 2026 22:21:20 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 31 Jan 2026 22:21:20 GMT
CMD ["php-fpm"]
# Mon, 02 Feb 2026 17:04:22 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Mon, 02 Feb 2026 17:17:43 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 20 Feb 2026 22:33:59 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Fri, 20 Feb 2026 22:33:59 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 11 Mar 2026 22:09:54 GMT
RUN set -eux; 	version='6.9.4'; 	sha1='018542f4c3e15db0d8e38aaf0fcf1b5dc56dbb79'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 11 Mar 2026 22:09:54 GMT
VOLUME [/var/www/html]
# Wed, 11 Mar 2026 22:09:54 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 11 Mar 2026 22:09:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 11 Mar 2026 22:09:55 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Wed, 11 Mar 2026 22:09:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2026 22:09:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d64a68485fdb9ab2ec4159ac3e04e0bb79d9f1d037e580e928ca2b9604180f`  
		Last Modified: Wed, 28 Jan 2026 10:13:59 GMT  
		Size: 3.7 MB (3741000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b030c1b113432578231e8fe7c8a1bc913f2dc5dcba512e805fa9ab07768c9bd4`  
		Last Modified: Wed, 28 Jan 2026 10:13:58 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32a0e9bcb36b34307b4eada1f50c1cd4244d43d19ee57d962818dcb0ff0b110`  
		Last Modified: Wed, 28 Jan 2026 10:13:58 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead4ca3c629698e3534fd379700b8815a0848d2ead89181ff18fdb7ce2be80bd`  
		Last Modified: Thu, 29 Jan 2026 00:19:17 GMT  
		Size: 12.6 MB (12632651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da22c56868349bf186f5d414b0dd5f09aa3de8582d759e6dceea6179c5b02b70`  
		Last Modified: Thu, 29 Jan 2026 00:19:13 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d55b36c8b9d6cde6fa33439adab2832c4d3a19f499822669273415c1c62eae7`  
		Last Modified: Thu, 29 Jan 2026 01:14:29 GMT  
		Size: 12.8 MB (12775242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98517bd277b61647ba3599c000b7970669222c7c62dd64f96b3a4f721feb5894`  
		Last Modified: Thu, 29 Jan 2026 01:14:27 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148ba13c6bd97b74c8caa5d17ce65ea4fbe8b3ab4ab6d8b62348d4f016c2baed`  
		Last Modified: Thu, 29 Jan 2026 01:14:27 GMT  
		Size: 23.3 KB (23334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8537273a8eae8f6bb3d23a875a2f779aade4763c54bd1905a5f147dc9d32cbbb`  
		Last Modified: Thu, 29 Jan 2026 01:14:27 GMT  
		Size: 23.4 KB (23355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142e0c9d7c9839608d8698f63e2feaa2838eb35b5ba071119584cfaeef005003`  
		Last Modified: Sat, 31 Jan 2026 22:21:53 GMT  
		Size: 9.3 KB (9264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28f89713a2253fabab25cb3c6aafce5d6bb2d3e8e38bd25aa55d3e0f43605fed`  
		Last Modified: Mon, 02 Feb 2026 17:19:57 GMT  
		Size: 32.6 MB (32642216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:047c80817c3be86b509ca419668cbfe45c02118a17bbe5438ae02a2bbd6004ad`  
		Last Modified: Mon, 02 Feb 2026 17:19:49 GMT  
		Size: 7.0 MB (7048879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ef71569bc484fdfca09b8015737702539c4fee0cf54775a767f43afa940bc2`  
		Last Modified: Fri, 20 Feb 2026 22:36:30 GMT  
		Size: 321.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23f77a6f5e17f5004dccf4bfaaecbc673db8021871e5818ff7c492e0427a438`  
		Last Modified: Fri, 20 Feb 2026 22:36:30 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5d8de99030c02bc648dec39b16676b24ec3692a14b22c5154ba76cd02fc9a29`  
		Last Modified: Wed, 11 Mar 2026 22:11:43 GMT  
		Size: 27.0 MB (27032058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b142c5eca0cb474f5622e786f096d42bf29c12813ceecf76ae1d63499aa88d`  
		Last Modified: Wed, 11 Mar 2026 22:11:39 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cc45862f8a20d81f21f6156d4d8c44bf519175c866cbc9e39b2d8d9ca526f8`  
		Last Modified: Wed, 11 Mar 2026 22:11:39 GMT  
		Size: 1.8 KB (1774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a44d9ca848f9daa0e881766c3220d77fec081c9907b0e72c6ef26e0c65819cdb`  
		Last Modified: Wed, 11 Mar 2026 22:11:39 GMT  
		Size: 199.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:91a7c9fd008a00b317ed4c3001ab0d038ee92c3381d267e5e907c632a0c34171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1175768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbc8bafe0d56a3f56ca3ca1bcbb6e76c6275511c063edc9b8ef5f4ab4492f9ee`

```dockerfile
```

-	Layers:
	-	`sha256:5e56fa072060250354f7ce8bf1614748b95027264a6062096fbd8ca301ad4477`  
		Last Modified: Wed, 11 Mar 2026 22:11:39 GMT  
		Size: 1.1 MB (1122693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e5694141aed0287f3840abccb979328cc1405774c3b9953118f803a1c365d37`  
		Last Modified: Wed, 11 Mar 2026 22:11:38 GMT  
		Size: 53.1 KB (53075 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-fpm-alpine` - linux; s390x

```console
$ docker pull wordpress@sha256:f25050a9d83406b03620f288521ff2f066763b10c685e641d758e8e6b54057a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.2 MB (103196592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a1d0f932afd1d00bf40468a2dab327bf677b3d8b75cce48c8c88b8f4d7518e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:23:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 28 Jan 2026 02:23:22 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 28 Jan 2026 02:23:22 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 28 Jan 2026 02:23:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 28 Jan 2026 02:23:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 28 Jan 2026 02:23:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:23:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 02:23:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 28 Jan 2026 02:23:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 28 Jan 2026 02:23:22 GMT
ENV PHP_VERSION=8.3.30
# Wed, 28 Jan 2026 02:23:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.30.tar.xz.asc
# Wed, 28 Jan 2026 02:23:22 GMT
ENV PHP_SHA256=67f084d36852daab6809561a7c8023d130ca07fc6af8fb040684dd1414934d48
# Wed, 28 Jan 2026 02:37:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 28 Jan 2026 02:37:01 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 30 Jan 2026 01:50:19 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 30 Jan 2026 01:50:19 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 30 Jan 2026 01:50:19 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 30 Jan 2026 01:50:20 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 30 Jan 2026 01:50:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 30 Jan 2026 01:50:20 GMT
WORKDIR /var/www/html
# Fri, 30 Jan 2026 01:50:20 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 30 Jan 2026 01:50:20 GMT
STOPSIGNAL SIGQUIT
# Fri, 30 Jan 2026 01:50:20 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 30 Jan 2026 01:50:20 GMT
CMD ["php-fpm"]
# Tue, 10 Mar 2026 21:39:05 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 10 Mar 2026 21:40:11 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 10 Mar 2026 21:40:11 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 10 Mar 2026 21:40:11 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 11 Mar 2026 20:35:57 GMT
RUN set -eux; 	version='6.9.4'; 	sha1='018542f4c3e15db0d8e38aaf0fcf1b5dc56dbb79'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 11 Mar 2026 20:35:57 GMT
VOLUME [/var/www/html]
# Wed, 11 Mar 2026 20:35:57 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 11 Mar 2026 20:35:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 11 Mar 2026 20:35:57 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Wed, 11 Mar 2026 20:35:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Mar 2026 20:35:57 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ddec292ce8d22cd45e25f291194336fe15e71a195e9527615f1f4cb93f051a`  
		Last Modified: Wed, 28 Jan 2026 02:27:24 GMT  
		Size: 3.8 MB (3795094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c3a271895fa21f842dc6a628c9be8ba868f3ab56244b4dba69e5063768250e`  
		Last Modified: Wed, 28 Jan 2026 02:27:24 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efeb84f4380740d6c7657500d1fa1467fdcbd30beb8d1f4599234a969e915e28`  
		Last Modified: Wed, 28 Jan 2026 02:27:24 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:768b1ecc8d15562b1905e3a2ecd7fbbf3c53be7e8e6e4d26ccc00b258a7bb12d`  
		Last Modified: Wed, 28 Jan 2026 02:40:00 GMT  
		Size: 12.6 MB (12632645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7503d1a401dc4b3c82c28f7ef417ed28bb9c7d87ace1f289d974cc74dbf8c44d`  
		Last Modified: Wed, 28 Jan 2026 02:40:00 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2251a4b67e1ed3f5c649490cc91edbc8a87b63412c80ca4f58606e88ab50f0ae`  
		Last Modified: Fri, 30 Jan 2026 01:50:30 GMT  
		Size: 13.2 MB (13236437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7fba6ea098f4a79e09a007a87217902f8febeca5bfdb560eecb938aa00694e`  
		Last Modified: Fri, 30 Jan 2026 01:50:30 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f7796842c0feee4516b491c242b19f525c0a52b0603f94d0156bdd8418ff5c`  
		Last Modified: Fri, 30 Jan 2026 01:50:30 GMT  
		Size: 23.3 KB (23341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d49dd889eb7700bb609d389d4c2e756eae73f80b135cea49b98dc245786e851`  
		Last Modified: Fri, 30 Jan 2026 01:50:30 GMT  
		Size: 23.4 KB (23364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f677ad060e65ebd3945aacd35c253898b8bea8ad34690f37c832381f79b3692`  
		Last Modified: Fri, 30 Jan 2026 01:50:31 GMT  
		Size: 9.2 KB (9248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1009e32503aa72587402e005fd1e04b1838d82f63efc05484015fe9843e7e18`  
		Last Modified: Tue, 10 Mar 2026 21:40:30 GMT  
		Size: 34.0 MB (34005752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9702a704352c2320467d7f147e3f966231a27a1279579a9127db3f7458b6fedd`  
		Last Modified: Tue, 10 Mar 2026 21:40:30 GMT  
		Size: 8.7 MB (8704112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33e4fe1585da55dce06fe890a6d36e89a5b83ee46c1f662029402570a2f9983`  
		Last Modified: Tue, 10 Mar 2026 21:40:29 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1f12925d26e7e3a1da3d0ed5fc20da2c0718071528c608f3307465cb14cc5ff`  
		Last Modified: Tue, 10 Mar 2026 21:40:29 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a4ecd75d7c043476adb6047e0fc54fc12111d9268aa4a9895395e20b16d8fc`  
		Last Modified: Wed, 11 Mar 2026 20:36:11 GMT  
		Size: 27.0 MB (27032038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813369d76bf4604adbf6bd08dae660ab65b0de139df1ed6f6f7bd4ab3141dac9`  
		Last Modified: Wed, 11 Mar 2026 20:36:11 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae0024058b6b26b0174723bb5516e9994c014f45df0014e168e64eebd6747d0a`  
		Last Modified: Wed, 11 Mar 2026 20:36:11 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b04d3542a5d4aa381973225fabe0ef497ffbb192d1b38a82d82c9c04005c599`  
		Last Modified: Wed, 11 Mar 2026 20:36:11 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:8644abcb41f300daccf7762f65ba699546d0cfd0c89012abe97e3c0c4d687995
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1175636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0b9aa05d8419336a3e67d7b0e5e2953e2c19a5c663d12266c72d214a7626df`

```dockerfile
```

-	Layers:
	-	`sha256:77093a8a99208f87819ee94dc1f1e19c99dd658384d6c18d84ab463aaa601dbc`  
		Last Modified: Wed, 11 Mar 2026 20:36:11 GMT  
		Size: 1.1 MB (1122639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:665b8a61aaf244f2d3a6f96ef84e0af9ca05b4cf6b184c9d1367d3962d7133a8`  
		Last Modified: Wed, 11 Mar 2026 20:36:11 GMT  
		Size: 53.0 KB (52997 bytes)  
		MIME: application/vnd.in-toto+json
