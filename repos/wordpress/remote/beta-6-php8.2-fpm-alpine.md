## `wordpress:beta-6-php8.2-fpm-alpine`

```console
$ docker pull wordpress@sha256:1a14f1543ae10e7355ee3015d9e523fdea623d0cc31833c56d9e6fd0e1d392c6
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

### `wordpress:beta-6-php8.2-fpm-alpine` - linux; amd64

```console
$ docker pull wordpress@sha256:fabdad12da9b947c80b8e8b5cfa9acf1c2d6d11948f7aa1d20a432e052e46c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.7 MB (90733230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42687da70a724de30464ea096702bd7a6a2b749c8e0088d571a90ae758057df7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 00:32:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 16 Mar 2024 00:32:11 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 16 Mar 2024 00:32:11 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 16 Mar 2024 00:32:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 16 Mar 2024 00:32:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 16 Mar 2024 00:32:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 16 Mar 2024 00:32:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 16 Mar 2024 00:32:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 16 Mar 2024 01:34:46 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 11 Apr 2024 19:14:17 GMT
ENV PHP_VERSION=8.2.18
# Thu, 11 Apr 2024 19:14:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.18.tar.xz.asc
# Thu, 11 Apr 2024 19:14:17 GMT
ENV PHP_SHA256=44b306fc021e56441f691da6c3108788bd9e450f293b3bc70fcd64b08dd41a50
# Thu, 11 Apr 2024 19:14:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 11 Apr 2024 19:14:24 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 11 Apr 2024 19:22:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 11 Apr 2024 19:22:12 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 11 Apr 2024 19:22:13 GMT
RUN docker-php-ext-enable sodium
# Thu, 11 Apr 2024 19:22:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Apr 2024 19:22:14 GMT
WORKDIR /var/www/html
# Thu, 11 Apr 2024 19:22:14 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 11 Apr 2024 19:22:14 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Apr 2024 19:22:14 GMT
EXPOSE 9000
# Thu, 11 Apr 2024 19:22:14 GMT
CMD ["php-fpm"]
# Fri, 03 May 2024 01:03:10 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN set -eux; 	version='6.5.3-RC1'; 	sha1='e46f50a3878d59e1130a13be650f5b32577edee9'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Fri, 03 May 2024 01:03:10 GMT
VOLUME [/var/www/html]
# Fri, 03 May 2024 01:03:10 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Fri, 03 May 2024 01:03:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 May 2024 01:03:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 May 2024 01:03:10 GMT
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
	-	`sha256:0150bd92669e20735014cc4cdd3025dcc133ddf84e3c341b7e4845924574ebd5`  
		Last Modified: Thu, 11 Apr 2024 19:48:30 GMT  
		Size: 12.1 MB (12110598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:036a86a4ae3854aafbc2f0d72aabcbef83490743d20012002547de8270618662`  
		Last Modified: Thu, 11 Apr 2024 19:48:29 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d2a8eea798d655cbdbe974e0eac6057c5eda6b8ae68f0ae5887b539f340d3c`  
		Last Modified: Thu, 11 Apr 2024 19:48:56 GMT  
		Size: 15.4 MB (15426830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23484683932f65e3cd2a534782c9fb58f3055c23421557499b38f294ada7cdc9`  
		Last Modified: Thu, 11 Apr 2024 19:48:54 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f832e65336554dcff623b4dc40273aae13cb3e3e7988846186ce9be459cb6f`  
		Last Modified: Thu, 11 Apr 2024 19:48:53 GMT  
		Size: 19.3 KB (19298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b483e4a592eb1d0de70f9bfa94948ad779e9d9896be878157c81dec27dc2ef20`  
		Last Modified: Thu, 11 Apr 2024 19:48:54 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e9730c53d5d9dccd171546c92e516b5d8cf1ac6f9983daa373c063e5aeb545`  
		Last Modified: Mon, 06 May 2024 23:06:26 GMT  
		Size: 28.6 MB (28646242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67583be7df02cdd32f94d4755b3dcd6d08435bff9b491de6d913ec205bc77a3e`  
		Last Modified: Mon, 06 May 2024 23:06:26 GMT  
		Size: 3.8 MB (3754405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d97b9d3e06b921510ec4bdc1355e3ec20f7eaa75f22a08789ecc4f02c325857d`  
		Last Modified: Mon, 06 May 2024 23:06:26 GMT  
		Size: 59.4 KB (59393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cddf5385540b815d70f707508365a418eb89c4012ba3edc0f4e77de92719f157`  
		Last Modified: Mon, 06 May 2024 23:06:26 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40708bbfdf9a85a7363eec03b98bf2e25b2cf197de006f7c0b5ed1ea7190cfd2`  
		Last Modified: Mon, 06 May 2024 23:06:27 GMT  
		Size: 24.5 MB (24528109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72c3ce42773085c2654b58e36ae62cf3a0600a1974bc39982360b9e34e9d13a`  
		Last Modified: Mon, 06 May 2024 23:06:27 GMT  
		Size: 2.3 KB (2343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c14574bd21a83b039442747de3fd03ba5e215d61bec03e0ff357d2890976aa5`  
		Last Modified: Mon, 06 May 2024 23:06:27 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:51216c66822041a732bd003599c07a97725ee0ea5c2e1d50c1a7a2a9d7950efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1063703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b91b3700e4cf9dfbe9fcf71c3c788b6cb360f50033f1f172c6ff24dea30ddf6`

```dockerfile
```

-	Layers:
	-	`sha256:1df19e9b52fd2096d849b8733ef775edcd25092aaaf019bc6e689c7d40b334ec`  
		Last Modified: Mon, 06 May 2024 23:06:26 GMT  
		Size: 1.0 MB (1013313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9d11a424d3e9533df13c0d841e262499a34daf927a9e5a9bf5402059a3a72be`  
		Last Modified: Mon, 06 May 2024 23:06:26 GMT  
		Size: 50.4 KB (50390 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6-php8.2-fpm-alpine` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:54980d73b1cd44f98b35587d2701a1d86ef24c578c163299804c29baf105a7ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 MB (88411333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435f668b6006c23e2f106be3782b18d5299aba7e876a3d07beacddc6cc86e7f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 23:49:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Mar 2024 23:49:30 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 15 Mar 2024 23:49:31 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Mar 2024 23:49:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Mar 2024 23:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 15 Mar 2024 23:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Mar 2024 23:49:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Mar 2024 23:49:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 16 Mar 2024 00:12:18 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 11 Apr 2024 21:42:59 GMT
ENV PHP_VERSION=8.2.18
# Thu, 11 Apr 2024 21:42:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.18.tar.xz.asc
# Thu, 11 Apr 2024 21:42:59 GMT
ENV PHP_SHA256=44b306fc021e56441f691da6c3108788bd9e450f293b3bc70fcd64b08dd41a50
# Thu, 11 Apr 2024 21:43:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 11 Apr 2024 21:43:08 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 11 Apr 2024 21:50:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 11 Apr 2024 21:50:38 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 11 Apr 2024 21:50:39 GMT
RUN docker-php-ext-enable sodium
# Thu, 11 Apr 2024 21:50:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Apr 2024 21:50:40 GMT
WORKDIR /var/www/html
# Thu, 11 Apr 2024 21:50:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 11 Apr 2024 21:50:41 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Apr 2024 21:50:41 GMT
EXPOSE 9000
# Thu, 11 Apr 2024 21:50:41 GMT
CMD ["php-fpm"]
# Fri, 03 May 2024 01:03:10 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN set -eux; 	version='6.5.3-RC1'; 	sha1='e46f50a3878d59e1130a13be650f5b32577edee9'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Fri, 03 May 2024 01:03:10 GMT
VOLUME [/var/www/html]
# Fri, 03 May 2024 01:03:10 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Fri, 03 May 2024 01:03:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 May 2024 01:03:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 May 2024 01:03:10 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59be61bd2ba9f18af71b96c422917e0014880c902aa3ccb7f8257383b11b69ac`  
		Last Modified: Sat, 16 Mar 2024 01:01:12 GMT  
		Size: 2.8 MB (2764506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95722804161331c4c8c5fb5c67c2930e7f200746da0b87efc2cc1ca230b2bdf`  
		Last Modified: Sat, 16 Mar 2024 01:01:11 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9405a5b710e6142fb5b24b32edc3d286164167c9a50bc8d571a93dba40d73564`  
		Last Modified: Sat, 16 Mar 2024 01:01:10 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566790e68d663eaf96c105e0150d25b1183a063bc2714e8f892c8da6c26b0e4f`  
		Last Modified: Thu, 11 Apr 2024 22:07:08 GMT  
		Size: 12.1 MB (12110628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ba6664fd8c3e1cf575cc10362d111588ce5ae7b8fe7e95f359bcde6ab7486d`  
		Last Modified: Thu, 11 Apr 2024 22:07:06 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c56f40591de6dd04c863dcfae0fba405642c0b55c6928417747eb4f690cbf6`  
		Last Modified: Thu, 11 Apr 2024 22:07:36 GMT  
		Size: 14.0 MB (13967300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ab2eecacd3bfb3f074d7abd1baf7e60fe1acb0c4d5207a854f747bdf2cd37c`  
		Last Modified: Thu, 11 Apr 2024 22:07:33 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85af8acd63ec9ecad2462279f0396fdde1f2462168068aeecd4edb6e5bda00d`  
		Last Modified: Thu, 11 Apr 2024 22:07:32 GMT  
		Size: 19.2 KB (19152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da8e75d2b34769c8cc98bf7fe0456c0d90f41b117e702d02ba34c9ff8e944e0`  
		Last Modified: Thu, 11 Apr 2024 22:07:33 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c30698cc8277fcf47a226bcf7414453587f1a396a027dcac114b00afd3b120`  
		Last Modified: Mon, 06 May 2024 23:19:13 GMT  
		Size: 28.2 MB (28172759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95f6d9658b905d05d393fce5d1ae913eefc92d3637190ebe65ad279b391d30b`  
		Last Modified: Mon, 06 May 2024 23:19:12 GMT  
		Size: 3.6 MB (3605943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481c476028ab7c605c9379868f56a3c4447c05d389396ec97fe29b3e09e7786c`  
		Last Modified: Mon, 06 May 2024 23:19:12 GMT  
		Size: 59.4 KB (59423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eee7d2a5206a1dafdb7f8e37501a0099c10a23334035715e94d8802cd13dfbb`  
		Last Modified: Mon, 06 May 2024 23:19:12 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1c8c15ec0ce0bbfbe7436a8850d8147259c06339970ad28dd1856bd92bf54f`  
		Last Modified: Mon, 06 May 2024 23:19:14 GMT  
		Size: 24.5 MB (24528108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402d8f1ee076c32e2267ed26ffd671065abe771fc5d08fe70ca63f70ad6971cb`  
		Last Modified: Mon, 06 May 2024 23:19:13 GMT  
		Size: 2.3 KB (2345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbf3aaea498ea731c148031a09aa9dd8e3f32be7a531cb0e897ea3c6c22ffcb`  
		Last Modified: Mon, 06 May 2024 23:19:13 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:75e87ca33e62341225d57cd304b41e75207355f76c37b661229b69f0a1ba82e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 KB (50341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b845102ecb00b3d9c7a630eca57e1f7a31fcc9125184f59f1c1ddb51b0b22206`

```dockerfile
```

-	Layers:
	-	`sha256:788a282e4e39dc29e6b9928b618255ead0d18dcbdb6ff0ac5c088ac0b33dcf41`  
		Last Modified: Mon, 06 May 2024 23:19:11 GMT  
		Size: 50.3 KB (50341 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6-php8.2-fpm-alpine` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:04da7342a29d390adc33a062118dee5837c4c3507cb24bad1070b6bbf8427024
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85588652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:845d05aaec424a71de3940684a5b8b030f649b04a36096c73520aa34a47f5d31`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 09:01:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 16 Mar 2024 09:01:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 16 Mar 2024 09:01:15 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 16 Mar 2024 09:01:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 16 Mar 2024 09:01:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 16 Mar 2024 09:01:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 16 Mar 2024 09:01:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 16 Mar 2024 09:01:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 16 Mar 2024 09:39:19 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 11 Apr 2024 21:10:27 GMT
ENV PHP_VERSION=8.2.18
# Thu, 11 Apr 2024 21:10:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.18.tar.xz.asc
# Thu, 11 Apr 2024 21:10:27 GMT
ENV PHP_SHA256=44b306fc021e56441f691da6c3108788bd9e450f293b3bc70fcd64b08dd41a50
# Thu, 11 Apr 2024 21:10:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 11 Apr 2024 21:10:35 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 11 Apr 2024 21:16:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 11 Apr 2024 21:16:15 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 11 Apr 2024 21:16:18 GMT
RUN docker-php-ext-enable sodium
# Thu, 11 Apr 2024 21:16:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Apr 2024 21:16:19 GMT
WORKDIR /var/www/html
# Thu, 11 Apr 2024 21:16:20 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 11 Apr 2024 21:16:20 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Apr 2024 21:16:21 GMT
EXPOSE 9000
# Thu, 11 Apr 2024 21:16:21 GMT
CMD ["php-fpm"]
# Fri, 03 May 2024 01:03:10 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN set -eux; 	version='6.5.3-RC1'; 	sha1='e46f50a3878d59e1130a13be650f5b32577edee9'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Fri, 03 May 2024 01:03:10 GMT
VOLUME [/var/www/html]
# Fri, 03 May 2024 01:03:10 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Fri, 03 May 2024 01:03:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 May 2024 01:03:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 May 2024 01:03:10 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24a3155a604085efaa4c70bd2859739b6141d4fd0670fa3e15fd67cab1a2154`  
		Last Modified: Sat, 16 Mar 2024 11:00:26 GMT  
		Size: 2.6 MB (2612666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91bbcf35c6eddf26fa13dc8c811f2ac147d03bba1af2fa37c43084f218a04ca`  
		Last Modified: Sat, 16 Mar 2024 11:00:25 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb37d0aeb5ad8612608d36edcbe0f65f4004674effbc82dceac7fda7895b9f1`  
		Last Modified: Sat, 16 Mar 2024 11:00:25 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff653f071660a0ab48dcc56b09d61cd662571ebadd7e1425a30f9dbfec01678`  
		Last Modified: Thu, 11 Apr 2024 21:42:11 GMT  
		Size: 12.1 MB (12110618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9900e6e2b6f7c11595e4ed3dc78eed5776b38a5a01ace652a8638f28d408fe`  
		Last Modified: Thu, 11 Apr 2024 21:42:10 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e99401eac7b65caa473d5b037785810ad6768f5dbd9668c19766fe40f5751e`  
		Last Modified: Thu, 11 Apr 2024 21:42:39 GMT  
		Size: 13.1 MB (13075941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b770b3f229aaf431c88b0998dabe5810ff8e540be2a65f8ed7468885fc96a65`  
		Last Modified: Thu, 11 Apr 2024 21:42:36 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091062f1b890c444830211b9e1d852730beefec2f1341a0e92ad2025ea50b616`  
		Last Modified: Thu, 11 Apr 2024 21:42:37 GMT  
		Size: 19.1 KB (19116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb172fce9a96395d0895e16b595c073427caed719cecef482f1243f095ccdd3a`  
		Last Modified: Thu, 11 Apr 2024 21:42:36 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac9214c3c7cb1f5497356c6169b4dc5679e071e2da3c30bbca7d4526c00902d`  
		Last Modified: Tue, 07 May 2024 00:21:17 GMT  
		Size: 26.6 MB (26604493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72cd8ae5a15775a077234693d368810444443eda7ec1634ebf63a153eaa9f6d2`  
		Last Modified: Tue, 07 May 2024 00:21:17 GMT  
		Size: 3.6 MB (3641285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed185ce8d449b17ffd9f8adf0d9021b2a0e0d283e3142617691a9c5f26542331`  
		Last Modified: Tue, 07 May 2024 00:21:16 GMT  
		Size: 59.4 KB (59411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:746ef276404c668676763b8719fa7a8b6eebded0899b59454f912615b6074904`  
		Last Modified: Tue, 07 May 2024 00:21:16 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14c5a6d34ee4d1113c94761950b1450ced3b268e636ebcf3cdec8a5a441aad0`  
		Last Modified: Tue, 07 May 2024 00:21:18 GMT  
		Size: 24.5 MB (24528103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb5f05bedbbe6693f1ce1518a31090350a715fd9539f82567e891c3405f1f5b`  
		Last Modified: Tue, 07 May 2024 00:21:17 GMT  
		Size: 2.3 KB (2347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7875c7436fe63d7d848d15aba9e589b628545c70c7a6566f7b3497795b41528`  
		Last Modified: Tue, 07 May 2024 00:21:18 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:5221fd68db4179b857eefed79c016e1740fe136567a10a3937986dd82cd8d402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1062332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2755d9a89ad729824ff673639baba1f54ac097ce930c614a19bce1596f72e54a`

```dockerfile
```

-	Layers:
	-	`sha256:cd8701f301ee680797e00a00d377d3471f4bc993b22e568b33e29643eb9c39ea`  
		Last Modified: Tue, 07 May 2024 00:21:16 GMT  
		Size: 1.0 MB (1013397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5e1f68587ab59ea9dba92fa48f2bd96a998952155a78a217da8cac653d64042`  
		Last Modified: Tue, 07 May 2024 00:21:16 GMT  
		Size: 48.9 KB (48935 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6-php8.2-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:46adfd626c22bd8803a8e362b05782b2d8b991c2e6dee1ad9967ec2a0bae1aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 MB (88387874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9f862f84a8e1a883e78c1c09b777a4f032f63a766b6bfe3b5540237cfeb38c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 00:36:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 16 Mar 2024 00:36:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 16 Mar 2024 00:36:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 16 Mar 2024 00:36:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 16 Mar 2024 00:36:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 16 Mar 2024 00:36:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 16 Mar 2024 00:36:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 16 Mar 2024 00:36:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 16 Mar 2024 01:26:54 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 16 Mar 2024 01:26:54 GMT
ENV PHP_VERSION=8.2.17
# Sat, 16 Mar 2024 01:26:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.17.tar.xz.asc
# Sat, 16 Mar 2024 01:26:54 GMT
ENV PHP_SHA256=1cc4ef733ba58f6557db648012471f1916e5bac316303aa165535bedab08ee35
# Sat, 16 Mar 2024 01:27:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 16 Mar 2024 01:27:01 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 16 Mar 2024 01:34:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 16 Mar 2024 01:34:29 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 16 Mar 2024 01:34:30 GMT
RUN docker-php-ext-enable sodium
# Sat, 16 Mar 2024 01:34:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 16 Mar 2024 01:34:30 GMT
WORKDIR /var/www/html
# Sat, 16 Mar 2024 01:34:30 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 16 Mar 2024 01:34:30 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Mar 2024 01:34:30 GMT
EXPOSE 9000
# Sat, 16 Mar 2024 01:34:30 GMT
CMD ["php-fpm"]
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -eux; 	version='6.5-RC4'; 	sha1='2c93035e42009d5ae37ee5be7e6738e1dfa04102'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
VOLUME [/var/www/html]
# Thu, 28 Mar 2024 19:03:12 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 19:03:12 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af252c8885a7ef2b1e85bce006efb30a7c8fb938ae8b50557ac99f551db6347d`  
		Last Modified: Sat, 16 Mar 2024 02:17:26 GMT  
		Size: 2.8 MB (2815736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41380dbb2574885d6efd5d44c03067af395ce0303f74e6aa7a08b639904dfb09`  
		Last Modified: Sat, 16 Mar 2024 02:17:26 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0a53e1b8079d8de445a7d2739eb1b065a4df2f537d45e8ceaeeb4469bc61a2`  
		Last Modified: Sat, 16 Mar 2024 02:17:26 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1961129304a9e56071b3989396314104deec7f57f4ec58e2de45374508733ffd`  
		Last Modified: Sat, 16 Mar 2024 02:21:55 GMT  
		Size: 12.1 MB (12113513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f5a93d7cf2072d6ddd072d0c166baa5e29647d2657ed4fd6b50f6354d03999`  
		Last Modified: Sat, 16 Mar 2024 02:21:54 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3d94b2545fd86a41d944d2eff187b10c5151d5d5b902151083fd3e0f34a872`  
		Last Modified: Sat, 16 Mar 2024 02:22:18 GMT  
		Size: 12.9 MB (12913110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67218c81d7ccaffa5cdcf6f5a5d3c6f2b570ad1ace716a79563bc9599a37660d`  
		Last Modified: Sat, 16 Mar 2024 02:22:16 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7aaf86ae784c3f102a655411104555cc858e6de4271868aafb2ed57813b644`  
		Last Modified: Sat, 16 Mar 2024 02:22:17 GMT  
		Size: 19.1 KB (19091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1686e682d675c78c25ab78d81c76d6845f30378b3401153dae89d7540da69975`  
		Last Modified: Sat, 16 Mar 2024 02:22:16 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5ce7d853c92a66340baf920d13c1537496cfe3c55a3e21b777f4e000331f5d`  
		Last Modified: Sat, 16 Mar 2024 19:18:50 GMT  
		Size: 28.8 MB (28770893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3fda6792770be4be662223bda515285ef650202e18840445a9a99bcb0079200`  
		Last Modified: Sat, 16 Mar 2024 19:18:50 GMT  
		Size: 3.8 MB (3805003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980d77fa7b69d68f4c04c463a4c146ebc567d1e61ae85959bfb79ea7579ce9e5`  
		Last Modified: Sat, 16 Mar 2024 19:18:49 GMT  
		Size: 59.4 KB (59362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb8ace0a8a524a9938d16b768e3f99d2615791372601502fe21f8fa691f6861`  
		Last Modified: Sat, 16 Mar 2024 19:18:49 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7654c0c3e5fb570b2e726a18df45bab3930de4dd35efc0844b59c873fd02fa72`  
		Last Modified: Fri, 29 Mar 2024 00:55:26 GMT  
		Size: 24.5 MB (24525320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ef5b9d68c7aa6aba20f18d6dd49c617c340855673cb05b8fb7eef8474b0caa`  
		Last Modified: Fri, 29 Mar 2024 00:55:25 GMT  
		Size: 2.4 KB (2352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4575a789ab4945659cecead8ea90b5df556a8c6c43ea97fe629e6d781e22530`  
		Last Modified: Fri, 29 Mar 2024 00:55:25 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:9572f050e52bb94af3370d641a5ac1f3032a7e6850bf368ec58c8ae682daceb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1060721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73b131dc02a434fde02897ccdda37a18c0da5a91c1a8fb02a25681e5f2b335be`

```dockerfile
```

-	Layers:
	-	`sha256:be881ae0132183a3be5977eaed610d4ab4bd82c1d20d959881b52cda46239734`  
		Last Modified: Fri, 29 Mar 2024 00:55:25 GMT  
		Size: 1.0 MB (1012638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9ab9f0926fa207ae0c27418c5c65bcc3d95e3c819a69386d05d824d47482148`  
		Last Modified: Fri, 29 Mar 2024 00:55:25 GMT  
		Size: 48.1 KB (48083 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6-php8.2-fpm-alpine` - linux; 386

```console
$ docker pull wordpress@sha256:415fa8e674e0f09a0d5e29fadc269dbee4db5da28f7a9275a694c25e88965101
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91202288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97a281ad8fa45f001558b85b13c7cd75fd01632cf4dc1db97d0c42db92ef8aa6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 01:59:39 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 16 Mar 2024 01:59:41 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 16 Mar 2024 01:59:42 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 16 Mar 2024 01:59:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 16 Mar 2024 01:59:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 16 Mar 2024 01:59:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 16 Mar 2024 01:59:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 16 Mar 2024 01:59:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 16 Mar 2024 03:31:37 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 11 Apr 2024 20:02:45 GMT
ENV PHP_VERSION=8.2.18
# Thu, 11 Apr 2024 20:02:45 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.18.tar.xz.asc
# Thu, 11 Apr 2024 20:02:45 GMT
ENV PHP_SHA256=44b306fc021e56441f691da6c3108788bd9e450f293b3bc70fcd64b08dd41a50
# Thu, 11 Apr 2024 20:02:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 11 Apr 2024 20:02:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 11 Apr 2024 20:16:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 11 Apr 2024 20:16:35 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 11 Apr 2024 20:16:36 GMT
RUN docker-php-ext-enable sodium
# Thu, 11 Apr 2024 20:16:37 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Apr 2024 20:16:37 GMT
WORKDIR /var/www/html
# Thu, 11 Apr 2024 20:16:37 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 11 Apr 2024 20:16:37 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Apr 2024 20:16:38 GMT
EXPOSE 9000
# Thu, 11 Apr 2024 20:16:38 GMT
CMD ["php-fpm"]
# Fri, 03 May 2024 01:03:10 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN set -eux; 	version='6.5.3-RC1'; 	sha1='e46f50a3878d59e1130a13be650f5b32577edee9'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Fri, 03 May 2024 01:03:10 GMT
VOLUME [/var/www/html]
# Fri, 03 May 2024 01:03:10 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Fri, 03 May 2024 01:03:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 May 2024 01:03:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 May 2024 01:03:10 GMT
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
	-	`sha256:75de9c825fa1be5ff06416830da1dc4e3861e5d73ab0dc50e856aa686de38931`  
		Last Modified: Thu, 11 Apr 2024 20:55:36 GMT  
		Size: 12.1 MB (12110618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:863c35f4dd5d82776e3238ed77c6b0b4a195c4a2ffa90d06a6dda9ec36986684`  
		Last Modified: Thu, 11 Apr 2024 20:55:34 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:661616b4153c68aa105d710623a6595f8e44dcfa7504d1a6be4fff06dcc7bc3b`  
		Last Modified: Thu, 11 Apr 2024 20:56:07 GMT  
		Size: 15.6 MB (15597269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1521b33089d06e61ec2271e5426ea1a4d164818c1fb668d5b2a6aa4a65533d3`  
		Last Modified: Thu, 11 Apr 2024 20:56:03 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8e8a5d0a548bdbde61f23d149b31f809c4a7cad219f100543482526401e799`  
		Last Modified: Thu, 11 Apr 2024 20:56:03 GMT  
		Size: 19.3 KB (19301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6758c44085440787ee5c7a5b844bacc28ea497e2338ec898fcbbfb530a59688`  
		Last Modified: Thu, 11 Apr 2024 20:56:03 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0569e813f84ad11115ae095fa697182704904a93786f4569c147eeb45c7ce7a8`  
		Last Modified: Mon, 06 May 2024 23:06:46 GMT  
		Size: 28.9 MB (28877148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7df55fa7627e9964e45f40d160a270ca4073372577f1ae62151a776b5fdcba8`  
		Last Modified: Mon, 06 May 2024 23:06:45 GMT  
		Size: 3.9 MB (3922893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ee990b63ba0ccefc2b04b63a93722495ed9a29e43a74712ff068000498fac9`  
		Last Modified: Mon, 06 May 2024 23:06:45 GMT  
		Size: 59.4 KB (59395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab79851871fe598da84c4763c54568255bae997a6ee4f8cbb05b1c936a4d7ae9`  
		Last Modified: Mon, 06 May 2024 23:06:44 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:452a761e0c54bf6a9c05627a03fc6e84af65b5aced8446cf90eb634504a26913`  
		Last Modified: Mon, 06 May 2024 23:06:47 GMT  
		Size: 24.5 MB (24528119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a625681ab7c1331a79eaca5a3fde29804e39d64ce14437b43f15cbff777e998`  
		Last Modified: Mon, 06 May 2024 23:06:46 GMT  
		Size: 2.3 KB (2347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65a3aa823f278fd9af372a6b63c692958e12ea9dc1c1aeaac4ec4b243ee56d3`  
		Last Modified: Mon, 06 May 2024 23:06:46 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:a8addc02481c8c72d024a870d71d5559da7db59dc99b540b445adbe0ed6c3f29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1063580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f2b7bc1730684d75e78f7f1f023e93a25b5026ed1fded4a5a5733329c30e3f8`

```dockerfile
```

-	Layers:
	-	`sha256:5b43dffbecfb2405295205c171171e9c0dade0542e63d6d461d5818fc43d22d9`  
		Last Modified: Mon, 06 May 2024 23:06:44 GMT  
		Size: 1.0 MB (1013258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:15fb721d9b58e6cdf43b1fe350b660c5d75a0b3f644e37303ae493d5bf403027`  
		Last Modified: Mon, 06 May 2024 23:06:45 GMT  
		Size: 50.3 KB (50322 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6-php8.2-fpm-alpine` - linux; ppc64le

```console
$ docker pull wordpress@sha256:a4cca4f4d0bc68bfda3aa7c93355616d66624d24200cfbf9e10c12b35dc6643c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89573185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862201455a75cbff946d3d6d18ad9180ec68ae35e53a03fc0d2a2e02c55d77c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:32:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 16 Mar 2024 05:32:10 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 16 Mar 2024 05:32:11 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 16 Mar 2024 05:32:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 16 Mar 2024 05:32:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 16 Mar 2024 05:32:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 16 Mar 2024 05:32:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 16 Mar 2024 05:32:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 16 Mar 2024 06:15:55 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 16 Mar 2024 06:15:56 GMT
ENV PHP_VERSION=8.2.17
# Sat, 16 Mar 2024 06:15:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.17.tar.xz.asc
# Sat, 16 Mar 2024 06:15:56 GMT
ENV PHP_SHA256=1cc4ef733ba58f6557db648012471f1916e5bac316303aa165535bedab08ee35
# Sat, 16 Mar 2024 06:16:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 16 Mar 2024 06:16:05 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 16 Mar 2024 06:21:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 16 Mar 2024 06:21:23 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 16 Mar 2024 06:21:25 GMT
RUN docker-php-ext-enable sodium
# Sat, 16 Mar 2024 06:21:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 16 Mar 2024 06:21:26 GMT
WORKDIR /var/www/html
# Sat, 16 Mar 2024 06:21:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 16 Mar 2024 06:21:28 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Mar 2024 06:21:29 GMT
EXPOSE 9000
# Sat, 16 Mar 2024 06:21:29 GMT
CMD ["php-fpm"]
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -eux; 	version='6.5-RC4'; 	sha1='2c93035e42009d5ae37ee5be7e6738e1dfa04102'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
VOLUME [/var/www/html]
# Thu, 28 Mar 2024 19:03:12 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 19:03:12 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8351cc51b7233ca6780794a860d1cb9c98abff8e8277d2b87c1fafd5d06239d8`  
		Last Modified: Sat, 16 Mar 2024 06:55:33 GMT  
		Size: 2.8 MB (2842850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83541649479862a60e6e0a63881477379ac3ebccf9b657c4646de7eb1d4dc0f7`  
		Last Modified: Sat, 16 Mar 2024 06:55:32 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b3f7fb8aafed95ce8f9c79f9af65ce6e4439edfd71c1ba169b88443d61e05a`  
		Last Modified: Sat, 16 Mar 2024 06:55:32 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095e8023220b266f01152cf2f07a609f6efea7d540ce1241b802e17169cfbf6e`  
		Last Modified: Sat, 16 Mar 2024 07:01:00 GMT  
		Size: 12.1 MB (12113519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f99c2e90dd3010ebdd1bd0666b5618166f0804822beb402b9e29f7a0d6c573`  
		Last Modified: Sat, 16 Mar 2024 07:00:59 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b932d1477133fb91aa1824fd4a9a98fadf55964c1374912f118d152129a7c2`  
		Last Modified: Sat, 16 Mar 2024 07:01:30 GMT  
		Size: 13.3 MB (13340672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8c26f8c26194524ea482733e6245a47a9251075f4b2a05f875dff2c5c1eab8`  
		Last Modified: Sat, 16 Mar 2024 07:01:27 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11a9c70051f3f297fd7448021dd50e5c18a4832f4a8f7251e924cea995e054f`  
		Last Modified: Sat, 16 Mar 2024 07:01:27 GMT  
		Size: 19.1 KB (19111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0a4842e7bc51beaf585e0e8a67f421049d0976f1599eeb212ffd003515aae3`  
		Last Modified: Sat, 16 Mar 2024 07:01:27 GMT  
		Size: 9.2 KB (9175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06a63aec4ad0644573f008fb233157b08141ce82f3eb18cef81270c0db90121`  
		Last Modified: Sat, 16 Mar 2024 15:27:48 GMT  
		Size: 29.4 MB (29379301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a24bcfd51231a9b2ca7163378ae73e37ce2f9214cd7fb1e56d72dd50c754da8`  
		Last Modified: Sat, 16 Mar 2024 15:27:48 GMT  
		Size: 3.9 MB (3916512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ea899cb06d80e4df282f1041d6aeef97dd367eb5e7c45d2b9d0f62a13f9a5d`  
		Last Modified: Sat, 16 Mar 2024 15:27:47 GMT  
		Size: 59.4 KB (59413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce2aac5febc7d3a7fa62817514035af616e239064ed604649e5ea6731f7184b`  
		Last Modified: Sat, 16 Mar 2024 15:27:47 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701bfe61a7923fce42064080fb1f0470e93cdfd9e4d7e0c32961f11234120271`  
		Last Modified: Fri, 29 Mar 2024 01:17:25 GMT  
		Size: 24.5 MB (24525323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92873fa2d306cefd631da58acf29b9c82c49f185fd4149626e6ef62eb471a3a`  
		Last Modified: Fri, 29 Mar 2024 01:17:24 GMT  
		Size: 2.4 KB (2353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d8fe0473dc326a35ab165398ba032a9e7792d59de7f78566a7b63df065ec78`  
		Last Modified: Fri, 29 Mar 2024 01:17:24 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:1990a0e7c8f8d3ac23b628f80040caf2a900e470f7149c457b6467817f11f52d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1058858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:321b273626168ca941e3b23819e4c5dd0824e1e008a1224090dbd0ff3cf72d38`

```dockerfile
```

-	Layers:
	-	`sha256:b0a55c1ff54cc6335e4f76c45dadd3602d599c67cc7d4eefe5149556b4d4db9c`  
		Last Modified: Fri, 29 Mar 2024 01:17:24 GMT  
		Size: 1.0 MB (1010723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86e10f139eaff8e74fe6f1f200998ba9966cdae306e7e4ac09231c12d715c6fa`  
		Last Modified: Fri, 29 Mar 2024 01:17:23 GMT  
		Size: 48.1 KB (48135 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6-php8.2-fpm-alpine` - linux; s390x

```console
$ docker pull wordpress@sha256:572a0bbcad20b6050a3be1e15ef4380d628f888254aa14d0435d11c6dff906d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.4 MB (91422552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19e662529b3fc6d1ee63d0650681ce1530ad658fcb6208442115658bdc1ca386`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 12:14:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 16 Mar 2024 12:14:23 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 16 Mar 2024 12:14:23 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 16 Mar 2024 12:14:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 16 Mar 2024 12:14:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 16 Mar 2024 12:14:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 16 Mar 2024 12:14:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 16 Mar 2024 12:14:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 16 Mar 2024 13:13:41 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 11 Apr 2024 22:39:05 GMT
ENV PHP_VERSION=8.2.18
# Thu, 11 Apr 2024 22:39:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.18.tar.xz.asc
# Thu, 11 Apr 2024 22:39:06 GMT
ENV PHP_SHA256=44b306fc021e56441f691da6c3108788bd9e450f293b3bc70fcd64b08dd41a50
# Thu, 11 Apr 2024 22:39:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 11 Apr 2024 22:39:14 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 11 Apr 2024 22:46:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 11 Apr 2024 22:46:44 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 11 Apr 2024 22:46:45 GMT
RUN docker-php-ext-enable sodium
# Thu, 11 Apr 2024 22:46:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Apr 2024 22:46:45 GMT
WORKDIR /var/www/html
# Thu, 11 Apr 2024 22:46:46 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 11 Apr 2024 22:46:46 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Apr 2024 22:46:46 GMT
EXPOSE 9000
# Thu, 11 Apr 2024 22:46:46 GMT
CMD ["php-fpm"]
# Fri, 03 May 2024 01:03:10 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Fri, 03 May 2024 01:03:10 GMT
RUN set -eux; 	version='6.5.3-RC1'; 	sha1='e46f50a3878d59e1130a13be650f5b32577edee9'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Fri, 03 May 2024 01:03:10 GMT
VOLUME [/var/www/html]
# Fri, 03 May 2024 01:03:10 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Fri, 03 May 2024 01:03:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 03 May 2024 01:03:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 May 2024 01:03:10 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01acb6f7038172bde2ff1bda8f1d1adcc1ab12d84810d2aa5acf1971fb749a71`  
		Last Modified: Sat, 16 Mar 2024 14:18:54 GMT  
		Size: 2.9 MB (2940586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce621a8f961e9b9055c4dc41216537b964b8ad5eea518ed588f6d169fba2dae`  
		Last Modified: Sat, 16 Mar 2024 14:18:53 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c74ef430cf1ac125831e6082e733c08a93c0954eddcb8ddb042b1c73977b0c9`  
		Last Modified: Sat, 16 Mar 2024 14:18:53 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401b5c15547dca65236380114e8c2665b255bf437f42d2d81bbe2f192d22d5a2`  
		Last Modified: Thu, 11 Apr 2024 23:35:37 GMT  
		Size: 12.1 MB (12110621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc5e34a3a07f679103f054fc76c2ca00b2851a1ba79d3361aefb10a54b6efee`  
		Last Modified: Thu, 11 Apr 2024 23:35:37 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:891a565ef9627834ba4d782694a9cb6e75ed926a39dddd085b6e4ca58e7ad230`  
		Last Modified: Thu, 11 Apr 2024 23:35:59 GMT  
		Size: 15.0 MB (14974702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b684f19a4427fbb3ea8f04ef0e1780dfd52ed5cf51f25ab67cc55da960ffd02`  
		Last Modified: Thu, 11 Apr 2024 23:35:56 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026c76094e49d460dc0bf02681276aeab9be64623484c5a12de4cce91fa53681`  
		Last Modified: Thu, 11 Apr 2024 23:35:56 GMT  
		Size: 19.1 KB (19123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53ef0838f3012886262f4254741bb84f28e92e8c07690bb9198b207b2cbb9949`  
		Last Modified: Thu, 11 Apr 2024 23:35:57 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0157f117b409d9610d0b95706c4d2e573675344b1083c17d562f78e3b313e523`  
		Last Modified: Sun, 14 Apr 2024 12:56:16 GMT  
		Size: 29.6 MB (29631203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b77deb536c6b0bfd585c07b449c2630fb0ce3eb9a6ea1fba7a61fc1ec95b60`  
		Last Modified: Sun, 14 Apr 2024 12:56:15 GMT  
		Size: 3.9 MB (3898047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5180e9644783fd1604c5d82d97de5469541bd7458faa771f4264897eb2c8e3f7`  
		Last Modified: Sun, 14 Apr 2024 12:56:15 GMT  
		Size: 59.4 KB (59419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07238378e92f175d38d85546fc35f0dccd8755d7822b5191c9c17f0bf64e2526`  
		Last Modified: Sun, 14 Apr 2024 12:56:15 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eebd31c20d04d76decd053e7e86dcaa6ec33be7735f78a7046fad32a75637ae2`  
		Last Modified: Tue, 07 May 2024 00:15:25 GMT  
		Size: 24.5 MB (24528091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a272b5839eecddcecce589823481cd5822218aa0da2693d5c2b87f2656f3a8b7`  
		Last Modified: Tue, 07 May 2024 00:15:25 GMT  
		Size: 2.4 KB (2350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497948306aa9e9a15aabc0fcdf95fa1a592de90c1c312932e95525d43bc695cb`  
		Last Modified: Tue, 07 May 2024 00:15:25 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:48aba9218fcf6439ab57026e77ee282e4428a748ffbc1ae8cfae8ef6c392b421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1060124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c08e5bb86ecea25b46c42d01bea52f7b5a576bef7ea08f72954bbd74212bf687`

```dockerfile
```

-	Layers:
	-	`sha256:ae4846c88d5f724cfdea7d7507859e245841b78b054d96b1ba8e08e8c13823c5`  
		Last Modified: Tue, 07 May 2024 00:15:25 GMT  
		Size: 1.0 MB (1011359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f877140b667f33dc5bdc8b0d54c45e80c768e8f6700dc3f331a1178a6853ed19`  
		Last Modified: Tue, 07 May 2024 00:15:25 GMT  
		Size: 48.8 KB (48765 bytes)  
		MIME: application/vnd.in-toto+json
