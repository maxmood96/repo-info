## `wordpress:beta-php8.2-fpm-alpine`

```console
$ docker pull wordpress@sha256:1f6c73ced2cc67597cac899df959ec83034c42fda738414ec5198bea13c16502
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

### `wordpress:beta-php8.2-fpm-alpine` - linux; amd64

```console
$ docker pull wordpress@sha256:a16843fde55df1c3295dce327c0bc2305583b4dd8edbaf697ebb6762078b5af4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.1 MB (97060462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24efb42d844a579eb668639587b7a501d2f3bf021995e0ec126409538a36426a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 31 Jul 2025 19:22:09 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
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
# Tue, 02 Dec 2025 01:15:56 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 02 Dec 2025 01:16:42 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:16:42 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:16:42 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:16:44 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:16:44 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:16:44 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:16:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:16:44 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:16:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:16:44 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fd7c6eefd35f4580755798ea7340e4f03c218ad93d6416dac46044b02a1ec6c`  
		Last Modified: Wed, 08 Oct 2025 23:36:37 GMT  
		Size: 3.5 MB (3463766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0d7b4192954e2fae4ab6deda7d3f2a5d03c221134d998a4b66fd56a2cc48d02`  
		Last Modified: Wed, 08 Oct 2025 23:36:37 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb12a823ec4ab42cfedddc3fbda1412035bb2fa181e638d833ec32221bcc0e86`  
		Last Modified: Wed, 08 Oct 2025 23:36:35 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fef2a36e2008a19bd46dd5f854dd66a427888cfe96f933c2a5105ce62e2959`  
		Last Modified: Wed, 08 Oct 2025 23:36:37 GMT  
		Size: 12.2 MB (12183661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bae90d9337e877f295eff7e0160a0befeb09a1ffc8dfcfaba606b2c3c76feea`  
		Last Modified: Wed, 08 Oct 2025 23:36:35 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4ce5fd74ba0c0be74b6af95ec0e6bbfcbefa5aabd4c8789244d8a6885b19de`  
		Last Modified: Wed, 08 Oct 2025 23:36:36 GMT  
		Size: 13.0 MB (13024560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66986873056476189f78f075df13fdeba7b3d7a80b33ccd811e217d113f4df4`  
		Last Modified: Wed, 08 Oct 2025 23:36:34 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95ba67a18eb5b6385904108cd9ad6229a16bc5f717a3daeb2e38a8886f4951bd`  
		Last Modified: Wed, 08 Oct 2025 23:36:34 GMT  
		Size: 20.1 KB (20075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5266aa323972b10cd763c1fc6e9b31efa71858d05fa70ed36ad44da6e96bca6b`  
		Last Modified: Wed, 08 Oct 2025 23:36:34 GMT  
		Size: 20.1 KB (20076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea260021112069d7ca69140f7f1224ac1c5e912ce7359f8e51102043bb738e0f`  
		Last Modified: Wed, 08 Oct 2025 23:36:34 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7fc58e242a5b6f56ed48afa48644e54140c27748387f9012f3a7b74a6932ac`  
		Last Modified: Tue, 02 Dec 2025 01:17:22 GMT  
		Size: 28.3 MB (28282766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1346cdc968452d0ae774d77e21193d51fd5082fe7d3981684670b6ea2901f9f7`  
		Last Modified: Tue, 02 Dec 2025 01:17:19 GMT  
		Size: 9.2 MB (9219512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61830fa44b4d41b607a3ab88e93d2c3b1327a5074a843086015976e853f7d75`  
		Last Modified: Tue, 02 Dec 2025 01:17:18 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24865fcaac1d3fc59a2b5be529874f4a90d721ee642f6f406cd754f9562f1ed0`  
		Last Modified: Tue, 02 Dec 2025 01:17:19 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef7f9773af374a799b1c75c213a506c14c3d9fcde3cb454c50042e4aaa62688`  
		Last Modified: Tue, 02 Dec 2025 01:17:21 GMT  
		Size: 27.0 MB (27025200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061131e697bca5fac2238329bfcc1db0cc11a737ab2371bd95e0617e07b23fa2`  
		Last Modified: Tue, 02 Dec 2025 01:17:18 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a988e2e8740e2e49b61a6ec091e45f88a3106700e015921c3880f1e8dc494b3`  
		Last Modified: Tue, 02 Dec 2025 01:17:18 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c53423c34c2b5e26e93b480a1246402c609610ac538bd56b8a67aab6e543246`  
		Last Modified: Tue, 02 Dec 2025 01:17:19 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:d3dfb5c6f9774433bc22731bdd662558d55fed237877994d6204426784e89f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1133539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:579b80da2629ec34343f645fca77cad589f59909b1ab91afb92454ee9945d0a7`

```dockerfile
```

-	Layers:
	-	`sha256:4dbf13e4dfbd70df75f1b87cad42a0573950acd40bb2ee6261f43267ec3f4d46`  
		Last Modified: Tue, 02 Dec 2025 02:27:07 GMT  
		Size: 1.1 MB (1081771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:406746cd6326bdf8963f0c5039f327f7397d65d19648852756237f7a016fb700`  
		Last Modified: Tue, 02 Dec 2025 02:27:07 GMT  
		Size: 51.8 KB (51768 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.2-fpm-alpine` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:8ae8ecf084a8f10efc967a0afa190d9e9e4ec8738555ba9350bfc0ed5d941f04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.0 MB (89993033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69bc5ceac40a772ad44eecb39320d7640616fceed46f72cd6602fb3d733bc71b`
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
# Tue, 02 Dec 2025 01:14:47 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 02 Dec 2025 01:16:00 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:16:00 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:16:00 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:16:02 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:16:02 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:16:02 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:16:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:16:02 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:16:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:16:02 GMT
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
	-	`sha256:ddcd48be71496f787aa60ca402101168562f7d3c3ecaea117a94e9adc7752eaf`  
		Last Modified: Tue, 02 Dec 2025 01:16:40 GMT  
		Size: 24.4 MB (24377238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a532cf08c5b09e3e9d56ffc0ebcd80602db155a92bacbfbcf7e85abfd174f309`  
		Last Modified: Tue, 02 Dec 2025 01:16:33 GMT  
		Size: 7.7 MB (7653587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d1ffc531194b6d0864c9aab95dd5e1d447b4d702f9006a613cab25f313240df`  
		Last Modified: Tue, 02 Dec 2025 01:16:33 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62ad78dbf37980760071d3596804299a7c207c544190cd4d1f802502a9342d4`  
		Last Modified: Tue, 02 Dec 2025 01:16:33 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e06cf042bebbcb77151ddc832967d616999e1e80c50fdaf416366321b47bdd`  
		Last Modified: Tue, 02 Dec 2025 01:16:35 GMT  
		Size: 27.0 MB (27025200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89d5a8e81573a934a720b6965ceb7601b7d1a7e71d641771d1f619c97a5b5c0c`  
		Last Modified: Tue, 02 Dec 2025 01:16:33 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10eb4dde6dc68167398cdf42f41f4f7248afdd17ecf3d12f81eac3ac970ce5e4`  
		Last Modified: Tue, 02 Dec 2025 01:16:33 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5127856b7eab396548c4ebd1deadaec1387fe4b57404e322c9ff7d9f7955716f`  
		Last Modified: Tue, 02 Dec 2025 01:16:33 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:3051920ee51c7ce98defda1a0320f3a74e0d61d4feeda64b967393e36600c388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 KB (51699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aaa6ae51b6c6210b889acfdd21c8193a199682388812542a9488da6538e5fb2`

```dockerfile
```

-	Layers:
	-	`sha256:78c14ef1de1eb757911b08e129e8872bf92d11436c5d514ce1c7eb422f6f8873`  
		Last Modified: Tue, 02 Dec 2025 02:27:11 GMT  
		Size: 51.7 KB (51699 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.2-fpm-alpine` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:d9c469772b096a8ddf240a2e0da211cd2f55ed4a71e156356972a7ce99a6c8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88715621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c01d73bb10791a631afca9c8aa29e28d2a660d09b67a4c0a4c0829294377c5f`
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
# Tue, 02 Dec 2025 01:19:17 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 02 Dec 2025 01:20:25 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:20:25 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:20:25 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:20:27 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:20:27 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:20:27 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:20:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:20:27 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:20:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:20:27 GMT
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
	-	`sha256:3882528af62e9c23aa26e7bcd6e7f052565d2334070e2cb25ed1d364e82320d8`  
		Last Modified: Tue, 02 Dec 2025 01:21:04 GMT  
		Size: 23.2 MB (23152258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283c4714442bd85500e0e69b5175fa45ad941807c0ecd60b68bb81929e7de96b`  
		Last Modified: Tue, 02 Dec 2025 01:20:57 GMT  
		Size: 8.8 MB (8756373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:385f163df55b914d20c4ce2333bce5521a0fc6dbc30469dca837faf90c640215`  
		Last Modified: Tue, 02 Dec 2025 01:20:57 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb507968fca06c3596bf7b11481c5437a7b6a693edcebb31e1704799ac1e8df`  
		Last Modified: Tue, 02 Dec 2025 01:20:58 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15e84bf7b1d02bea3d11a08da6c35478d40c311f22ab406c4e42c7580b07377f`  
		Last Modified: Tue, 02 Dec 2025 01:21:10 GMT  
		Size: 27.0 MB (27025194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbe46d47a694bdc1bd1d1e98019f199d6cd4bb897aeb2a8191d23f3c879ae47b`  
		Last Modified: Tue, 02 Dec 2025 01:20:58 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3203bbb1501f9e894385ca20740b308f051a1cda281026de19ed23e22fa9e8`  
		Last Modified: Tue, 02 Dec 2025 01:20:59 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ff9eb0018ba58ad8943bb412157c987c355ac0a980363ceef82c272e196af8`  
		Last Modified: Tue, 02 Dec 2025 01:20:59 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:ba1c1f86d3087492a31fc198f04a09a606b7e49e7254f1a7fa9920692f6f6536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1132477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1bcce756eb5a2a7ab1cce010eac1107f61217bee60002e2c54eacaa038f99e`

```dockerfile
```

-	Layers:
	-	`sha256:8f2e0c639201a717a923328b40780b398e77cfc921aadd8d1ce8ac4cd7d12bab`  
		Last Modified: Tue, 02 Dec 2025 02:27:14 GMT  
		Size: 1.1 MB (1080563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ddc213e67450a7ce0997c32db11202f6d8916478c01292145780de67e96e302`  
		Last Modified: Tue, 02 Dec 2025 02:27:15 GMT  
		Size: 51.9 KB (51914 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.2-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:0c29d535810de8efe2fd7a42dbb365474b64c00134bb407370dbe4a902edb56c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97463538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e7c7a24bae28c87c51dc13337dedb490003c6b0d102b47429257e7f9f12f301`
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
# Tue, 25 Nov 2025 19:10:31 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 25 Nov 2025 19:11:32 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 25 Nov 2025 19:11:33 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 25 Nov 2025 19:11:33 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 25 Nov 2025 19:11:35 GMT
RUN set -eux; 	version='6.9-RC3'; 	sha1='f98c7ce5304d9a3543101678e43a2622f76abcd9'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 25 Nov 2025 19:11:35 GMT
VOLUME [/var/www/html]
# Tue, 25 Nov 2025 19:11:35 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 25 Nov 2025 19:11:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Nov 2025 19:11:35 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 25 Nov 2025 19:11:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Nov 2025 19:11:35 GMT
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
	-	`sha256:60ff5990bed8ece5f1c6c3d897082ed502ba19aa6d8440b9dc1fdce76e38e0f4`  
		Last Modified: Tue, 25 Nov 2025 22:58:00 GMT  
		Size: 28.1 MB (28107498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cfcf200213337e3bb9dd75d4a2eb9cdeeb895bae0d142a959fa9dca246f1241`  
		Last Modified: Tue, 25 Nov 2025 19:11:55 GMT  
		Size: 9.4 MB (9399182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90c5caecc100ce0f163a51dcdefae9f5ef24f25c3445df7ab95a4b5b2457a3f3`  
		Last Modified: Tue, 25 Nov 2025 19:11:53 GMT  
		Size: 62.5 KB (62487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8e15b5cffba7dc84d92c57e7fb45800affe08d461c2dceb3d4687c7b2b228b`  
		Last Modified: Tue, 25 Nov 2025 19:11:53 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a9251f9047e9f9ae1c4e6b00b66daa8b2ebc6d78446401643f4a48aff0f46c`  
		Last Modified: Tue, 25 Nov 2025 19:12:04 GMT  
		Size: 27.0 MB (27024972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640bc394b5534fb7e4f63f65ed0b89eed92af2a39f94661f0a5861039d7efdda`  
		Last Modified: Tue, 25 Nov 2025 19:11:54 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3153311e93cc4165fc5566456509bd24abb8513535a58aa209f25aafa866837f`  
		Last Modified: Tue, 25 Nov 2025 19:11:54 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7876770f85f0d1ecf9fa0b0475d97a5bbd05be962830fe56bb818673886edfaf`  
		Last Modified: Tue, 25 Nov 2025 19:11:54 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:c693602f1f5467d5dc20c7118ad07bd7cc7f9a9cc05f75b3783d51a72fbab7fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1132486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19398f50589d271d85136d050a7cb4109e082a3d0c4429419f43f03abc175a50`

```dockerfile
```

-	Layers:
	-	`sha256:a01536e6ab502d2f0646e3a1c927af8fd0ad07ac3e2020ef307d78ff3546c70d`  
		Last Modified: Tue, 25 Nov 2025 20:18:44 GMT  
		Size: 1.1 MB (1080583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54c6426f893b6249209aee5ddfd09499b4dffb23e2260a8ee36342b5d35a300c`  
		Last Modified: Tue, 25 Nov 2025 20:18:46 GMT  
		Size: 51.9 KB (51903 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.2-fpm-alpine` - linux; 386

```console
$ docker pull wordpress@sha256:0b4e5d35f9f9a3e06fa2aa831a06d0fd9ae2a96e13f9d319f82121dd580182cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.3 MB (96308060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468be5ca2658fd2a1db9ee9caada46cbccbdea0e40613cb014c9f14a6b89ac47`
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
# Tue, 02 Dec 2025 01:11:31 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 02 Dec 2025 01:12:25 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:12:25 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:12:25 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:12:27 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:12:27 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:12:27 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:12:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:12:27 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:12:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:12:27 GMT
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
	-	`sha256:bdf7117f7a27b52bf38e2bf281208a8fe55f9082571729aafe09248eb71c0776`  
		Last Modified: Tue, 02 Dec 2025 01:12:38 GMT  
		Size: 28.5 MB (28494187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0125c66a232ee64deda3efd08ebbf4f1f77eaa684643cc3601227ec1d2bd95`  
		Last Modified: Tue, 02 Dec 2025 01:12:38 GMT  
		Size: 8.1 MB (8056598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bdb79b17217b115934a853403a64b997828367d38fb716386f4315bb3e5561c`  
		Last Modified: Tue, 02 Dec 2025 01:12:38 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:021ae07494976c0b5cca3558a27c93ac0f25c8e0057996fc6492c40fc4add415`  
		Last Modified: Tue, 02 Dec 2025 01:12:38 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a46c7fd41542b288e6017e6057c79e8748a855e05daadde2727161cf67ce8f29`  
		Last Modified: Tue, 02 Dec 2025 01:12:40 GMT  
		Size: 27.0 MB (27025200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6acec24fe4bddc79845346fb998ff4caf5d953dc2ccf5f92fd772115d3e949`  
		Last Modified: Tue, 02 Dec 2025 01:12:39 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6245d7f859df9a63c2dba7a7f56c247a756ffb827c7a78ce6baad74edda7ca0a`  
		Last Modified: Tue, 02 Dec 2025 01:12:39 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7e2a55c24937cf3af50e1d55c51fae1bf67f46e266796216fb2de3c94c0c63`  
		Last Modified: Tue, 02 Dec 2025 01:12:40 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:371a938613817a303d2b77d05b6ffc85b8424cbc210e151dac89b5d8bf12e1b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1133473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4af7ba577a007dbbd9433dc74e93fb08041ecc20ebf941e0a0b8aa3b014b76`

```dockerfile
```

-	Layers:
	-	`sha256:6abec7474c90a67417331baaaefb1ac0003edb066b7b8229c252e5f1e7567e3e`  
		Last Modified: Tue, 02 Dec 2025 02:27:22 GMT  
		Size: 1.1 MB (1081746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16e55b13d53035e9610c30f3d72334c358b33c48e641adcb81b4c5d7ec8599db`  
		Last Modified: Tue, 02 Dec 2025 02:27:23 GMT  
		Size: 51.7 KB (51727 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.2-fpm-alpine` - linux; ppc64le

```console
$ docker pull wordpress@sha256:cf8e642ed6bd1795fd32f63a1d6840a77c52b454b888b729a3c749675e044d94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.1 MB (98064295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2be78677d93c6864d7812436ec09088022aa53d678865f310f9e13456b8c26c1`
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
# Tue, 25 Nov 2025 19:25:51 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 25 Nov 2025 19:27:54 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 25 Nov 2025 19:27:56 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 25 Nov 2025 19:27:57 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 25 Nov 2025 19:28:02 GMT
RUN set -eux; 	version='6.9-RC3'; 	sha1='f98c7ce5304d9a3543101678e43a2622f76abcd9'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 25 Nov 2025 19:28:03 GMT
VOLUME [/var/www/html]
# Tue, 25 Nov 2025 19:28:03 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 25 Nov 2025 19:28:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Nov 2025 19:28:04 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 25 Nov 2025 19:28:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Nov 2025 19:28:04 GMT
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
	-	`sha256:ea1a4a1904e7ab4fd96c18bc16759e68a4778b3669b75786d8693723a81ee803`  
		Last Modified: Tue, 25 Nov 2025 19:28:50 GMT  
		Size: 28.9 MB (28931094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c99936136da01fe2df77fc5346f7a9ebdf4712d0eeb9389cc760f148b2d7f470`  
		Last Modified: Tue, 25 Nov 2025 19:28:48 GMT  
		Size: 9.0 MB (8963704 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326137dec02a79161ec133a0ea44026b2fd94eaef385a17654d02019fe731609`  
		Last Modified: Tue, 25 Nov 2025 19:28:47 GMT  
		Size: 62.5 KB (62467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81cfe2d4d87a1328f791ea88dcd461e439fd75c7c1df90f9619af88edd306dc5`  
		Last Modified: Tue, 25 Nov 2025 19:28:47 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bac5e3a7e2a59eab971eea6beccdb3535ea0406e1f9430b452f84e03013f442`  
		Last Modified: Tue, 25 Nov 2025 19:28:49 GMT  
		Size: 27.0 MB (27024975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15b81e2d06fe065165c2bf06dab2b6dce8d616a5a5b17b03619ea1b6f432ccb7`  
		Last Modified: Tue, 25 Nov 2025 19:28:47 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04bc93c78ace386caad4c06feac0b9951512b211da0546eb40564d49485edd50`  
		Last Modified: Tue, 25 Nov 2025 19:28:47 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5454c56645c6e33346196a56b15872f6b1d15431ad496e8190aae44f53fc57dd`  
		Last Modified: Tue, 25 Nov 2025 19:28:47 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:86af57cbbdb41ae251a14707ae21f333521157101535916a7461a5adc6e98234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1130388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4e6a699dc25e638e0f97304df83bd47861293bfec613532f923a959e0858891`

```dockerfile
```

-	Layers:
	-	`sha256:626756f6643dcace2a0b0621134a75ed7ad1de9c465ac9cf60240e766dc9a0f9`  
		Last Modified: Tue, 25 Nov 2025 20:18:55 GMT  
		Size: 1.1 MB (1078610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e46eedacf675c4dc93613ce61faefc87d762c2a245a7f1d071b4403ba7f2f1c1`  
		Last Modified: Tue, 25 Nov 2025 20:18:56 GMT  
		Size: 51.8 KB (51778 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.2-fpm-alpine` - linux; riscv64

```console
$ docker pull wordpress@sha256:2333927c2233602c08426b41f37c7ae478f68a2c01fdb8ba1899f2a4aba47536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.9 MB (93852252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7510511ddef34dcc9a3e2657f3b5f68258d35fb8e2ec4df7569a9fcf0be08a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 31 Jul 2025 19:22:09 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
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
# Thu, 20 Nov 2025 21:56:04 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Thu, 20 Nov 2025 22:09:05 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 20 Nov 2025 22:09:11 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 20 Nov 2025 22:09:11 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 25 Nov 2025 23:13:30 GMT
RUN set -eux; 	version='6.9-RC3'; 	sha1='f98c7ce5304d9a3543101678e43a2622f76abcd9'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 25 Nov 2025 23:13:30 GMT
VOLUME [/var/www/html]
# Tue, 25 Nov 2025 23:13:30 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 25 Nov 2025 23:13:30 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Nov 2025 23:13:30 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 25 Nov 2025 23:13:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Nov 2025 23:13:30 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58e9f10e445dbf7ba866462dd44d0f912a09342dc97a4685769a2d057bcc7a9`  
		Last Modified: Thu, 09 Oct 2025 06:22:36 GMT  
		Size: 3.6 MB (3600269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2579c35b4a5055268b9ccb82f8c3307c0a781af77168952679399ed4bde3b60a`  
		Last Modified: Thu, 09 Oct 2025 06:22:36 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b6a920874b5f6759a41702af348a1eefb32a0674eeae4cd9d750418594caed`  
		Last Modified: Thu, 09 Oct 2025 06:22:36 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e488044b38fedf2b0c5a42fee0d7f8266277e151bbc0aada6a071b34ec2fcfe`  
		Last Modified: Thu, 09 Oct 2025 23:00:37 GMT  
		Size: 12.2 MB (12183652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccad6f0a1f0db89e61f61fa65505f5f655a026a9c873b83bbbd58c9526e7494b`  
		Last Modified: Thu, 09 Oct 2025 23:00:34 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9abf8b8478e62469efe6d3abfede6020f33393ffac1b72aa0b91e9d1a75f7605`  
		Last Modified: Thu, 09 Oct 2025 23:00:36 GMT  
		Size: 12.3 MB (12305613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67efc630d93c3d04a3ca760bbb92609977841b9323c82277f06b4ac29d15778f`  
		Last Modified: Thu, 09 Oct 2025 23:00:35 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d065e4cd8623adcce4cf56e044e1d5e2ab880b4349596bbec7b3de07b7b9f59`  
		Last Modified: Thu, 09 Oct 2025 23:00:35 GMT  
		Size: 19.9 KB (19862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5888e1c23b5213a4f4965ec9beaddd3cd9c38b1ca29eaba42073eeb328e73809`  
		Last Modified: Thu, 09 Oct 2025 23:00:36 GMT  
		Size: 19.9 KB (19853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917fb9942fffe1a4e8c73946846e4c69c8e66a3d7ab1df8fb15f6054ed64a9bd`  
		Last Modified: Thu, 09 Oct 2025 23:00:37 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5556034ddf9ea4bf0a25b140f2159eb67fa20d8f1f4a2d13b2dd178dca2c1bd`  
		Last Modified: Thu, 20 Nov 2025 22:11:28 GMT  
		Size: 28.1 MB (28089106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497354df818476e1c4f4f9eccefca1540bf3e15c639ac86699ff92e80f0f6993`  
		Last Modified: Thu, 20 Nov 2025 22:11:26 GMT  
		Size: 7.0 MB (7013105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167af4bf0aa8899be86156ad8224b8dac63d4b14905726de9a3ad39048edde31`  
		Last Modified: Thu, 20 Nov 2025 22:11:26 GMT  
		Size: 62.5 KB (62468 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1795dd38287d461ad1334b61ae9a4e96ebc80eecdba9434caf89639869946a2b`  
		Last Modified: Thu, 20 Nov 2025 22:11:26 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e35eb932fd9ea8af3c93cc83819102c3214297e56673e95d025f77ce05aac906`  
		Last Modified: Tue, 25 Nov 2025 23:15:27 GMT  
		Size: 27.0 MB (27024970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f727e37064bb9e07f64bde17b28aeeaffc51663a5e604eaa43702d0865103a2`  
		Last Modified: Tue, 25 Nov 2025 23:15:18 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fcf464978866b4c12406ec5c140ab95ea8f200d7975d285fa0e9fe58f1bf0a`  
		Last Modified: Tue, 25 Nov 2025 23:15:18 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d117855a76f2b0d8f86e977a438e84ca873e357282d1b8e0eedfe68c57c63542`  
		Last Modified: Tue, 25 Nov 2025 23:15:18 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:9ffd46bce8dbd3956485beceaa6d5f9fd4c547422e3a9a67d53d197f2b1ad0eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1130384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a733ab991598d13dec4833513a256f8149718726184471943c5337dbe74994`

```dockerfile
```

-	Layers:
	-	`sha256:659fc8c7121d260099232d168d22fa3a8c199bfc5cd34d23018d8531a96147ea`  
		Last Modified: Wed, 26 Nov 2025 02:14:40 GMT  
		Size: 1.1 MB (1078606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:361219d0ebc7f7d8987fb60ac41793a7d9657d636bf05d31ad8b9b6721d76a7f`  
		Last Modified: Wed, 26 Nov 2025 02:14:40 GMT  
		Size: 51.8 KB (51778 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.2-fpm-alpine` - linux; s390x

```console
$ docker pull wordpress@sha256:68c5508729d450c26bd43aa5e7230bb75ceda52e5b1688f70714c43b2f10bca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.5 MB (97541462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b13a373756485328b9171447c7f53bb445c25d0e6bf61e68903f64508e7b123`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 31 Jul 2025 19:22:09 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
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
# Tue, 25 Nov 2025 19:12:58 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 25 Nov 2025 19:13:55 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 25 Nov 2025 19:13:56 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 25 Nov 2025 19:13:56 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 25 Nov 2025 19:13:58 GMT
RUN set -eux; 	version='6.9-RC3'; 	sha1='f98c7ce5304d9a3543101678e43a2622f76abcd9'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 25 Nov 2025 19:13:58 GMT
VOLUME [/var/www/html]
# Tue, 25 Nov 2025 19:13:58 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 25 Nov 2025 19:13:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 25 Nov 2025 19:13:58 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 25 Nov 2025 19:13:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 25 Nov 2025 19:13:58 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503d2dd4bd3263db65246a0eede02512575e505bf72959ea5d8d1c7f5b3dea5e`  
		Last Modified: Thu, 09 Oct 2025 00:54:03 GMT  
		Size: 3.7 MB (3692716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e39eb5e282665e4bd0e90c53a85f696e72ef63e8ef403c40cc9e67742ffe824`  
		Last Modified: Thu, 09 Oct 2025 00:54:03 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0608d8b4902677a8ba1ccd4d718738714fa13e782091c89842c948b06a52f8`  
		Last Modified: Thu, 09 Oct 2025 00:54:03 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67516b8f02966476a2ac367f1c1762ddfb0d00c7ee8d7c61e93a4513d64874b0`  
		Last Modified: Thu, 09 Oct 2025 04:59:26 GMT  
		Size: 12.2 MB (12183674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1503a156a632da17ed8630b68eb6ef4a3de869be2e9a5e3b159a000ae826cf33`  
		Last Modified: Thu, 09 Oct 2025 02:31:12 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b087e436dc3393eadc1866c028198167a48d9ddb04ef16c01b9347d5e122d9`  
		Last Modified: Thu, 09 Oct 2025 04:59:29 GMT  
		Size: 13.0 MB (12980182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef2fac77f59c551b27e4efd9e67e93de776f574a623f9fb5cd2946ca77933c0`  
		Last Modified: Thu, 09 Oct 2025 02:31:12 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526ecfed0f8b095c2094a0d2c68c60aa59f5c3f8c3cbd4ad1222499c643d9008`  
		Last Modified: Thu, 09 Oct 2025 02:31:12 GMT  
		Size: 19.9 KB (19879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94678bc4482a10603b530d431379f16580d1000e7d26d837c64f4a0bbb6de23f`  
		Last Modified: Thu, 09 Oct 2025 01:42:03 GMT  
		Size: 19.9 KB (19869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58a34ab5d7f41a2ab1161aa8a838cdf11f23e90158e192239b2095bd00f62502`  
		Last Modified: Thu, 09 Oct 2025 01:42:03 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d48d31733dadf7354e3152d7aef65180307e4d80f94f99c62225d2408a1a32`  
		Last Modified: Tue, 25 Nov 2025 19:14:23 GMT  
		Size: 29.3 MB (29255990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65fa3782a914c67d46664012a5570b5875e6875c562722ca840b6b0a5f4a707e`  
		Last Modified: Tue, 25 Nov 2025 19:14:19 GMT  
		Size: 8.6 MB (8634370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c928d6a584d60337429413dd071e38177dfd60dcf8771bff473b9b96c110c4`  
		Last Modified: Tue, 25 Nov 2025 19:14:19 GMT  
		Size: 62.5 KB (62481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a250cd42f981d61f714d7a12737c94b6383be7fd6c76320b55927f097609ac84`  
		Last Modified: Tue, 25 Nov 2025 19:14:19 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74177495e41c567f57d239348d30333fef192a4d1fdfa80f8ba2f39ea789089`  
		Last Modified: Tue, 25 Nov 2025 19:14:22 GMT  
		Size: 27.0 MB (27024971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72cff5ec1c175cfeeda6b7be98addd61fcc31cbedd941de4da589bbdb21e5201`  
		Last Modified: Tue, 25 Nov 2025 19:14:19 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9eb22c030076b396b7fef376501a125b39bfcd6ae512d181ae6bc048c6d0d10`  
		Last Modified: Tue, 25 Nov 2025 19:14:18 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b636c1da6dd63a5f397bae6e43390af4c56432ceb66e397269cc659066c6c061`  
		Last Modified: Tue, 25 Nov 2025 19:14:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:51fe6b2214f4ef429ebb5e9b17af860769367af028d228cab31286761ff02422
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1130300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3971c1bece7cfab09cbc21df5b27ac2dbe541592a9b5e095d20a6662c2fc74c6`

```dockerfile
```

-	Layers:
	-	`sha256:8536634b6cee4f6aaf50e16104f0026e451b753aa55595c00024e26aa52b27a6`  
		Last Modified: Tue, 25 Nov 2025 20:19:02 GMT  
		Size: 1.1 MB (1078576 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8b8983e007acc8201a96f06a05e803cab190550e038d86b7062a308bfa236d1`  
		Last Modified: Tue, 25 Nov 2025 20:19:03 GMT  
		Size: 51.7 KB (51724 bytes)  
		MIME: application/vnd.in-toto+json
