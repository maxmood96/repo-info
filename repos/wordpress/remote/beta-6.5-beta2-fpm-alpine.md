## `wordpress:beta-6.5-beta2-fpm-alpine`

```console
$ docker pull wordpress@sha256:86cf05643b97fc59adcfc28d9ed199899e4ab570fda84c1dd33fb3b0f4621691
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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
	-	linux; s390x
	-	unknown; unknown

### `wordpress:beta-6.5-beta2-fpm-alpine` - linux; amd64

```console
$ docker pull wordpress@sha256:2b0f59d27bda2fe3008400822994aa378e938ad873e0388e404c0c7ccaca53bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88659094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:860659f1a4b206d96271c1e60f62bdabcbe312834cb3bfce50832e8819e829cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:23:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 27 Jan 2024 04:23:26 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 27 Jan 2024 04:23:27 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 27 Jan 2024 04:23:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 27 Jan 2024 04:23:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 27 Jan 2024 04:23:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 04:23:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 04:23:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 27 Jan 2024 04:47:22 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 16 Feb 2024 22:16:42 GMT
ENV PHP_VERSION=8.2.16
# Fri, 16 Feb 2024 22:16:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.16.tar.xz.asc
# Fri, 16 Feb 2024 22:16:42 GMT
ENV PHP_SHA256=28cdc995b7d5421711c7044294885fcde4390c9f67504a994b4cf9bc1b5cc593
# Fri, 16 Feb 2024 22:16:49 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 16 Feb 2024 22:16:49 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 16 Feb 2024 22:24:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 16 Feb 2024 22:24:17 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 16 Feb 2024 22:24:19 GMT
RUN docker-php-ext-enable sodium
# Fri, 16 Feb 2024 22:24:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Feb 2024 22:24:19 GMT
WORKDIR /var/www/html
# Fri, 16 Feb 2024 22:24:19 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 16 Feb 2024 22:24:19 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Feb 2024 22:24:19 GMT
EXPOSE 9000
# Fri, 16 Feb 2024 22:24:20 GMT
CMD ["php-fpm"]
# Tue, 20 Feb 2024 20:03:10 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
RUN set -eux; 	version='6.5-beta2'; 	sha1='f8a0187b5c143fa20b756efd9d456da9da077d7c'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
VOLUME [/var/www/html]
# Tue, 20 Feb 2024 20:03:10 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Feb 2024 20:03:10 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9ef19a461f9d419fc91c59399a9daa1f3302d30f099065a185a8bfeea3c9a8`  
		Last Modified: Sat, 27 Jan 2024 05:36:08 GMT  
		Size: 2.8 MB (2761515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2fc49c6a93ebf520a5ecba9c061dbdd22083df74d0de9dcac9011f3f927d9f`  
		Last Modified: Sat, 27 Jan 2024 05:36:08 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a4aa92ed6361a95da0e916e30e661754a1edf38c0b8b15bee6872d055e3603`  
		Last Modified: Sat, 27 Jan 2024 05:36:08 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd0dbc075989eba7f2459368ee1acde50328b69f2aa0b318773bf0c01294c1dd`  
		Last Modified: Fri, 16 Feb 2024 22:50:03 GMT  
		Size: 12.1 MB (12106429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f7ccdb7d34754d610213c860f5175342db1e2f9b455efcfcdd9a37513619a3`  
		Last Modified: Fri, 16 Feb 2024 22:50:02 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9597f5d988d7d091482b41b7500f8882962d99437285ce426409151d8e0b3d7`  
		Last Modified: Fri, 16 Feb 2024 22:50:30 GMT  
		Size: 12.9 MB (12850052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a35aa494b3d6a52cfb29411b3bb5ea5ff0454a5bfa0b9bdfb041be8d36d4097`  
		Last Modified: Fri, 16 Feb 2024 22:50:28 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c166c0ae96c63e523fde4a7b25ddea0ff1aed2062e3a02c0795d1fdcd947c89`  
		Last Modified: Fri, 16 Feb 2024 22:50:28 GMT  
		Size: 19.3 KB (19294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88edba531d78c8412a6ff1be3c894b13ccb06a40e84d284437be9cbf17730646`  
		Last Modified: Fri, 16 Feb 2024 22:50:28 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a825afc05d021090dfdaa586857c89262abbe332c4fe32bec7fd03c36d993a0b`  
		Last Modified: Wed, 21 Feb 2024 00:51:43 GMT  
		Size: 28.6 MB (28637057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f81ab0ea488607e21f48af7fc6ad8317298074d5c70f1075cd725ef7e1334cd`  
		Last Modified: Wed, 21 Feb 2024 00:51:43 GMT  
		Size: 4.3 MB (4298278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9126bc382b15599f30fc3f000a70a35a221fe638eefddda8ca5a6b5e2953f37`  
		Last Modified: Wed, 21 Feb 2024 00:51:42 GMT  
		Size: 59.4 KB (59379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab884ae5083b26e2fc675f21d8687885aa2ddc34532c7d23e1acf9518882ae6`  
		Last Modified: Wed, 21 Feb 2024 00:51:42 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f32132dd0de2aaf634184f1f71e6daf20d4b946a576d0d2cf98bd5b33be72a`  
		Last Modified: Wed, 21 Feb 2024 00:51:44 GMT  
		Size: 24.5 MB (24500244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528ea9cd06faf247a068c8eef7650c15a664b8d57501f2b698e2129d1aceb95d`  
		Last Modified: Wed, 21 Feb 2024 00:51:44 GMT  
		Size: 2.3 KB (2343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c15101e91961e165333c3380b0e0d9627bc6a92fc9eccbcc44ae03cddc83890`  
		Last Modified: Wed, 21 Feb 2024 00:51:44 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.5-beta2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:6e2d9371318f5777c21baf884a6d3d914069994954ddb96c1768f1b301f76c0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1060278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac46ee6139a6225dd792666a146a05954c61cc4e57c6663660f7e3e1750a3271`

```dockerfile
```

-	Layers:
	-	`sha256:3200650e93a5268a1c1e7e63c0e701d3b4b31cdff82b8de3b5179a2a3ce3ec93`  
		Last Modified: Wed, 21 Feb 2024 00:51:42 GMT  
		Size: 1.0 MB (1012627 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4d04c87dd58dce5a51b6e417ad4266f8c3a37e0890b47e9198a1e925940db85`  
		Last Modified: Wed, 21 Feb 2024 00:51:42 GMT  
		Size: 47.7 KB (47651 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.5-beta2-fpm-alpine` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:4f28a249aa7c15b3e800bff3fa59a22ea7c76e67f784c69c7646ee8702a1fc5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86623526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:babcc3f37ec15f78bd1b9472821454b8be593d1fe47be069c1de2a141c73adbd`
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
# Sat, 27 Jan 2024 05:52:06 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 16 Feb 2024 20:14:21 GMT
ENV PHP_VERSION=8.2.16
# Fri, 16 Feb 2024 20:14:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.16.tar.xz.asc
# Fri, 16 Feb 2024 20:14:21 GMT
ENV PHP_SHA256=28cdc995b7d5421711c7044294885fcde4390c9f67504a994b4cf9bc1b5cc593
# Fri, 16 Feb 2024 20:14:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 16 Feb 2024 20:14:29 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 16 Feb 2024 20:24:29 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 16 Feb 2024 20:24:30 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 16 Feb 2024 20:24:31 GMT
RUN docker-php-ext-enable sodium
# Fri, 16 Feb 2024 20:24:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Feb 2024 20:24:31 GMT
WORKDIR /var/www/html
# Fri, 16 Feb 2024 20:24:32 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 16 Feb 2024 20:24:32 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Feb 2024 20:24:32 GMT
EXPOSE 9000
# Fri, 16 Feb 2024 20:24:32 GMT
CMD ["php-fpm"]
# Tue, 20 Feb 2024 20:03:10 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
RUN set -eux; 	version='6.5-beta2'; 	sha1='f8a0187b5c143fa20b756efd9d456da9da077d7c'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
VOLUME [/var/www/html]
# Tue, 20 Feb 2024 20:03:10 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Feb 2024 20:03:10 GMT
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
	-	`sha256:403e40b5fd606e671869240fc77ba95ba712be24d453e69493dc11946199a5ee`  
		Last Modified: Fri, 16 Feb 2024 20:47:39 GMT  
		Size: 12.1 MB (12106446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259f7cdbb933a648248b1e724897c4eef373a696f64d713945665fa1a189ebd1`  
		Last Modified: Fri, 16 Feb 2024 20:47:38 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b751b97b01c947f2789990769455367d1b104d31f285297bc45bf08cee3de61a`  
		Last Modified: Fri, 16 Feb 2024 20:48:09 GMT  
		Size: 11.7 MB (11694926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbbe2039844df3ab6c61b42352b4721a3877956f6abf2cea062d42081d6301d4`  
		Last Modified: Fri, 16 Feb 2024 20:48:06 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d47ffe959afefcc138192721a0b0a8f9c97b03dfd4118dcc56a2f24ab28a645`  
		Last Modified: Fri, 16 Feb 2024 20:48:06 GMT  
		Size: 19.1 KB (19138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:687aa25cc875cdccab429e504e311bb5861505f8837535de4db82474968079be`  
		Last Modified: Fri, 16 Feb 2024 20:48:06 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e632381af4fd1909910d09507bb1f71880cb49a4bd93bb5960dbf0cbdb846aa`  
		Last Modified: Wed, 21 Feb 2024 07:38:59 GMT  
		Size: 28.2 MB (28163515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caea6115d356cc065cb1fa819f2723794f1946a6202495d4643625c2da08008b`  
		Last Modified: Wed, 21 Feb 2024 07:38:58 GMT  
		Size: 4.1 MB (4131840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29403fd50553cd568d8cf7b13d3b8e7e312651ee10294f9a040241ddc472abd`  
		Last Modified: Wed, 21 Feb 2024 07:38:58 GMT  
		Size: 59.4 KB (59417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f925c63791548776edfa70e2b4af76a0aff43fdc0cb4844b0fdcd1d8c587097`  
		Last Modified: Wed, 21 Feb 2024 07:38:58 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b549028d0e8e87e4cfd3e6e93ea6932db6faadf4c8e66c5c706b9cec4d907481`  
		Last Modified: Wed, 21 Feb 2024 07:39:00 GMT  
		Size: 24.5 MB (24500249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:595b1ccf72634116cff315174c60e491d127e35825119bc0ac569d2cd2e4e50f`  
		Last Modified: Wed, 21 Feb 2024 07:38:59 GMT  
		Size: 2.3 KB (2347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4949793bf78f4880e7853ed188cfbb9c26faba248f243ceece95e96d6db49fe6`  
		Last Modified: Wed, 21 Feb 2024 07:38:59 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.5-beta2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:bf6f5a90fe40db6b340771a0ada652df5163cddb5fbb14182de5a05bf8f74fed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 KB (47590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d16fa91db86703e0e7bba2e1f8f6a8bc25037742f7325fe64d10cdf9a077e7d`

```dockerfile
```

-	Layers:
	-	`sha256:efbfb8934dde7128b6c553cdaf8fa24651762fe44502b940e7a110547aa2caa9`  
		Last Modified: Wed, 21 Feb 2024 07:38:57 GMT  
		Size: 47.6 KB (47590 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.5-beta2-fpm-alpine` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:ed93024f658b243ad7207cbf6ea6c81849593635f8376d655355d16a6dd5a2e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.0 MB (83971185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:032592c123b68abc45b1a14b6cb2a01ac438c7a5916ee2a82f9fc26d796124fe`
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
# Sat, 27 Jan 2024 06:55:08 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 16 Feb 2024 21:32:34 GMT
ENV PHP_VERSION=8.2.16
# Fri, 16 Feb 2024 21:32:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.16.tar.xz.asc
# Fri, 16 Feb 2024 21:32:35 GMT
ENV PHP_SHA256=28cdc995b7d5421711c7044294885fcde4390c9f67504a994b4cf9bc1b5cc593
# Fri, 16 Feb 2024 21:32:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 16 Feb 2024 21:32:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 16 Feb 2024 21:38:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 16 Feb 2024 21:38:31 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 16 Feb 2024 21:38:32 GMT
RUN docker-php-ext-enable sodium
# Fri, 16 Feb 2024 21:38:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Feb 2024 21:38:32 GMT
WORKDIR /var/www/html
# Fri, 16 Feb 2024 21:38:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 16 Feb 2024 21:38:33 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Feb 2024 21:38:33 GMT
EXPOSE 9000
# Fri, 16 Feb 2024 21:38:33 GMT
CMD ["php-fpm"]
# Tue, 20 Feb 2024 20:03:10 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
RUN set -eux; 	version='6.5-beta2'; 	sha1='f8a0187b5c143fa20b756efd9d456da9da077d7c'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
VOLUME [/var/www/html]
# Tue, 20 Feb 2024 20:03:10 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Feb 2024 20:03:10 GMT
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
	-	`sha256:99d089158941b984e7d5b784810cc92556bd7db0b0a241d01fbe13e410b4d911`  
		Last Modified: Fri, 16 Feb 2024 22:01:54 GMT  
		Size: 12.1 MB (12106444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9bdaf5327164aa91a3bcc96434aa48f12ecfe2cc5c2d0bc2e30fa4928f8972`  
		Last Modified: Fri, 16 Feb 2024 22:01:53 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59f5a7102cbcde4301398b617119299be3626f4cbe7c6e8a5f29c7e11b72df4`  
		Last Modified: Fri, 16 Feb 2024 22:02:27 GMT  
		Size: 11.0 MB (10965955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af94b595398886520944b197a0e0f46c334b7b4ede2bd4d95e359c883c7081e1`  
		Last Modified: Fri, 16 Feb 2024 22:02:25 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af3be24c3f26a458db8866ac23be508bd4bc96c6d2dd118a57e6ee2c8cace0b`  
		Last Modified: Fri, 16 Feb 2024 22:02:25 GMT  
		Size: 19.1 KB (19117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad904eeba2b912c71d7ae0b1f349004aab08e8ef3a19426c40667c688d36f248`  
		Last Modified: Fri, 16 Feb 2024 22:02:25 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b854d0ed9a838924c623d23d87a87296ab79465376826eddbe198f0c1f18792`  
		Last Modified: Sat, 17 Feb 2024 08:01:39 GMT  
		Size: 26.6 MB (26597750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb2470abf433d35a5907d9d7bbbbb934727b6775fb7808c6c3f2699c77b052b`  
		Last Modified: Sat, 17 Feb 2024 08:01:38 GMT  
		Size: 4.2 MB (4172657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54605debc1df2e20e5e28dcc2c2a4ccfeed26457f89975fd7dddad63fda11e8e`  
		Last Modified: Sat, 17 Feb 2024 08:01:38 GMT  
		Size: 59.4 KB (59401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066ff246ec97ff9dc6f62701047a49efd4879b2d1a5b47e651176486f298cc87`  
		Last Modified: Sat, 17 Feb 2024 08:01:38 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5d8f04f220940fb08c1345019dbf14ce72105b9752deaf26999a48baba894c`  
		Last Modified: Wed, 21 Feb 2024 14:15:31 GMT  
		Size: 24.5 MB (24500216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ba45dbfd0825f0d3b894774ab3a1f9b632e376cbe3ea04c277a985b9807d59`  
		Last Modified: Wed, 21 Feb 2024 14:15:30 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338566c5c4e07855af3c99b765b5563fa8039e8a969293ea42bae7db645f7bf0`  
		Last Modified: Wed, 21 Feb 2024 14:15:30 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.5-beta2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:17ab7b3f7632b6b538dcf4e9ce20d2366c5428a1200c20a47a648f650b73e636
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1058874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4923e1f3adfb5bfc86f4ffdb3ae2cca78d9666dcc585de4fe2dd09710ffa5a1c`

```dockerfile
```

-	Layers:
	-	`sha256:3247de4fb2f698037fe77d641aa308a92b7f93f53761c514c76f240ead078d0f`  
		Last Modified: Wed, 21 Feb 2024 14:15:30 GMT  
		Size: 1.0 MB (1012695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b52ed670b5db6719b2dcdfdc47951baaab546a8dcc1c79ad485de29c6cb580d`  
		Last Modified: Wed, 21 Feb 2024 14:15:30 GMT  
		Size: 46.2 KB (46179 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.5-beta2-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:3d9bad87f372d2c6418f94033437642a896a7fd5d0f44b075c4b6e66a3e4df97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.9 MB (88888001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:797ff2ab52e59c084e9edf08d6b393e3afece3dc71335b7e58f46ca4bd6672f2`
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
# Sat, 27 Jan 2024 07:53:27 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 17 Feb 2024 00:08:31 GMT
ENV PHP_VERSION=8.2.16
# Sat, 17 Feb 2024 00:08:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.16.tar.xz.asc
# Sat, 17 Feb 2024 00:08:31 GMT
ENV PHP_SHA256=28cdc995b7d5421711c7044294885fcde4390c9f67504a994b4cf9bc1b5cc593
# Sat, 17 Feb 2024 00:08:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 17 Feb 2024 00:08:39 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 17 Feb 2024 00:16:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 17 Feb 2024 00:16:49 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 17 Feb 2024 00:16:50 GMT
RUN docker-php-ext-enable sodium
# Sat, 17 Feb 2024 00:16:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 17 Feb 2024 00:16:51 GMT
WORKDIR /var/www/html
# Sat, 17 Feb 2024 00:16:51 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 17 Feb 2024 00:16:51 GMT
STOPSIGNAL SIGQUIT
# Sat, 17 Feb 2024 00:16:51 GMT
EXPOSE 9000
# Sat, 17 Feb 2024 00:16:51 GMT
CMD ["php-fpm"]
# Tue, 20 Feb 2024 20:03:10 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
RUN set -eux; 	version='6.5-beta2'; 	sha1='f8a0187b5c143fa20b756efd9d456da9da077d7c'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
VOLUME [/var/www/html]
# Tue, 20 Feb 2024 20:03:10 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Feb 2024 20:03:10 GMT
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
	-	`sha256:6dac19050fc2b8531fca918e38279d16a61cb2c3ed4c61aaeeb6f216dfe62517`  
		Last Modified: Sat, 17 Feb 2024 00:42:53 GMT  
		Size: 12.1 MB (12106445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621db1a685c14a42f7923dbe31d39e1b14d7b744ccdc18d6a32ff4aa916c985f`  
		Last Modified: Sat, 17 Feb 2024 00:42:52 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922ed6b389e044a07a617b31e309f87d92e8f338e1a98aeb42e2c1e5445120d2`  
		Last Modified: Sat, 17 Feb 2024 00:43:17 GMT  
		Size: 12.9 MB (12911412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e088f63cc11e586e013b275936527b034e3d07c31d80cedb69a8bc10ffa8168`  
		Last Modified: Sat, 17 Feb 2024 00:43:16 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b97bdb0eaf16cc00e281b1188995a1f9d81c3d8ae6dc55ccfc53d93122b18bbf`  
		Last Modified: Sat, 17 Feb 2024 00:43:16 GMT  
		Size: 19.1 KB (19093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699ebc43f268bd3405d766c6f32dce083b28a58032c4f92807b78ff3040b7c7e`  
		Last Modified: Sat, 17 Feb 2024 00:43:16 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a847704affba418df9ee8df2b6872e2d8d6f4086ff976245e597a35446c09972`  
		Last Modified: Sun, 18 Feb 2024 05:34:39 GMT  
		Size: 28.8 MB (28770547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1abc2bc42d6a01f93cb8e3f01c79ebb2425854e6f45c521a75ef6fc15a4d23`  
		Last Modified: Sun, 18 Feb 2024 05:34:39 GMT  
		Size: 4.3 MB (4339322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d7eb9c51f733025b52e6f9c3c6c5f44ffd9cf3a532d33454d271324f8c3fe02`  
		Last Modified: Sun, 18 Feb 2024 05:34:38 GMT  
		Size: 59.4 KB (59359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72aa1ab5cb7d02120aa968abf498213d809306f14c85677e62ad5abc31ad86a1`  
		Last Modified: Sun, 18 Feb 2024 05:34:38 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b575bf8a9263b28305a336cc95a9cea974a6a179b1b53bb259cb6112d4326a4c`  
		Last Modified: Wed, 21 Feb 2024 04:42:32 GMT  
		Size: 24.5 MB (24500224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08039a7ea990b856be91c236d3c5169865071bb9f580301e9323dd83c3ccb09`  
		Last Modified: Wed, 21 Feb 2024 04:42:30 GMT  
		Size: 2.4 KB (2350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a88e5dc569a3fd5df4cd671051ec692f86cbe3299ffea0ae381fb3c852a8cf`  
		Last Modified: Wed, 21 Feb 2024 04:42:30 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.5-beta2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:d3fdba49f6c4ab3f9435a972eace265738e9ed38162103ab68ab258e94fadeef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1058690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f271b79b5cd1e4fe640fda0a7bac92184fd773b7294754a56326e22bb0098ec4`

```dockerfile
```

-	Layers:
	-	`sha256:15aa283e1698ef53091af735af855ed872ddf034f9fb2903f897fbde98973fd7`  
		Last Modified: Wed, 21 Feb 2024 04:42:30 GMT  
		Size: 1.0 MB (1012646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f93de28e2e9ff13661710414ae56992a62214dd73017aa945ca3adfd35d87fcb`  
		Last Modified: Wed, 21 Feb 2024 04:42:30 GMT  
		Size: 46.0 KB (46044 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.5-beta2-fpm-alpine` - linux; 386

```console
$ docker pull wordpress@sha256:647adcb2b18a2e8fab3e2a7752904a128665b90e260a03b3713bf9d46aeed789
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.3 MB (89280244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d08cb6428b3ea6f49da9272f30d4617fc31d736e7dba8f0f3a02940811743c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:42:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 27 Jan 2024 04:42:11 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 27 Jan 2024 04:42:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 27 Jan 2024 04:42:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 27 Jan 2024 04:42:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 27 Jan 2024 04:42:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 04:42:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 04:42:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 27 Jan 2024 05:24:12 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 16 Feb 2024 22:21:11 GMT
ENV PHP_VERSION=8.2.16
# Fri, 16 Feb 2024 22:21:11 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.16.tar.xz.asc
# Fri, 16 Feb 2024 22:21:11 GMT
ENV PHP_SHA256=28cdc995b7d5421711c7044294885fcde4390c9f67504a994b4cf9bc1b5cc593
# Fri, 16 Feb 2024 22:21:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 16 Feb 2024 22:21:20 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 16 Feb 2024 22:34:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 16 Feb 2024 22:34:59 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 16 Feb 2024 22:35:00 GMT
RUN docker-php-ext-enable sodium
# Fri, 16 Feb 2024 22:35:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Feb 2024 22:35:01 GMT
WORKDIR /var/www/html
# Fri, 16 Feb 2024 22:35:01 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 16 Feb 2024 22:35:01 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Feb 2024 22:35:01 GMT
EXPOSE 9000
# Fri, 16 Feb 2024 22:35:02 GMT
CMD ["php-fpm"]
# Tue, 20 Feb 2024 20:03:10 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
RUN set -eux; 	version='6.5-beta2'; 	sha1='f8a0187b5c143fa20b756efd9d456da9da077d7c'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
VOLUME [/var/www/html]
# Tue, 20 Feb 2024 20:03:10 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Feb 2024 20:03:10 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf91a7316d2e2098b1a91882947964b19bab201421576e249c440063e956bcab`  
		Last Modified: Sat, 27 Jan 2024 06:46:12 GMT  
		Size: 2.8 MB (2825332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a5caaf92a60154c94967702a2fdee5954dec8352f776f8abc87659c4de67f6`  
		Last Modified: Sat, 27 Jan 2024 06:46:11 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d170158e1d1cffac62a145eb90dbbfd417840d1e2a9a4ae707cafa0bcc2781`  
		Last Modified: Sat, 27 Jan 2024 06:46:11 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d9caef1e571163b3e7f9d821630dd9dde97669e189f9d7ccc063ace6f5ee91`  
		Last Modified: Fri, 16 Feb 2024 23:14:16 GMT  
		Size: 12.1 MB (12106438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bacc0a421d99e2c00276fcec41ffb195a9635c6993cd5973bdc1803fff3579b5`  
		Last Modified: Fri, 16 Feb 2024 23:14:15 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd182e3c0d4912b874560b9044e0d05db433051ce8d861c04d4da7fbd9a7f6f`  
		Last Modified: Fri, 16 Feb 2024 23:14:46 GMT  
		Size: 13.2 MB (13196591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b36a12c034cc731250376bd05c2a1b27edd7ffa2471be9ac9d782f5de35979d4`  
		Last Modified: Fri, 16 Feb 2024 23:14:43 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904dd6efc3579e5076021f1e969a3f8dd80d880473e08b6ac3f15516f6803719`  
		Last Modified: Fri, 16 Feb 2024 23:14:43 GMT  
		Size: 19.3 KB (19304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:440cd596500c5b001558425a09ef3385c112bbbc1b7341e838dc7c06cf348d45`  
		Last Modified: Fri, 16 Feb 2024 23:14:43 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69498fe3ceb02d70ffd12d7d139128181d3a967be98b4905851df6d79c36d57`  
		Last Modified: Wed, 21 Feb 2024 00:51:52 GMT  
		Size: 28.9 MB (28877552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6255b35754198e4dc232102f432ca0ef7186f462f597966266b937cd2c95bdae`  
		Last Modified: Wed, 21 Feb 2024 00:51:52 GMT  
		Size: 4.4 MB (4433179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6638e0f00067a90d880b0641b01d6f00d9d9372f0423b2d20c3b3f6d8c966523`  
		Last Modified: Wed, 21 Feb 2024 00:51:52 GMT  
		Size: 59.4 KB (59392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0fa5efd191ce21623f8089d9a996ad56d908f726101fe5fbc30f9c9fc8b70ac`  
		Last Modified: Wed, 21 Feb 2024 00:51:52 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7c9a3abed599321b24774ca15a30059795392c87da863acf860e066deadd79`  
		Last Modified: Wed, 21 Feb 2024 00:51:54 GMT  
		Size: 24.5 MB (24500253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a80feeb004a2d16e5c64a0c92d583bf22e5f6583b7b7417a6ee1c3fbe43bdf52`  
		Last Modified: Wed, 21 Feb 2024 00:51:53 GMT  
		Size: 2.3 KB (2344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ddd9dcc2ee4dba4fe733bd9eefa136ba39e625eb739505e6b0093f0b3b0a3a`  
		Last Modified: Wed, 21 Feb 2024 00:51:53 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.5-beta2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:a5108d0a472ee1411703ec725f06ed32bcee1547f451ff517bb1dcf9dc079342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1060176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43aee35bf0465f9a1a85a6d0741218949278f83e1e91f38806b0f8e3b9916b29`

```dockerfile
```

-	Layers:
	-	`sha256:aaa653baafc58cbb73d49a74086e4774f480463a55aa3db23d3a46b68176314f`  
		Last Modified: Wed, 21 Feb 2024 00:51:52 GMT  
		Size: 1.0 MB (1012582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bad3afc817118bc0eec9da8b66ba838a5c1df319c81c76cb92c6fbae8b512f4`  
		Last Modified: Wed, 21 Feb 2024 00:51:51 GMT  
		Size: 47.6 KB (47594 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.5-beta2-fpm-alpine` - linux; s390x

```console
$ docker pull wordpress@sha256:f6d050ea9c18198c88dd316a82ebb1f54905751d96654a3217726999c3f2af49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89538239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:289fc759c4263a639e846d683ba1c3ab8dcc44d630adf118b2b1fba6fb2f1f7d`
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
# Sat, 27 Jan 2024 11:36:32 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 16 Feb 2024 22:35:48 GMT
ENV PHP_VERSION=8.2.16
# Fri, 16 Feb 2024 22:35:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.16.tar.xz.asc
# Fri, 16 Feb 2024 22:35:48 GMT
ENV PHP_SHA256=28cdc995b7d5421711c7044294885fcde4390c9f67504a994b4cf9bc1b5cc593
# Fri, 16 Feb 2024 22:35:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 16 Feb 2024 22:35:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 16 Feb 2024 22:42:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 16 Feb 2024 22:42:35 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 16 Feb 2024 22:42:36 GMT
RUN docker-php-ext-enable sodium
# Fri, 16 Feb 2024 22:42:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Feb 2024 22:42:36 GMT
WORKDIR /var/www/html
# Fri, 16 Feb 2024 22:42:36 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 16 Feb 2024 22:42:37 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Feb 2024 22:42:37 GMT
EXPOSE 9000
# Fri, 16 Feb 2024 22:42:37 GMT
CMD ["php-fpm"]
# Tue, 20 Feb 2024 20:03:10 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
RUN set -eux; 	version='6.5-beta2'; 	sha1='f8a0187b5c143fa20b756efd9d456da9da077d7c'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
VOLUME [/var/www/html]
# Tue, 20 Feb 2024 20:03:10 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 20 Feb 2024 20:03:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 20 Feb 2024 20:03:10 GMT
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
	-	`sha256:8dc0897166a08814709b01c54c04a82880e1b72019180ef3913a41552c545791`  
		Last Modified: Fri, 16 Feb 2024 23:23:24 GMT  
		Size: 12.1 MB (12106450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a9edb885365f41d6ad2fa6aec518a5b5a21be3a752c12e8df8439116a542451`  
		Last Modified: Fri, 16 Feb 2024 23:23:23 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa5f89aa201c8af5af316f6cf41d709c5c489da266fbf8babc0df26ef8b2a6f`  
		Last Modified: Fri, 16 Feb 2024 23:23:40 GMT  
		Size: 12.6 MB (12598760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11d134900562fdef932ac459d361bee259d93d9349667df64049b8815a3eea9`  
		Last Modified: Fri, 16 Feb 2024 23:23:38 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40a0c6b07975cde48df0ceafb8e17c0ac6254789a42104b0d8235a06172ddb27`  
		Last Modified: Fri, 16 Feb 2024 23:23:38 GMT  
		Size: 19.1 KB (19105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3b3c7b4b210747bda29fb0b4c92c9e96efce84a22ad327346a5a70b9e634ab`  
		Last Modified: Fri, 16 Feb 2024 23:23:38 GMT  
		Size: 9.2 KB (9175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82fb5bc7ec1cb920d2c3b6289f49e05729058057e40f1721150a905b2c4e5a1`  
		Last Modified: Sun, 18 Feb 2024 09:05:36 GMT  
		Size: 29.6 MB (29624638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5719b410bfc4799667eca2dd1de8289651deb72ca81553ccf3198864905621`  
		Last Modified: Sun, 18 Feb 2024 09:05:36 GMT  
		Size: 4.4 MB (4428343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31213283165763a2d794ad0b124aefdfce03b38d0823f7b0f872e4a339377a8f`  
		Last Modified: Sun, 18 Feb 2024 09:05:36 GMT  
		Size: 59.4 KB (59405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762af74af8103236e9c072a750cc5163eba45b36e0c4a1df74816e53e531b99f`  
		Last Modified: Sun, 18 Feb 2024 09:05:36 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de27655532e6bb82ac8c3f40e175fb2e253377c5be180f504e1700757ac0c7c`  
		Last Modified: Wed, 21 Feb 2024 07:21:09 GMT  
		Size: 24.5 MB (24500224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245bc0222ab2f624d493e022111af707ddee2e1b49ad8645c1b49b4b9a4d9935`  
		Last Modified: Wed, 21 Feb 2024 07:21:09 GMT  
		Size: 2.3 KB (2347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae69b20c1f717aadd3dd98bb03287baa222d5583bc2035a439182e86efabdaf`  
		Last Modified: Wed, 21 Feb 2024 07:21:09 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.5-beta2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:3ebcad73f90f3e6c4bf9793f994819f191263c3626f86252b6ee0be91f4b38c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1056699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb669173b00fbf532b2d572efbb1ae1f461edf231f8c5527108e1ae759c78f75`

```dockerfile
```

-	Layers:
	-	`sha256:ce6596740759b4de2cfefd1817b707f6eee0e3f44060f93bdebf5faee1c3411c`  
		Last Modified: Wed, 21 Feb 2024 07:21:08 GMT  
		Size: 1.0 MB (1010673 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44f9ae96e711bafec58ce9628bdfd22db92aa13fe653d7e8e2de7c8f75baa574`  
		Last Modified: Wed, 21 Feb 2024 07:21:08 GMT  
		Size: 46.0 KB (46026 bytes)  
		MIME: application/vnd.in-toto+json
