## `wordpress:beta-6.9-beta1-php8.2-fpm-alpine`

```console
$ docker pull wordpress@sha256:e03368b43fae70bcf121ad1cbc5064c68727f8e2e159826bdfe2f5725d67f70e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
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

### `wordpress:beta-6.9-beta1-php8.2-fpm-alpine` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:6fed922ffdecf1ba9a7756919923f712036d9cc8e155cfbe9178867e34076128
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90135018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d55fdb815aa2d7c542907b5ef3d5b4709417c668861cca04bfc16688e0afc2de`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 31 Jul 2025 19:22:09 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["/bin/sh"]
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 31 Jul 2025 19:22:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 31 Jul 2025 19:22:09 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_VERSION=8.2.29
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 31 Jul 2025 19:22:09 GMT
WORKDIR /var/www/html
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
STOPSIGNAL SIGQUIT
# Thu, 31 Jul 2025 19:22:09 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["php-fpm"]
# Tue, 21 Oct 2025 19:03:12 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
RUN set -eux; 	version='6.9-beta1'; 	sha1='e46584af5e1021b8fde7f896794b2c7ff7ebd516'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
VOLUME [/var/www/html]
# Tue, 21 Oct 2025 19:03:12 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 19:03:12 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd3a02d3731bbe5de86691d53c14fc5098fe7da2c24769341668d80b3130671`  
		Last Modified: Wed, 08 Oct 2025 21:46:33 GMT  
		Size: 3.4 MB (3428326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62281be74ffe4f2725c7350e69b3fd5c9cbf7f195313174b10c5a13d6961d8c4`  
		Last Modified: Wed, 08 Oct 2025 21:46:18 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d4751de166e66aa98bb57666f93a0afc12ad11313c55df6a92bb4501adf5d0`  
		Last Modified: Wed, 08 Oct 2025 21:46:18 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a0bd195a823c854b1b251950e82fe3a70ac4d5cb3cedb326ec87740894209b`  
		Last Modified: Wed, 08 Oct 2025 21:56:10 GMT  
		Size: 12.2 MB (12183660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4be4b30cee64ffb796b818d86eaad361c2410a218a6ca98dd1228da9203a76`  
		Last Modified: Wed, 08 Oct 2025 21:56:09 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233a24649eba4d83ecff69e4e5e84a136aaa51a6657157cd9defa2c59c199abd`  
		Last Modified: Wed, 08 Oct 2025 21:56:09 GMT  
		Size: 11.8 MB (11762827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:883d5dc0bb74a45db09bb153da2d4f00ae9b0ee93786271e3470799916537182`  
		Last Modified: Wed, 08 Oct 2025 21:56:09 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d0af49c8f00e4d4759da3a10039f958b42da497232c6997dd1225873b0dd66`  
		Last Modified: Wed, 08 Oct 2025 21:56:09 GMT  
		Size: 19.9 KB (19862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0cde31999a8fc25f7d6a65b6434832d42724abb1bf85d240667d6f6c26ad2d`  
		Last Modified: Wed, 08 Oct 2025 21:56:09 GMT  
		Size: 19.9 KB (19856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a075c48dde190771d245e49c2d33d01ec4bf2a030785316c9343544cfffe5b`  
		Last Modified: Wed, 08 Oct 2025 21:56:09 GMT  
		Size: 9.2 KB (9172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14e0cd813a216e0f5629a8d75a4120ad70b6aa0c997e90157e30c5748ce1adbb`  
		Last Modified: Wed, 22 Oct 2025 00:02:24 GMT  
		Size: 24.4 MB (24377529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0885466b0ecd75e93508e88a3476500b60aafb13d62c5ed3ace462cbf16460`  
		Last Modified: Wed, 22 Oct 2025 00:02:25 GMT  
		Size: 7.7 MB (7653539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca1854fa47ce58833960e8e57baa7ad8faf253274353bb23fb5326355234f64`  
		Last Modified: Wed, 22 Oct 2025 00:02:22 GMT  
		Size: 62.5 KB (62484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133c74ac1c770cf64c3ea90bbf9ea3c80bc4a2762b721e9661cf5c0a6b984a52`  
		Last Modified: Wed, 22 Oct 2025 00:02:22 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dd9bdfec4d4ad15952381384d289b99d48b1302efcba6df3bd765362428898`  
		Last Modified: Wed, 22 Oct 2025 00:02:24 GMT  
		Size: 27.1 MB (27104770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f4da4d257e9cd3407708240d06015dd76f595ef25af3ccae2d6757baf326d0`  
		Last Modified: Wed, 22 Oct 2025 00:02:22 GMT  
		Size: 2.4 KB (2434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1ba2f5433795cfbc79c12413132a8e3499a34c74b34df3c5848cfc2794f49f`  
		Last Modified: Wed, 22 Oct 2025 00:02:22 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6828a93ec461f6772d5b8b4a465a5e422533348bc153b133559a91bb220932`  
		Last Modified: Wed, 22 Oct 2025 00:02:22 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-beta1-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:e69097da11cb191f09af37bdf3a6023e7e46bccb28ad9c1183a38b6eb4c56897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 KB (51706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:787b1bd577e06c580731844d3f75080160cb7461e2e9d886b11bf76f16a40454`

```dockerfile
```

-	Layers:
	-	`sha256:9905fd48814ad629447fb00b993010846875bd4c4e2fca7cc0a20ff007247731`  
		Last Modified: Wed, 22 Oct 2025 01:19:37 GMT  
		Size: 51.7 KB (51706 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.9-beta1-php8.2-fpm-alpine` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:7a0b770763483449c102ff88b5010815c3c04b73547eb7c89dcafb5c1c84ec23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.9 MB (88857276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d50c9221e8890a8d28920f6821e2ca638069fd5a00778a700899fe6081bff003`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 31 Jul 2025 19:22:09 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["/bin/sh"]
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 31 Jul 2025 19:22:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 31 Jul 2025 19:22:09 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_VERSION=8.2.29
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 31 Jul 2025 19:22:09 GMT
WORKDIR /var/www/html
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
STOPSIGNAL SIGQUIT
# Thu, 31 Jul 2025 19:22:09 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["php-fpm"]
# Tue, 21 Oct 2025 19:03:12 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
RUN set -eux; 	version='6.9-beta1'; 	sha1='e46584af5e1021b8fde7f896794b2c7ff7ebd516'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
VOLUME [/var/www/html]
# Tue, 21 Oct 2025 19:03:12 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 19:03:12 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01dff801184d313bb2a088e51c23a84fdcb550a5efbe243a6ebccc4811943d00`  
		Last Modified: Wed, 08 Oct 2025 21:54:13 GMT  
		Size: 3.2 MB (3244410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4efcd206adad42cec871a48a6bbe23175b815bd598e566ece47c6287fa37a22`  
		Last Modified: Wed, 08 Oct 2025 21:54:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0064a66bb0ad16511631b3384a35aff43f0a7476c972aff4044f9767b2922374`  
		Last Modified: Wed, 08 Oct 2025 21:54:13 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b0c80f7cc41f497273dd7fafb12b6568587e8d5e64764b7bba002bc12cb7af`  
		Last Modified: Wed, 08 Oct 2025 21:57:24 GMT  
		Size: 12.2 MB (12183651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80cea2f9fbc59ccf9912f80701d59b3f0115f9932abd1c14822bb3491a8121b`  
		Last Modified: Wed, 08 Oct 2025 21:57:22 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c7f89d0b518338195822fd4369abf2695ff514b36db0c45a864c3e8e8e07bff`  
		Last Modified: Wed, 08 Oct 2025 21:57:25 GMT  
		Size: 11.1 MB (11074078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9fb79a01c864dd229454e30c3e774b9ff0026f5f356c250ca75ddc37eb8710`  
		Last Modified: Wed, 08 Oct 2025 21:57:22 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d04c166cb935d1e64a95467ed02b1227242c8896e0b9bb54571835e646fea1e`  
		Last Modified: Wed, 08 Oct 2025 21:57:22 GMT  
		Size: 19.9 KB (19850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931bdd62990780ad4e62ed83db12114dd078e2659b55b2c9403663594ffde833`  
		Last Modified: Wed, 08 Oct 2025 21:57:23 GMT  
		Size: 19.9 KB (19850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4fdd8a6c959de7d243df135c36881e1d71ad90ad8d5b0ce94b54a47ddd719a4`  
		Last Modified: Wed, 08 Oct 2025 21:57:23 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7eeadda9283247ca6e09b8bab301e1914bc7fc6a43231268cb112ae55a1ebd`  
		Last Modified: Wed, 22 Oct 2025 00:02:16 GMT  
		Size: 23.2 MB (23152211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1258f6ea2104a145ff3902d007a67925679db983c9ebf963ffaae7adbc529e`  
		Last Modified: Wed, 22 Oct 2025 00:02:15 GMT  
		Size: 8.8 MB (8756373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe20baa66e9b3c8dfea7dafce85f3dbb003c09c958f90b41dc3819b2ba241d1b`  
		Last Modified: Wed, 22 Oct 2025 00:02:15 GMT  
		Size: 62.4 KB (62443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec6b467945f5a55f26aa9f0af8a2d3b276f644a4f46be1fbc15897ba22a45e46`  
		Last Modified: Wed, 22 Oct 2025 00:02:14 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbd82ae4f195f14063768df35d82389de6752694ed9c9f8bb95d89904360c99`  
		Last Modified: Wed, 22 Oct 2025 00:02:16 GMT  
		Size: 27.1 MB (27104771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84557ba7f868fceb9ab9c2fdbb2e8f8c5acec63caae496b61ae55baaa80ab5c3`  
		Last Modified: Wed, 22 Oct 2025 00:02:13 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48cb44fe1f8886783ba474a8dc18b4839c149061ee5a75f43c756db6f6cf7877`  
		Last Modified: Wed, 22 Oct 2025 00:02:13 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92943faccbe8861483de3d648f127ce36e39c50bfdd00c30a61640cf042663fa`  
		Last Modified: Wed, 22 Oct 2025 00:02:14 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-beta1-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:a4149677e7cdfba194488fe8253a087cb4d9625ea36d34e5c0bc4a638885f816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1132489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba0960dcf4d21559cb1cde1e0574bd2bc9f8fb1d4b2434b0e4097126f64521de`

```dockerfile
```

-	Layers:
	-	`sha256:ef25aaf6c5417ef66e5fdb60ef6d4c8e108a3e1a8644ad8786f19eeb8c741539`  
		Last Modified: Wed, 22 Oct 2025 01:19:40 GMT  
		Size: 1.1 MB (1080567 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bff3a7703daa8c34c8fa14c417ff804a6da7868387dde809f1c181c9975e150b`  
		Last Modified: Wed, 22 Oct 2025 01:19:41 GMT  
		Size: 51.9 KB (51922 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.9-beta1-php8.2-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:47f55806f3a041728c25bdfb47517ca70b3096b7ae4f5d8c7d9f0a9db56f5d10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97544155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80c1857128d214b084eea07a94bccc088eccaa816dd6f083c92001b15916baa8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 31 Jul 2025 19:22:09 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["/bin/sh"]
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 31 Jul 2025 19:22:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 31 Jul 2025 19:22:09 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_VERSION=8.2.29
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 31 Jul 2025 19:22:09 GMT
WORKDIR /var/www/html
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
STOPSIGNAL SIGQUIT
# Thu, 31 Jul 2025 19:22:09 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["php-fpm"]
# Tue, 21 Oct 2025 19:03:12 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
RUN set -eux; 	version='6.9-beta1'; 	sha1='e46584af5e1021b8fde7f896794b2c7ff7ebd516'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
VOLUME [/var/www/html]
# Tue, 21 Oct 2025 19:03:12 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 19:03:12 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ebec91d5e3bf4e32730e408e0d3d7d67b64b4f916d210a55ad102fa97e08a2`  
		Last Modified: Wed, 08 Oct 2025 21:33:09 GMT  
		Size: 3.5 MB (3466801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f52d1dbb7f7fbfc95e099c5650807b88916220f5a5cd4ba59cad5a0a6d2bc0c`  
		Last Modified: Wed, 08 Oct 2025 21:33:09 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8789e309aa9c45d4e867dc44d5e25723a71fc6b95f6fec153bdefdb22101a43`  
		Last Modified: Wed, 08 Oct 2025 21:33:09 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfea53bfd8cc990e62bfa419bfc527d49bf1d20d05cc50db2c7998ab07405def`  
		Last Modified: Wed, 08 Oct 2025 21:38:07 GMT  
		Size: 12.2 MB (12183654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffcaea5787ca81a6970e367a81f156a7950079d9f47bcad2f2a800f041f57d50`  
		Last Modified: Wed, 08 Oct 2025 21:38:06 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e068ddba6d2f141d070f97712910a9905b6db9a400472b88f2ccb724f1fd88`  
		Last Modified: Wed, 08 Oct 2025 21:38:07 GMT  
		Size: 13.0 MB (13023071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8b7c007f888d023c4adeb1dd117e2f88c1e08edc555994bbec3c8f5acbe39f`  
		Last Modified: Wed, 08 Oct 2025 21:38:06 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c061d22523a1c02a51c8f3b926f5fadefd98103ef986d63f03a66865c663fca1`  
		Last Modified: Wed, 08 Oct 2025 21:38:06 GMT  
		Size: 19.9 KB (19853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1741a90c64b83f1480ec8ec3b5340148fa421802240bad8131a5953eec667f6c`  
		Last Modified: Wed, 08 Oct 2025 21:38:06 GMT  
		Size: 19.9 KB (19855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec72bcc553c9579f3065903c433d45c327fb11ca01a4aaa5e379017a0cb2cfb7`  
		Last Modified: Wed, 08 Oct 2025 21:38:06 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d39ecd4c33bb8a6313e78a4431c0462f3accdb2b4ac2173d96266be5023e43`  
		Last Modified: Wed, 22 Oct 2025 00:02:57 GMT  
		Size: 28.1 MB (28108446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ffd26911cf8c85f2901232744ca80ae3e6fabec359f9aa94bab32243661870`  
		Last Modified: Wed, 22 Oct 2025 00:02:55 GMT  
		Size: 9.4 MB (9399074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac88cd4ef38354dc21df4417663b9cfade913fe5d049946a29ec0e5e0cb2b5f9`  
		Last Modified: Wed, 22 Oct 2025 00:02:54 GMT  
		Size: 62.5 KB (62473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b63890adff819e17c49af1842ea49eac40532c41b30782fb53ef69469d40a42`  
		Last Modified: Wed, 22 Oct 2025 00:02:54 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388e10376a5313dca769808e51cc62920dea9f8851974e9afb958e8c801564b9`  
		Last Modified: Wed, 22 Oct 2025 00:02:56 GMT  
		Size: 27.1 MB (27104771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffc861751479375db9350c83efae680498c6b12fc686303bffe642928242ccc5`  
		Last Modified: Wed, 22 Oct 2025 00:02:54 GMT  
		Size: 2.4 KB (2434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b99e3a894864bc3433a4fd1e6d3a5a9d52752fb3856ac3a10ea6db9a4b2dafa`  
		Last Modified: Wed, 22 Oct 2025 00:02:54 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08aa8ac75082247cbc725c63f3d7ac18dbca4a360a362fee42ae5681b70380d`  
		Last Modified: Wed, 22 Oct 2025 00:02:54 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-beta1-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:3c79fa07cfca91499f4b941e527a6ded2eda2fb37132d583239af3e4d96de511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1132541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a980e2ea7d5af22ee75a571b066034ada01babaff85c1cc96b47f56fc70c9cbf`

```dockerfile
```

-	Layers:
	-	`sha256:23ff7696cdddd7533f57d3c62c43ebf172c5b8a55a17a87bae03185a64abf2fc`  
		Last Modified: Wed, 22 Oct 2025 01:19:44 GMT  
		Size: 1.1 MB (1080587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:803617dbdd2566e005387a1515c71ca9c4b13c987c68489d7e63ba4a3e3b1b99`  
		Last Modified: Wed, 22 Oct 2025 01:19:45 GMT  
		Size: 52.0 KB (51954 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.9-beta1-php8.2-fpm-alpine` - linux; 386

```console
$ docker pull wordpress@sha256:7c090ee7f6019f95c60462bf339d14f032b32488220b6ec1fa15168f9512e219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.5 MB (96450601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:740f468e173bea0f1a2cb92491e49471d0ddd0bd57a9a26fbb7221204ef945d7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 31 Jul 2025 19:22:09 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["/bin/sh"]
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 31 Jul 2025 19:22:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 31 Jul 2025 19:22:09 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_VERSION=8.2.29
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 31 Jul 2025 19:22:09 GMT
WORKDIR /var/www/html
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
STOPSIGNAL SIGQUIT
# Thu, 31 Jul 2025 19:22:09 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["php-fpm"]
# Tue, 21 Oct 2025 19:03:12 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
RUN set -eux; 	version='6.9-beta1'; 	sha1='e46584af5e1021b8fde7f896794b2c7ff7ebd516'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
VOLUME [/var/www/html]
# Tue, 21 Oct 2025 19:03:12 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 19:03:12 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8447d37f1556e7cc88d30c48cc8e8cf0af5b255bbd92a7230769a8669ba2689f`  
		Last Modified: Wed, 08 Oct 2025 21:34:10 GMT  
		Size: 3.5 MB (3522948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86fa2ff0a6696a7e651f896a4eaa4cc8ad3e4f7b47aec66e66d2589a63bbfcec`  
		Last Modified: Wed, 08 Oct 2025 21:34:10 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f94b848f32599cfe36dcbaa1f0c61516eea4c75ddf52bd7833452fbdcb3dc2c3`  
		Last Modified: Wed, 08 Oct 2025 21:34:10 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6914e4f4a3ee59989098a4dd2bfbdce295bca748396f1ca4dec9f3f931aeeac`  
		Last Modified: Wed, 08 Oct 2025 21:34:11 GMT  
		Size: 12.2 MB (12183621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffdc3aa79c772d4f3858ff8edd943ed8e9d850ec30b2cba81fdaeb7359b35c41`  
		Last Modified: Wed, 08 Oct 2025 21:34:10 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09876d435169e28fd68e32be06fc38a8cc12a4ba7432b018e1d979f17506da9`  
		Last Modified: Wed, 08 Oct 2025 21:34:11 GMT  
		Size: 13.3 MB (13348073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1deb3cfe1ecfa249769f9d0783a7bf04e13cc703ad6f2fa5abf9232d98bdf47`  
		Last Modified: Wed, 08 Oct 2025 21:34:10 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a43d00af8db8b7d2326e27de1b6ff40ed4c2c3925b3639cb2e494f3ba9b1cab`  
		Last Modified: Wed, 08 Oct 2025 21:34:10 GMT  
		Size: 20.1 KB (20054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898bb831e36d441b97879236a3ca75f1922d3d5935cbe83fca6cc9ea4ad5b166`  
		Last Modified: Wed, 08 Oct 2025 21:34:10 GMT  
		Size: 20.0 KB (20046 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2025ccf037d0f9bfaba2281c83d64fc1b1f8d97eefa7215427146a1d77581a17`  
		Last Modified: Wed, 08 Oct 2025 21:34:10 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0c702a97008fd7d2410439397716424087a6a93350daf62d859be498a6e938`  
		Last Modified: Wed, 22 Oct 2025 00:00:49 GMT  
		Size: 28.5 MB (28495006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211f17a103699df12215767d1a4df25c407f6a35c2e96997c050d6d2c26206ad`  
		Last Modified: Wed, 22 Oct 2025 00:00:47 GMT  
		Size: 8.1 MB (8056627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87f5a68d8af2795d92d461d670d10426a4bb172a07d8b6544eef1e91c4fcf91`  
		Last Modified: Wed, 22 Oct 2025 00:00:46 GMT  
		Size: 62.4 KB (62439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf2c17a266692844e76fb036ba894036db54fe8d541a2d572967b65faea9b34`  
		Last Modified: Wed, 22 Oct 2025 00:00:46 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1985778a49577471403ee3137d574cc824fb462dfde1788fd18056af6c5accb1`  
		Last Modified: Wed, 22 Oct 2025 00:00:49 GMT  
		Size: 27.1 MB (27104773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23156ff0a65154bf0b21d487014f191f8bad5b7efdc6d6c987bc9eb87e633368`  
		Last Modified: Wed, 22 Oct 2025 00:00:46 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa89b0f456ac26e015f3ac5d925150ff8eeeaad8fe02f30dc39ff97fea02d193`  
		Last Modified: Wed, 22 Oct 2025 00:00:46 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d071be8eb3aa77c1138d5d68b6bc65b8329bcb7c6cdb7fc1ecae1d83d94da2`  
		Last Modified: Wed, 22 Oct 2025 00:00:46 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-beta1-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:f94008eda36e57bda3d930d5b7144e1784b92d6d163425ad8a959b900e22bdcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1133484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2bbc30547ce710afd6317f36167c327d6be17e4771b0cf004cf9d4e44e6b1cf`

```dockerfile
```

-	Layers:
	-	`sha256:f69a3249f9fed7d4ff10490dd907344cad3663547a99277d42198cac7a4d83f5`  
		Last Modified: Wed, 22 Oct 2025 01:19:48 GMT  
		Size: 1.1 MB (1081750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:352944c5a207ded7f5df1d6be7333de705146e0b69f00ee38d0abad07f17c85c`  
		Last Modified: Wed, 22 Oct 2025 01:19:49 GMT  
		Size: 51.7 KB (51734 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.9-beta1-php8.2-fpm-alpine` - linux; ppc64le

```console
$ docker pull wordpress@sha256:03b2ae2ddc17a93fe6bdc7665ada508d69a9aa6fd7af3da663526b6855309359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98147199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ba3caaf2f7759d4f7de189dfbf2c33f06ca0d288df8482378105a68e3a1e48`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 31 Jul 2025 19:22:09 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["/bin/sh"]
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 31 Jul 2025 19:22:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 31 Jul 2025 19:22:09 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_VERSION=8.2.29
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Thu, 31 Jul 2025 19:22:09 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 31 Jul 2025 19:22:09 GMT
WORKDIR /var/www/html
# Thu, 31 Jul 2025 19:22:09 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 31 Jul 2025 19:22:09 GMT
STOPSIGNAL SIGQUIT
# Thu, 31 Jul 2025 19:22:09 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 31 Jul 2025 19:22:09 GMT
CMD ["php-fpm"]
# Tue, 21 Oct 2025 19:03:12 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
RUN set -eux; 	version='6.9-beta1'; 	sha1='e46584af5e1021b8fde7f896794b2c7ff7ebd516'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
VOLUME [/var/www/html]
# Tue, 21 Oct 2025 19:03:12 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 21 Oct 2025 19:03:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 21 Oct 2025 19:03:12 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95a0b03903475651b081c7c705a4ab0f68ab5f5bba328735e8dae6e168526c7`  
		Last Modified: Thu, 09 Oct 2025 00:56:03 GMT  
		Size: 3.6 MB (3614664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436cae3ea479232d2bcf67ca55e6705ab3775fa412e53331855937a2a7340b65`  
		Last Modified: Thu, 09 Oct 2025 00:56:03 GMT  
		Size: 937.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1164e359044b0e56f99538c30031735fcef9128820673f06e10663118d04d0e3`  
		Last Modified: Thu, 09 Oct 2025 00:56:03 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2366352666e4dd557dd7d6eacd17b46c7e42c50c724fbfccb0adfe0124e5f334`  
		Last Modified: Thu, 09 Oct 2025 02:01:34 GMT  
		Size: 12.2 MB (12183657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73282ba125c1b3ae777455c1347cbdd413abccdec275b5f14354238014866d31`  
		Last Modified: Thu, 09 Oct 2025 02:01:33 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe0c6606058be632259df81caaf2d9b23596fe64cfdd19762eccfedd519c0ad`  
		Last Modified: Thu, 09 Oct 2025 02:05:09 GMT  
		Size: 13.5 MB (13493643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eb9f80bd37bd503600f1eb9bcf6f199bd0b43ccd81243c1dd6d3b1307cae8d0`  
		Last Modified: Thu, 09 Oct 2025 02:05:06 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83d9b9b15fa70a931752828a03a141341b86ed3cc7c74aa680def6a9b3f8fd7`  
		Last Modified: Thu, 09 Oct 2025 02:05:06 GMT  
		Size: 19.9 KB (19879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958ed36e5d829231e40f16fddc1cccee4648c2006d429a3f8f1eaca11cd3ee4e`  
		Last Modified: Thu, 09 Oct 2025 02:05:06 GMT  
		Size: 19.9 KB (19865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:704bfb25038e03807b2ca7112359f87d02db1cf7c874bf3e12dd4d488d8995cd`  
		Last Modified: Thu, 09 Oct 2025 02:05:06 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3a05cc62e64942fab3ca3f174511c2547ae87c801dc02ecdde2b9b1b80792b`  
		Last Modified: Thu, 09 Oct 2025 05:38:30 GMT  
		Size: 28.9 MB (28934194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0981541ecbeaa40a3f30c6b6949dd3a82af39a8a50ec6c92c6b17ab3c817cad9`  
		Last Modified: Thu, 09 Oct 2025 05:38:21 GMT  
		Size: 9.0 MB (8963714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61fc4357667607782e27683ae96ce840008d95a5e47191a7072a409fc9ab520e`  
		Last Modified: Thu, 09 Oct 2025 05:38:20 GMT  
		Size: 62.5 KB (62461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d817d0f4ffc17391c4faab982b588d82e40a72543584956ea93becab68a30fa0`  
		Last Modified: Thu, 09 Oct 2025 05:38:20 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1b9f4d650be48e33c58a75769ef363bc924a7b6a28560716ee88964dbf8aff`  
		Last Modified: Wed, 22 Oct 2025 00:27:57 GMT  
		Size: 27.1 MB (27104773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccef526b98180e51f326dd0d6e882b813404eb761911377699d82f3e6721050`  
		Last Modified: Wed, 22 Oct 2025 00:27:55 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1252ad03614f36c74a8f8b70f1cf868f9e3bcdffb50a5141fc29162bb7448a70`  
		Last Modified: Wed, 22 Oct 2025 00:27:55 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8769d5df757b7ba1ed9dfc8506bc37b75fb4b967c77a6c20e033c68388a600ad`  
		Last Modified: Wed, 22 Oct 2025 00:27:55 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-beta1-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:50dbbed617818cd731571ddba4c25111370721dd8da5bbb20c1ec3dc4dc5f9b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1130445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b061ae57b32e6f3c962ce5f5872ef87347809a9326b2a9bc9b6897ef4406f98`

```dockerfile
```

-	Layers:
	-	`sha256:913ee06aa2a1e814cd75903c4eb4b0414c295f37fa0129a9ad787d7cfc71cd40`  
		Last Modified: Wed, 22 Oct 2025 01:19:52 GMT  
		Size: 1.1 MB (1078614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0957f55eb231c67207c9e0598319fe1ce1ad42cdcd49ef2591e232e699f0b8aa`  
		Last Modified: Wed, 22 Oct 2025 01:19:53 GMT  
		Size: 51.8 KB (51831 bytes)  
		MIME: application/vnd.in-toto+json
