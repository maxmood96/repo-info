## `wordpress:php8.5-fpm-alpine`

```console
$ docker pull wordpress@sha256:c6a6592a03bba44dc9616624431d63a4ac47879dbee79ef47547dd791d9455a7
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

### `wordpress:php8.5-fpm-alpine` - linux; amd64

```console
$ docker pull wordpress@sha256:3a9bfc0c8492a80ebe73519facfd6706a45a73a59cc3773f40e083f947686c53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102545164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f7a55c06b1bb11dd68b701af3aa3c695226f34697551772e31643cdb5bae913`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 20 Nov 2025 19:50:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Nov 2025 19:50:06 GMT
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 20 Nov 2025 19:50:07 GMT
ENV PHP_VERSION=8.5.0
# Thu, 20 Nov 2025 19:50:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.0.tar.xz.asc
# Thu, 20 Nov 2025 19:50:07 GMT
ENV PHP_SHA256=39cb6e4acd679b574d3d3276f148213e935fc25f90403eb84fb1b836a806ef1e
# Thu, 20 Nov 2025 19:50:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 20 Nov 2025 19:50:10 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 19:53:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 19:53:05 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 19:53:06 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 19:53:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 19:53:06 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 19:53:06 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 20 Nov 2025 19:53:06 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Nov 2025 19:53:06 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 20 Nov 2025 19:53:06 GMT
CMD ["php-fpm"]
# Tue, 02 Dec 2025 01:14:11 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 02 Dec 2025 01:15:14 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:15:14 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:15:14 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:15:15 GMT
RUN set -eux; 	version='6.8.3'; 	sha1='fd56bcdc15f1877e45dce67942ea75949ed650e8'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:15:15 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:15:15 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:15:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:15:15 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:15:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:15:15 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a0c3273211b5e26c34ef0e0bd0f2d25ecc87d31a2726263bf6e8c2c12e372f`  
		Last Modified: Thu, 20 Nov 2025 19:53:25 GMT  
		Size: 3.5 MB (3463760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:653527f673f69dfc5634cf39747e7b044108cb4912ecd65549e3ec5b89aa7bc8`  
		Last Modified: Thu, 20 Nov 2025 19:53:26 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:815d6c9d275579e907e8dacee753269d7f057649d8b48804ae2ff348d18603fd`  
		Last Modified: Thu, 20 Nov 2025 19:53:22 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84649691874d20900355db075ad6b268c5d2fa4330653640290da53d43584900`  
		Last Modified: Thu, 20 Nov 2025 19:53:26 GMT  
		Size: 14.3 MB (14336696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b512f071908a7fd4c0353a8fcbf77156af9a65f06ca588165146b920ecc02e39`  
		Last Modified: Thu, 20 Nov 2025 19:53:23 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df8c0e2cc0bbf6a23f4b4bc58e4d8d07dbbf0013a693dd2e287f5b6c04b1e072`  
		Last Modified: Thu, 20 Nov 2025 19:53:25 GMT  
		Size: 16.4 MB (16449435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe7dcc4e9e415476f566be9a604a1df9a175fed3e0520a5c74b81608bcd5e1d`  
		Last Modified: Thu, 20 Nov 2025 19:53:23 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff442efc7bae703b060fb6512dc5aba22c76a2278b436ee71d5779dfc0481801`  
		Last Modified: Thu, 20 Nov 2025 19:53:23 GMT  
		Size: 20.1 KB (20077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32827cf7ce9f6b86f86350967e6266981fe8bf8cd25e121dab2504b1cc9d1e6b`  
		Last Modified: Thu, 20 Nov 2025 19:53:23 GMT  
		Size: 9.2 KB (9186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8935ff976be50da883eb192c858748bda3cedba2b32715a875eb640caef9c84`  
		Last Modified: Tue, 02 Dec 2025 01:15:26 GMT  
		Size: 28.3 MB (28282738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d269abbbfd2e9b7b5fb6e2f0e38e01050a82d7aaafa33ddd7789583032dfce82`  
		Last Modified: Tue, 02 Dec 2025 01:15:26 GMT  
		Size: 9.3 MB (9271932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fc9e47d7849753d8507c12225bb4f5b9fd384e1d090ecf709242119446b120`  
		Last Modified: Tue, 02 Dec 2025 01:15:25 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1728a72adbedf02f97e5dada10fc498634b5fe160d64b3ee34e7dcc94b10d002`  
		Last Modified: Tue, 02 Dec 2025 01:15:25 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a0de873b5d120766d7cd5b4d3b5859f900f9fe74e8073c5ad5307b03618c8c`  
		Last Modified: Tue, 02 Dec 2025 01:15:27 GMT  
		Size: 26.9 MB (26899659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab18e2ca7a41ef572377bf8f74769679f454c38ca2510b65e538ae9150187fa`  
		Last Modified: Tue, 02 Dec 2025 01:15:27 GMT  
		Size: 2.4 KB (2433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d062286d46f53e06a6200ae34f95837042e9d7057c20a5fb9b33a0a674061a`  
		Last Modified: Tue, 02 Dec 2025 01:15:27 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2203d0fbaa8ee5275c522957d0acb84f46d5bdc88299c7be7c294799eea7687e`  
		Last Modified: Tue, 02 Dec 2025 01:15:28 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.5-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:4338a9912751322f1744c2244f15282c9d03227083a7f0464e88cb2628b3d457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1130582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f415635de7ee236bd438a413747a035ad96e432c2c843b62c7746e96e3829dad`

```dockerfile
```

-	Layers:
	-	`sha256:ee446d1a0553e3945d8324895eed357f229521af32a86d058443e2d53f6a8ac3`  
		Last Modified: Tue, 02 Dec 2025 02:19:33 GMT  
		Size: 1.1 MB (1080279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35595cd90adc1b498f24155032364e37f474c012c770bfb25a609ddf4253f820`  
		Last Modified: Tue, 02 Dec 2025 02:19:34 GMT  
		Size: 50.3 KB (50303 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.5-fpm-alpine` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:804c63f763efcc0c353eb68317d0d7a3e5cca14a17885c202c12bd531b9bd9cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.7 MB (94709794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90882d23b92ba2734473d021285965cc64c6afb9cbef9db961a31789a7c2c298`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 20 Nov 2025 19:45:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Nov 2025 19:45:17 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 20 Nov 2025 19:45:17 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 20 Nov 2025 19:45:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 19:45:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 19:45:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:45:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:45:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 19:45:18 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 20 Nov 2025 19:45:18 GMT
ENV PHP_VERSION=8.5.0
# Thu, 20 Nov 2025 19:45:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.0.tar.xz.asc
# Thu, 20 Nov 2025 19:45:18 GMT
ENV PHP_SHA256=39cb6e4acd679b574d3d3276f148213e935fc25f90403eb84fb1b836a806ef1e
# Thu, 20 Nov 2025 19:45:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 20 Nov 2025 19:45:21 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 19:48:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 19:48:25 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 19:48:26 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 19:48:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 19:48:26 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 19:48:26 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 20 Nov 2025 19:48:26 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Nov 2025 19:48:26 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 20 Nov 2025 19:48:26 GMT
CMD ["php-fpm"]
# Tue, 02 Dec 2025 01:10:04 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 02 Dec 2025 01:11:54 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:11:54 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:11:54 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:11:56 GMT
RUN set -eux; 	version='6.8.3'; 	sha1='fd56bcdc15f1877e45dce67942ea75949ed650e8'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:11:56 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:11:56 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:11:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:11:57 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:11:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:11:57 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62bad5c84f04d050d041f3c5030d6c4f8e67c13a30c354738c9e4f976ece8a8c`  
		Last Modified: Thu, 20 Nov 2025 19:48:40 GMT  
		Size: 3.4 MB (3428328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fde1be9e486f06f836820e8ac8aba53ff599804f05171eaf2ff6edf9ac88e5a`  
		Last Modified: Thu, 20 Nov 2025 19:48:39 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fab8f479b628b893e0f30f2c91a23e251fe02c0bc9fc4f67e729c0e89b526696`  
		Last Modified: Thu, 20 Nov 2025 19:48:39 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ee9130fbc3deb9212b69f397e68b6c248b477b81fa4739ae2b9a144eef7a09`  
		Last Modified: Thu, 20 Nov 2025 19:48:40 GMT  
		Size: 14.3 MB (14336686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84361cdac8b898a21ffda0e64e47f8791f3b7bbe8dd19752390b29c97476a00f`  
		Last Modified: Thu, 20 Nov 2025 19:48:39 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b30710866a5aee04479c336ffdfffbd3811c0847ad9f21b9024b6cf8e9186c6`  
		Last Modified: Thu, 20 Nov 2025 19:48:41 GMT  
		Size: 14.4 MB (14425972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685badd4471494845795100d1232a0164c54eb8dec74c5439c9c20affaa1e179`  
		Last Modified: Thu, 20 Nov 2025 19:48:39 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785c29b20e82df08593d724de6a02511df7458e807f1d198c45d08059544a445`  
		Last Modified: Thu, 20 Nov 2025 19:48:39 GMT  
		Size: 19.9 KB (19864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c74cfe111e3a137c9c7aa0f67ac170ae4788e02398f05fb337d4afb62921a806`  
		Last Modified: Thu, 20 Nov 2025 19:48:40 GMT  
		Size: 9.2 KB (9188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4113747039c6bc5bf87d0e01fcf6a395999a125d8389e4b9015003561851cbf8`  
		Last Modified: Tue, 02 Dec 2025 01:12:31 GMT  
		Size: 24.4 MB (24377249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54349bbcc2d65784611c3affde3afc14d06d84425d72dc9e0b786772eee7fdcd`  
		Last Modified: Tue, 02 Dec 2025 01:12:29 GMT  
		Size: 7.7 MB (7699530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ab4e82801f6de05c7992a58590d0029c80405818b676ab490091994adaae0c`  
		Last Modified: Tue, 02 Dec 2025 01:12:28 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c9d04ce190a834701353c869a6d1b2bdd07be5a35d6c93be5569ef22e3052d`  
		Last Modified: Tue, 02 Dec 2025 01:12:29 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abe9b3b926ff8d425c0cb911ec69b819506236088e9cf0c929536d47d0003d6`  
		Last Modified: Tue, 02 Dec 2025 01:12:35 GMT  
		Size: 26.9 MB (26899670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e157bce05c7fec6316b60c6cf53bf2f95ee2877fc0a90bca4ff4a29721d91a8d`  
		Last Modified: Tue, 02 Dec 2025 01:12:29 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562705d34e9bcc54c46766b1e5e66ff4cd3a354d20c175ff358ed89d26bffa5b`  
		Last Modified: Tue, 02 Dec 2025 01:12:29 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fa1c7e7c8c1da9ae77d60f70b2f9601c230a3108091f5a8e1c9bb9880d0ff93`  
		Last Modified: Tue, 02 Dec 2025 01:12:29 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.5-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:ec94b4fd0ea93c6741b885118e737c3c0da4a7046f3e7b20f8946e86f2acdb3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 KB (50233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b32606297400960fe3db12c90e67f3df448617a35fbbbd7b12d6aca81768f67`

```dockerfile
```

-	Layers:
	-	`sha256:a2ad290afbdcddb8d43ae923eecfbdab0cc28de15b0df26558dff91dfecd7a56`  
		Last Modified: Tue, 02 Dec 2025 02:19:38 GMT  
		Size: 50.2 KB (50233 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.5-fpm-alpine` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:9cbc2b8ebf6c0291819aeb8602bb5f3032b4a0c89111de35ae4f47bee4c9d107
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93329423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fe7ebcc7e341be53b26b0697f033e0618e5e28ee6c8f38416156fb01953b252`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 20 Nov 2025 20:01:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Nov 2025 20:01:52 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 20 Nov 2025 20:01:52 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 20 Nov 2025 20:01:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 20:01:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 20:01:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:01:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 20:01:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 20:01:52 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 20 Nov 2025 20:01:52 GMT
ENV PHP_VERSION=8.5.0
# Thu, 20 Nov 2025 20:01:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.0.tar.xz.asc
# Thu, 20 Nov 2025 20:01:52 GMT
ENV PHP_SHA256=39cb6e4acd679b574d3d3276f148213e935fc25f90403eb84fb1b836a806ef1e
# Thu, 20 Nov 2025 20:01:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 20 Nov 2025 20:01:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:05:05 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 20:05:05 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 20:05:06 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 20:05:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 20:05:06 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 20:05:06 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 20 Nov 2025 20:05:06 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Nov 2025 20:05:06 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 20 Nov 2025 20:05:06 GMT
CMD ["php-fpm"]
# Tue, 02 Dec 2025 01:14:29 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 02 Dec 2025 01:16:17 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:16:17 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:16:17 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:16:19 GMT
RUN set -eux; 	version='6.8.3'; 	sha1='fd56bcdc15f1877e45dce67942ea75949ed650e8'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:16:19 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:16:19 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:16:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:16:19 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:16:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:16:19 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35cb857f1c49ab2cd7d8eb438ed74fd9d89994b68cd657158e1767a90b2221a7`  
		Last Modified: Thu, 20 Nov 2025 20:05:33 GMT  
		Size: 3.2 MB (3244393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0452bdd8bbe5a8f5c197568a4b44f37e13736c20fb814abd03064e591454cd5e`  
		Last Modified: Thu, 20 Nov 2025 20:05:33 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e283de893a58516c4a63c998a081b985dd0e60da85ad056dfa720afc21bcad5`  
		Last Modified: Thu, 20 Nov 2025 20:05:12 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e7948af65c6defa195ac0aac292b522f3597cf89793e915f67e6a7d7a3c7c39`  
		Last Modified: Thu, 20 Nov 2025 20:05:34 GMT  
		Size: 14.3 MB (14336683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a24ea27e6a6e49108202444e49d2a22cfe0383c7f5a93d8803ef58b7cd765ff`  
		Last Modified: Thu, 20 Nov 2025 20:05:13 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8579adacc93dee3c449528ab3085d6eee70f8042c74610a6fb079eda08e47c7c`  
		Last Modified: Thu, 20 Nov 2025 20:05:34 GMT  
		Size: 13.6 MB (13640558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7edc76e10a1e51de33ae27fcef306e13834fd01899d584e6ccc69478b63dc45`  
		Last Modified: Thu, 20 Nov 2025 20:05:33 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2244fa8b221672765483f32845ca5c680e9160601f51a396713f0af50380d285`  
		Last Modified: Thu, 20 Nov 2025 20:05:33 GMT  
		Size: 19.9 KB (19852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926cbb77bffe3228b401fdf6e325e86fb5bbb8b27048ce6b17c20e8541878a57`  
		Last Modified: Thu, 20 Nov 2025 20:05:34 GMT  
		Size: 9.2 KB (9187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ddb64b6906c0fb03b853baccd06400c9fbfae298adfc821d04845224b96c2d3`  
		Last Modified: Tue, 02 Dec 2025 01:16:50 GMT  
		Size: 23.2 MB (23152262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42e7a2c32c1c48cec9a4e94f0a33707b8d9ec48867635d5e8f4833fc43bdada`  
		Last Modified: Tue, 02 Dec 2025 01:16:49 GMT  
		Size: 8.8 MB (8796057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2340b999b71f20eb5e7526ccccb10f7c7e84ae88286b628974d524f07e21dff0`  
		Last Modified: Tue, 02 Dec 2025 01:16:49 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f52ee34474a2fc4c9e0c1af1f4e681aeb8e3b10190b85096ff122bf8b2258d`  
		Last Modified: Tue, 02 Dec 2025 01:16:49 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a324ea8e3d3d65cfa279e4e913b52c2313ba92ee77ce08554d36b11f2058c36`  
		Last Modified: Tue, 02 Dec 2025 01:16:51 GMT  
		Size: 26.9 MB (26899664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b93cb1f77de3155e6f0588a4a36eb61e9552c3d2a1150351516e53cb49a71d0`  
		Last Modified: Tue, 02 Dec 2025 01:16:49 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b42b872664f3d08b0760bcf3dada4bbca86b44e01bdb24aefdcc4c2319c819`  
		Last Modified: Tue, 02 Dec 2025 01:16:49 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f02493c8630ba06ae2f73881119b0009fd037f5e5a9a55adbec9a6ed700667b`  
		Last Modified: Tue, 02 Dec 2025 01:16:49 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.5-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:3e412b6483af109bc6d94cfb59e10f377cd2947a9c87a835969981208b47c877
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1129521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:166f1a0692a44f19909fad8d3d8ae460da72b2297c0d66a5558ccec2a9cd2ec0`

```dockerfile
```

-	Layers:
	-	`sha256:4ce11af7b70da3acd40d3b524c45ed858acbc925fe786a95eb97432a95de3ae8`  
		Last Modified: Tue, 02 Dec 2025 02:19:41 GMT  
		Size: 1.1 MB (1079073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81ae7de0519c7617d19c9f37368880105bfd38c17cdea0258f01e3fe52fb1e9c`  
		Last Modified: Tue, 02 Dec 2025 02:19:42 GMT  
		Size: 50.4 KB (50448 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.5-fpm-alpine` - linux; 386

```console
$ docker pull wordpress@sha256:71502a99cb72affa424963715c229760db63a269eb2176aaf2e90cfd4a3b0970
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101902021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9829868b191b1b09395a082e1b5bd385b83f79f1a9b267ec8c7ecc1ec6a9333a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Thu, 20 Nov 2025 19:51:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Nov 2025 19:51:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 20 Nov 2025 19:51:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 20 Nov 2025 19:51:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Nov 2025 19:51:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 20 Nov 2025 19:51:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:51:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Nov 2025 19:51:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Nov 2025 19:51:43 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 20 Nov 2025 19:51:43 GMT
ENV PHP_VERSION=8.5.0
# Thu, 20 Nov 2025 19:51:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.0.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.0.tar.xz.asc
# Thu, 20 Nov 2025 19:51:43 GMT
ENV PHP_SHA256=39cb6e4acd679b574d3d3276f148213e935fc25f90403eb84fb1b836a806ef1e
# Thu, 20 Nov 2025 19:51:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 20 Nov 2025 19:51:46 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 19:55:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 20 Nov 2025 19:55:06 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 20 Nov 2025 19:55:06 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 20 Nov 2025 19:55:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Nov 2025 19:55:06 GMT
WORKDIR /var/www/html
# Thu, 20 Nov 2025 19:55:06 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 20 Nov 2025 19:55:06 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Nov 2025 19:55:06 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 20 Nov 2025 19:55:06 GMT
CMD ["php-fpm"]
# Tue, 02 Dec 2025 01:09:36 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 02 Dec 2025 01:10:34 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:10:34 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:10:34 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:10:36 GMT
RUN set -eux; 	version='6.8.3'; 	sha1='fd56bcdc15f1877e45dce67942ea75949ed650e8'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:10:36 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:10:36 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:10:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:10:36 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:10:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:10:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e641f844ec697d3da5372c2ff9b50cceb08065a6addb3f8398d9f39a7b56c6`  
		Last Modified: Thu, 20 Nov 2025 19:55:23 GMT  
		Size: 3.5 MB (3522989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20951f42c214fb3607375003f32a1fffa058fa6ce8a2c355ef5cb72b5183ee92`  
		Last Modified: Thu, 20 Nov 2025 19:55:22 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044428e8a7cddad945326dfc45a66a81f2b22193662863c0f6cc6ae2f2bbd2b7`  
		Last Modified: Thu, 20 Nov 2025 19:55:22 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994778bcc5628c69b71f958a145451a50fdc4117bcd9d8c75429b918cd23275b`  
		Last Modified: Thu, 20 Nov 2025 19:55:23 GMT  
		Size: 14.3 MB (14336664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbffe66fb422db8c98bff86212c61abbc241ba299bb7cdab1473553c888a10d7`  
		Last Modified: Thu, 20 Nov 2025 19:55:22 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92fd0bda451a62d98ce171ca51038ffd3050aa7273a4946d2864c106b8bbdea6`  
		Last Modified: Thu, 20 Nov 2025 19:55:24 GMT  
		Size: 16.9 MB (16887660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdc4cb3ebaee920ec65c88f289cf99e766e4ac2cc7ffdedf4ddc67c576408704`  
		Last Modified: Thu, 20 Nov 2025 19:55:22 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2099ab3725a9cbbe7959ff210115acf8a6c0cae48b359595dfe73793f8f20417`  
		Last Modified: Thu, 20 Nov 2025 19:55:23 GMT  
		Size: 20.0 KB (20048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2bdf7a72473919e4cbccd870365704c35408b31f3c2bb80f919b0a521b19705`  
		Last Modified: Thu, 20 Nov 2025 19:55:23 GMT  
		Size: 9.2 KB (9186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07910963c251641cb296a5699dd92a04176e78addce2c2e64dc43c871bb7df6`  
		Last Modified: Tue, 02 Dec 2025 01:10:58 GMT  
		Size: 28.5 MB (28494200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345cd6451228dcf1e93274ad0d99a2d60bdfe1dae95e3f80c33a3efedc4fc323`  
		Last Modified: Tue, 02 Dec 2025 01:10:54 GMT  
		Size: 8.1 MB (8103465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efae445a2b463a921631838232cd40644fcd1b4b6ba97bcc9f2a2f4f8232e66a`  
		Last Modified: Tue, 02 Dec 2025 01:10:53 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aeea3196736af812dd5f76354d492988d9202a51310a7b73a2ddd5c4f8eee03`  
		Last Modified: Tue, 02 Dec 2025 01:10:53 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243ff288823ca6cd236d359bf10b60925ac4644d4e41dfc0157a2426ef796b6e`  
		Last Modified: Tue, 02 Dec 2025 01:10:57 GMT  
		Size: 26.9 MB (26899669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b42e3277204a8540f4bd00229e04a93bad0c4dee8e2e22a1756a497057a997`  
		Last Modified: Tue, 02 Dec 2025 01:10:53 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66229a00b2e0245cf3bc50e07b36051e2695dd7b5bf9b4670d540ad704a1d7e7`  
		Last Modified: Tue, 02 Dec 2025 01:10:54 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1fb50eb20beafd89defd73734f976d0b92865ac241c81c9cb80d2e251e6a427`  
		Last Modified: Tue, 02 Dec 2025 01:10:54 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.5-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:4ab187fab5127ccc94b5b78bcca69b6f8d97c6816d5c92768a1743d5923e2e0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1130515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:965ed618087361f68da3ee14d19206ebad6eb9ed0621f3dfd08e1c75075529c8`

```dockerfile
```

-	Layers:
	-	`sha256:c4c16ac0daeb34960c3c0b288ac2aca4ff1f16c717a7f970c9ed27517d27fe02`  
		Last Modified: Tue, 02 Dec 2025 02:19:46 GMT  
		Size: 1.1 MB (1080254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:015a64ce9445083956d2df22a315c1c8c9293dcb02679c0adac8ffca81902c72`  
		Last Modified: Tue, 02 Dec 2025 02:19:47 GMT  
		Size: 50.3 KB (50261 bytes)  
		MIME: application/vnd.in-toto+json
