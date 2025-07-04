## `wordpress:php8.3-fpm-alpine`

```console
$ docker pull wordpress@sha256:11ffaa876d4714283677e7406fff146f4209bc8a444cf3f397b9ca671ff5441f
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

### `wordpress:php8.3-fpm-alpine` - linux; amd64

```console
$ docker pull wordpress@sha256:ea6ee6df3b59f5464c7b51499fc7585c37fe1303308d8ceff0e750430fb63394
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.1 MB (100116694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:957dac9012711b9b4bb4e931418e936465364e14deedc620b94ce940c6922430`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 09 Jun 2025 23:45:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 09 Jun 2025 23:45:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_VERSION=8.3.23
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 09 Jun 2025 23:45:55 GMT
WORKDIR /var/www/html
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
STOPSIGNAL SIGQUIT
# Mon, 09 Jun 2025 23:45:55 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 09 Jun 2025 23:45:55 GMT
CMD ["php-fpm"]
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	version='6.8.1'; 	sha1='52d5f05c96a9155f78ed84700264307e5dea14b4'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
VOLUME [/var/www/html]
# Mon, 09 Jun 2025 23:45:55 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jun 2025 23:45:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef952cbf360f9accebc7c2beaa1888046fd2decdb103e9cb37ca7fe8901e8448`  
		Last Modified: Thu, 03 Jul 2025 23:05:43 GMT  
		Size: 5.9 MB (5944405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb247df7bed499a5b20b7a8f5275f005942ae29ff269444f08485852b0a82ba`  
		Last Modified: Thu, 03 Jul 2025 23:05:43 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b896673d396d677374e76584f6148d05009f4bf9cb800ff16ece4e2b1cf7f785`  
		Last Modified: Thu, 03 Jul 2025 23:05:42 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b045c0c09a16557279905f885315501ebc707dad24429e3f76c4ba889eaea8`  
		Last Modified: Thu, 03 Jul 2025 23:05:43 GMT  
		Size: 12.6 MB (12599155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0c8125335db3c68c8f6abc01bbf84258e57476bb185eff879d4c1a3466b8eb`  
		Last Modified: Thu, 03 Jul 2025 23:05:42 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63d7dbac9207c1e11b7b23ce6aad0740e3ba427719588e966776cc44421a861`  
		Last Modified: Thu, 03 Jul 2025 23:05:44 GMT  
		Size: 13.3 MB (13261724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ac6221624b83e2f407497538d9cda65f3c6bb6028088b26532eb138997df78`  
		Last Modified: Thu, 03 Jul 2025 23:05:42 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80922a9956d152b4e0a3bc8fd473151f805337d5823f8bd37b68e79cdb206f7e`  
		Last Modified: Thu, 03 Jul 2025 23:05:42 GMT  
		Size: 20.2 KB (20208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26906d4e70978b9475681f326ed2a302b23ae885e81ae8770bb41a1c51135f3c`  
		Last Modified: Thu, 03 Jul 2025 23:05:42 GMT  
		Size: 20.2 KB (20204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4226ad16511c854708eeb106b22f950a04e5db658db5aee0703cfdc687c5a9dd`  
		Last Modified: Thu, 03 Jul 2025 23:05:43 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:438bad1877a371a3136e995b7687a758d7ce05168b2c5123432e78fc9fe132d7`  
		Last Modified: Thu, 03 Jul 2025 23:13:02 GMT  
		Size: 28.3 MB (28272553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11010cecd477019755a4a6e6a2e44d46a3408f0ea7b5483c171a074ccd8f0244`  
		Last Modified: Thu, 03 Jul 2025 23:13:02 GMT  
		Size: 9.2 MB (9225959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ab184feadc7d00be208fb459ecc38ad372550c08bfb9d3d0ba50ee21432037`  
		Last Modified: Thu, 03 Jul 2025 23:13:01 GMT  
		Size: 62.6 KB (62564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d94ba733b7f35e2d606725dce87368efce60120f05a82d727ddb58485823df20`  
		Last Modified: Thu, 03 Jul 2025 23:13:00 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb42ad4190660c8d42542f3f67dc535ce078382eabf6154ad86ad17e64035eb`  
		Last Modified: Thu, 03 Jul 2025 23:13:02 GMT  
		Size: 26.9 MB (26895006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb0a7d1b1d4ccffd56a6f46c95486e69f0acc0bc4650d703f2363eeaf09327f`  
		Last Modified: Thu, 03 Jul 2025 23:13:00 GMT  
		Size: 2.4 KB (2433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3614f83bdc6af81c7208823d7c89a0f3b2abd4f087884b513c1c661998c26d1e`  
		Last Modified: Thu, 03 Jul 2025 23:13:00 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a402e23ae3c5dee42b229efe6d2eb0986675a2e5d10a04c4172c49088f954d`  
		Last Modified: Thu, 03 Jul 2025 23:13:00 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:5346dcc3d74010e2c64e9dcad4e4ef5585e562aae9382995e90f3c15dd86b7cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1133927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bddd255ca0d0dd378ef93208e37c299756b5003c05a85a917bc0ffc5b94b6b44`

```dockerfile
```

-	Layers:
	-	`sha256:09a5d1ff9b6e17a0bd2bb887c0037ca4aeaf0de2c6c0e8acbf0895ca66bbb6ca`  
		Last Modified: Fri, 04 Jul 2025 01:13:50 GMT  
		Size: 1.1 MB (1082201 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0afad7177d0c965bc84702e359d59e4a2363f8c77538b8c82d7d9b0a4f301514`  
		Last Modified: Fri, 04 Jul 2025 01:13:50 GMT  
		Size: 51.7 KB (51726 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.3-fpm-alpine` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:4444b3c0cbebacd13275fcadeacb61b174752ae91ded2d4ca59ba8417db3c8e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93674755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c3619421ba9422b5567b1cf164a5e90b7af4a9aa90248c6e403246517a7f935`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 09 Jun 2025 23:45:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 09 Jun 2025 23:45:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_VERSION=8.3.23
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 09 Jun 2025 23:45:55 GMT
WORKDIR /var/www/html
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
STOPSIGNAL SIGQUIT
# Mon, 09 Jun 2025 23:45:55 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 09 Jun 2025 23:45:55 GMT
CMD ["php-fpm"]
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	version='6.8.1'; 	sha1='52d5f05c96a9155f78ed84700264307e5dea14b4'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
VOLUME [/var/www/html]
# Mon, 09 Jun 2025 23:45:55 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jun 2025 23:45:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b2fddcddb67f07dabc88b449999588f7b51998c1114a9e3f0ae4ad9519b41e`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 3.4 MB (3432459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f159e81bd801861164e94e01093125bcc7ed5b9fb65bed9a9f3ce4d3a707c8c`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045dfb1ee98b64d4099b6b9d91bdb57fab7a640182f195075c814d3071429a5b`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6146672ba2c374cbf86842c858594d7c0b44ab2080ad5e2ec35b1d430d956546`  
		Last Modified: Thu, 03 Jul 2025 23:34:21 GMT  
		Size: 12.6 MB (12599121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21fb5f1af16a6958fa9af152ac28632aff56dd315585de1020a729fb999c3dee`  
		Last Modified: Thu, 03 Jul 2025 23:34:19 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3d236cf740ccc769ceb4ead8aa9d45e86ed16335a52d930c4fe0a9c0557f9f`  
		Last Modified: Thu, 03 Jul 2025 23:39:44 GMT  
		Size: 15.1 MB (15107434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f14679d7fe0b4602f2402b4899b623f618df96d2ba33280d5cf4a4afc825bb7`  
		Last Modified: Thu, 03 Jul 2025 23:39:42 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd7a906289e5476e4a4fbca6e72f2a28c1274a886810de274c3d9d075537bdba`  
		Last Modified: Thu, 03 Jul 2025 23:39:43 GMT  
		Size: 20.0 KB (19996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab072a5208326c03096cd254e9205b7fd25f2fe20d9e8723ba9f85b55faab72`  
		Last Modified: Thu, 03 Jul 2025 23:39:42 GMT  
		Size: 20.0 KB (19996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a1a3d59f66b3f5f865439aa342092b634c80b67cc2b0976838e9806ffba9bd8`  
		Last Modified: Thu, 03 Jul 2025 23:39:44 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9164637014765c3a0db3f6d00159cb4472f322069c2873f124e8f397d7267180`  
		Last Modified: Fri, 04 Jul 2025 00:55:31 GMT  
		Size: 24.4 MB (24359738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37cc533991a4c45fff916a31e4fc81c9faa833e9790a45ff29d6510b97aa9a3a`  
		Last Modified: Fri, 04 Jul 2025 00:55:31 GMT  
		Size: 7.7 MB (7659416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3040be3c48f6a20d21b0aecfab3d45859b01b0c2374a59dbe1e55c50e4acfa29`  
		Last Modified: Fri, 04 Jul 2025 00:55:30 GMT  
		Size: 62.6 KB (62551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b22e1a5f6ac29a3701b6339dc3e154ac5a2597dfd3fb005a1fb9b53a8c3b5c6`  
		Last Modified: Fri, 04 Jul 2025 00:55:30 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:006d6773ecf06ca40da00b08809e2dc59005279714934d8ef937202b80629176`  
		Last Modified: Fri, 04 Jul 2025 00:55:31 GMT  
		Size: 26.9 MB (26895018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c0cbff72d95395026e4c5d95980543ae60de6c361f6b40c155767dc2eb84a65`  
		Last Modified: Fri, 04 Jul 2025 00:55:30 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bccdaf5f20ded7a9240f1670fd9902d83d8adbeb9d85da922b60b681c272ec0`  
		Last Modified: Fri, 04 Jul 2025 00:55:30 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762f6a0ecf26fc8577229788e52fe8944260b856aca63038aeb57385a68c78da`  
		Last Modified: Fri, 04 Jul 2025 00:55:30 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:9f8ce7595b4b6226b882db54c1a5a2c54e7df881adf9e8d1027487a66fbbfab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 KB (51653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c1b0ce61baa16728f2c528e84a29628e06f36a487eca58500a123547b90c31f`

```dockerfile
```

-	Layers:
	-	`sha256:2689c1f86efd3feea954b4abb2129e8f66c0943ae4fbf471ea72d7e29096e633`  
		Last Modified: Fri, 04 Jul 2025 01:13:54 GMT  
		Size: 51.7 KB (51653 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.3-fpm-alpine` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:599aa89bd311825b863e6fa40eeeb9d6cfdc2941faa89d63bef8f4be2a02f72c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 MB (92161589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:696f828fa549a9f810dcad5e9a721ecfae9692b2351ec3686eb545c84d47c839`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 09 Jun 2025 23:45:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 09 Jun 2025 23:45:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_VERSION=8.3.23
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 09 Jun 2025 23:45:55 GMT
WORKDIR /var/www/html
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
STOPSIGNAL SIGQUIT
# Mon, 09 Jun 2025 23:45:55 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 09 Jun 2025 23:45:55 GMT
CMD ["php-fpm"]
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	version='6.8.1'; 	sha1='52d5f05c96a9155f78ed84700264307e5dea14b4'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
VOLUME [/var/www/html]
# Mon, 09 Jun 2025 23:45:55 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jun 2025 23:45:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec113fe1f048c8128d671c69cfadec1876ed37d14a445b7755326cbfa9acee36`  
		Last Modified: Wed, 11 Jun 2025 11:39:14 GMT  
		Size: 3.2 MB (3247470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3d974efcf5fd7ed95cd66bd2537770b4f31b8d7af064ae6e9119868bac3309`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29a62342af1e9fd2e1392885a9e1a9439cdee5d849c8f557fb8693b5650363b`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10b98e00e904012800430f69cf8aa74332ce1ebba99fec9635378d4af95147c`  
		Last Modified: Fri, 04 Jul 2025 00:56:41 GMT  
		Size: 12.6 MB (12599135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2f60ea7cbd06e3b78423de30e2481ff24a10dc4900a14d875723aad2768ad1`  
		Last Modified: Fri, 04 Jul 2025 00:56:39 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb773ed9018828b3805869de0c29dadb3d8afe8bbeb5822a9bff92c509f1546`  
		Last Modified: Fri, 04 Jul 2025 01:00:37 GMT  
		Size: 14.2 MB (14183204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a190e2dc48065b7d79d07964079aaae471c5266f4ff8a5b4a74844f8c4ab4873`  
		Last Modified: Fri, 04 Jul 2025 01:00:34 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:232d95fcde3e122763b3e8cf8c659f3cd57854c41b3dcfa893ff0c0154ae3cc7`  
		Last Modified: Fri, 04 Jul 2025 01:00:35 GMT  
		Size: 20.0 KB (19994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05cb02f2dc6fc67eb54948f0631c60eb801811b049464f631461da3fe4d7b8b0`  
		Last Modified: Fri, 04 Jul 2025 01:00:36 GMT  
		Size: 20.0 KB (19990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2ae500fa45bd59acbd59702482718a33f1d4d98384e11ef6d394ccf019f51a`  
		Last Modified: Fri, 04 Jul 2025 01:00:36 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f262d951c4899803a06d020df7deae6fca9840667987d610e8fc8716085ea0`  
		Last Modified: Fri, 04 Jul 2025 03:08:45 GMT  
		Size: 23.1 MB (23137814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf6ccf54bd26ff29b9efab2a541a12dfb14bf559624d26dd8bfda96952cb651`  
		Last Modified: Fri, 04 Jul 2025 03:08:43 GMT  
		Size: 8.8 MB (8759185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ae4342c39db612079aa25b13c0094efb746bcdbed23b8feb7f9ec1db9a86cc`  
		Last Modified: Fri, 04 Jul 2025 03:08:43 GMT  
		Size: 62.5 KB (62518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a1f30c0d802aac86fe8fdf06dd446b4e8872f4a00ab0934c9bb450f1d7520e`  
		Last Modified: Fri, 04 Jul 2025 03:08:43 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea9bd4cdf21ef095ada4f767fab4f57debcb23b7ec422e693409d08c297d4d28`  
		Last Modified: Fri, 04 Jul 2025 03:08:44 GMT  
		Size: 26.9 MB (26895008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b788a0adfe59b25753c054e45a0a6b30ae95b06d84de0a25ac2e342bc32118`  
		Last Modified: Fri, 04 Jul 2025 03:08:43 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2dc7530194b51bd3f0602c31774b0b8bc6312eca31702d2506f82382dcb2c49`  
		Last Modified: Fri, 04 Jul 2025 03:08:43 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435bcaf17068ce865844d271dfb43d7d7bf7b5bd61e9fd73e1a1f5532cb90dba`  
		Last Modified: Fri, 04 Jul 2025 03:08:43 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:a33f6293e53d2fc446a8c6d059aab84af12ed014838bb07212d67d4d61a87b57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1132861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0a758605e7853a0582ebcfbcbef86b1def9dd4a2eb668c2bc4d22a670fc1227`

```dockerfile
```

-	Layers:
	-	`sha256:3c49c352bc28b22f4856892820f797ebdaf183fc0aae1677c711514be425b7b9`  
		Last Modified: Fri, 04 Jul 2025 04:16:50 GMT  
		Size: 1.1 MB (1080993 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93a8316e137be20952f67becc4dcce58b5f2b7a6795d057459e646ded365d625`  
		Last Modified: Fri, 04 Jul 2025 04:16:51 GMT  
		Size: 51.9 KB (51868 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.3-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:e1f43766c560b81d7580f3f55a349485f9335664a8f5404d3b634239c5ada7c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.7 MB (100718848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f7e78f943b7365bf368e8a04daa3947109b4025cce68697531ab3dfd0389e68`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 09 Jun 2025 23:45:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 09 Jun 2025 23:45:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_VERSION=8.3.23
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 09 Jun 2025 23:45:55 GMT
WORKDIR /var/www/html
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
STOPSIGNAL SIGQUIT
# Mon, 09 Jun 2025 23:45:55 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 09 Jun 2025 23:45:55 GMT
CMD ["php-fpm"]
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	version='6.8.1'; 	sha1='52d5f05c96a9155f78ed84700264307e5dea14b4'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
VOLUME [/var/www/html]
# Mon, 09 Jun 2025 23:45:55 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jun 2025 23:45:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73985aec8f2b878dbb559825b96bc42ecedc3f93d14e5f1b9a6ca2e1816299c`  
		Last Modified: Thu, 03 Jul 2025 23:26:01 GMT  
		Size: 6.2 MB (6231904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2edf112b2c5bea025053bf307e764ef87252d3b53a912374edb00c6b9cda47`  
		Last Modified: Thu, 03 Jul 2025 23:26:00 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106cb39859ac9004e783043bb75563ecfc6db5970ab2b1965a10cfec3c797d10`  
		Last Modified: Thu, 03 Jul 2025 23:26:00 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c1dc6ad948ff6b6024c13aeb8e1504ab7c78c613d2c0c92070d4d25d125ea3`  
		Last Modified: Fri, 04 Jul 2025 00:22:31 GMT  
		Size: 12.6 MB (12599144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f819ea982f77ab1a8ba8076019600ba3f9145ff91f7458fb0dcf5614950956`  
		Last Modified: Fri, 04 Jul 2025 00:22:29 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37d5631afd1425fe5eb2c8e749a3c65200e29d24c36d318080ca48b2cd90c53`  
		Last Modified: Fri, 04 Jul 2025 00:27:41 GMT  
		Size: 13.2 MB (13248864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c934bc624a617ff8f7747e6413a288c2e89d5b658c0f017d2ea39ba3f3c409a0`  
		Last Modified: Fri, 04 Jul 2025 00:27:39 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba469df90540c13439c3903a06bc064d1b88891a0ac0890503f07e7e9392d5be`  
		Last Modified: Fri, 04 Jul 2025 00:27:39 GMT  
		Size: 20.0 KB (20005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d902dfe696ab15d26a6522405d9b7fd7cc42fd2a15a790f9700e3a1b3344207`  
		Last Modified: Fri, 04 Jul 2025 00:27:40 GMT  
		Size: 20.0 KB (19995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d77b378ed1259e9def290ea50e62e695383be8cb81433a8155ef802d3ebf414`  
		Last Modified: Fri, 04 Jul 2025 00:27:39 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f97ecbab12ee67762c1cb757a1d39fa49f2527a200a692405f2974e57cd021e`  
		Last Modified: Fri, 04 Jul 2025 03:45:53 GMT  
		Size: 28.1 MB (28082061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27ea9a647f4fa785de9e79838ffb3e2918a510189813f585921f536fa254aa0a`  
		Last Modified: Fri, 04 Jul 2025 03:45:51 GMT  
		Size: 9.4 MB (9405261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b42b1fe1789800c48cd6c285dd4adfe04cfe8cca9a73fd8fa6a863a09f8a60`  
		Last Modified: Fri, 04 Jul 2025 03:45:50 GMT  
		Size: 62.6 KB (62565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc13e0c2e2276ce193a5df4c138399a14eb28976137f15da72e39d4f957644b`  
		Last Modified: Fri, 04 Jul 2025 03:45:50 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab0cc446293b399af4febc937f9b4c68c11092d0939aebc8e7ce449cb3ac439`  
		Last Modified: Fri, 04 Jul 2025 03:45:53 GMT  
		Size: 26.9 MB (26895026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2757c6a536a16f7891dbe47eb397a4153bf94875dc3877aeb8878160be356e2f`  
		Last Modified: Fri, 04 Jul 2025 03:45:50 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56420abf00b78dc9638b124b184ebed4eb20f91fd16f3f3be949968c10ba931`  
		Last Modified: Fri, 04 Jul 2025 03:45:50 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:632fd8e53905c282a4c5b8daf2857d31b0fc5b199e1b7f3843c804217b3ef740`  
		Last Modified: Fri, 04 Jul 2025 03:45:50 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:7d01e36987dea7a022824ab242be251db0f94cd5dfdc8b8624be7a3941f4fed3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1132919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79d17c3e1254762954e44b4b7720142b8c96344e1c9208e36557db768941a502`

```dockerfile
```

-	Layers:
	-	`sha256:243246fd36142a307c789f878dbffe5af7dcacc696ca1da8f03f4b175e28678f`  
		Last Modified: Fri, 04 Jul 2025 04:16:55 GMT  
		Size: 1.1 MB (1081013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:620403e1c11e3f65788f2e5cea31b248602783a1364861519f0bd16491fbb76d`  
		Last Modified: Fri, 04 Jul 2025 04:16:55 GMT  
		Size: 51.9 KB (51906 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.3-fpm-alpine` - linux; 386

```console
$ docker pull wordpress@sha256:d3f3a3b2d2f2970547ed9e27cea81708a6e0b80cf02c38d75300bf64bcd9b07a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.2 MB (99159175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff420a0b1f1306f86ca23300e6272d98f2d867256c194b406cc2e68d8a9767db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 09 Jun 2025 23:45:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 09 Jun 2025 23:45:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_VERSION=8.3.23
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 09 Jun 2025 23:45:55 GMT
WORKDIR /var/www/html
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
STOPSIGNAL SIGQUIT
# Mon, 09 Jun 2025 23:45:55 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 09 Jun 2025 23:45:55 GMT
CMD ["php-fpm"]
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	version='6.8.1'; 	sha1='52d5f05c96a9155f78ed84700264307e5dea14b4'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
VOLUME [/var/www/html]
# Mon, 09 Jun 2025 23:45:55 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jun 2025 23:45:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8807332f552a5d43d50bf321942aaff6f62a51ea718c4bc5c92889c7da5518cc`  
		Last Modified: Thu, 03 Jul 2025 23:05:46 GMT  
		Size: 5.8 MB (5806969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5952ed3b34bc2bb95e5d92041b0d1e2f1102370e20445fde4e6ae170753fd54f`  
		Last Modified: Thu, 03 Jul 2025 23:05:45 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d26cd4edff9c58bc8c1207c850646d9dfdfc9668c692e2b02ccedbcd463e458`  
		Last Modified: Thu, 03 Jul 2025 23:05:45 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d3b172088b57748f502c5aa1cb684e21421b0497fea01813cd1a37fc90acd2`  
		Last Modified: Thu, 03 Jul 2025 23:05:46 GMT  
		Size: 12.6 MB (12599126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f0cd325f2b5b783c7b8a674f750116f3312bd602ddc978c5b9f679705430ed`  
		Last Modified: Thu, 03 Jul 2025 23:05:45 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337a1d58746e581f9623e1af350bf3217a46d1bf2421a049c667ce7611ed9234`  
		Last Modified: Thu, 03 Jul 2025 23:05:47 GMT  
		Size: 13.6 MB (13572591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86069b8c031ffbd54f99dcbf2ae53e9e0957fc9842ceeaa4a5c8036b2f82643`  
		Last Modified: Thu, 03 Jul 2025 23:05:45 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aef072b2e721a30c9933cc7e4efd20c954bbd7be2cf4635995276b751a09425`  
		Last Modified: Thu, 03 Jul 2025 23:05:45 GMT  
		Size: 20.2 KB (20198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959b7b0119a26af8eff640f542e3e4ca243bddb6c7bffcb62f9018e53e27a28d`  
		Last Modified: Thu, 03 Jul 2025 23:05:45 GMT  
		Size: 20.2 KB (20191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64bce8958e293647dbc8485a223c57de84e18b7d627799a89f7217e466b8dc86`  
		Last Modified: Thu, 03 Jul 2025 23:05:46 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2004ff2858197efdf865e6afac9368639718971cd53936bd54f94cd9fa293cdb`  
		Last Modified: Thu, 03 Jul 2025 23:13:14 GMT  
		Size: 28.5 MB (28487039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e26987cb31be71eb1118a2da291e2eb95c316f74733321aa488eebaf1ddab4`  
		Last Modified: Thu, 03 Jul 2025 23:13:12 GMT  
		Size: 8.1 MB (8061432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86fe17fe34bfbce5ecc7713b03d00a943011eb5727728070cca8efaf98262a5f`  
		Last Modified: Thu, 03 Jul 2025 23:13:12 GMT  
		Size: 62.5 KB (62519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3188992da641ad60ba3118506515a6365490478f6ad43d6f34695e8c60367c`  
		Last Modified: Thu, 03 Jul 2025 23:13:12 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b38a279d7e46572cd00be810817d9d118cece4e79574dda92089c9aca58026`  
		Last Modified: Thu, 03 Jul 2025 23:13:13 GMT  
		Size: 26.9 MB (26895016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255bfbd8e0566a93a823055c844e22023fdc3e30346f1f015fefb419100aca9a`  
		Last Modified: Thu, 03 Jul 2025 23:13:12 GMT  
		Size: 2.4 KB (2434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae0c3a03d4cc5b7698f71db28ee3b2bb2fb6e159bf77c03abf276bedcdfe8ca`  
		Last Modified: Thu, 03 Jul 2025 23:13:12 GMT  
		Size: 1.8 KB (1759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4743a753bcc59272626b7c6ee7f1ebe7c4b4cf57d940b8ba0f6d8a2c854cce4d`  
		Last Modified: Thu, 03 Jul 2025 23:13:12 GMT  
		Size: 191.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:f23e3288d41d78a026241662b4749390c26167203076a974c985b15adb4f2b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1133861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a882a7826992f7ff9a7ebb7858960e3e56a6a15e57ef341cfe74d1ecd9efe9d`

```dockerfile
```

-	Layers:
	-	`sha256:e32a69205817d25301fbdacc31c1cf24543743c931fbf8adeba9346cca241b9c`  
		Last Modified: Fri, 04 Jul 2025 01:14:06 GMT  
		Size: 1.1 MB (1082176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e28aa416cae03605b45984de5f6b61b5d4a1ad36764f4d8cf3ff341a966b2b6`  
		Last Modified: Fri, 04 Jul 2025 01:14:07 GMT  
		Size: 51.7 KB (51685 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.3-fpm-alpine` - linux; ppc64le

```console
$ docker pull wordpress@sha256:2feaddb3292ddd8c4915a915368365328d0e71c06abf376e54857eb1f54affe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.9 MB (100911239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b403efd9cb1771e4e45632645e6423cd2ec5a7c098d1d521faa78f077ed4e705`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 09 Jun 2025 23:45:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 09 Jun 2025 23:45:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_VERSION=8.3.23
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 09 Jun 2025 23:45:55 GMT
WORKDIR /var/www/html
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
STOPSIGNAL SIGQUIT
# Mon, 09 Jun 2025 23:45:55 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 09 Jun 2025 23:45:55 GMT
CMD ["php-fpm"]
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	version='6.8.1'; 	sha1='52d5f05c96a9155f78ed84700264307e5dea14b4'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
VOLUME [/var/www/html]
# Mon, 09 Jun 2025 23:45:55 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jun 2025 23:45:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7db3af28cc31124a8bce98c13cd1b2512963d13f437d0d67f9918df0d57d2b`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 5.9 MB (5946924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ec39d79edfa484fac002ed8c640f17ae8077df4dce88811d8d186865593a6b`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 939.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2995d4272705fc452f2b3ea9e2d118681efbad9f858c7743f6f69364d73a50`  
		Last Modified: Thu, 03 Jul 2025 23:15:35 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2daa18a322ff81fffc7ceb1c57d422d1adf54055433564c7dc442f903760a8f1`  
		Last Modified: Thu, 03 Jul 2025 23:54:52 GMT  
		Size: 12.6 MB (12599136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b3f6203202b10d68495a456bb29733beccaa33785d2412fb041f620278679d`  
		Last Modified: Thu, 03 Jul 2025 23:54:51 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e866d6eb8c3a035680c0d3efabfbca205989bcd4bee91b8a71c55a705ce9184`  
		Last Modified: Thu, 03 Jul 2025 23:58:30 GMT  
		Size: 13.7 MB (13732933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531b83a89125d0ee7a5f425580e0142fe836b2078ec7b9b0a04717c2d8c675b6`  
		Last Modified: Thu, 03 Jul 2025 23:58:28 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a316ae9dff514804b8e62c75c316fc9f7a2a98cdcf43b08a879887c8865e8d2`  
		Last Modified: Thu, 03 Jul 2025 23:58:28 GMT  
		Size: 20.0 KB (20007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5068cb2008a5c83784fe82cf109b583e810ad10f6cf9461dba75b4bc3693fdfd`  
		Last Modified: Thu, 03 Jul 2025 23:58:28 GMT  
		Size: 20.0 KB (20001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abe3a1077df05c4646ceddd1e7ac63a985083bf3e92537bbb928a3367fb9045a`  
		Last Modified: Thu, 03 Jul 2025 23:58:28 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:991b3f4ca6e4eeb544aae25b0da78cc053d114b089348e14d5ebc7a5815b8e32`  
		Last Modified: Fri, 04 Jul 2025 02:03:39 GMT  
		Size: 28.9 MB (28916020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcad041241e1d9f1ab559e1aa4df8d62d75eaa4318cd25737654891b94a71c7e`  
		Last Modified: Fri, 04 Jul 2025 02:03:37 GMT  
		Size: 9.0 MB (8970383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d9bbb1c10d400ec39e5045cd368d697261cf75ca39669971de1f499ce2af57c`  
		Last Modified: Fri, 04 Jul 2025 02:03:34 GMT  
		Size: 62.6 KB (62556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d2ff3abc93a00f875b35621a8ece7431e893b8801f096a307582ed9edfb94d`  
		Last Modified: Fri, 04 Jul 2025 02:03:35 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbbbfcc8d1994b6ca20d039cfd3d5ab0cfac43b2da49fd8e8a9a55702e165cd`  
		Last Modified: Fri, 04 Jul 2025 02:03:39 GMT  
		Size: 26.9 MB (26895006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c3b377a38f7ea3a8b8503cd6c74f308682e53be8b99855fcd054aa82c03166`  
		Last Modified: Fri, 04 Jul 2025 02:03:35 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50982f64d73862ba000fcf44570bdb5037a36257e7115124d3ffd7816c44023b`  
		Last Modified: Fri, 04 Jul 2025 02:03:34 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c51aa33cedd848941a172afc59d9e93d0a8c2d53f4cbc37ae58868cac6253ece`  
		Last Modified: Fri, 04 Jul 2025 02:03:35 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:b1ff64ae55d9a482c7fec6f5d5d23c9db581f015bde20f7c624b3a993f580962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1130821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:160e5a8b0f933610bab20b5984ab840d6f73ab6321d36a0cdb83c44405a057d4`

```dockerfile
```

-	Layers:
	-	`sha256:10db5823e271f2822326c81e1cc0c483d5ba049fd4ddbde284120e5029b02b11`  
		Last Modified: Fri, 04 Jul 2025 04:17:02 GMT  
		Size: 1.1 MB (1079040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b90a92061efe2619eaed18efdeb513e37e5a86ab62d1092e3cb38ec6516c180f`  
		Last Modified: Fri, 04 Jul 2025 04:17:03 GMT  
		Size: 51.8 KB (51781 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.3-fpm-alpine` - linux; riscv64

```console
$ docker pull wordpress@sha256:074f7c01bcee56c752ddc1f4479afa2d067dd4acd6a05a0f673e3886e225ce99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.7 MB (97715405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3028cb663f6ba28ed26d1f53473e844a8b06a6538ccee191946ac02c779dfcf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 09 Jun 2025 23:45:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 09 Jun 2025 23:45:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_VERSION=8.3.23
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 09 Jun 2025 23:45:55 GMT
WORKDIR /var/www/html
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
STOPSIGNAL SIGQUIT
# Mon, 09 Jun 2025 23:45:55 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 09 Jun 2025 23:45:55 GMT
CMD ["php-fpm"]
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	version='6.8.1'; 	sha1='52d5f05c96a9155f78ed84700264307e5dea14b4'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
VOLUME [/var/www/html]
# Mon, 09 Jun 2025 23:45:55 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jun 2025 23:45:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc9c1f5ef55f1b2ff3a6b36284b619ab1578de78bc84c439b1898065ffdd4f1`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 3.6 MB (3603347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799ef8c3b461dc47d68354281bf2ae2d00422c181fa7d8f8084c1489e4f74b7c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6faf4f4cbdf1dd7a77faca53bd9b20a1a4be9c74973d2b4d795fed979f275c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5464c517d9e6720b4e8fdc4c913e99f247fa283c98af29a23ad77fa07d10fa`  
		Last Modified: Fri, 04 Jul 2025 05:14:28 GMT  
		Size: 12.6 MB (12599140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b6f8e9432616bc8a35861d7967df8c41dbddabc97acaf99e16e5127ae84453`  
		Last Modified: Fri, 04 Jul 2025 05:14:26 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9c5ef26c2ede74471e6e644f2de24c34274c1c7d8af99aaebc236c50afa5e6e`  
		Last Modified: Fri, 04 Jul 2025 06:09:10 GMT  
		Size: 15.9 MB (15896060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a59c2457c586e70baa05a9aeb5719261334bec84c6e712c0a0548eb6b210249`  
		Last Modified: Fri, 04 Jul 2025 06:09:06 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12192fa50f1885f52847f3e80ea41fac11920eb411a457b398490eb36c06fe6`  
		Last Modified: Fri, 04 Jul 2025 06:09:07 GMT  
		Size: 20.0 KB (19997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8a773359adfbf464d0f13e58fdce34baa6a9536636559f8a3f4d5380e9a755`  
		Last Modified: Fri, 04 Jul 2025 06:09:09 GMT  
		Size: 20.0 KB (19997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b443c105e94395af53c367981c97c4d07fcf894464f4c6d38c7c0e2e87439c`  
		Last Modified: Fri, 04 Jul 2025 06:09:08 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2815614755015f251e5442f15adc655a9444df07217a753d5a021e80595d2b14`  
		Last Modified: Fri, 04 Jul 2025 20:20:01 GMT  
		Size: 28.1 MB (28067889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557d203b4f3dd95df894472b34ce0eb72e3557dab4ba44079db16d5789e8ff96`  
		Last Modified: Fri, 04 Jul 2025 20:19:51 GMT  
		Size: 7.0 MB (7019450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c7168780fda05dc6a583249356563ac1ed754ee9f21ac18f7053c3b7adb5ce`  
		Last Modified: Fri, 04 Jul 2025 20:19:50 GMT  
		Size: 62.6 KB (62572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42462eb99eb7b331f2500f0888fd804cd19ea47f06e97c17daebc0623010bd6`  
		Last Modified: Fri, 04 Jul 2025 20:19:50 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dbbdbf000d87e5b539467a479182c05809eea8e4b5c39bbf58c43492caa07c8`  
		Last Modified: Fri, 04 Jul 2025 20:19:51 GMT  
		Size: 26.9 MB (26895034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e518e04aff2e207aa7999a7e83c12b05d0b3eb3ff8f77c064e3040a4f586049`  
		Last Modified: Fri, 04 Jul 2025 20:19:50 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc4ca6a468a6c5bac99a21c0fb2062aa0dbcb7ace35196bd1a3e7e50484ec37`  
		Last Modified: Fri, 04 Jul 2025 20:19:50 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f57ff88eb32c6e0254f45bec7b96956439ca5b3259820be82911b75e962e15b`  
		Last Modified: Fri, 04 Jul 2025 20:19:50 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:da429e8370e5a044510671ec6e1d14c09bc28ee436cbf7162ed6529b45945f81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1130817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643578153378add98fda12785ae8aaddb3cbdf6bc86330d7fb3501972b099698`

```dockerfile
```

-	Layers:
	-	`sha256:9036290b5b2cfeb3297ad33236b2d9eb6d2aa730dadea486ee7bce7533d6e283`  
		Last Modified: Fri, 04 Jul 2025 22:13:09 GMT  
		Size: 1.1 MB (1079036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:996b730ed35c2e04ff59b01f43ef75821d07dd3668a3a9e7d52146ad055305fa`  
		Last Modified: Fri, 04 Jul 2025 22:13:09 GMT  
		Size: 51.8 KB (51781 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.3-fpm-alpine` - linux; s390x

```console
$ docker pull wordpress@sha256:4007815a8ff7f57bbecdb37ad8340096205b17464a48e9fef15c46f3eb5787f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.3 MB (100294876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d407f17617fae6e0c8d93c042d910ece5fef062db3db956010506e10a57784`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 09 Jun 2025 23:45:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 09 Jun 2025 23:45:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_VERSION=8.3.23
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.23.tar.xz.asc
# Mon, 09 Jun 2025 23:45:55 GMT
ENV PHP_SHA256=08be64700f703bca6ff1284bf1fdaffa37ae1b9734b6559f8350248e8960a6db
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 09 Jun 2025 23:45:55 GMT
WORKDIR /var/www/html
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
STOPSIGNAL SIGQUIT
# Mon, 09 Jun 2025 23:45:55 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 09 Jun 2025 23:45:55 GMT
CMD ["php-fpm"]
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN set -eux; 	version='6.8.1'; 	sha1='52d5f05c96a9155f78ed84700264307e5dea14b4'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
VOLUME [/var/www/html]
# Mon, 09 Jun 2025 23:45:55 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Mon, 09 Jun 2025 23:45:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 09 Jun 2025 23:45:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abd3e67b018bcd8c0aa4d0434d7ec04dcdb3a3cfbf444a313e2be49d0524ec2`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 5.9 MB (5932552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f41e4866617495859c5133b898f769b3867a6a3ae061aa9561da765981c5ad`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9335ac6e22dd0c0b2e07f4a5406c437168067a987662ebd8bcd3b269496018`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416dc488e82ac5d95b592019f37aa9b64fdb6535ead41862f2acaa1677ad8e8e`  
		Last Modified: Thu, 03 Jul 2025 23:57:30 GMT  
		Size: 12.6 MB (12599148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ba56106dd7084cdbb4d9ab2d30f1b097ce958de942d3197fc708ee1f3e636a`  
		Last Modified: Thu, 03 Jul 2025 23:57:28 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25d63e1e4d6962369161cd89600b93f34b435063aad41926a421597342eb6e9`  
		Last Modified: Fri, 04 Jul 2025 00:01:25 GMT  
		Size: 13.2 MB (13210606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56deef95c718f1fbe14547d0fcd0e8682120447b39ddcddabbcf51078ea78e27`  
		Last Modified: Fri, 04 Jul 2025 00:01:24 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4071eca4de4ffe44b642f2d9e429cfb38ffed2ba8f05c01b05987bd9e09168`  
		Last Modified: Fri, 04 Jul 2025 00:01:24 GMT  
		Size: 20.0 KB (20001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a7b47a68df718bf2a7d4445bdade317550e020b85d2aa4a94525ae1ad4b31a8`  
		Last Modified: Fri, 04 Jul 2025 00:01:24 GMT  
		Size: 20.0 KB (19996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13964924a7e5d79c0c083de7d22047114b2d6303f4218c86261b01153e6269f`  
		Last Modified: Fri, 04 Jul 2025 00:01:24 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3451957800d9d6565293f879082dc03b161ca9a51fb5c5a5da6001166a730f53`  
		Last Modified: Fri, 04 Jul 2025 01:48:09 GMT  
		Size: 29.3 MB (29250117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:424415028e1625304df344895eaba227abd6e77420980f6cae71631caf1273f0`  
		Last Modified: Fri, 04 Jul 2025 01:48:09 GMT  
		Size: 8.6 MB (8639291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e1f0243993d31985792f2affe6aee9d94a1d3f9e7d95ded240e8ad9feabde74`  
		Last Modified: Fri, 04 Jul 2025 01:48:07 GMT  
		Size: 62.5 KB (62547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff78e1d99b122bf5789c89aa99b647c54860e70411b9387bf2601b693042d7b4`  
		Last Modified: Fri, 04 Jul 2025 01:48:08 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea45f9ee47e584c6c08a4e0d94800d3ade4c22f62740b6f6a1453cb788baf121`  
		Last Modified: Fri, 04 Jul 2025 01:48:10 GMT  
		Size: 26.9 MB (26895001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f4ffd5add047cc2064f8e192c49715b0eb5dd0d37af96cc3da606cdd16a327`  
		Last Modified: Fri, 04 Jul 2025 01:48:08 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8acaf399f503adde0a20c5f86e9edabd943010f3249e1e8213f93afcbe6b6cdb`  
		Last Modified: Fri, 04 Jul 2025 01:48:08 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f294f2dc929515d0bb17b1eb3308ec42d4df70a7f6dd712d97616a181cc32ec5`  
		Last Modified: Fri, 04 Jul 2025 01:48:08 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:cd284aba093cf07f3e053f54b37189eddef079326df1704b9d1b2ef569075746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1130733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ec035aa36b3296bff2662ad1987d4a3466ec99bb4c662ae688311ee210d3ba`

```dockerfile
```

-	Layers:
	-	`sha256:95de1384882129696636839679ed13b74968370c00fe40a5ae6598e98729195d`  
		Last Modified: Fri, 04 Jul 2025 04:17:09 GMT  
		Size: 1.1 MB (1079006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59ba84c35679c1f7c1bb7c239605e202fa584bd6a864b252e750e81ffb92be17`  
		Last Modified: Fri, 04 Jul 2025 04:17:09 GMT  
		Size: 51.7 KB (51727 bytes)  
		MIME: application/vnd.in-toto+json
