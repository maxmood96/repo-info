## `wordpress:php8.3-fpm-alpine`

```console
$ docker pull wordpress@sha256:028dfda5be381ff825c8b701fc7f7809f8972b5b6115a9d45b47283b3d2a123a
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

### `wordpress:php8.3-fpm-alpine` - linux; amd64

```console
$ docker pull wordpress@sha256:ae42d91f6e4023590e7689d0890de1c9149c59798a220e81c3bfd9d9bfc8e692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.1 MB (89056183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e835157115cdb323cdc6897a59b9adbae62a964be7a5726cd25c992b5f2b71f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 06 Dec 2023 20:31:30 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Wed, 06 Dec 2023 20:31:30 GMT
CMD ["/bin/sh"]
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 06 Dec 2023 20:31:30 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Dec 2023 20:31:30 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_VERSION=8.3.0
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.0.tar.xz.asc
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_SHA256=1db84fec57125aa93638b51bb2b15103e12ac196e2f960f0d124275b2687ea54
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 06 Dec 2023 20:31:30 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 06 Dec 2023 20:31:30 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 06 Dec 2023 20:31:30 GMT
RUN docker-php-ext-enable sodium
# Wed, 06 Dec 2023 20:31:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Dec 2023 20:31:30 GMT
WORKDIR /var/www/html
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 06 Dec 2023 20:31:30 GMT
STOPSIGNAL SIGQUIT
# Wed, 06 Dec 2023 20:31:30 GMT
EXPOSE 9000
# Wed, 06 Dec 2023 20:31:30 GMT
CMD ["php-fpm"]
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	version='6.4.2'; 	sha1='d1aedbfea77b243b09e0ab05b100b782497406dd'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
VOLUME [/var/www/html]
# Wed, 06 Dec 2023 20:31:30 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Dec 2023 20:31:30 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc99979baa6760dc40a927f812328a1431e3870d0f166b035365166ef2cf8d4`  
		Last Modified: Tue, 12 Dec 2023 23:24:24 GMT  
		Size: 2.8 MB (2755737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47536423e0797b82f7a737a4efeb29297c96a33e8662ddcd121d728a01eac477`  
		Last Modified: Tue, 12 Dec 2023 23:24:23 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be6d4fc569fcdbdb835c5ee3607367e6ba4779809c0fad97de75045144220f8`  
		Last Modified: Tue, 12 Dec 2023 23:24:23 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6970d99b9a10b135bc761aac8d5e43a8a1610cdec9eef9619fc11f567578fb4`  
		Last Modified: Tue, 12 Dec 2023 23:26:37 GMT  
		Size: 12.5 MB (12452290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:621aa29822cea27221557011785bd84ebc6bc2de17474a67b0b9894da5724ed9`  
		Last Modified: Tue, 12 Dec 2023 23:26:36 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d43c992ef9c22e4c081de6a6c9b85d098c8d29cc257a91fd56edcf1132318d`  
		Last Modified: Sat, 16 Dec 2023 06:44:03 GMT  
		Size: 13.1 MB (13107895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e82091b52157d2f1c11a0c7fd622d445184d1dc43f4cf1bd4d06f021689b32`  
		Last Modified: Sat, 16 Dec 2023 06:44:01 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda1dfb62366c444703b509894490726c33b9521a7de874eba159c00c39a1607`  
		Last Modified: Sat, 16 Dec 2023 06:44:01 GMT  
		Size: 19.3 KB (19287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e7a9f31999ec86ed6775f052d11e9c5fdfd0006491571d67ce969cc23ce2cd`  
		Last Modified: Sat, 16 Dec 2023 06:44:01 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710ee8b50b6e72d238c55118a5e40365387ef1418b0ca52315a452361592e159`  
		Last Modified: Sat, 16 Dec 2023 10:50:21 GMT  
		Size: 28.6 MB (28623371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b721964a4416dcd65ebbed30c979c8e0ef1d21ae8fc6d378ae146af14321d2a4`  
		Last Modified: Sat, 16 Dec 2023 10:50:20 GMT  
		Size: 4.3 MB (4305241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d85f81e8c48c73b8706388c95eb9e0e07d5523ca611145c4b37766a413d2a4`  
		Last Modified: Sat, 16 Dec 2023 10:50:20 GMT  
		Size: 59.3 KB (59335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35b878d934a3ba2ed371244a7ed1cfff0a8a3de7a4d919d59eedee7dbb004aa`  
		Last Modified: Sat, 16 Dec 2023 10:50:20 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ccb3ebc12fe703a1fec23a6d4c714665090d996101d96e637a291294cab6958`  
		Last Modified: Sat, 16 Dec 2023 10:50:22 GMT  
		Size: 24.3 MB (24306440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb057d56b9911dc4c4a0e7795ec070b7c31fac047d89f37b18f63692589dae96`  
		Last Modified: Sat, 16 Dec 2023 10:50:21 GMT  
		Size: 2.3 KB (2344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d20841b6c16f284b538156caec9cd5406c302ce73cf664d19db001502729af`  
		Last Modified: Sat, 16 Dec 2023 10:50:21 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:3a2473809392a3294910a619ad926666d7e3781b55e7b258fbe94a15a531df77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **909.1 KB (909115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3074ef01e2dd45cc6ba8ec746be66706599552af4c1e882ded3ebc2a68bd3b`

```dockerfile
```

-	Layers:
	-	`sha256:418f9735349d4c4c3855ca175e33ef56e980ffac3c97722ed3b940965621f060`  
		Last Modified: Sat, 16 Dec 2023 10:50:20 GMT  
		Size: 862.8 KB (862849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e2523aa892cc614e9f9bbe1a3e68eb2939805a6c30279b1ed8fafe1aaa0b799`  
		Last Modified: Sat, 16 Dec 2023 10:50:20 GMT  
		Size: 46.3 KB (46266 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.3-fpm-alpine` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:54bb5f3822d18d65513718b75e78536dac0264fca200ec03eda1532a7cc81a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.0 MB (87001897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68ce2b2424e8ef10f982df9385b85bef55379132a86ccf5fd18f6af67449c429`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 06 Dec 2023 20:31:30 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Wed, 06 Dec 2023 20:31:30 GMT
CMD ["/bin/sh"]
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 06 Dec 2023 20:31:30 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Dec 2023 20:31:30 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_VERSION=8.3.0
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.0.tar.xz.asc
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_SHA256=1db84fec57125aa93638b51bb2b15103e12ac196e2f960f0d124275b2687ea54
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 06 Dec 2023 20:31:30 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 06 Dec 2023 20:31:30 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 06 Dec 2023 20:31:30 GMT
RUN docker-php-ext-enable sodium
# Wed, 06 Dec 2023 20:31:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Dec 2023 20:31:30 GMT
WORKDIR /var/www/html
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 06 Dec 2023 20:31:30 GMT
STOPSIGNAL SIGQUIT
# Wed, 06 Dec 2023 20:31:30 GMT
EXPOSE 9000
# Wed, 06 Dec 2023 20:31:30 GMT
CMD ["php-fpm"]
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	version='6.4.2'; 	sha1='d1aedbfea77b243b09e0ab05b100b782497406dd'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
VOLUME [/var/www/html]
# Wed, 06 Dec 2023 20:31:30 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Dec 2023 20:31:30 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b6157a5053a6ba5646a1361153760014335e77813c8792b60d226dedefbb229`  
		Last Modified: Tue, 12 Dec 2023 22:10:24 GMT  
		Size: 2.8 MB (2761045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2682a06d9f91bef66466bcb1b37715dc344282ac9f062ffff8405cf448d71f51`  
		Last Modified: Tue, 12 Dec 2023 22:10:23 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982a61382f7fcec3d428935d516ac99bf603d105e72ebe0c2952b860f329675f`  
		Last Modified: Tue, 12 Dec 2023 22:10:22 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b685965178c3b16eb767adeac66568def914dac6c889e0a31d66eb02614bbcd1`  
		Last Modified: Tue, 12 Dec 2023 22:12:14 GMT  
		Size: 12.5 MB (12452307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac96e1f59001b1557c375aeb6f7585c80fe4b34bbbe8751fe83b065e104e6d07`  
		Last Modified: Tue, 12 Dec 2023 22:12:13 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bac7c86fed5175f393c9e32493ec6d465b289e6ef72cdea947cd3ab6b63c1e1`  
		Last Modified: Sat, 16 Dec 2023 03:34:03 GMT  
		Size: 11.9 MB (11932616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e0a2634b3af2373ce567ece8e01887893b188d96dc37341d7eff0a98593065`  
		Last Modified: Sat, 16 Dec 2023 03:33:59 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92cdd4d97fa83c74a4d8998513d9a42979157d0d8cdd7f12786af279027023dc`  
		Last Modified: Sat, 16 Dec 2023 03:33:59 GMT  
		Size: 19.1 KB (19125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ff816694f8acf076ebe0a4f65ae750852a8fe0a5d86997dbf6ec6c1c5a48be`  
		Last Modified: Sat, 16 Dec 2023 03:33:59 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9458d5650932eb21403892f0e53c29da665211b26e849651866af985d8faaac`  
		Last Modified: Sat, 16 Dec 2023 05:22:02 GMT  
		Size: 28.1 MB (28148216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe861f258166f4aec131363330120e250a0ce7c56fd41f0d11e271e7b7a6ec2`  
		Last Modified: Sat, 16 Dec 2023 05:22:01 GMT  
		Size: 4.1 MB (4139517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b707db8aadb4050b81ae70c0cd56ec9d31899c28edce1960c304a9920313967`  
		Last Modified: Sat, 16 Dec 2023 05:22:00 GMT  
		Size: 59.4 KB (59365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3474631cd0b7439a87700d728b2293708caaa7da2b94d2cc4084310594c51be7`  
		Last Modified: Sat, 16 Dec 2023 05:22:00 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d970fc6754f0f57182ca90c32acb8d9e276a532488968f72dd0119c2b843965e`  
		Last Modified: Sat, 16 Dec 2023 05:22:03 GMT  
		Size: 24.3 MB (24306438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5b202422748b64ed0f56311d48016a0b3be3999c6212b8f724a74d5edc9a96`  
		Last Modified: Sat, 16 Dec 2023 05:22:02 GMT  
		Size: 2.3 KB (2349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e93dee9e11a16e2564413789ff183ba1da8522aa0b218c3569cf73547f7dab`  
		Last Modified: Sat, 16 Dec 2023 05:22:02 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:291575144457218388f5624c7a48bf4edfb84a51fb1f60dd676f7531d1708728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 KB (44548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:086f9b4097e461144b90f0dc4520f574512228407cb46cbbc37108a5cf0a12c1`

```dockerfile
```

-	Layers:
	-	`sha256:fca82b2b7c67ce8bb51dc5de0b915d031df31fe92ed6366ed95f053e8a190e3c`  
		Last Modified: Sat, 16 Dec 2023 05:22:00 GMT  
		Size: 44.5 KB (44548 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.3-fpm-alpine` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:c3466956fbf8450d9fb308720779f04035baed8ce8241633cd077035d3faa877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.3 MB (84341453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea3d5dc0c0654ec15a7f7178b6094d1fcc172f98ef6d6b6f56d36c7a631569c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 06 Dec 2023 20:31:30 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Wed, 06 Dec 2023 20:31:30 GMT
CMD ["/bin/sh"]
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 06 Dec 2023 20:31:30 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Dec 2023 20:31:30 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_VERSION=8.3.0
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.0.tar.xz.asc
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_SHA256=1db84fec57125aa93638b51bb2b15103e12ac196e2f960f0d124275b2687ea54
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 06 Dec 2023 20:31:30 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 06 Dec 2023 20:31:30 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 06 Dec 2023 20:31:30 GMT
RUN docker-php-ext-enable sodium
# Wed, 06 Dec 2023 20:31:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Dec 2023 20:31:30 GMT
WORKDIR /var/www/html
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 06 Dec 2023 20:31:30 GMT
STOPSIGNAL SIGQUIT
# Wed, 06 Dec 2023 20:31:30 GMT
EXPOSE 9000
# Wed, 06 Dec 2023 20:31:30 GMT
CMD ["php-fpm"]
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	version='6.4.2'; 	sha1='d1aedbfea77b243b09e0ab05b100b782497406dd'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
VOLUME [/var/www/html]
# Wed, 06 Dec 2023 20:31:30 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Dec 2023 20:31:30 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:1086c24c41097f090ce847d192c11307e1715eeb563a2cf4f410b2a199ae1942`  
		Last Modified: Fri, 08 Dec 2023 01:57:36 GMT  
		Size: 2.9 MB (2918701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00fcdc554dd7b708317247ba5731b0d76bc06dc68a48af57f662820d33c665cc`  
		Last Modified: Tue, 12 Dec 2023 22:36:17 GMT  
		Size: 2.6 MB (2608664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4717604343f2899832c4417228ef3cdb02080f72378a4152eb72083f09c96e`  
		Last Modified: Tue, 12 Dec 2023 22:36:15 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0a6a05c32e2329e654bc633b417da36b7c74ed6bf626231bf0e900f912838e`  
		Last Modified: Tue, 12 Dec 2023 22:36:15 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ddf5abc1a8a8bb146e597add8c4284e903d7f0a09f00292102e93e0e3fa993a`  
		Last Modified: Tue, 12 Dec 2023 22:38:31 GMT  
		Size: 12.5 MB (12452302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7510df02f5d6b2d77584d0653e06fedb81b8cc5900ab00ca1e5cfd28c27760a9`  
		Last Modified: Tue, 12 Dec 2023 22:38:30 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c04416d8e9f726bc7d07f5af5cfe7d917bd2e372506c34aa12637a2683af63`  
		Last Modified: Sat, 16 Dec 2023 06:14:58 GMT  
		Size: 11.2 MB (11195182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83de61b48566cae932970c454fec73e561cbffe9fa27622efb872112d1d80722`  
		Last Modified: Sat, 16 Dec 2023 06:14:56 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650a09692915f4046425bc4324440184e2d76b0791d16e47442285c19a268003`  
		Last Modified: Sat, 16 Dec 2023 06:14:56 GMT  
		Size: 19.1 KB (19105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7782d57256d2111f03a7e08c6e3a257d7c0c22d4074335143e2fcf7b7712d14`  
		Last Modified: Sat, 16 Dec 2023 06:14:56 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f742270102737319bbc0d489b344f4daa6a22722cb831ad2a650365d98a815e`  
		Last Modified: Sat, 16 Dec 2023 14:13:19 GMT  
		Size: 26.6 MB (26587323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1118fd20b6d7fb8f3d9a6ebb1fe6ebfed6e4104df1cd208ade6d61bc4d2211c`  
		Last Modified: Sat, 16 Dec 2023 14:13:18 GMT  
		Size: 4.2 MB (4176251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5980f9dd0439bc0e3becacb3f2a4978807966e65f32cd6e475284cf33edb747a`  
		Last Modified: Sat, 16 Dec 2023 14:13:18 GMT  
		Size: 59.4 KB (59356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13fb31ebced782aa6f724bad024e41a094ad731e961a12b97f0692b10fcbb43a`  
		Last Modified: Sat, 16 Dec 2023 14:13:18 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de68a8c320c02c7346f55bfcda8838e28c30fa0e6de80c2680719b0483f1174e`  
		Last Modified: Sat, 16 Dec 2023 14:13:20 GMT  
		Size: 24.3 MB (24306447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8ffd30da3c538daf374ccd606f37993196a05bdb9d5ffb6f28e9ce352aa9e0`  
		Last Modified: Sat, 16 Dec 2023 14:13:19 GMT  
		Size: 2.4 KB (2350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a33928bc108a2591c4c5c1901fa7f7564a0fadb1496d0bae657fa4658ae3d20`  
		Last Modified: Sat, 16 Dec 2023 14:13:19 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:0e3048fbd93c79e20d41a40c7defae2729fdbfb5d08aaf10f29fee2a5717b425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **907.6 KB (907647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16e697822529d47a7e14ab075ac8a3ea3de3b398d897865c475b1ca17c04f8df`

```dockerfile
```

-	Layers:
	-	`sha256:6d2be0ba1905bef57593bec2a106ee353853550acf8e62b5dc30f0d8c26e5ffd`  
		Last Modified: Sat, 16 Dec 2023 14:13:17 GMT  
		Size: 862.9 KB (862885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58adc36ce7eb29aa1203606657817629cc91360a19bdb66d561ce1aebbea3096`  
		Last Modified: Sat, 16 Dec 2023 14:13:17 GMT  
		Size: 44.8 KB (44762 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.3-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:85c1062a76be4d6e46da9b30f86edcc1a87cbcab2007493dbc6cb05eba91a1c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.3 MB (89281037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081e1a90237e38aad22d207a8766118598ba35caef89c2e1ff67c96cfb5ec202`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 06 Dec 2023 20:31:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Wed, 06 Dec 2023 20:31:30 GMT
CMD ["/bin/sh"]
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 06 Dec 2023 20:31:30 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Dec 2023 20:31:30 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_VERSION=8.3.0
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.0.tar.xz.asc
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_SHA256=1db84fec57125aa93638b51bb2b15103e12ac196e2f960f0d124275b2687ea54
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 06 Dec 2023 20:31:30 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 06 Dec 2023 20:31:30 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 06 Dec 2023 20:31:30 GMT
RUN docker-php-ext-enable sodium
# Wed, 06 Dec 2023 20:31:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Dec 2023 20:31:30 GMT
WORKDIR /var/www/html
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 06 Dec 2023 20:31:30 GMT
STOPSIGNAL SIGQUIT
# Wed, 06 Dec 2023 20:31:30 GMT
EXPOSE 9000
# Wed, 06 Dec 2023 20:31:30 GMT
CMD ["php-fpm"]
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	version='6.4.2'; 	sha1='d1aedbfea77b243b09e0ab05b100b782497406dd'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
VOLUME [/var/www/html]
# Wed, 06 Dec 2023 20:31:30 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Dec 2023 20:31:30 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a19b0853c69aaf4e0a33f42601f1bddea728304bef39e2fc08f66f3d518576`  
		Last Modified: Tue, 12 Dec 2023 23:00:29 GMT  
		Size: 2.8 MB (2810204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:872ba87116831a71587816ab8564d1a2b7137e1163524eb7e5abf40966e6882c`  
		Last Modified: Tue, 12 Dec 2023 23:00:28 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3a9508fcdd73dc8c678f841adc3269e9919da38f14917ddaa2162b636d4661c`  
		Last Modified: Tue, 12 Dec 2023 23:00:28 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b6d892bc61713316e58b3b40ab8de5a7487c72df7536a64f2243b499b07351`  
		Last Modified: Tue, 12 Dec 2023 23:02:49 GMT  
		Size: 12.5 MB (12452306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07409f498678a1811f0c075d86d88701eff2478c5c034e1bfad340eab4b187f3`  
		Last Modified: Tue, 12 Dec 2023 23:02:48 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095a59aef9b4ec3cfe5b469e729a6584aadd6f46d203ba4a6b84c05a371154ee`  
		Last Modified: Sat, 16 Dec 2023 06:01:59 GMT  
		Size: 13.2 MB (13160035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:459eaf0cc231202617972252bd216fe462fd5ee75885150104c5e468e5be9034`  
		Last Modified: Sat, 16 Dec 2023 06:01:57 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df721df8f93be0c43840ef134bcecb6520415fde9247432846975bec98df854`  
		Last Modified: Sat, 16 Dec 2023 06:01:57 GMT  
		Size: 19.1 KB (19077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1305e49e98faf3e981a64ca56853b7125f54057b289122c184db31931b916c`  
		Last Modified: Sat, 16 Dec 2023 06:01:57 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8830621c0eab1e4d30633e3c6b7c203474144893a885afc9bd046f832475b133`  
		Last Modified: Sat, 16 Dec 2023 21:55:11 GMT  
		Size: 28.8 MB (28765238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e74c3068bff3f3ba1d36ae9b5baefde09af591c8ad0bde0ab091f7606c30cb0`  
		Last Modified: Sat, 16 Dec 2023 21:55:10 GMT  
		Size: 4.3 MB (4342487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e6cc6bd75f01e7874c5f45bd1333273472f9e5d56fada9d1288b53e917499b`  
		Last Modified: Sat, 16 Dec 2023 21:55:10 GMT  
		Size: 59.3 KB (59324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9354fcb42826b72b2f62d0c18d05ebc9d47a83ec2d17d79456ac23b80e56ec8`  
		Last Modified: Sat, 16 Dec 2023 21:55:10 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ebeb8f058d9720116dfa07e5a685872a545ebc60c2de8795c6b569450824a6e`  
		Last Modified: Sat, 16 Dec 2023 21:55:12 GMT  
		Size: 24.3 MB (24306451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25054002910f13c5433e0674271fef4625d362104ee206c9b445693774e1ed63`  
		Last Modified: Sat, 16 Dec 2023 21:55:11 GMT  
		Size: 2.4 KB (2350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e255414ae29dc8aa03febbcaea5cb5dfd36032271cdd63563ea7c693d6c13ae`  
		Last Modified: Sat, 16 Dec 2023 21:55:12 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:8f042027af481b29e08038cfd2336d1fcb3b39e55c57cbb1d41c165027d16093
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **907.5 KB (907511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c3f86e77fb1a52e1e3d79365b3130fb6870b86c9ecdd029553189fc58ab375`

```dockerfile
```

-	Layers:
	-	`sha256:29b7b300c2b592e5688ea2731866d397952ea792acbfc5b237ee08ca59918571`  
		Last Modified: Sat, 16 Dec 2023 21:55:10 GMT  
		Size: 862.9 KB (862860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57c502fb22715c684fbbbdfceaa7bc2b32d39e0d13684bcc6af187fadd032a19`  
		Last Modified: Sat, 16 Dec 2023 21:55:10 GMT  
		Size: 44.7 KB (44651 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.3-fpm-alpine` - linux; 386

```console
$ docker pull wordpress@sha256:2794c6f9cabe28fd852e1a300f2b719c9658047bf156037d47110b095d02bbfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89648529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89da40b206f83179d2eb24a14e391056e3bd731951635c1f9ad780f63c3d0640`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 06 Dec 2023 20:31:30 GMT
ADD file:bd52540f209ba362654d795d7893669c819d35011a16f9f319301727a33b3bd9 in / 
# Wed, 06 Dec 2023 20:31:30 GMT
CMD ["/bin/sh"]
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 06 Dec 2023 20:31:30 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Dec 2023 20:31:30 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_VERSION=8.3.0
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.0.tar.xz.asc
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_SHA256=1db84fec57125aa93638b51bb2b15103e12ac196e2f960f0d124275b2687ea54
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 06 Dec 2023 20:31:30 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 06 Dec 2023 20:31:30 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 06 Dec 2023 20:31:30 GMT
RUN docker-php-ext-enable sodium
# Wed, 06 Dec 2023 20:31:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Dec 2023 20:31:30 GMT
WORKDIR /var/www/html
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 06 Dec 2023 20:31:30 GMT
STOPSIGNAL SIGQUIT
# Wed, 06 Dec 2023 20:31:30 GMT
EXPOSE 9000
# Wed, 06 Dec 2023 20:31:30 GMT
CMD ["php-fpm"]
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	version='6.4.2'; 	sha1='d1aedbfea77b243b09e0ab05b100b782497406dd'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
VOLUME [/var/www/html]
# Wed, 06 Dec 2023 20:31:30 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Dec 2023 20:31:30 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9acd8b4c9d4385585f74dabb4bc6b3351888710ae37ec5dbd9ea950281b8f9bb`  
		Last Modified: Fri, 08 Dec 2023 01:38:43 GMT  
		Size: 3.2 MB (3244115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35c853c51aa63c9f21d6c91fa6948b8160ed6a90764a48e7b1891c38e016590`  
		Last Modified: Wed, 13 Dec 2023 00:34:22 GMT  
		Size: 2.8 MB (2820917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6af7fb9ea0ea850c653027fa7b1b18f1d4c405aade35df3c3ec2151bb8251f`  
		Last Modified: Wed, 13 Dec 2023 00:34:21 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9233674231d3f63e2099e1d4253bf67fd488ef3d4fcd72e3e741ffb7a41f385e`  
		Last Modified: Wed, 13 Dec 2023 00:34:20 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25570a3ea487bec2ff6666f653989c75aebe33565a52454485364190f01703b`  
		Last Modified: Wed, 13 Dec 2023 00:36:56 GMT  
		Size: 12.5 MB (12452294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a1b56cb05998b29c1609da285a926cab06b1e91ec335a18e588621f69bc695`  
		Last Modified: Wed, 13 Dec 2023 00:36:55 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce7f268ab553c70e551c2ecdf3d709f6c7e6decd6690829c726289a6d9637b0`  
		Last Modified: Sat, 16 Dec 2023 10:08:28 GMT  
		Size: 13.4 MB (13431414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efed049382a16265c606ad605d69a0f08980e3a7c8dc2e8728e7dceb3675d36`  
		Last Modified: Sat, 16 Dec 2023 10:08:24 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca0b566edf9d4db1a097001311ec86394df412e65768a60b4807ec19b03e659`  
		Last Modified: Sat, 16 Dec 2023 10:08:24 GMT  
		Size: 19.3 KB (19287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d0e02d153c141785ea8f804903c2324a0e6b1d04f60c12cceccfc5f5dffe3d`  
		Last Modified: Sat, 16 Dec 2023 10:08:24 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df69f5ec355f74df6d6296613bd8792cd9ea5c8189e78e32e45cfbfbbaeca99e`  
		Last Modified: Sat, 16 Dec 2023 21:50:25 GMT  
		Size: 28.9 MB (28858950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bebbb740b1eda4d8dba78598abd0b8393855ad4a22d82d44a584b57bb97d7394`  
		Last Modified: Sat, 16 Dec 2023 21:50:24 GMT  
		Size: 4.4 MB (4437641 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a67d7e6e5ad3f63090790750c4cd0f5d3fe24fa70daec3cb0cbf76fdea72a8`  
		Last Modified: Sat, 16 Dec 2023 21:50:24 GMT  
		Size: 59.4 KB (59350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe751d94c41217182bf484c8c69e42712252e8bb325056073437195d26f8338`  
		Last Modified: Sat, 16 Dec 2023 21:50:24 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6a70a3ebb541c62500a1e1f0380f069d3caa8bd3b9169f9393149e6080729a`  
		Last Modified: Sat, 16 Dec 2023 21:50:26 GMT  
		Size: 24.3 MB (24306447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0118cab128078b48b272e4372907672164a58c6d243168141fe405e28b551ca`  
		Last Modified: Sat, 16 Dec 2023 21:50:25 GMT  
		Size: 2.3 KB (2346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c424818644a261ec77d7496a4f1021aa797fde47535fb7b441dc032b39b6da6`  
		Last Modified: Sat, 16 Dec 2023 21:50:25 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:638710a5c7ef0d0348b7ae0c60200d2f2961fce304f73007e92616c039d35409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 KB (46014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66946d134f5c2e758fd8c596e020c6f68be7deaa00f6fdc903a4f31d2969b9a5`

```dockerfile
```

-	Layers:
	-	`sha256:faec427105318e466a6aec32bc1f65d8ffca36433d1a5c231a53aab763e6112e`  
		Last Modified: Sat, 16 Dec 2023 21:50:24 GMT  
		Size: 46.0 KB (46014 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.3-fpm-alpine` - linux; ppc64le

```console
$ docker pull wordpress@sha256:fca149cb4398855bde321d9789738d0c0ae5dbf1fbfc38847703f5c510cc6dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.5 MB (90484493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32828f3482b70cc8a6c13387b78f272a4d42f7e7ca8330a59ccfa96865d360b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 06 Dec 2023 20:31:30 GMT
ADD file:052421189f8d269382daaaa8beb63c687e4d8ca908c421abdce53bcc627a40b4 in / 
# Wed, 06 Dec 2023 20:31:30 GMT
CMD ["/bin/sh"]
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 06 Dec 2023 20:31:30 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Dec 2023 20:31:30 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_VERSION=8.3.0
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.0.tar.xz.asc
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_SHA256=1db84fec57125aa93638b51bb2b15103e12ac196e2f960f0d124275b2687ea54
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 06 Dec 2023 20:31:30 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 06 Dec 2023 20:31:30 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 06 Dec 2023 20:31:30 GMT
RUN docker-php-ext-enable sodium
# Wed, 06 Dec 2023 20:31:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Dec 2023 20:31:30 GMT
WORKDIR /var/www/html
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 06 Dec 2023 20:31:30 GMT
STOPSIGNAL SIGQUIT
# Wed, 06 Dec 2023 20:31:30 GMT
EXPOSE 9000
# Wed, 06 Dec 2023 20:31:30 GMT
CMD ["php-fpm"]
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	version='6.4.2'; 	sha1='d1aedbfea77b243b09e0ab05b100b782497406dd'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
VOLUME [/var/www/html]
# Wed, 06 Dec 2023 20:31:30 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Dec 2023 20:31:30 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:243ac51c334a47917a84be93e972ee6378987e9b3b917a5a8df29025e161c1f3`  
		Last Modified: Fri, 08 Dec 2023 01:23:14 GMT  
		Size: 3.4 MB (3358233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89935d2f947cbd3585545f82639d347027ef82fbbf413f8684101953ea74bd6`  
		Last Modified: Tue, 12 Dec 2023 22:41:51 GMT  
		Size: 2.8 MB (2838539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b208bea042d5cdcbe6436f88d2f7ea51b03a91df91ae099118f57b644b87bdb2`  
		Last Modified: Tue, 12 Dec 2023 22:41:50 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dcb83a14858379fd485cb474c02417cd209b148b775365e9bae3ab90f5fe798`  
		Last Modified: Tue, 12 Dec 2023 22:41:50 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c56763bbe66e30de393c4bedb62aaa78a18e5159b53a8290a58bef7a2324cf`  
		Last Modified: Tue, 12 Dec 2023 22:44:22 GMT  
		Size: 12.5 MB (12452304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31aa011d78b3813c30fe283ee2bca58e38049e56fde0bece69b861d67aa6edf9`  
		Last Modified: Tue, 12 Dec 2023 22:44:21 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f453576986870dbfc1481650f8c7be77729f2f8e161c1635950af89624f2a6e`  
		Last Modified: Sat, 16 Dec 2023 06:09:40 GMT  
		Size: 13.6 MB (13607444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5318aadcb3f728aa835e67d5cdaacec19a77546813841ba414db90f2c0574a72`  
		Last Modified: Sat, 16 Dec 2023 06:09:37 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493745c72edbf9574c214da9d71c8adfdf12ec488095de9e583e08e019cd86e5`  
		Last Modified: Sat, 16 Dec 2023 06:09:37 GMT  
		Size: 19.1 KB (19101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c01b130ef0a0b31c623ff58ecb2748e13f5e6e59e3e7881a2ebf7fe1897126`  
		Last Modified: Sat, 16 Dec 2023 06:09:37 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1f2afe34553839c4546f7179832fef6664cfcf7e71cf9939abdd3da154cc2b4`  
		Last Modified: Sat, 16 Dec 2023 18:13:57 GMT  
		Size: 29.4 MB (29369457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92897d5649dee8cea74c76d5303616946299b33c22ab252b25fd5aa8e83a7c4`  
		Last Modified: Sat, 16 Dec 2023 18:13:56 GMT  
		Size: 4.5 MB (4455476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69144d0139bef74bcd5b2bc85038154826a91b3d379acfa7b0ce690d60bde26`  
		Last Modified: Sat, 16 Dec 2023 18:13:56 GMT  
		Size: 59.4 KB (59360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204a93e366fd46585d551ec8936cd23baa1796777b2228fce0d5a74b438ec9f6`  
		Last Modified: Sat, 16 Dec 2023 18:13:56 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a91874fa7f33b68f0a4975e537384ae10b04379a09ccbbf2720a4ca39ad0af`  
		Last Modified: Sat, 16 Dec 2023 18:13:58 GMT  
		Size: 24.3 MB (24306452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5962b13871d7bd0d28c67acc0f2452ec3ad32d4ff54c084f85c28f9f43ce59`  
		Last Modified: Sat, 16 Dec 2023 18:13:57 GMT  
		Size: 2.3 KB (2349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93f9ea73ab6668d45d8eea3ad34865f2eccac7be652bfc44f181c932959b5e5c`  
		Last Modified: Sat, 16 Dec 2023 18:13:58 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:b64d9490b472bc05c06ca440293fab4684037524df5db7677e49b83b981494c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **905.9 KB (905934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a82c9719ca0165b356f02ac2e2c3c13db26b9ada1b0e0a08b12bff8b6de266d`

```dockerfile
```

-	Layers:
	-	`sha256:33f7849e1aedf3877f05939ab6a60d84c26c314d5d1411c6d39d0251b030bbf9`  
		Last Modified: Sat, 16 Dec 2023 18:13:56 GMT  
		Size: 861.2 KB (861247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0d4665026e3cf8ca520247a77c6a77b2d4a2672ffba99974d7c05ab4161da4a`  
		Last Modified: Sat, 16 Dec 2023 18:13:56 GMT  
		Size: 44.7 KB (44687 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.3-fpm-alpine` - linux; s390x

```console
$ docker pull wordpress@sha256:5f9422af22520b5c96185a23579ff14d0bdc217f3a046095855ec8b3071af68c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.9 MB (89932061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94765eb8805bc7ad20afcef0eb1768f04852a6546a2eb4149766c7c057762410`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 06 Dec 2023 20:31:30 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
# Wed, 06 Dec 2023 20:31:30 GMT
CMD ["/bin/sh"]
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 06 Dec 2023 20:31:30 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Dec 2023 20:31:30 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_VERSION=8.3.0
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.0.tar.xz.asc
# Wed, 06 Dec 2023 20:31:30 GMT
ENV PHP_SHA256=1db84fec57125aa93638b51bb2b15103e12ac196e2f960f0d124275b2687ea54
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 06 Dec 2023 20:31:30 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 06 Dec 2023 20:31:30 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 06 Dec 2023 20:31:30 GMT
RUN docker-php-ext-enable sodium
# Wed, 06 Dec 2023 20:31:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Dec 2023 20:31:30 GMT
WORKDIR /var/www/html
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 06 Dec 2023 20:31:30 GMT
STOPSIGNAL SIGQUIT
# Wed, 06 Dec 2023 20:31:30 GMT
EXPOSE 9000
# Wed, 06 Dec 2023 20:31:30 GMT
CMD ["php-fpm"]
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
RUN set -eux; 	version='6.4.2'; 	sha1='d1aedbfea77b243b09e0ab05b100b782497406dd'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
VOLUME [/var/www/html]
# Wed, 06 Dec 2023 20:31:30 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 06 Dec 2023 20:31:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Dec 2023 20:31:30 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0180a7268e169fa6dd82fc04f9270dbd4fe716cf09b03fc82f84618025bad4`  
		Last Modified: Tue, 12 Dec 2023 22:07:16 GMT  
		Size: 2.9 MB (2937974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ecaefbf268f4b1e4d9f16c5d67523f3b76e72db0c3fc7a2f3fb6fd7fbdec547`  
		Last Modified: Tue, 12 Dec 2023 22:07:16 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f0d18e8f1067fcb105dea2ad180f140d138c6d99310025696d1aaa322017db`  
		Last Modified: Tue, 12 Dec 2023 22:07:16 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29229bf842a35e0f2fbaaf7d4ac99a03cd25e73c3d1e2b3cf7c9faa421594fe1`  
		Last Modified: Tue, 12 Dec 2023 22:09:01 GMT  
		Size: 12.5 MB (12452312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda911fba6baa41094156504359c3aa5e605ccda6527ca1c026c16b7f6e069fd`  
		Last Modified: Tue, 12 Dec 2023 22:09:01 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c9e6d6b9e172da545a74dfe0d686e1dc275b8939e8feab16aa8be9fd1b305b`  
		Last Modified: Sat, 16 Dec 2023 04:55:02 GMT  
		Size: 12.9 MB (12852088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43ae3bbe78b821f53de07d54e6432ba5ef1c9c7dc4358464f6641b36d2fe8773`  
		Last Modified: Sat, 16 Dec 2023 04:55:00 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eec3f8515cf254e2f4bd5e8131cd4f7f92438c87e4b3250bbd1bec7c38cdea2`  
		Last Modified: Sat, 16 Dec 2023 04:55:00 GMT  
		Size: 19.1 KB (19099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f15e73d741b0e2aebd2e2d9b627404a11e13f3a28666196b9cc06362ac018f69`  
		Last Modified: Sat, 16 Dec 2023 04:55:00 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ea21bd59a39dbaf911b1ceb19c5a67b322b17a3e681a94a13d385eb73a096a`  
		Last Modified: Sat, 16 Dec 2023 14:08:46 GMT  
		Size: 29.6 MB (29613837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef8d01a432eded89af67f357d5f513f0c72f1be657b7ff3abedf7115249c44d`  
		Last Modified: Sat, 16 Dec 2023 14:08:46 GMT  
		Size: 4.4 MB (4430489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ab8f63414286299d1e33d53b441e9c9d85eac70afd1bec1bdc082c85ad1c98`  
		Last Modified: Sat, 16 Dec 2023 14:08:45 GMT  
		Size: 59.4 KB (59370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:565ec92b4759cb45a91396ab10035fe9752ca0603593e852846b526c6a86c35c`  
		Last Modified: Sat, 16 Dec 2023 14:08:45 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5bc14fa9d222eba2265a71a8f88ed07bf6aee62b673d56125765ab0fc223bf`  
		Last Modified: Sat, 16 Dec 2023 14:08:47 GMT  
		Size: 24.3 MB (24306442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:472c3c2c54cc42e1d5a755dd9a376e9931927f30dec1ea0820e51bbc2672abbd`  
		Last Modified: Sat, 16 Dec 2023 14:08:46 GMT  
		Size: 2.4 KB (2350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c825800467b5a19a8320277940180cd385e5db2d039b214d61f5483f336e4c`  
		Last Modified: Sat, 16 Dec 2023 14:08:47 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:0863a824af149eda8fa732b850b290c970d89d6ee2723f6fbc66e03f9050a6d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **905.9 KB (905854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8066d8a92935a6693af558c9fe83a6a69ca2c0e3be29b376abaac98ffee7f305`

```dockerfile
```

-	Layers:
	-	`sha256:c775d00a89082981201ccd5d34fff66e2d61536ff551a03d8c222146035e026b`  
		Last Modified: Sat, 16 Dec 2023 14:08:45 GMT  
		Size: 861.2 KB (861213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a353288e37b034548e2bfd3d24ed7a40f360876edf5d5b413bf7947ad64e8f15`  
		Last Modified: Sat, 16 Dec 2023 14:08:45 GMT  
		Size: 44.6 KB (44641 bytes)  
		MIME: application/vnd.in-toto+json
