## `wordpress:beta-6.9-RC4-php8.5-fpm-alpine`

```console
$ docker pull wordpress@sha256:4f2b5efd517a4136ff8a270eebf84fa97d24e0d4567bb44cb0a6ee6ed78b6ab2
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

### `wordpress:beta-6.9-RC4-php8.5-fpm-alpine` - linux; amd64

```console
$ docker pull wordpress@sha256:fa91f443a9d6db3b4ec171788ed59a44260e6b438167b008b72754c74d6ae706
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.7 MB (102670680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4516a57b657ea6245c0ce24aed52a758bfc8a1c4f7442e176c7fa5846c8c5bc`
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
# Tue, 02 Dec 2025 01:17:10 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 02 Dec 2025 01:18:16 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:18:16 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:18:16 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:18:18 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:18:18 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:18:18 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:18:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:18:18 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:18:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:18:18 GMT
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
	-	`sha256:4b4e18d9a46a500893a2e34254b6f293ff7c85f3af56a7625d7a33e9e7f65559`  
		Last Modified: Tue, 02 Dec 2025 01:18:44 GMT  
		Size: 28.3 MB (28282810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aff3689d163bbd4af9c09a94ad7a74dda5389e21fb47b8b4e6c615942acbfb0`  
		Last Modified: Tue, 02 Dec 2025 02:34:07 GMT  
		Size: 9.3 MB (9271834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd01d143d595158f3373f0a91956b536cf168337578b1d92bc360d2e79ad9dc5`  
		Last Modified: Tue, 02 Dec 2025 01:18:42 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb430288102add72bd7c69e31658f1006f4406bb02e354ace9344fca3686408`  
		Last Modified: Tue, 02 Dec 2025 01:18:37 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34580383202fa8d43692b2c81afe8582d4beb7d0f34bf72df8f129b885aedfd1`  
		Last Modified: Tue, 02 Dec 2025 01:18:39 GMT  
		Size: 27.0 MB (27025202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d762fdf3a6e0e17808122724339c257f1bda8d25a09c7f3b2d936bd084c027a8`  
		Last Modified: Tue, 02 Dec 2025 01:18:37 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a79aa3517905abde2d9626a1216eef26b873b35598393ac185a5ab20117534`  
		Last Modified: Tue, 02 Dec 2025 01:18:37 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49428f726d9874d51bb129fca640157d2ff70dd8ab0d7178518786e3c063893`  
		Last Modified: Tue, 02 Dec 2025 01:18:37 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.5-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:1c76443e31a4e02ebc2a413747908c17f9007b8b58e02ddbe92f332b85fad76b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1130855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1bb5a91c35e33853689a026978b5ac61166a52e73bbf4694d24096154aa95a3`

```dockerfile
```

-	Layers:
	-	`sha256:369ddf4b37834bf0d27089a461bfbab630406057f9d1f531875442c616a22d23`  
		Last Modified: Tue, 02 Dec 2025 02:29:27 GMT  
		Size: 1.1 MB (1080508 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43f3152251805cfcc5e55b38d63f8b6cd459aae0795ce3cec3e59d2ce13d4556`  
		Last Modified: Tue, 02 Dec 2025 02:29:27 GMT  
		Size: 50.3 KB (50347 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.9-RC4-php8.5-fpm-alpine` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:d17dfd5528417057454e3667165f32767799b1891c4c58eed0f60f79a3483e66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94835257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7a320d481891422a5ca5678e6fa4d68c63760d66d35e72db572fc82ba4c352`
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
# Tue, 02 Dec 2025 01:17:03 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 02 Dec 2025 01:18:50 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:18:50 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:18:50 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:18:52 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:18:52 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:18:52 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:18:52 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:18:52 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:18:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:18:52 GMT
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
	-	`sha256:111e75ab8570f66fd9bacaff9b1e1733a4f380ae4060d50f6c7cab0ed00bdf30`  
		Last Modified: Tue, 02 Dec 2025 01:19:09 GMT  
		Size: 24.4 MB (24377229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3efa4d0c77ebef97ef5d0d17026a2b75554c909fb7872eaa6664e3c0e6850efc`  
		Last Modified: Tue, 02 Dec 2025 01:19:08 GMT  
		Size: 7.7 MB (7699485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e137790b02a507e07dcfaa043f3996fd08a05d07ea6007a01a50650666b0b3d8`  
		Last Modified: Tue, 02 Dec 2025 01:19:08 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c00a54944bd248e8fb63d3a4012fc5eb813ad62c70fba3bb5224806dcac0907`  
		Last Modified: Tue, 02 Dec 2025 01:19:08 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3658acfb248113672d35c80d414cab24435b26d6203da8d06fb5865c074b852`  
		Last Modified: Tue, 02 Dec 2025 01:19:12 GMT  
		Size: 27.0 MB (27025202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84749e95027d7acd663fb233de6c74f0af463e9979a81fd1536cae8ea6215e65`  
		Last Modified: Tue, 02 Dec 2025 01:19:08 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbccfb45f077a2f0da03ad68cb060ea17d06ba740836c9c3f5570d51ee343eba`  
		Last Modified: Tue, 02 Dec 2025 01:19:08 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ee88f6c13b6631f73c85ee1c26601195328a773193a6c9aea8e0e23da4729c9`  
		Last Modified: Tue, 02 Dec 2025 01:19:08 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.5-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:9e680a4bd40970caa03eac6b1fd7338a56497215b77a95ea8c9a5d5fc3013167
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 KB (50277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34cf7fa4994470ba71cf676a1050827c510c4b267d6eba8ae3d64d7ee408caa5`

```dockerfile
```

-	Layers:
	-	`sha256:844bd822bc9cfdb93510999e66e64372198c2e8b3744d969d58c111afe3f0aa0`  
		Last Modified: Tue, 02 Dec 2025 02:29:31 GMT  
		Size: 50.3 KB (50277 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.9-RC4-php8.5-fpm-alpine` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:56618cd3a877b76c330446b9675be3035956b64f37e03fa794dcf8e4f6d074f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93454992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ebb0c11454f9ffc80c56470d7fae756bf2c8643ef59fa8a9364d79a2227338`
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
# Tue, 02 Dec 2025 01:21:05 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 02 Dec 2025 01:22:55 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 02 Dec 2025 01:22:55 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 02 Dec 2025 01:22:55 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 02 Dec 2025 01:22:57 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:22:57 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:22:57 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:22:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:22:57 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:22:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:22:57 GMT
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
	-	`sha256:3e9d7dc55d263086cc5a7e3f4697afd8437ecf2a5aafb5992ab68a347d4f4461`  
		Last Modified: Tue, 02 Dec 2025 01:23:30 GMT  
		Size: 23.2 MB (23152136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b86e09b7dc318fb31807952132f586d6757e1a77392d930acbe90bb17bcb194`  
		Last Modified: Tue, 02 Dec 2025 01:23:29 GMT  
		Size: 8.8 MB (8796221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e8ce632e93dff55de2c780932afd3f28efb940537269a7d3d7bffaad238485b`  
		Last Modified: Tue, 02 Dec 2025 01:23:28 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bc1fda9ef0c12e1ff64bb6e64a3c88eecbb6de54062b13f90993620889e0cc9`  
		Last Modified: Tue, 02 Dec 2025 01:23:28 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698391c49807b762ebbd59db4964196618b5750c4e413067482019b56f3bef06`  
		Last Modified: Tue, 02 Dec 2025 01:23:32 GMT  
		Size: 27.0 MB (27025194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107c21aa3fe4d8c5648be5b070da1d41e7a98d842757c22cb118a8d986fcc183`  
		Last Modified: Tue, 02 Dec 2025 01:23:29 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba205116476b50c8aeddc9ce04c99f644a467d70eee116a46619a15ec46ff89e`  
		Last Modified: Tue, 02 Dec 2025 01:23:29 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6096d4a8aab06e694187a619f46387547985fd18dfb9309a5e748906bb6bdb68`  
		Last Modified: Tue, 02 Dec 2025 01:23:30 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.5-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:23e9e2ed8dfe19a569f81cb653cf45db23f6cb7497bd6a502898312ff13baf8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1129794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13c05ee5da2c10588dc8d0b4a3b7c9a1c4189bb3b4e9d86dbaaec27f51c44de`

```dockerfile
```

-	Layers:
	-	`sha256:722d8cdd0d4d246025c4f130ec8779dbc100003ffec7a597b05e946fd148fc99`  
		Last Modified: Tue, 02 Dec 2025 02:29:34 GMT  
		Size: 1.1 MB (1079302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da15e0979acd76c165f57123e8797c89fe0a27acd5722201963b63784227dde9`  
		Last Modified: Tue, 02 Dec 2025 02:29:35 GMT  
		Size: 50.5 KB (50492 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.9-RC4-php8.5-fpm-alpine` - linux; 386

```console
$ docker pull wordpress@sha256:45f254da175fd2df06125761edaed7d71adf5f2bb31f406893a7240213552cc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.0 MB (102027544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f7cc7ba90d4bda9f436bfb1b40dd1e59bc880dce504b031b53d6d2402f8b9b`
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
# Tue, 02 Dec 2025 01:13:06 GMT
RUN set -eux; 	version='6.9-RC4'; 	sha1='6ea7ab11aa35b69d85c316700efafc45ea10e5da'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 02 Dec 2025 01:13:06 GMT
VOLUME [/var/www/html]
# Tue, 02 Dec 2025 01:13:06 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 02 Dec 2025 01:13:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Dec 2025 01:13:07 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 02 Dec 2025 01:13:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Dec 2025 01:13:07 GMT
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
	-	`sha256:cdcffe587a7b70aa268f1db75b754c561f03c3e46f1e8b3b587d4ad8890ee7b9`  
		Last Modified: Tue, 02 Dec 2025 01:13:32 GMT  
		Size: 27.0 MB (27025191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d6d6df47a4861283eb9f148c73f50e53dcdd0af8f1de87c5861d0f318bd7d5`  
		Last Modified: Tue, 02 Dec 2025 01:13:31 GMT  
		Size: 2.4 KB (2434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7e266c11d053f0f01c6debe0d3754dd4e974706e15b05db8c9676c9ebdbb03`  
		Last Modified: Tue, 02 Dec 2025 01:13:30 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be519092debd826592ce9c19a62f5983cfe31bda6902313d437e8191d90ca40`  
		Last Modified: Tue, 02 Dec 2025 01:13:30 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.9-RC4-php8.5-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:1798dad06ca5403fe16ad46bd77d79a7c7cbef2b743b6ed2c68058505e5226ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1130787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92ed52050f83e0c488b3e8da5e32e62305662e89bb2dfa1c0298796ab3f722b6`

```dockerfile
```

-	Layers:
	-	`sha256:f5511a0b1c2b91f4ab2a98fb73b7355b45d58c57e042cefda83e9391a7d65a39`  
		Last Modified: Tue, 02 Dec 2025 02:29:38 GMT  
		Size: 1.1 MB (1080483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01c1dadfb7b36a49da84d040d9ff8b7ace9377dd6523e528e62ee721ba0e2628`  
		Last Modified: Tue, 02 Dec 2025 02:29:39 GMT  
		Size: 50.3 KB (50304 bytes)  
		MIME: application/vnd.in-toto+json
