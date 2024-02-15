## `wordpress:beta-fpm-alpine`

```console
$ docker pull wordpress@sha256:6b63754f62ed01d0c0c64394f1dc21c8932ebe1dc8f53ad7fee308e4e71824d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `wordpress:beta-fpm-alpine` - linux; amd64

```console
$ docker pull wordpress@sha256:011a845fe2e3d1a1d681736eb831034341f625adcd20ea6e6748d656d813a15f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88646349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:611da8480ae47283b9d6395bc6d39f04cb78960b8f5d02f4b9939d4e52cec1bf`
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
# Sat, 27 Jan 2024 04:47:22 GMT
ENV PHP_VERSION=8.2.15
# Sat, 27 Jan 2024 04:47:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Sat, 27 Jan 2024 04:47:22 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Sat, 27 Jan 2024 04:47:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 27 Jan 2024 04:47:30 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 27 Jan 2024 04:54:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 27 Jan 2024 04:54:55 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 27 Jan 2024 04:54:56 GMT
RUN docker-php-ext-enable sodium
# Sat, 27 Jan 2024 04:54:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 27 Jan 2024 04:54:56 GMT
WORKDIR /var/www/html
# Sat, 27 Jan 2024 04:54:57 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 27 Jan 2024 04:54:57 GMT
STOPSIGNAL SIGQUIT
# Sat, 27 Jan 2024 04:54:57 GMT
EXPOSE 9000
# Sat, 27 Jan 2024 04:54:57 GMT
CMD ["php-fpm"]
# Tue, 13 Feb 2024 20:03:10 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
RUN set -eux; 	version='6.5-beta1'; 	sha1='872eb3105b7c1c3d365a7df183b4748f6822c267'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
VOLUME [/var/www/html]
# Tue, 13 Feb 2024 20:03:10 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 20:03:10 GMT
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
	-	`sha256:3bdde487d2c3c481b0aa4cd0406254b43519751c01aa878faabca1606841a70b`  
		Last Modified: Sat, 27 Jan 2024 05:38:36 GMT  
		Size: 12.1 MB (12096363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243db39c4f41b17d1f4c981d29228b0eb61f114ae253a3f4f129690393294e2e`  
		Last Modified: Sat, 27 Jan 2024 05:38:36 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53efed4e67e9e058bf4248baae909225e8465dce9c5b817f002aaf6ec44ca830`  
		Last Modified: Sat, 27 Jan 2024 05:39:19 GMT  
		Size: 12.8 MB (12848982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea1e3b7a6c96ad81accc89f994fd1703472ee8c09610defadf7413dd14a84b4`  
		Last Modified: Sat, 27 Jan 2024 05:39:17 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a808721a61eca53c289206c4a2077823696d71938aa6303f8de9b54394e062c9`  
		Last Modified: Sat, 27 Jan 2024 05:39:17 GMT  
		Size: 19.3 KB (19288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a3cc5a1024bad9c8ddf1e09b9099dbf48cffbb02da3f524161f7b3a52a470f`  
		Last Modified: Sat, 27 Jan 2024 05:39:18 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d716b92cd6c348b6e5cd53867b0b439b41d80efa23b7b5518e341001a68db6`  
		Last Modified: Wed, 14 Feb 2024 19:54:47 GMT  
		Size: 28.6 MB (28637069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f378160e0c4547960a15068a2f7edcedce9b83639336bef00dba45af90faead`  
		Last Modified: Wed, 14 Feb 2024 19:54:47 GMT  
		Size: 4.3 MB (4298498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf35ad6d3953c072f8d6b5ea5b873d57e07d000434a261f454405980d9adcf88`  
		Last Modified: Wed, 14 Feb 2024 19:54:47 GMT  
		Size: 59.4 KB (59386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29c6d1866d666020cc948e4209649e9b523df4d9f8510b0c56d8a30570396e9c`  
		Last Modified: Wed, 14 Feb 2024 19:54:47 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc7719e33ee8a92d9f6b4cd46e36f9f11475e5279e0bc7a6c37a2406f0357d8`  
		Last Modified: Wed, 14 Feb 2024 19:54:48 GMT  
		Size: 24.5 MB (24498407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4fd8e5e131bf6401859c2b99c0612e7301341082d0844f423918373acc7ae84`  
		Last Modified: Wed, 14 Feb 2024 19:54:48 GMT  
		Size: 2.3 KB (2344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a43d22ee97031713daaef7949561bd77a3f93e18ebd2630660b99954d9ebc3a7`  
		Last Modified: Wed, 14 Feb 2024 19:54:48 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:997e6bfabf88795c515610c23924b43759680fb892c1eb1ece78a553a7ea82d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **911.9 KB (911877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66c3b58ca085d60db66d09345ac3fafb11488b688dcd8b1f6b06a0b296d788e`

```dockerfile
```

-	Layers:
	-	`sha256:0a194184237271f657b1687d355989a55fdd35eec4d4a0348b1345dbe1682b49`  
		Last Modified: Wed, 14 Feb 2024 19:54:47 GMT  
		Size: 864.2 KB (864227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e40d68e5ebf30ab583697e71da4f037de93ba4b48296063ea0710f54f0053750`  
		Last Modified: Wed, 14 Feb 2024 19:54:47 GMT  
		Size: 47.6 KB (47650 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-fpm-alpine` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:d33be5f7f8116f4a2a2cdd55dbd625183b2208ecd5ed3bc37b9918d109e594d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86425643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e8a3c34b63eff852d1fdb6e25738fda1b810a8578c622879ad6277ba36309dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 26 Jan 2024 08:03:10 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 08:03:10 GMT
CMD ["/bin/sh"]
# Fri, 26 Jan 2024 08:03:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 26 Jan 2024 08:03:10 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 26 Jan 2024 08:03:10 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 26 Jan 2024 08:03:10 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 26 Jan 2024 08:03:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 26 Jan 2024 08:03:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 26 Jan 2024 08:03:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 26 Jan 2024 08:03:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 26 Jan 2024 08:03:10 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 26 Jan 2024 08:03:10 GMT
ENV PHP_VERSION=8.2.15
# Fri, 26 Jan 2024 08:03:10 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Fri, 26 Jan 2024 08:03:10 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Fri, 26 Jan 2024 08:03:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 26 Jan 2024 08:03:10 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 26 Jan 2024 08:03:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 26 Jan 2024 08:03:10 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 26 Jan 2024 08:03:10 GMT
RUN docker-php-ext-enable sodium
# Fri, 26 Jan 2024 08:03:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 26 Jan 2024 08:03:10 GMT
WORKDIR /var/www/html
# Fri, 26 Jan 2024 08:03:10 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 26 Jan 2024 08:03:10 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Jan 2024 08:03:10 GMT
EXPOSE 9000
# Fri, 26 Jan 2024 08:03:10 GMT
CMD ["php-fpm"]
# Fri, 26 Jan 2024 08:03:10 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Fri, 26 Jan 2024 08:03:10 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 26 Jan 2024 08:03:10 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 26 Jan 2024 08:03:10 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 26 Jan 2024 08:03:10 GMT
RUN set -eux; 	version='6.4.3-RC1'; 	sha1='d3b54f017115c761f4ea19851ec607307a0c4f1e'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Fri, 26 Jan 2024 08:03:10 GMT
VOLUME [/var/www/html]
# Fri, 26 Jan 2024 08:03:10 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Fri, 26 Jan 2024 08:03:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 26 Jan 2024 08:03:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Jan 2024 08:03:10 GMT
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
	-	`sha256:55005ed483beb1ca337359ab17a9675e229b931426997399767cc9d13937a3ad`  
		Last Modified: Sat, 27 Jan 2024 06:46:51 GMT  
		Size: 12.1 MB (12096382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aedab67bb2ee246ae317cf484a9d5751a7fe4e6b2b339dedaa0cac726c5f706`  
		Last Modified: Sat, 27 Jan 2024 06:46:50 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6ccdb14914594e3628577188a6abab005164d7a4d2693b4221f6e7f929f00d`  
		Last Modified: Sat, 27 Jan 2024 06:47:17 GMT  
		Size: 11.7 MB (11693476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f82c42b68ca4f7920ec45aee2afe77286c2034a2d6d39adaa6b82e87724f997`  
		Last Modified: Sat, 27 Jan 2024 06:47:14 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3c06177b0de9717f3d106277b69e1f907e80d34b2b7f9cdaeffe0a38d2b3a9`  
		Last Modified: Sat, 27 Jan 2024 06:47:15 GMT  
		Size: 19.1 KB (19133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76346ff4270699ce5621489a14f91f2659156895337742c85457fb76cf476dd0`  
		Last Modified: Sat, 27 Jan 2024 06:47:15 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17dbcff973b97beeb3755e81ae88740e4b58256607424b30337799d643a90f76`  
		Last Modified: Tue, 30 Jan 2024 22:49:25 GMT  
		Size: 28.2 MB (28163537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96cc45a68a80791edf173d4d36f98b2dccdb9a609728df39b35c69ebc821541b`  
		Last Modified: Tue, 30 Jan 2024 22:49:24 GMT  
		Size: 4.1 MB (4131656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b73a69d13e6c02e5575768ae76313006cda57a01c5967c54d42fda54bf241a`  
		Last Modified: Tue, 30 Jan 2024 22:49:24 GMT  
		Size: 59.4 KB (59376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af51c5c8e8b78789a1d9228e0694089b475dc2298b4c97e54e7892a6f32f1dbc`  
		Last Modified: Tue, 30 Jan 2024 22:49:24 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eb21bdc0d062ae79c30bc049684df1d5be31431f58274263e10f44deeb00b7c`  
		Last Modified: Tue, 30 Jan 2024 23:02:18 GMT  
		Size: 24.3 MB (24314089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e713d047434c6cd4bf41aaf22fd7da176ce01162da3b067b4e7e269aa2bcab6a`  
		Last Modified: Tue, 30 Jan 2024 23:02:17 GMT  
		Size: 2.3 KB (2347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e613f6fd4d75dcf18b8dbf288fde6c30bb731a222d782a0630283cd8797f8753`  
		Last Modified: Tue, 30 Jan 2024 23:02:17 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:3a532aadcb0bea5696bb52b6e658e6b2d8068baf577eac81cd75fa6e521134cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 KB (46662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47dc479fab85ea2c7d1f751bde1b74b888531526d8dfb9d1c19c3bb9fc33b92`

```dockerfile
```

-	Layers:
	-	`sha256:dab7009c49f456033757a62a5279f0a693d975987480b9a880efa54715efdb13`  
		Last Modified: Tue, 30 Jan 2024 23:02:16 GMT  
		Size: 46.7 KB (46662 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-fpm-alpine` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:b85843cb99e2aab68aa4d3ead526d8717bf942a445b1d4509808b8ebe76b0870
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.6 MB (98555516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d65c727a8aba0b414d13cf3755760487dc7b539c7d39a8f4d33e5f5839e2783d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 07 Aug 2023 19:57:33 GMT
ADD file:911497ffc967e53c16d8356f320bf61fe06b85fc3250b7c01183f7bcfbfef404 in / 
# Mon, 07 Aug 2023 19:57:33 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 02:54:37 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 21 Oct 2023 02:54:39 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Sat, 21 Oct 2023 02:54:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 21 Oct 2023 02:54:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 21 Oct 2023 02:54:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 21 Oct 2023 02:54:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 21 Oct 2023 02:54:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 21 Oct 2023 02:54:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 21 Oct 2023 03:32:08 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F 2C16C765DBE54A088130F1BC4B9B5F600B55F3B4 39B641343D8C104B2B146DC3F9C39DC0B9698544
# Sat, 21 Oct 2023 03:32:08 GMT
ENV PHP_VERSION=8.0.30
# Sat, 21 Oct 2023 03:32:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.30.tar.xz.asc
# Sat, 21 Oct 2023 03:32:08 GMT
ENV PHP_SHA256=216ab305737a5d392107112d618a755dc5df42058226f1670e9db90e77d777d9
# Sat, 21 Oct 2023 03:32:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 21 Oct 2023 03:32:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 21 Oct 2023 03:37:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 21 Oct 2023 03:37:38 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 21 Oct 2023 03:37:39 GMT
RUN docker-php-ext-enable sodium
# Sat, 21 Oct 2023 03:37:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 21 Oct 2023 03:37:39 GMT
WORKDIR /var/www/html
# Sat, 21 Oct 2023 03:37:39 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 21 Oct 2023 03:37:39 GMT
STOPSIGNAL SIGQUIT
# Sat, 21 Oct 2023 03:37:39 GMT
EXPOSE 9000
# Sat, 21 Oct 2023 03:37:39 GMT
CMD ["php-fpm"]
# Sat, 21 Oct 2023 06:09:00 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	;
# Sat, 21 Oct 2023 06:09:48 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Sat, 21 Oct 2023 06:09:49 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 21 Oct 2023 06:09:50 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Sat, 04 Nov 2023 00:32:53 GMT
RUN set -eux; 	version='6.4-RC3'; 	sha1='c2a033b4d3d2b3fe2a78724fa7be0c5067ef60b1'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content
# Sat, 04 Nov 2023 00:32:54 GMT
VOLUME [/var/www/html]
# Sat, 04 Nov 2023 00:32:54 GMT
COPY --chown=www-data:www-datafile:d38fd3c0db552e13465e83c5d7bbd85c7c3d036bf1285495988cc4ab2ffaf7f5 in /usr/src/wordpress/ 
# Sat, 04 Nov 2023 00:32:54 GMT
COPY file:5be6bcc31206cb827f037769d89fd092037ed61a1e10d6cae7939a37055beb4c in /usr/local/bin/ 
# Sat, 04 Nov 2023 00:32:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 04 Nov 2023 00:32:54 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d27c9f7e5791cecbf0251c0e7638ad6fbd2b510f038f66cc06c933da98c75979`  
		Last Modified: Mon, 07 Aug 2023 19:58:18 GMT  
		Size: 2.4 MB (2419274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee28d7774c683e5fd44e8b5f395d15311d75b1cf5300040efac8c1a085da3d4a`  
		Last Modified: Sat, 21 Oct 2023 03:51:19 GMT  
		Size: 2.8 MB (2791922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a51f4b1ed371a17cb9c1f2e82837093fd51d9a2dd3f0e942cf9688f15da8fd6`  
		Last Modified: Sat, 21 Oct 2023 03:51:18 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ebc794bac90c8f790e8c5dad9fc57b1b79d9e58e02efe176e2ecdb10b511f2`  
		Last Modified: Sat, 21 Oct 2023 03:51:18 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c695bb1574ba1ff1645d8578822d2e3d2f837a45f8cc150a67fdffbcec32b93`  
		Last Modified: Sat, 21 Oct 2023 03:54:27 GMT  
		Size: 10.8 MB (10841077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb217111faca192bcffc9d5e109310ccf1ba2f83cb7b343eaf409ae58176403e`  
		Last Modified: Sat, 21 Oct 2023 03:54:26 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf20cfffe306c25cc306016ca339259bf959dc8e04bfb7dfbb17e44a2713012`  
		Last Modified: Sat, 21 Oct 2023 03:54:51 GMT  
		Size: 10.4 MB (10350156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593a395541ae95adb3f2e03b402a721103bdffd676b606d1e2129660342bd672`  
		Last Modified: Sat, 21 Oct 2023 03:54:49 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c7210a2e242f534c2fc26577eb08436124174fbebe4a6cc80dc7fa9e34eea7`  
		Last Modified: Sat, 21 Oct 2023 03:54:49 GMT  
		Size: 18.7 KB (18666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7baa4a188b711385b21d7117cb5f2bcd5489a8dc7d456f8120803b25681b2c6`  
		Last Modified: Sat, 21 Oct 2023 03:54:49 GMT  
		Size: 8.7 KB (8711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d58c13b7051d2cdde60f037c9566ac3c4577639b3547bc45653254e055bc0e57`  
		Last Modified: Sat, 21 Oct 2023 06:17:28 GMT  
		Size: 41.1 MB (41144050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2786cfc98040bb3323bf8c771fcd172c877da1582f384310421f51e87e534ae`  
		Last Modified: Sat, 21 Oct 2023 06:17:23 GMT  
		Size: 3.9 MB (3857237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5fac747d5b06b1dadab4835d410556f37ba7e554675208144876d6db2b68247`  
		Last Modified: Sat, 21 Oct 2023 06:17:21 GMT  
		Size: 65.8 KB (65782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:213c48f84b637a6a7437ccb72020183b825c5c457fcfad5021b4f1f6018bc7a0`  
		Last Modified: Sat, 21 Oct 2023 06:17:21 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83821dde2d4b2d96de9e882a9c9256f13f17feed170dfb6d472ff714e88ae142`  
		Last Modified: Sat, 04 Nov 2023 00:36:46 GMT  
		Size: 27.0 MB (27049694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25795049f44c2808b901a1195bf6fe93bb5f99d672d69281113fda42d8437157`  
		Last Modified: Sat, 04 Nov 2023 00:36:42 GMT  
		Size: 2.3 KB (2349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e446aca062cb0e6749851e58c75e6e08a3c3fd7cd598ff9de12c59300b8db11`  
		Last Modified: Sat, 04 Nov 2023 00:36:42 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `wordpress:beta-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:e0ee8d9c475d0727c4918a3545ad15586b799ab84f01d617945c2af1f02ebd9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.9 MB (88875420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d0aa869d1fb16be5023832ca32f416818457c935fafa67dbb126b829a390b8`
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
# Sat, 27 Jan 2024 07:53:27 GMT
ENV PHP_VERSION=8.2.15
# Sat, 27 Jan 2024 07:53:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Sat, 27 Jan 2024 07:53:27 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Sat, 27 Jan 2024 07:53:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 27 Jan 2024 07:53:34 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 27 Jan 2024 08:01:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 27 Jan 2024 08:01:00 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 27 Jan 2024 08:01:01 GMT
RUN docker-php-ext-enable sodium
# Sat, 27 Jan 2024 08:01:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 27 Jan 2024 08:01:01 GMT
WORKDIR /var/www/html
# Sat, 27 Jan 2024 08:01:02 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 27 Jan 2024 08:01:02 GMT
STOPSIGNAL SIGQUIT
# Sat, 27 Jan 2024 08:01:02 GMT
EXPOSE 9000
# Sat, 27 Jan 2024 08:01:02 GMT
CMD ["php-fpm"]
# Tue, 13 Feb 2024 20:03:10 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
RUN set -eux; 	version='6.5-beta1'; 	sha1='872eb3105b7c1c3d365a7df183b4748f6822c267'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
VOLUME [/var/www/html]
# Tue, 13 Feb 2024 20:03:10 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 20:03:10 GMT
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
	-	`sha256:7635cf7aef4c63fed820cf1a7d4016022d00a0480ceb121fb03561da21ed4c16`  
		Last Modified: Sat, 27 Jan 2024 08:42:44 GMT  
		Size: 12.1 MB (12096388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acdb20c879b0f1f0e303192e729f69ee98706f083dd82eb93e38de241a74bed`  
		Last Modified: Sat, 27 Jan 2024 08:42:44 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffde6eec435e25aa53b0067ead3bd5314467757f6e43cdee2f32dd82befa4052`  
		Last Modified: Sat, 27 Jan 2024 08:43:07 GMT  
		Size: 12.9 MB (12910806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea6f640d6c7975cd9e94e989db6ac71fa97a651c18bfbf72ffb65da53583596`  
		Last Modified: Sat, 27 Jan 2024 08:43:05 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514d668a5c83dbca5542a242a3c9350431b9fcd194bb47c2e3f22e2d00e5d2f2`  
		Last Modified: Sat, 27 Jan 2024 08:43:05 GMT  
		Size: 19.1 KB (19085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9997ebf78f09b231338f3c151603fdedc673a84e9340cef8300b5aa9432c4174`  
		Last Modified: Sat, 27 Jan 2024 08:43:05 GMT  
		Size: 9.2 KB (9175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f4bc871324170a180923549127b0454977269d7ecb09518f4e31ffcb4852f2`  
		Last Modified: Wed, 14 Feb 2024 23:23:18 GMT  
		Size: 28.8 MB (28770663 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d22315e78b8eaa14c0fb8aa2f61a29085c950ded1a1917497ba54f0a5d525e0d`  
		Last Modified: Wed, 14 Feb 2024 23:23:17 GMT  
		Size: 4.3 MB (4339127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262c66a450f2bcd752a0df118b52b836b71a201d6b0aa892d97a9ce71f1622a2`  
		Last Modified: Wed, 14 Feb 2024 23:23:17 GMT  
		Size: 59.4 KB (59364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74db2436b81190d550c9088ce9dc7084669d4f96c8bec883e847a07380281995`  
		Last Modified: Wed, 14 Feb 2024 23:23:17 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9646d2dd4f7d2b9ca7fb4cd032893c4319b12955274c1342c35bf21db8c5de1`  
		Last Modified: Wed, 14 Feb 2024 23:23:19 GMT  
		Size: 24.5 MB (24498406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915dac258a299947e0c9fdf548c352bf95f3bb5fdf9de1673cc10fe782c07063`  
		Last Modified: Wed, 14 Feb 2024 23:23:19 GMT  
		Size: 2.3 KB (2346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad225dc7ebc22b531c3bb1e9a59f332ca24bb53d86f0daa11f8e31fe2037183`  
		Last Modified: Wed, 14 Feb 2024 23:23:19 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:dfade529725096e78ad9713ad17434e65bbb5741588fdda1e32b6d71554bc7a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **910.3 KB (910290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:285ae70370851c3d2b775add69e55f31ca232d4bbcf2ba1428f38f6e00258580`

```dockerfile
```

-	Layers:
	-	`sha256:d341dc5102976a25d6cab9a871ee15e4e425d11edc2f1510657a41d9dab2e1bb`  
		Last Modified: Wed, 14 Feb 2024 23:23:17 GMT  
		Size: 864.2 KB (864246 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9df15831e8965372e69f1e5143d22a7bf713a101f7ec98e39515de8f1df80139`  
		Last Modified: Wed, 14 Feb 2024 23:23:17 GMT  
		Size: 46.0 KB (46044 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-fpm-alpine` - linux; 386

```console
$ docker pull wordpress@sha256:8efa02f30626005e7504ca1f67a314446bdff99570940fb431dcc099fd0db9e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.3 MB (89267666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c2805e71f75bd793b71bbfeaa2826c0fa6749be231b6ede4ced495a554bbf1`
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
# Sat, 27 Jan 2024 05:24:12 GMT
ENV PHP_VERSION=8.2.15
# Sat, 27 Jan 2024 05:24:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Sat, 27 Jan 2024 05:24:13 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Sat, 27 Jan 2024 05:24:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 27 Jan 2024 05:24:20 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 27 Jan 2024 05:37:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 27 Jan 2024 05:37:39 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 27 Jan 2024 05:37:40 GMT
RUN docker-php-ext-enable sodium
# Sat, 27 Jan 2024 05:37:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 27 Jan 2024 05:37:40 GMT
WORKDIR /var/www/html
# Sat, 27 Jan 2024 05:37:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 27 Jan 2024 05:37:41 GMT
STOPSIGNAL SIGQUIT
# Sat, 27 Jan 2024 05:37:41 GMT
EXPOSE 9000
# Sat, 27 Jan 2024 05:37:41 GMT
CMD ["php-fpm"]
# Tue, 13 Feb 2024 20:03:10 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
RUN set -eux; 	version='6.5-beta1'; 	sha1='872eb3105b7c1c3d365a7df183b4748f6822c267'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
VOLUME [/var/www/html]
# Tue, 13 Feb 2024 20:03:10 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 20:03:10 GMT
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
	-	`sha256:b705d96a822720c651828184408f1a6c9eea23d8197c63f104bccb6e1d73ba73`  
		Last Modified: Sat, 27 Jan 2024 06:49:03 GMT  
		Size: 12.1 MB (12096383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87bce88821860841ad9fb8f2aa35e55484bf761143949eab88642252b79cad41`  
		Last Modified: Sat, 27 Jan 2024 06:49:02 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed75cac09ec5f9766a622ae1979291bcfa3db20e87749b8b96bdf1ce9fa7344`  
		Last Modified: Sat, 27 Jan 2024 06:49:31 GMT  
		Size: 13.2 MB (13195968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9ed1af92f7cd9d4833f43b5ec3fda659b5fcda099579bd9b1157f8fb3d7593`  
		Last Modified: Sat, 27 Jan 2024 06:49:28 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ec9b7459eb3fb9025e10bfa088ab0bd24e214c524d477abddd714fe74a22da`  
		Last Modified: Sat, 27 Jan 2024 06:49:28 GMT  
		Size: 19.3 KB (19292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd34332b4b5e6c9f8687d99b6d843b070f7aa9e20d70d6cf3b3dd2fe11b6964`  
		Last Modified: Sat, 27 Jan 2024 06:49:28 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd1635b476ed62b3e8d05b91b85d433f70c7d416fd9c050c479756da4ae5c2c`  
		Last Modified: Wed, 14 Feb 2024 19:54:50 GMT  
		Size: 28.9 MB (28877528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756f8b1a5698ad9f267d85ad9e6cc77d907bf8f23f3f945433b7b464703dd850`  
		Last Modified: Wed, 14 Feb 2024 19:54:49 GMT  
		Size: 4.4 MB (4433161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49c022f9a5e77f6f4ec9ad048839344a7bd38d0e978ed0af13f2c9ce3cc7c932`  
		Last Modified: Wed, 14 Feb 2024 19:54:49 GMT  
		Size: 59.4 KB (59392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9100c3dca44d92820d35e5919882f016139bd09a0172a9ebcbe7f485c7cd37d1`  
		Last Modified: Wed, 14 Feb 2024 19:54:49 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a9f118916a33ac7d0dfce1f49acf44bcc28d910901f0696aa37b6eed599a47`  
		Last Modified: Wed, 14 Feb 2024 19:54:51 GMT  
		Size: 24.5 MB (24498408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a0c8dafe4bc476417175ed02bd02ace2f54db04fcd633bd4f8a9f4830ea5905`  
		Last Modified: Wed, 14 Feb 2024 19:54:50 GMT  
		Size: 2.3 KB (2347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb72d4b8506a77212e04d759868203b51b720227bb24f6727ce75345f7bad3f2`  
		Last Modified: Wed, 14 Feb 2024 19:54:50 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:7e8a952889bc9c46ff6c1eb349b38c5ca58088d9021c9c2b3f648b9f85077e1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **911.8 KB (911776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f9bc4f809a10a147345ccc7f0d8b38ed362371147d576e337e4ee121c076f8`

```dockerfile
```

-	Layers:
	-	`sha256:abc3d2401e15922789005f820e350e5341a07f27876ea527072334342dbf6696`  
		Last Modified: Wed, 14 Feb 2024 19:54:49 GMT  
		Size: 864.2 KB (864182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:110403a2e6c712799f063d34da1ec1e074e183929a0868a237732b63c94ad46e`  
		Last Modified: Wed, 14 Feb 2024 19:54:49 GMT  
		Size: 47.6 KB (47594 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-fpm-alpine` - linux; ppc64le

```console
$ docker pull wordpress@sha256:2eb3b4fa2996576857b1e964b019d1c1f13c5e3e094b6b6a20ac76b746e38d61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.1 MB (90059955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff21612bc22a966f4254061432d70df5f758eb448f54b82ed37cef190f707ed`
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
# Sat, 27 Jan 2024 03:44:28 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 27 Jan 2024 03:44:29 GMT
ENV PHP_VERSION=8.2.15
# Sat, 27 Jan 2024 03:44:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Sat, 27 Jan 2024 03:44:30 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Sat, 27 Jan 2024 03:44:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 27 Jan 2024 03:44:39 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 27 Jan 2024 03:49:58 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 27 Jan 2024 03:50:00 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 27 Jan 2024 03:50:02 GMT
RUN docker-php-ext-enable sodium
# Sat, 27 Jan 2024 03:50:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 27 Jan 2024 03:50:04 GMT
WORKDIR /var/www/html
# Sat, 27 Jan 2024 03:50:07 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 27 Jan 2024 03:50:07 GMT
STOPSIGNAL SIGQUIT
# Sat, 27 Jan 2024 03:50:08 GMT
EXPOSE 9000
# Sat, 27 Jan 2024 03:50:08 GMT
CMD ["php-fpm"]
# Tue, 13 Feb 2024 20:03:10 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
RUN set -eux; 	version='6.5-beta1'; 	sha1='872eb3105b7c1c3d365a7df183b4748f6822c267'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
VOLUME [/var/www/html]
# Tue, 13 Feb 2024 20:03:10 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 13 Feb 2024 20:03:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 13 Feb 2024 20:03:10 GMT
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
	-	`sha256:91dfc65a6989d02faf8ba64268e70055439b4184c1af31338fcc69df9aa4f4b4`  
		Last Modified: Sat, 27 Jan 2024 04:24:19 GMT  
		Size: 12.1 MB (12096378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc874be9fcdd85b468fdcd00a7ac26557a1dfa6ce3d214db4870df31d7669dd`  
		Last Modified: Sat, 27 Jan 2024 04:24:18 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee81264d77cbed5dd874c4a761f4e67f0318331456d87eddcfe8d4e300d3248`  
		Last Modified: Sat, 27 Jan 2024 04:24:48 GMT  
		Size: 13.3 MB (13338992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f291bcd4f88be6c7991d439cc1a391b19dac2294394a49112b4f5b107ee2b3d0`  
		Last Modified: Sat, 27 Jan 2024 04:24:46 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6b9d2ddd88902f6fb0a5c19a8b7ef7e3e5ba6782d74407d0345c3974feb779`  
		Last Modified: Sat, 27 Jan 2024 04:24:45 GMT  
		Size: 19.1 KB (19105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ce7c07f8ad7e826f226f530b811bd96fc32d55f47f15f89d99bb5a51c051e6`  
		Last Modified: Sat, 27 Jan 2024 04:24:45 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5ae5ac9534f96f0907b865b363f176137e21f41604eba47533c296c414be43`  
		Last Modified: Wed, 14 Feb 2024 20:25:58 GMT  
		Size: 29.4 MB (29379011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62fb89b0344de3ee675712287fca52e1dd42684591f6e45c23e2edde10425eb1`  
		Last Modified: Wed, 14 Feb 2024 20:25:57 GMT  
		Size: 4.4 MB (4449361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195902de5b4a91f554ebecad4e5b1df04d6539cac008efd94052a734f0fb72dc`  
		Last Modified: Wed, 14 Feb 2024 20:25:56 GMT  
		Size: 59.4 KB (59410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217420d66c83b4b8b80dfd9862b4df96cfc50e7e958d30b0c4142073f809ce57`  
		Last Modified: Wed, 14 Feb 2024 20:25:56 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3752d0baf43a66f34ac9d42cbebb02123034d57ae0d952425d08b5af459efd32`  
		Last Modified: Wed, 14 Feb 2024 20:25:59 GMT  
		Size: 24.5 MB (24498396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71acc8b252facebbab55b71d2a770aa7e575ef1418880667e07b0e8a4d583788`  
		Last Modified: Wed, 14 Feb 2024 20:25:58 GMT  
		Size: 2.3 KB (2348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd095623edf84ce158e20210e50514c9e6668696acfbe4bf8ee237a195d63b7a`  
		Last Modified: Wed, 14 Feb 2024 20:25:58 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:78d034d629fba7cfd2a819932ef9c12bdc2e8d438c20e5ab5e6341c08aa07b16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **908.7 KB (908745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a45b63fb7c6c8ba1a962c0660117b8dc61a5896a24e5f5c8b55058f43effb761`

```dockerfile
```

-	Layers:
	-	`sha256:ae8c65f18341b27b056cbd676bb8df8898b32c579a8dbf4c50dabed78e8baeb3`  
		Last Modified: Wed, 14 Feb 2024 20:25:56 GMT  
		Size: 862.6 KB (862649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:819d98cbdaf7eb14643f286390ad3b83a555d09c5881ab8f2cf958ace8b29cad`  
		Last Modified: Wed, 14 Feb 2024 20:25:56 GMT  
		Size: 46.1 KB (46096 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-fpm-alpine` - linux; s390x

```console
$ docker pull wordpress@sha256:a2ba651365a44aa358198a7740d9ac71f3c54f986849a50b7a2d0dd2014e2490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.3 MB (89339483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30eee71777eb7aaaa0d806fe4c9ac53d8922feffdf353feebda55fbf396ebe87`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 26 Jan 2024 08:03:10 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Fri, 26 Jan 2024 08:03:10 GMT
CMD ["/bin/sh"]
# Fri, 26 Jan 2024 08:03:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 26 Jan 2024 08:03:10 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 26 Jan 2024 08:03:10 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 26 Jan 2024 08:03:10 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 26 Jan 2024 08:03:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 26 Jan 2024 08:03:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 26 Jan 2024 08:03:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 26 Jan 2024 08:03:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 26 Jan 2024 08:03:10 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 26 Jan 2024 08:03:10 GMT
ENV PHP_VERSION=8.2.15
# Fri, 26 Jan 2024 08:03:10 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Fri, 26 Jan 2024 08:03:10 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Fri, 26 Jan 2024 08:03:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 26 Jan 2024 08:03:10 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 26 Jan 2024 08:03:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 26 Jan 2024 08:03:10 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 26 Jan 2024 08:03:10 GMT
RUN docker-php-ext-enable sodium
# Fri, 26 Jan 2024 08:03:10 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 26 Jan 2024 08:03:10 GMT
WORKDIR /var/www/html
# Fri, 26 Jan 2024 08:03:10 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 26 Jan 2024 08:03:10 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Jan 2024 08:03:10 GMT
EXPOSE 9000
# Fri, 26 Jan 2024 08:03:10 GMT
CMD ["php-fpm"]
# Fri, 26 Jan 2024 08:03:10 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Fri, 26 Jan 2024 08:03:10 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 26 Jan 2024 08:03:10 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 26 Jan 2024 08:03:10 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 26 Jan 2024 08:03:10 GMT
RUN set -eux; 	version='6.4.3-RC1'; 	sha1='d3b54f017115c761f4ea19851ec607307a0c4f1e'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Fri, 26 Jan 2024 08:03:10 GMT
VOLUME [/var/www/html]
# Fri, 26 Jan 2024 08:03:10 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Fri, 26 Jan 2024 08:03:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 26 Jan 2024 08:03:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Jan 2024 08:03:10 GMT
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
	-	`sha256:a462cee53e581fac0e8347d52eed10b734f2a96ee657bf3cc72d33a361e73044`  
		Last Modified: Sat, 27 Jan 2024 13:03:39 GMT  
		Size: 12.1 MB (12096382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae86ccd47b275d52ff8c597ac07ba00821d6a49f6a160672da08626ffb3e4ee`  
		Last Modified: Sat, 27 Jan 2024 13:03:38 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a6ba7dd265c8e072c655641baac3d3c8207b14989b48f9530d7f6e466a1e3d`  
		Last Modified: Sat, 27 Jan 2024 13:04:01 GMT  
		Size: 12.6 MB (12597111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1fc6b555c1bf94facd39821f1301332cc3716571dd766868cf4428635638c8`  
		Last Modified: Sat, 27 Jan 2024 13:03:58 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92fb3222089f4ec15592befdafef43dd0fe5b0370e8e110922dfcf455bdbd413`  
		Last Modified: Sat, 27 Jan 2024 13:03:57 GMT  
		Size: 19.1 KB (19096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05da8d383b0b4509103b709fb6d0219680ca89038b861f3286d79a0b18d404a0`  
		Last Modified: Sat, 27 Jan 2024 13:03:57 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609c74167ff68c20fe76ea97ecdc9565da15178c53dc80d9f911331cc8108565`  
		Last Modified: Sun, 28 Jan 2024 20:27:32 GMT  
		Size: 29.6 MB (29623908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bfd6d9b8b47dad7c48359f316dbc1bf732f9904e0c7a1b6987b14b88d0c5e17`  
		Last Modified: Sun, 28 Jan 2024 20:27:32 GMT  
		Size: 4.4 MB (4428221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef06b8b2908fd9ea19673652cfc9cd88e49c398f9168446de4aeccc9df6972cd`  
		Last Modified: Sun, 28 Jan 2024 20:27:32 GMT  
		Size: 59.4 KB (59376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089c135459c1d50a39cd67a76ef97fb14b49d41327a2ca0d0fe81c615281a8de`  
		Last Modified: Sun, 28 Jan 2024 20:27:31 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04333c78782e792d4e4253b813125cddffb6135288ffb097cce37338c8f2a327`  
		Last Modified: Sun, 28 Jan 2024 21:54:07 GMT  
		Size: 24.3 MB (24314083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66305cb31b119a27c79b1d825ac807d35be150ee273ab33f5511f939a555db9c`  
		Last Modified: Sun, 28 Jan 2024 21:54:06 GMT  
		Size: 2.3 KB (2347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c41e9fec13539ae860fe442fc78fc8564dc17e00b466483dc74fac284e5be81`  
		Last Modified: Sun, 28 Jan 2024 21:54:07 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:a5ab9aee4ad2eeeb4ddec113d589fb4f98c158e7a4079217f0f989c2d79a86f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **910.0 KB (909982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e096d3a78da90c5792a52196f49cc9d012cf4215b16f9b86f5371e480f7425ae`

```dockerfile
```

-	Layers:
	-	`sha256:91c4690d8d1df34ed31634faff0ab0412d5dfd3274a307cb14c74f4fdab0d777`  
		Last Modified: Sun, 28 Jan 2024 21:54:06 GMT  
		Size: 863.3 KB (863274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:437751b767b62bbe014fd13cc12bf8f4442719c9bae49301af13a26cacda7da8`  
		Last Modified: Sun, 28 Jan 2024 21:54:06 GMT  
		Size: 46.7 KB (46708 bytes)  
		MIME: application/vnd.in-toto+json
