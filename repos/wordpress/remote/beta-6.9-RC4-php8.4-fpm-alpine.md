## `wordpress:beta-6.9-RC4-php8.4-fpm-alpine`

```console
$ docker pull wordpress@sha256:27fcc6154f4e383ae828b84d869abfc2f6c009d3b6b186bfb61277f9e4338e17
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `wordpress:beta-6.9-RC4-php8.4-fpm-alpine` - linux; amd64

```console
$ docker pull wordpress@sha256:41e5b3d3132860fcf9be673d821a2f49c1bc9a0818ed6ab03326af979df004ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.6 MB (100606829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4f7ec29e6c7e831880477c145e1b55b24589e44e76e262ae0a8c3585ff75879`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 20 Nov 2025 19:56:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Nov 2025 19:56:07 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 20 Nov 2025 19:56:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 20 Nov 2025 19:56:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 19:56:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 19:56:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:56:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:56:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 19:56:07 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 20 Nov 2025 19:56:07 GMT
ENV PHP_VERSION=8.4.15
# Thu, 20 Nov 2025 19:56:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Thu, 20 Nov 2025 19:56:07 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Thu, 20 Nov 2025 19:56:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 20 Nov 2025 19:56:11 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 19:59:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 19:59:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 19:59:29 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 19:59:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 19:59:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 19:59:30 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 19:59:30 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 20 Nov 2025 19:59:30 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Nov 2025 19:59:30 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 20 Nov 2025 19:59:30 GMT
CMD ["php-fpm"]
# Tue, 02 Dec 2025 01:16:24 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 02 Dec 2025 01:17:10 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:17:10 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:17:10 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:17:12 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:17:12 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:17:12 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:17:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:17:12 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:17:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:17:12 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df5069f8c3d3da88a6f27509fd84e31cae1bb6fd9918bd59c16c61aae8f50918`  
		Last Modified: Thu, 20 Nov 2025 19:59:50 GMT  
		Size: 3.5 MB (3463764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ecf0dc6565fbcc698dad91bfa12b2ff9f6e5d9c0b600975ff334effd78bb89`  
		Last Modified: Thu, 20 Nov 2025 19:59:50 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3f8ac1a5c4727137901f33b76356b0f4ce012f7022e6e4a81a33f40bca52e7`  
		Last Modified: Thu, 20 Nov 2025 19:59:50 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a285d7c9f090289afafe6a7abd294e3a8e9d11094327c70c55aa2705900bc9ea`  
		Last Modified: Thu, 20 Nov 2025 19:59:51 GMT  
		Size: 13.7 MB (13673898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73113f50c8689875ee81b9b1d03bd0c98d5a19f86de24b6bb470a67a5097f31a`  
		Last Modified: Thu, 20 Nov 2025 19:59:50 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50dd8c0a1b022cd7a1bb424aedca280a293dc89209ff117c906dfcfe2838b56`  
		Last Modified: Thu, 20 Nov 2025 19:59:52 GMT  
		Size: 15.0 MB (15035290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ef6ed91e76ea8f4674832b799e10bcc97a009ede7f54a605bb74f7ed4858bfc`  
		Last Modified: Thu, 20 Nov 2025 19:59:50 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc63626f647b28004697bfff266f75d2148c809202949cad4e0caf393112f79`  
		Last Modified: Thu, 20 Nov 2025 19:59:50 GMT  
		Size: 20.1 KB (20080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70908ec0ebb1750179f26ebb420ff2551496d2642f9c3c73191dcec48e4cf603`  
		Last Modified: Thu, 20 Nov 2025 19:59:50 GMT  
		Size: 20.1 KB (20077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceafe65c3d0e080cdd66b304f28c3eb2d3b7f8de0f07ae0693ee7d344f68b347`  
		Last Modified: Thu, 20 Nov 2025 19:59:51 GMT  
		Size: 9.2 KB (9192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80855b9436c4b379db682c316ecc7e813d9041d5b3196ff6b8b0b2077439e271`  
		Last Modified: Tue, 02 Dec 2025 01:17:39 GMT  
		Size: 28.3 MB (28282756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d461bb034b39029d10ca9d20c2ebdc3b191fff29cd9463b0021a68bb6bc04d`  
		Last Modified: Tue, 02 Dec 2025 01:17:37 GMT  
		Size: 9.3 MB (9264911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989c2fceff6980b9191074ad7c8713ecdea3cbd4c72eef0b158982d95de10121`  
		Last Modified: Tue, 02 Dec 2025 01:17:36 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538ecbfe641a867f40bae07b09a5ab7febeb2e6ae4ea0ee22deebcd2778880ca`  
		Last Modified: Tue, 02 Dec 2025 01:17:36 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45014a91e1eca49349a1f24b8e4522a7e07a245d087f0d7f2e9232edf83b1008`  
		Last Modified: Tue, 02 Dec 2025 01:17:39 GMT  
		Size: 27.0 MB (27025189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe51f17505fb5cd36054582cf46fe824351126b5332d1d2befa8d20dc465dd76`  
		Last Modified: Tue, 02 Dec 2025 01:17:36 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1597310b35a0b9b8f30eea3fe8608d914a7b8a17d6f3103cf5d9176c1d8a3279`  
		Last Modified: Tue, 02 Dec 2025 01:17:36 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f99703089b27e28d577096cd7be8b9b751e6414e6f494be8373fb58b32b68f31`  
		Last Modified: Tue, 02 Dec 2025 01:17:36 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:e1bea74c531ac746ab54513eb1f664998014727a2c0b1a565aab4d5c8fe690d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1133540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2661653c5ed3bcfe4bf40331f7ecacb78eb6d516583ae6212e7ece169d98864`

```dockerfile
```

-	Layers:
	-	`sha256:28779c7995eb085924b2828cdd89033ed22d8c304118db3c8c05c0939076ea0d`  
		Last Modified: Tue, 02 Dec 2025 02:28:23 GMT  
		Size: 1.1 MB (1081771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6cad992eb40d24bdeec79e04ee88bcb24f778aa6295e05725b18e7b3c56bf71`  
		Last Modified: Tue, 02 Dec 2025 02:28:23 GMT  
		Size: 51.8 KB (51769 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.9-RC4-php8.4-fpm-alpine` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:e931188cdf0b5dca68e82f49d973f91daabb0fc45af202760bc985b87a278e25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93306296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:656c8304e6318078d8c81baa421e36cb04bbb40527ee91daa561d5b51b9981ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 20 Nov 2025 19:50:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Nov 2025 19:50:07 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 20 Nov 2025 19:50:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 20 Nov 2025 19:50:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 19:50:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 19:50:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:50:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:50:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 19:50:07 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 20 Nov 2025 19:50:07 GMT
ENV PHP_VERSION=8.4.15
# Thu, 20 Nov 2025 19:50:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Thu, 20 Nov 2025 19:50:07 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Thu, 20 Nov 2025 19:50:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 20 Nov 2025 19:50:10 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 19:53:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 19:53:07 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 19:53:08 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 19:53:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 19:53:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 19:53:09 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 19:53:09 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 20 Nov 2025 19:53:09 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Nov 2025 19:53:09 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 20 Nov 2025 19:53:09 GMT
CMD ["php-fpm"]
# Tue, 02 Dec 2025 01:22:29 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 02 Dec 2025 01:23:48 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:23:48 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:23:48 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:23:50 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:23:50 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:23:50 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:23:50 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:23:50 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:23:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:23:50 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68abce577c294880d72f1d50ead332d7b58ff0375a15628cf4c815aca7ab8275`  
		Last Modified: Thu, 20 Nov 2025 19:53:23 GMT  
		Size: 3.4 MB (3428314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc66a7708a44e415da940e66ddbf3ec1dd9f544eee48b363796637853e0e95d0`  
		Last Modified: Thu, 20 Nov 2025 19:53:23 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815d6c9d275579e907e8dacee753269d7f057649d8b48804ae2ff348d18603fd`  
		Last Modified: Thu, 20 Nov 2025 19:53:22 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae3fe220057af5f2a540477eb2a8113e2eec72a815f0573bdfe564910bd47ea`  
		Last Modified: Thu, 20 Nov 2025 19:53:23 GMT  
		Size: 13.7 MB (13673898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b512f071908a7fd4c0353a8fcbf77156af9a65f06ca588165146b920ecc02e39`  
		Last Modified: Thu, 20 Nov 2025 19:53:23 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe54caac9f32455713af61a333f61a1a5dbabcb9ddd042efc7fccc8950d2656a`  
		Last Modified: Thu, 20 Nov 2025 19:53:24 GMT  
		Size: 13.5 MB (13538568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ea8eacb81a5b26743c5a5f62fdad7328bcf6004f78f7551b21644bfe895c9b0`  
		Last Modified: Thu, 20 Nov 2025 19:53:22 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c081201e2b4d52d8d44331f0975f4c3cac46137c9fda676d1956d022a32e20c`  
		Last Modified: Thu, 20 Nov 2025 19:53:22 GMT  
		Size: 19.9 KB (19861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f13e6a7332e7006ce59154a991c33d2a1ae33ec70a74d818bbfee477a3183c`  
		Last Modified: Thu, 20 Nov 2025 19:53:22 GMT  
		Size: 19.9 KB (19863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c8b11f0244f5140c741009d50f2130e394e362248a7ac11bff3c3a1b9d31ed`  
		Last Modified: Thu, 20 Nov 2025 19:53:22 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b663cc74a75a268f48cca0fcc05dc8e8c9fca678bc0d909f29740c24b839ff8f`  
		Last Modified: Tue, 02 Dec 2025 01:24:21 GMT  
		Size: 24.4 MB (24377241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2283fbd091ec6405f550b5ff9811a853a8af4edeef4e206b6150a7bf04996b40`  
		Last Modified: Tue, 02 Dec 2025 01:24:21 GMT  
		Size: 7.7 MB (7700832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db239697553881e07f25bfa708c7a69a4c59cfb2e2f75009e033a4bc2d8d6e5f`  
		Last Modified: Tue, 02 Dec 2025 01:24:19 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570f9c2c845209b909ca27c43e5e781dacf032faead9b6d6a4b3729c372ab9eb`  
		Last Modified: Tue, 02 Dec 2025 01:24:19 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67bc463f64e11d81f5ea8ca232e552ada666c2ab76f62c0138219e31af06020`  
		Last Modified: Tue, 02 Dec 2025 01:24:23 GMT  
		Size: 27.0 MB (27025216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f11dba05bdaadc14e580a205b1186eb464511d71a1b8238716077fbfc74715`  
		Last Modified: Tue, 02 Dec 2025 01:24:20 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1330afffbbf082822d73e6c94b7a3e1dea85b00e6b37f299ad21d14783edb8c7`  
		Last Modified: Tue, 02 Dec 2025 01:24:19 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88584c2616f23e0318470823a7af0813beebdbf4d319e53fb52a6d2055c2b304`  
		Last Modified: Tue, 02 Dec 2025 01:24:20 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:d3b8c3d32c690f0861178b3c9177c32499b458bd8770fea4e8516ff229dc9c40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 KB (51699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769ce6db500c35f95ce1b156bc4f4902b51323e232d2f59de4d3b837b2e06c55`

```dockerfile
```

-	Layers:
	-	`sha256:34341043ce23a1b1f461edb75dc846d99809e6540cc094fab9174da141ed829f`  
		Last Modified: Tue, 02 Dec 2025 02:28:27 GMT  
		Size: 51.7 KB (51699 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.9-RC4-php8.4-fpm-alpine` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:7d4c9ad1af60e07834ea79384372f7701b7179e59bd6ddc3b0c71abe59fce7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.0 MB (91953734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd24dbc928b66dd1ec51b35b70fa553e6ca92253f586be95237fc5ad6826a9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 20 Nov 2025 20:11:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Nov 2025 20:11:10 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 20 Nov 2025 20:11:10 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 20 Nov 2025 20:11:10 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 20:11:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 20:11:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:11:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:11:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 20:11:10 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 20 Nov 2025 20:11:10 GMT
ENV PHP_VERSION=8.4.15
# Thu, 20 Nov 2025 20:11:10 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Thu, 20 Nov 2025 20:11:10 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Thu, 20 Nov 2025 20:11:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 20 Nov 2025 20:11:14 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:14:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 20:14:17 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:14:18 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 20:14:18 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 20:14:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 20:14:18 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 20:14:19 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 20 Nov 2025 20:14:19 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Nov 2025 20:14:19 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 20 Nov 2025 20:14:19 GMT
CMD ["php-fpm"]
# Tue, 02 Dec 2025 01:20:15 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 02 Dec 2025 01:21:38 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:21:38 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:21:38 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:21:40 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:21:40 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:21:40 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:21:40 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:21:40 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:21:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:21:40 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2acbf355b49374246df617fe559619d8f7d3de031f5182fd0be75c174bc3d704`  
		Last Modified: Thu, 20 Nov 2025 21:01:20 GMT  
		Size: 3.2 MB (3244394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38bb5e03f91d6e3cc4ff561aa2ed06a97c23231de0d1689784810378f5ab035`  
		Last Modified: Thu, 20 Nov 2025 21:01:20 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:087bf23a5ab5f65b971116409c156cb7e29c9424cd1b57cf3ae79976dad5c877`  
		Last Modified: Thu, 20 Nov 2025 21:01:29 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd459e12020e86b4ba531823c709c6c95dedd66a53249da5521e63a6f059bcf`  
		Last Modified: Thu, 20 Nov 2025 21:22:45 GMT  
		Size: 13.7 MB (13673885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be824d6e63b91ba20849abfda31b087732ddb480acb7541e5a6c078986a0c46d`  
		Last Modified: Thu, 20 Nov 2025 21:01:30 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:def01952e26a2bff549ace467ec6d209658f7f0f73779397ae54410fe364a5fe`  
		Last Modified: Thu, 20 Nov 2025 21:22:44 GMT  
		Size: 12.8 MB (12784931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb8f9fa12f221428738cc615c279c78623add010edbca5d8722e095a9208fd0`  
		Last Modified: Thu, 20 Nov 2025 21:01:20 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4ebf612ed43df0c6ed897b336947dbdf9f7e193868570ac5380e878fe5ba32`  
		Last Modified: Thu, 20 Nov 2025 21:01:19 GMT  
		Size: 19.9 KB (19857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8996d184cef18cfc38708fe86149bc80a679a6066ece6f64800ba91c75702ca7`  
		Last Modified: Thu, 20 Nov 2025 21:01:21 GMT  
		Size: 19.8 KB (19849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca02ad685eef9d89bfadcb53c89eea1d13f01de0a9ed0ad26bcc62d8092f4229`  
		Last Modified: Thu, 20 Nov 2025 21:01:20 GMT  
		Size: 9.2 KB (9196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d2d53792ae2cd65165b35f5aa7493c87cba03e28b446149e1b3731136083a0`  
		Last Modified: Tue, 02 Dec 2025 01:22:13 GMT  
		Size: 23.2 MB (23152262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c04da2dc907a49622b069afcae4913338317470fc4a731ae3f7330785ba283d`  
		Last Modified: Tue, 02 Dec 2025 01:22:12 GMT  
		Size: 8.8 MB (8793355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b27b39a2424c79af195002a63bf9f3201a86f641fdcc7445e7887c41e5580c`  
		Last Modified: Tue, 02 Dec 2025 01:22:10 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec029d2c3c29fcc8c79da80907e007c5db466680435684b75af8548c7e145da`  
		Last Modified: Tue, 02 Dec 2025 01:22:10 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23dfe5f0ca72bf56a8ba5b7ad602ad47074423bde76073a5c34e351332c71874`  
		Last Modified: Tue, 02 Dec 2025 01:22:12 GMT  
		Size: 27.0 MB (27025212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7952328d454868ee6ffeb54b19d0c10244b79a0eb9fe28bb96b59ad9f35ce640`  
		Last Modified: Tue, 02 Dec 2025 01:22:10 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04bb6cd7bec22403cbcad13453c293dfbc79c625d8041724affb098f6e4570c8`  
		Last Modified: Tue, 02 Dec 2025 01:22:10 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e820695d9303ca0880ed1f71852727c74f56b60d663b620853f1b497bb72af2b`  
		Last Modified: Tue, 02 Dec 2025 01:22:10 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:86e0d1205863ea22ff5e5154beb5eee0b7d858926bc74ae3857bf82011b7a335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1132477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a46624d2cea4a914e652a3096bac4d357998ef4e0c889e82bff56e4577359a84`

```dockerfile
```

-	Layers:
	-	`sha256:cf37a0fe544178c0b2c4fcb6dd6c6f4a0c22cdd88ce990a997880fae3831df93`  
		Last Modified: Tue, 02 Dec 2025 02:28:31 GMT  
		Size: 1.1 MB (1080563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8e20b189fcfbd92dec8d023d7ebbd63565e2924d9fb7e42552cc0253c5db5c9`  
		Last Modified: Tue, 02 Dec 2025 02:28:31 GMT  
		Size: 51.9 KB (51914 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.9-RC4-php8.4-fpm-alpine` - linux; 386

```console
$ docker pull wordpress@sha256:43be8977ff41860b6773babf9931ce70fc031ad1836162f69205e6990e4c843e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.9 MB (99924638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:362741121f7818ddba54a61475f5fb6839d77147960d6bec557afd457fb31044`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 20 Nov 2025 19:59:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Nov 2025 19:59:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 20 Nov 2025 19:59:54 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 20 Nov 2025 19:59:54 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 19:59:54 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 19:59:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:59:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:59:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 19:59:54 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 20 Nov 2025 19:59:54 GMT
ENV PHP_VERSION=8.4.15
# Thu, 20 Nov 2025 19:59:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.15.tar.xz.asc
# Thu, 20 Nov 2025 19:59:54 GMT
ENV PHP_SHA256=a060684f614b8344f9b34c334b6ba8db1177555997edb5b1aceab0a4b807da7e
# Thu, 20 Nov 2025 19:59:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 20 Nov 2025 19:59:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:03:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 20:03:04 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:03:04 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 20 Nov 2025 20:03:05 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 20:03:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 20:03:05 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 20:03:05 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 20 Nov 2025 20:03:05 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Nov 2025 20:03:05 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 20 Nov 2025 20:03:05 GMT
CMD ["php-fpm"]
# Tue, 02 Dec 2025 01:12:27 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 02 Dec 2025 01:13:21 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:13:21 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:13:21 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:13:23 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:13:23 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:13:23 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:13:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:13:23 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:13:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:13:23 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6509e3b357df36f52696dfbe328393531f7e3356e402d07e199f3d973331203f`  
		Last Modified: Thu, 20 Nov 2025 20:03:29 GMT  
		Size: 3.5 MB (3522951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e039386f4b37dbfcbea789b4f5f316f5d4dd9d0e451b31a1f50c6386261e42`  
		Last Modified: Thu, 20 Nov 2025 20:03:29 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39301bd5b5ff1a20465358c20a4027ac1a97efc27ed5ae1eac1a398cd9fbfbd3`  
		Last Modified: Thu, 20 Nov 2025 20:03:29 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c56a1814d66ab69a099656fbc00dee27f4ad2c3e6ac85e4740f5091c29fa63`  
		Last Modified: Thu, 20 Nov 2025 20:03:31 GMT  
		Size: 13.7 MB (13673871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16675b874ecbd38b0d9c4491c160e711fa995fa94c40ee1afee54a7237e06f63`  
		Last Modified: Thu, 20 Nov 2025 20:03:29 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514b21365b498db4e4d185ff1c52d2ea6ed814e1b7a10e304a3e5d83a189a7dd`  
		Last Modified: Thu, 20 Nov 2025 20:03:32 GMT  
		Size: 15.4 MB (15432959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebb869e4ea2a98979966f0a9e8ff3731640e4110fee7acdcdf315c66d8e46a1`  
		Last Modified: Thu, 20 Nov 2025 20:03:30 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8bb45c4965701621e977b88304f11808a15db56408d9b377b62892e12a2398`  
		Last Modified: Thu, 20 Nov 2025 20:03:30 GMT  
		Size: 20.0 KB (20048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fa462833fdeebe4005c71245f31563f120a9e2f02df33278bf6f9ab86b9a208`  
		Last Modified: Thu, 20 Nov 2025 20:03:30 GMT  
		Size: 20.0 KB (20045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae606307634cfeb4cc4641cf71f2ee91c5ce9ef4ff4e031457226fa7cb64376`  
		Last Modified: Thu, 20 Nov 2025 20:03:30 GMT  
		Size: 9.2 KB (9192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3232ac781fe9c69406933f431b69e1b0633f637a3217c55d35bc05a0f87fab56`  
		Last Modified: Tue, 02 Dec 2025 01:14:04 GMT  
		Size: 28.5 MB (28494211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971cfff2caee184e1fed54103d8533e45b6c7a78af0e07ccca3178b7a8162313`  
		Last Modified: Tue, 02 Dec 2025 01:14:03 GMT  
		Size: 8.1 MB (8098006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c54a943ec5ddb0aaaa1460e20615bd6f6fbcffcd1dba29d8b798a11ce871582a`  
		Last Modified: Tue, 02 Dec 2025 01:14:01 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a29c6a0b425d600bdccbfd6e36d4e7ff9554a1f52c550ab549212bd43552edc1`  
		Last Modified: Tue, 02 Dec 2025 01:14:01 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e952ce163f445a347cf5db11eadb2a17bb7b401cd9283b44f76ce8974879f8`  
		Last Modified: Tue, 02 Dec 2025 01:14:03 GMT  
		Size: 27.0 MB (27025204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f281a1d7968865eeaa5f69fe74fb7a9ad957dd7d8b1f6bdcfb370ff6a6dcb265`  
		Last Modified: Tue, 02 Dec 2025 01:14:01 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6996fa2e8eb753cd008dd08a44559a381c8ea9f564393fa70c1c7d8630629e`  
		Last Modified: Tue, 02 Dec 2025 01:13:35 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67ae5db8add529c2b6b0abe79a09d495e948b01d76292f9dbb87f137e405e485`  
		Last Modified: Tue, 02 Dec 2025 01:13:35 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:e1bdd1371ac93a6f592920d758f3168795bb6c7012f79dccbffc831a80975836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1133473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1473bc0ec35abaccb903729402ad51e20a96c1a365dcd5b20eabcc561a0b569d`

```dockerfile
```

-	Layers:
	-	`sha256:ac7bd21bed2af3be41b191747337d25c9baf7d6f193f7411aea4d1e808d8e3dc`  
		Last Modified: Tue, 02 Dec 2025 02:28:40 GMT  
		Size: 1.1 MB (1081746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a573446182b5df3d0bb031d5818e6cb95fc982e4b9960fbdd11b48c32513fc9f`  
		Last Modified: Tue, 02 Dec 2025 02:28:41 GMT  
		Size: 51.7 KB (51727 bytes)  
		MIME: application/vnd.in-toto+json
