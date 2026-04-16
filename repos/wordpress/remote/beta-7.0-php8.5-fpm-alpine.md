## `wordpress:beta-7.0-php8.5-fpm-alpine`

```console
$ docker pull wordpress@sha256:44ff64e93bbb6fbd85f28d04f5a924c23dd6c49088b2c999ec44bde0a61f0c84
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

### `wordpress:beta-7.0-php8.5-fpm-alpine` - linux; amd64

```console
$ docker pull wordpress@sha256:73cceb96c28f32d134bd98d6f32fd44a7b4122fd13a6aefd186df0dc0341299b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.1 MB (110101857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a04e3380758adc6446618db5943af8bbdaad1d8958c6f9615d1062eaa0a2c8ce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:18:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:18:01 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:18:01 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:18:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:18:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:18:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:18:01 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:18:01 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:18:01 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 15 Apr 2026 20:18:01 GMT
ENV PHP_VERSION=8.5.5
# Wed, 15 Apr 2026 20:18:01 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 15 Apr 2026 20:18:01 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 15 Apr 2026 20:18:05 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:18:05 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:21:30 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:21:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:21:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:21:31 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 20:21:31 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 15 Apr 2026 20:21:31 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:21:31 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 15 Apr 2026 20:21:31 GMT
CMD ["php-fpm"]
# Wed, 15 Apr 2026 21:22:12 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 15 Apr 2026 21:23:09 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 15 Apr 2026 21:23:09 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Wed, 15 Apr 2026 21:23:09 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 15 Apr 2026 21:23:11 GMT
RUN set -eux; 	version='7.0-RC2'; 	sha1='829cd48a30fd8458902f19d5f35361ec6e335341'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 15 Apr 2026 21:23:11 GMT
VOLUME [/var/www/html]
# Wed, 15 Apr 2026 21:23:11 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 15 Apr 2026 21:23:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:23:11 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Wed, 15 Apr 2026 21:23:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:23:11 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e487c53d1acaf17b69fb83fbc32894f124ddc3cba3352cc5869eeda96fc2f7`  
		Last Modified: Wed, 15 Apr 2026 20:21:39 GMT  
		Size: 3.6 MB (3587422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c3db260efd2043a7367652215b9ec7ad3248d4165920ad2e32fc7b1a2b415d8`  
		Last Modified: Wed, 15 Apr 2026 20:21:38 GMT  
		Size: 929.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a1e3cccba5da112d23ec6ff9362301d1ad085ba71b910f1df328c2a1c19c01`  
		Last Modified: Wed, 15 Apr 2026 20:21:38 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5040a0692c51580613bbcb27114c9d5ae99ee4a1e0822dccd9b978b5130b4cba`  
		Last Modified: Wed, 15 Apr 2026 20:21:39 GMT  
		Size: 14.4 MB (14379181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f10cfc13d8422ddee0a8de712b24988af3f874fd7c6e16d44f00d9f2c432e5`  
		Last Modified: Wed, 15 Apr 2026 20:21:40 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a3db88b4073712e7c8a653f4792b7cc198ad7c0a88d670276fe24ae553ade7`  
		Last Modified: Wed, 15 Apr 2026 20:21:40 GMT  
		Size: 16.6 MB (16645446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36bd52e8fd1faabc8efe8d49da39584b734cc05465ce4dbaca0440cc5d3c79b6`  
		Last Modified: Wed, 15 Apr 2026 20:21:40 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d86b1f07852c38ce4e230f52321d6ac83643778a10b0fa7999396417f27045`  
		Last Modified: Wed, 15 Apr 2026 20:21:41 GMT  
		Size: 23.4 KB (23392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1eb0ec79d595be95a8fbe92cb6a4a41badef1ad3741b7564cdb985ab3f6f388`  
		Last Modified: Wed, 15 Apr 2026 20:21:41 GMT  
		Size: 9.3 KB (9262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443690b12319377a0c6d49127b8eb33a9f81e6e01988318f8f084208667f529f`  
		Last Modified: Wed, 15 Apr 2026 21:23:24 GMT  
		Size: 32.8 MB (32839285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c653de74fbe920668a8b252478e6e0ff2cfe5e2955a474a08364b6cde1efd0e3`  
		Last Modified: Wed, 15 Apr 2026 21:23:23 GMT  
		Size: 9.4 MB (9420626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da30d905bf880b7345141980d99f6db3f6f3a2164b8757809fc1263410fc6b5d`  
		Last Modified: Wed, 15 Apr 2026 21:23:23 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd071ae6f15d25cfdf199f11edfb3d89978e55bb0bddad172b8e88777ecae893`  
		Last Modified: Wed, 15 Apr 2026 21:23:22 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba55473d7d3dae2f6165248b0b686b6111db6eb9646cbb4b64182356d49dd4ea`  
		Last Modified: Wed, 15 Apr 2026 21:23:24 GMT  
		Size: 29.3 MB (29323854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28459e4a54c4a2765704cc43932854863dee1075841cbe825b73b4c66628c3fc`  
		Last Modified: Wed, 15 Apr 2026 21:23:24 GMT  
		Size: 2.4 KB (2433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bb746641cc2fb0c633dca6ef85af72c39b3c6da05b7dc91a49493abcd6f5d8`  
		Last Modified: Wed, 15 Apr 2026 21:23:24 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f2db9d3da214499abc7fd40b30598a16c7b8f24df732ac45b9c7c81825c26a`  
		Last Modified: Wed, 15 Apr 2026 21:23:25 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-7.0-php8.5-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:ca7bbbac6f1308b55013c56c4147ae3c4220d125b7a54354de52eb9f62aa81f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1169210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d17be87d05cfe4a61f70bed25f3585ba5a41a038109260b9af6cc7ad4b26e9`

```dockerfile
```

-	Layers:
	-	`sha256:e6382e429d759aa0aaeb8588903eb83fa69a3737e4dba040684d6749d17c6712`  
		Last Modified: Wed, 15 Apr 2026 21:23:22 GMT  
		Size: 1.1 MB (1118863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d6e39a83b95cb96d9ab67c6dbe1d13a15f18a84f9ca1527d1cfb361307487ca`  
		Last Modified: Wed, 15 Apr 2026 21:23:22 GMT  
		Size: 50.3 KB (50347 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-7.0-php8.5-fpm-alpine` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:0d2a7dc105cfa3ac19145ef3c8b3aa9f8ff2c20681358aaf4543910590b9c7fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.7 MB (101717078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:837963051de3413a608de08cfe5dfe8352501b2d170a921b86bb0a42a0e23a61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:19:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:19:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:19:16 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:19:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:19:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:19:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:19:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:19:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:19:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 15 Apr 2026 20:19:16 GMT
ENV PHP_VERSION=8.5.5
# Wed, 15 Apr 2026 20:19:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 15 Apr 2026 20:19:16 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 15 Apr 2026 20:19:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:19:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:22:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:22:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:22:29 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:22:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:22:29 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 20:22:29 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 15 Apr 2026 20:22:29 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:22:29 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 15 Apr 2026 20:22:29 GMT
CMD ["php-fpm"]
# Wed, 15 Apr 2026 21:19:36 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 15 Apr 2026 21:49:17 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 15 Apr 2026 21:49:17 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Wed, 15 Apr 2026 21:49:17 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 15 Apr 2026 21:49:19 GMT
RUN set -eux; 	version='7.0-RC2'; 	sha1='829cd48a30fd8458902f19d5f35361ec6e335341'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 15 Apr 2026 21:49:19 GMT
VOLUME [/var/www/html]
# Wed, 15 Apr 2026 21:49:19 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 15 Apr 2026 21:49:19 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:49:19 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Wed, 15 Apr 2026 21:49:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:49:19 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d6d2edc905715af430101e14f9660d8300b13cda3ee9dd7fe71b26cf5c95dc0`  
		Last Modified: Wed, 15 Apr 2026 20:22:35 GMT  
		Size: 3.5 MB (3543066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5c2022d796ccc079f7ced47d2a7410d8979401803bed26f6defb477dfbb84a`  
		Last Modified: Wed, 15 Apr 2026 20:22:34 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1355f70c84f1b9639980f76f20602ea2956b6a6c28461110be220e657de2cee`  
		Last Modified: Wed, 15 Apr 2026 20:22:34 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ddbc5011da0178cabefd1e32e1fe42bf0209293bf648fa57831497a25c6b2e`  
		Last Modified: Wed, 15 Apr 2026 20:22:35 GMT  
		Size: 14.4 MB (14379196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb83d2a100f2115f12b39a3f415012bfa46809465e98e3261e7608c7a4d29a87`  
		Last Modified: Wed, 15 Apr 2026 20:22:35 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c795e1348424330505f748794e3d42144d35ac873e11b07c55e0fc62ba5290`  
		Last Modified: Wed, 15 Apr 2026 20:22:36 GMT  
		Size: 14.6 MB (14578006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f704907db20153babb99d280622729a26880d7540573e1a332fe012654cafc37`  
		Last Modified: Wed, 15 Apr 2026 20:22:36 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db21c91962f59afe919f4d50d7344ce32d83f0788b07101f28b144102e40ba7`  
		Last Modified: Wed, 15 Apr 2026 20:22:36 GMT  
		Size: 23.2 KB (23206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5138f39f8ffeac596dcfa6bb943045da32b30d339fc6646f0cf5a669afb25dde`  
		Last Modified: Wed, 15 Apr 2026 20:22:37 GMT  
		Size: 9.3 KB (9260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7daf2a18e71ec6f83b9943a3b1bdfda8960e0170692b818872897c1990fde2b8`  
		Last Modified: Wed, 15 Apr 2026 21:49:27 GMT  
		Size: 28.6 MB (28550491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3032b63e38a511179112679c640db9ac18b4376a91c6fb33d1c69c6c08e749ba`  
		Last Modified: Wed, 15 Apr 2026 21:49:27 GMT  
		Size: 7.7 MB (7728899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca22a2d138c247a49aa02a8d03d1788c12c76f9dcc63ff8aa1d525f23483143`  
		Last Modified: Wed, 15 Apr 2026 21:49:26 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a038c093437d8f7e23df59c4151ffc6c538c015914f845fd7fc0d5debe782575`  
		Last Modified: Wed, 15 Apr 2026 21:49:31 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca03c3a606513a2edefe34f9889b3da05e1354495e58d63a00184263feaee33`  
		Last Modified: Wed, 15 Apr 2026 21:49:28 GMT  
		Size: 29.3 MB (29323873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7529d6b1bcbb81986706b9862fd326f6deb5898ffd101f126a31c958de97db`  
		Last Modified: Wed, 15 Apr 2026 21:49:28 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df3d14af0bc0fedc5cac0dc5cc03efe7310f7b78b22cbfd054ce9b53a1db754`  
		Last Modified: Wed, 15 Apr 2026 21:49:29 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06a292b8a149c564c33efecb1fb07977cfb5f599d05338afe26b066956fcea2`  
		Last Modified: Wed, 15 Apr 2026 21:49:29 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-7.0-php8.5-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:6475197ca78d858e8c2a75048d770e2e45fa060bdfee5d7d662c27ff8a2a993c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 KB (50277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8948f2228a9962d103a49fdc2e592e4deaf0079cf3abf0698511f9f4e3a064`

```dockerfile
```

-	Layers:
	-	`sha256:198e2b3b9e9bcce96261c6556aaca7928b27846146e3afba8ebe7b1bd260d99b`  
		Last Modified: Wed, 15 Apr 2026 21:49:26 GMT  
		Size: 50.3 KB (50277 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-7.0-php8.5-fpm-alpine` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:96d7f1a92f62f67fa44ef3371f4edc69d08af45a6b8aea359f4a1d9c047c92e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.8 MB (99777059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43efecdf4fe59e7652fd936901e107415f57795b46747cb4b425a18c8ba2be81`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:19:05 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:19:05 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:19:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:19:05 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_VERSION=8.5.5
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 15 Apr 2026 20:19:05 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 15 Apr 2026 20:19:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:19:09 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:22:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:22:13 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:22:14 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:22:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:22:14 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 20:22:14 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 15 Apr 2026 20:22:14 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:22:14 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 15 Apr 2026 20:22:14 GMT
CMD ["php-fpm"]
# Wed, 15 Apr 2026 21:31:02 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 15 Apr 2026 21:32:51 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 15 Apr 2026 21:32:51 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Wed, 15 Apr 2026 21:32:51 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 15 Apr 2026 21:32:53 GMT
RUN set -eux; 	version='7.0-RC2'; 	sha1='829cd48a30fd8458902f19d5f35361ec6e335341'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 15 Apr 2026 21:32:53 GMT
VOLUME [/var/www/html]
# Wed, 15 Apr 2026 21:32:53 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 15 Apr 2026 21:32:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:32:54 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Wed, 15 Apr 2026 21:32:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:32:54 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d097287e0cfb66680b2dc36b29ce93178f5250669510e4e1e4b1a16e4dac24d`  
		Last Modified: Wed, 15 Apr 2026 20:22:20 GMT  
		Size: 3.3 MB (3343346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df49c1a7b5dee4d633696635de988bfd5e1aa6a04105426cf6a94696874d72a7`  
		Last Modified: Wed, 15 Apr 2026 20:22:20 GMT  
		Size: 928.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f7ae4f484af388fdf75d5f67b786ac0ad2339b162afa90a5f2965f9fc245168`  
		Last Modified: Wed, 15 Apr 2026 20:22:20 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6f0d558219672e0fc364cf77406614dff17f26515c5fb71e64d313263c464d`  
		Last Modified: Wed, 15 Apr 2026 20:22:21 GMT  
		Size: 14.4 MB (14379199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c5c45c1e96c8b5536eb4b02296cc6ded1c5b9b455093242dbb011d687b40b0e`  
		Last Modified: Wed, 15 Apr 2026 20:22:21 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae1d1200583ed017771ed102597bb463f1b63cc83a92dbf3b9470c22e43bcd3a`  
		Last Modified: Wed, 15 Apr 2026 20:22:21 GMT  
		Size: 13.8 MB (13772364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b4eca4749f0bcf6db56dba5aa8b7584429f53d8fbb3b00eee03ac355953590`  
		Last Modified: Wed, 15 Apr 2026 20:22:21 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df1d1b10d7729a2bc0da26938b5eb483bd5246deec2c1aac5ad46e1b89576e0`  
		Last Modified: Wed, 15 Apr 2026 20:22:22 GMT  
		Size: 23.2 KB (23207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9cbeb58b6222eb6d3b431c7a600675302e4f75366fee8a843fce0254a08ab0`  
		Last Modified: Wed, 15 Apr 2026 20:22:22 GMT  
		Size: 9.3 KB (9261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417d63c791aab9aa19439c4cccfdad7841bc979f00a78e6be95c0c961618f2cd`  
		Last Modified: Wed, 15 Apr 2026 21:33:03 GMT  
		Size: 26.9 MB (26900815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639dd92e5fa86fe2b99ba419b353673dfff3af0d1c9189f52d94a4badc91a849`  
		Last Modified: Wed, 15 Apr 2026 21:33:03 GMT  
		Size: 8.7 MB (8732668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0efcbeb8110b53f40b0f8275d7ec2cea4eb0c9221c6bbf33617269d8a56b800e`  
		Last Modified: Wed, 15 Apr 2026 21:33:02 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71363289c2bcfe291d7fca3f21faae6b606cb5426c4f5046a057adb15786012`  
		Last Modified: Wed, 15 Apr 2026 21:33:02 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec4d88ec15de7c116797d373a1a012a654317a5c7c3dd61fe7150cc611b413`  
		Last Modified: Wed, 15 Apr 2026 21:33:04 GMT  
		Size: 29.3 MB (29323875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534f78a8d0a549b3604956d2ef87a6b3a03102a5c76b3b8b50653933152a214e`  
		Last Modified: Wed, 15 Apr 2026 21:33:04 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7b6c74dba8c29e66b49978d4555178b9b2f51cfad003e9af23b8b1c5220c1c`  
		Last Modified: Wed, 15 Apr 2026 21:33:04 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba8a61f58a0786765df4858b9ef987838f9fc5e39725acf68180be84cdf7c1d9`  
		Last Modified: Wed, 15 Apr 2026 21:33:05 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-7.0-php8.5-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:cc3cb7c9d97aa59d32dffc2968d60efb0216413d59daad2a6c6439e9ab5bc698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1167497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9bd6041f077459044fe4f8e9a4c95bb5275f1f3f5f56bd987b1e40a3229f00`

```dockerfile
```

-	Layers:
	-	`sha256:e3e4d15ba49a639153902652ea554ef04fc2ddcf2d0daa21ae90c570bda2d8ad`  
		Last Modified: Wed, 15 Apr 2026 21:33:02 GMT  
		Size: 1.1 MB (1117007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:033239511d498e8f721d30904f6a5d81733c1f42ba850330aba0a016dfd79d09`  
		Last Modified: Wed, 15 Apr 2026 21:33:02 GMT  
		Size: 50.5 KB (50490 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-7.0-php8.5-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:76b2fd9494bd82e35726d4819a2a334e016681b82e1e1ede52293e424898a184
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.2 MB (109190745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c90b82a83df517e01deb47bac714c9467aa1a8626546ff319f9297fd34959e26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:16:21 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:16:21 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:16:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:16:21 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_VERSION=8.5.5
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 15 Apr 2026 20:16:21 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 15 Apr 2026 20:16:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:16:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:19:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:19:54 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:19:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:19:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:19:55 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 20:19:55 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 15 Apr 2026 20:19:55 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:19:55 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 15 Apr 2026 20:19:55 GMT
CMD ["php-fpm"]
# Wed, 15 Apr 2026 21:37:10 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 15 Apr 2026 21:38:26 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 15 Apr 2026 21:38:26 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Wed, 15 Apr 2026 21:38:26 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 15 Apr 2026 21:38:28 GMT
RUN set -eux; 	version='7.0-RC2'; 	sha1='829cd48a30fd8458902f19d5f35361ec6e335341'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 15 Apr 2026 21:38:28 GMT
VOLUME [/var/www/html]
# Wed, 15 Apr 2026 21:38:28 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 15 Apr 2026 21:38:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 21:38:28 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Wed, 15 Apr 2026 21:38:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 21:38:28 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb06a5f44ff2e27382b40122cbea490f562cdae5f2ca795b9f0e29b768bdd5f5`  
		Last Modified: Wed, 15 Apr 2026 20:20:03 GMT  
		Size: 3.6 MB (3596151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c0edc310dc19501413b5668245bc984741c4ac5a3219932a74e83fb33b6f94`  
		Last Modified: Wed, 15 Apr 2026 20:20:02 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d665080207d06b6b7246d46376f6ec0b3a5d072b47f01ab3fe89eb95ea0b9310`  
		Last Modified: Wed, 15 Apr 2026 20:20:02 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de69444967d9cb641ef25e6d8a49c93461ac0e52973d87fdb7f488b1ab3819f1`  
		Last Modified: Wed, 15 Apr 2026 20:20:03 GMT  
		Size: 14.4 MB (14379183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da631dfa865e2d394e47bb93c95f041d309af42b22cd597826fab10299773bc`  
		Last Modified: Wed, 15 Apr 2026 20:20:03 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a07793fe9e504b32d25eab1c34f5705523e5e6cbfb8a4e6866cfebcb8b6157`  
		Last Modified: Wed, 15 Apr 2026 20:20:04 GMT  
		Size: 16.1 MB (16050421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200ac0ec9bbff4e2fbe60dba84cb1323e4e62f7236323483c01966a53c489de3`  
		Last Modified: Wed, 15 Apr 2026 20:20:04 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f862e0a569cbee79112f863d9b6df967cd5741fcacf230bf763d4a52e22e937`  
		Last Modified: Wed, 15 Apr 2026 20:20:04 GMT  
		Size: 23.2 KB (23215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697e03ddee6a82d7b1297c429e3eab590881e76969d5107a1342682d97bb2124`  
		Last Modified: Wed, 15 Apr 2026 20:20:05 GMT  
		Size: 9.3 KB (9262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97db58ab04e570e2ac89ab36bd2d33a8499a41d6a93a9cbf8f2e9012fdaaf0d`  
		Last Modified: Wed, 15 Apr 2026 21:38:40 GMT  
		Size: 32.5 MB (32479992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62b840a98c7ca9028ff1a6d7f421aa3c7c95a0f93a0f5159cd40303ec806ebf`  
		Last Modified: Wed, 15 Apr 2026 21:38:39 GMT  
		Size: 9.1 MB (9119563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d2db0e201b2bd2bffe85779dd8c63bebf6ab68f5db4263840c0f5ebc97b7ae`  
		Last Modified: Wed, 15 Apr 2026 21:38:39 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a563ea21c836cec7970733ed8cdc9356d850758689e51d7c4a15d2063cb7a6a1`  
		Last Modified: Wed, 15 Apr 2026 21:38:39 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f27962ebb104a3ee21ceb328a167e038e4483927cc16702db8a63ee1702a54`  
		Last Modified: Wed, 15 Apr 2026 21:38:41 GMT  
		Size: 29.3 MB (29323871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e10555205a72a4e0fc1dc577cd44cb1f8843a6a9fb9c6d606d1ec39cc7f2849`  
		Last Modified: Wed, 15 Apr 2026 21:38:40 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59aed69cbd8c11b1d863800411d152272d6af028dd73b57b725f62efc17f23f`  
		Last Modified: Wed, 15 Apr 2026 21:38:40 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e709fab838dcaace06f8412f0590bd7963bd8922be90d5c4045c9f3a2eee769`  
		Last Modified: Wed, 15 Apr 2026 21:38:41 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-7.0-php8.5-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:f92e05c9ae5ede6b8470073b12280b2691c2053f7fab37dcb41f49dd5047670f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1167553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceb257e2d3d968255d44518626889cfa2462a3d64410608a00cb1b1aae3927d3`

```dockerfile
```

-	Layers:
	-	`sha256:ae92ea06dcc2b4a592f084d06a77aafb0179aad39d6a9dfc37a6ed8810a55e49`  
		Last Modified: Wed, 15 Apr 2026 21:38:39 GMT  
		Size: 1.1 MB (1117027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8eebd3493a6654b0ae9977a22166e6e097e4593f526ca3dc86fce5e84dfdaaa`  
		Last Modified: Wed, 15 Apr 2026 21:38:38 GMT  
		Size: 50.5 KB (50526 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-7.0-php8.5-fpm-alpine` - linux; 386

```console
$ docker pull wordpress@sha256:bea9b1dc9977e22f8f8e9165d95b16666f4927d95d16895912fbcdd26b56b16f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109606317 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d04bbb30581e94c7b2d83f0a60dac18ad6588993dfb0222dd167392bf626495b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:21:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 22:21:08 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 22:21:08 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 22:21:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 22:21:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 22:21:08 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 22:21:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 22:21:08 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 22:21:08 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 15 Apr 2026 22:21:08 GMT
ENV PHP_VERSION=8.5.5
# Wed, 15 Apr 2026 22:21:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 15 Apr 2026 22:21:08 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 15 Apr 2026 22:21:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 22:21:13 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:24:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 22:24:17 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 22:24:17 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 22:24:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 22:24:17 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 22:24:17 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 15 Apr 2026 22:24:17 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 22:24:17 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 15 Apr 2026 22:24:17 GMT
CMD ["php-fpm"]
# Wed, 15 Apr 2026 23:16:04 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 15 Apr 2026 23:17:04 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 15 Apr 2026 23:17:04 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Wed, 15 Apr 2026 23:17:04 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 15 Apr 2026 23:17:06 GMT
RUN set -eux; 	version='7.0-RC2'; 	sha1='829cd48a30fd8458902f19d5f35361ec6e335341'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 15 Apr 2026 23:17:06 GMT
VOLUME [/var/www/html]
# Wed, 15 Apr 2026 23:17:06 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 15 Apr 2026 23:17:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 23:17:06 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Wed, 15 Apr 2026 23:17:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Apr 2026 23:17:06 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d9a505f547e3d9eb5663215e04e826d44f0d401d3785806e50d8a309cf6400`  
		Last Modified: Wed, 15 Apr 2026 22:24:24 GMT  
		Size: 3.6 MB (3625725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf478daa99cc48b7805f96ddb16a298870e4ff40452ee8447d76279d37ecb615`  
		Last Modified: Wed, 15 Apr 2026 22:24:24 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3051d9c840d84814ba87ce49c9977b75f90c33a72fd15251203bd1f31a3c3f7`  
		Last Modified: Wed, 15 Apr 2026 22:24:24 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46cd9a1464733d90b14e78659a9f56e2f0127d1d6097f9fab062cb48fdb138e3`  
		Last Modified: Wed, 15 Apr 2026 22:24:25 GMT  
		Size: 14.4 MB (14379180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84991a7bce009f0349f52c61f07d54f5b27d110479a722ab97b6ce66aef73e6`  
		Last Modified: Wed, 15 Apr 2026 22:24:25 GMT  
		Size: 482.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be03f8b3f49a3d01fc68e451e52320db1bbb4334df82bac9799c02581684412`  
		Last Modified: Wed, 15 Apr 2026 22:24:26 GMT  
		Size: 17.0 MB (16975213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2dfac4547f6962d344b34bc170644c822a0848742bd96cd122a2b8d07ff7730`  
		Last Modified: Wed, 15 Apr 2026 22:24:26 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab85a31569bcc2097487aed36084eef19eb0faf0d999bf26854a7a85272a4f66`  
		Last Modified: Wed, 15 Apr 2026 22:24:26 GMT  
		Size: 23.4 KB (23392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf94d3ffb1fdf78c2e7adc042ba02b7a3e9d88eb00c66beaa27042ccc63a1842`  
		Last Modified: Wed, 15 Apr 2026 22:24:27 GMT  
		Size: 9.3 KB (9257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d985881594d42af4a2645b1a28d28086489940c18a0bb2cba083707971dcf24`  
		Last Modified: Wed, 15 Apr 2026 23:17:17 GMT  
		Size: 33.3 MB (33305536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4acbed6a403d5b244d006e38f88875cef7a438cd87ff7c5c9270de0a9ac61c8d`  
		Last Modified: Wed, 15 Apr 2026 23:17:17 GMT  
		Size: 8.3 MB (8264520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92de9cbfd7bf25bed3295058d70521dd069e1e8c2c5fc8eabf3f07e496106e1c`  
		Last Modified: Wed, 15 Apr 2026 23:17:16 GMT  
		Size: 307.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901155b217554054cf2d87b66ec7545a946169966241718a5a6e7bef59110a19`  
		Last Modified: Wed, 15 Apr 2026 23:17:16 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888a3d0666bc9b82f155eb6085264740e2222926d2c4e65e75ead602a6a549c1`  
		Last Modified: Wed, 15 Apr 2026 23:17:18 GMT  
		Size: 29.3 MB (29323862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3872394d31b0e5ef794b793f07143a6d72d6a3a963115c27bf54f1e0b7d24f4`  
		Last Modified: Wed, 15 Apr 2026 23:17:18 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcdeb8686aee0e5e3e2b35ad9e7e221674610648abe8286db427a66a3e7bbdf4`  
		Last Modified: Wed, 15 Apr 2026 23:17:18 GMT  
		Size: 1.8 KB (1758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87559cd99e8ba1d5abac6a990566ecdad8585ca2f8463b670df99a5d1b0fb004`  
		Last Modified: Wed, 15 Apr 2026 23:17:19 GMT  
		Size: 190.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-7.0-php8.5-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:2672fc2830ead24630e4c4d92813b0a1d630addfd5dcd840021d42c80132c951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1169143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed5de63c8cc0907ab5de160e03e07e3d35489175d9a4b0c9d216aea6c66e9186`

```dockerfile
```

-	Layers:
	-	`sha256:f01080acbed002455114f47d80e517c8dacef9823c6eb5868c6a74364c6a8bba`  
		Last Modified: Wed, 15 Apr 2026 23:17:16 GMT  
		Size: 1.1 MB (1118838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:336cbc2323febe2d0bd31a3011c78e186798b161be4dff2e4085bd3a525ca1c3`  
		Last Modified: Wed, 15 Apr 2026 23:17:16 GMT  
		Size: 50.3 KB (50305 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-7.0-php8.5-fpm-alpine` - linux; ppc64le

```console
$ docker pull wordpress@sha256:bab3cd4c25963fa513cb5a0e47166cdd67c2b9010de52fa31c3144bfa4983289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.2 MB (111158476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a87528eb985434c77577c59ced4b7d8764664111e7f2ccf7be2d209ad4f26285`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:20:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:20:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:20:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:20:47 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_VERSION=8.5.5
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 15 Apr 2026 20:20:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 15 Apr 2026 20:20:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:26:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 15 Apr 2026 20:26:21 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 15 Apr 2026 20:26:23 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 15 Apr 2026 20:26:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 15 Apr 2026 20:26:23 GMT
WORKDIR /var/www/html
# Wed, 15 Apr 2026 20:26:24 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 15 Apr 2026 20:26:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:26:24 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 15 Apr 2026 20:26:24 GMT
CMD ["php-fpm"]
# Wed, 15 Apr 2026 23:58:23 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Thu, 16 Apr 2026 00:00:45 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 16 Apr 2026 00:00:45 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Thu, 16 Apr 2026 00:00:46 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 16 Apr 2026 00:06:26 GMT
RUN set -eux; 	version='7.0-RC2'; 	sha1='829cd48a30fd8458902f19d5f35361ec6e335341'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 16 Apr 2026 00:06:26 GMT
VOLUME [/var/www/html]
# Thu, 16 Apr 2026 00:06:26 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 16 Apr 2026 00:06:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Apr 2026 00:06:27 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Thu, 16 Apr 2026 00:06:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Apr 2026 00:06:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a59216db1edcf64b90905df63416f821bfacdba590544dcdb3c340ea538567c`  
		Last Modified: Wed, 15 Apr 2026 20:26:31 GMT  
		Size: 3.8 MB (3767095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dbb332183b4f53eb48b10e61f11a67b23c5647a6901cf35be6037e209a0f51`  
		Last Modified: Wed, 15 Apr 2026 20:26:31 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd758015c67cd7fae70202df89f7e42a01ff424cadf0cd92070805333b28821`  
		Last Modified: Wed, 15 Apr 2026 20:26:31 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e52ab3e8c2bdcda9a7d7fa46781ba1b64218f1a43cdbae79b0f884f0a4ac5979`  
		Last Modified: Wed, 15 Apr 2026 20:26:32 GMT  
		Size: 14.4 MB (14379191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393fc66660721ed61e917e80da810113cf7576555e17ec694197fa33041e629d`  
		Last Modified: Wed, 15 Apr 2026 20:26:33 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56904556e0f43d1903e11ea5703eb3181e1ac435a8ed7de10d6df5358084cf31`  
		Last Modified: Wed, 15 Apr 2026 20:26:37 GMT  
		Size: 16.7 MB (16739203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01e9f03fe5b55a0a4ffe779e2e1d4e92d7f54cbfca561dff8d2cb04f0e49c9e`  
		Last Modified: Wed, 15 Apr 2026 20:26:37 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce66c2b53da90dcfc42ca3e531a9ea84d748e59d91828ba06bd14d5b70486a6`  
		Last Modified: Wed, 15 Apr 2026 20:26:37 GMT  
		Size: 23.2 KB (23218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc31a575c6e39692b56b287545cedadc039d663696b1e1a5c20ec03c544d503`  
		Last Modified: Wed, 15 Apr 2026 20:26:37 GMT  
		Size: 9.3 KB (9263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b61d0b79cfb69012a3fb3cf6907ab517a2361ac0ed48d50f15f922e1dbddc57`  
		Last Modified: Thu, 16 Apr 2026 00:01:21 GMT  
		Size: 34.1 MB (34068803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b8e6a1bd0fa2f29191f9cc4944dae0ab1f9aa7d5173ef27963b58bd7a63306`  
		Last Modified: Thu, 16 Apr 2026 00:01:19 GMT  
		Size: 9.0 MB (9007678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9b194d87432856a8ddfc8a903dcfb0765676751f50b3e0292173817c37acd3`  
		Last Modified: Thu, 16 Apr 2026 00:01:19 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38fb640ceaffe35e328e99f843fd3346252a96072e92f9ade13980bee2d1d734`  
		Last Modified: Thu, 16 Apr 2026 00:01:21 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f6440c1f164695f6b161d960957093ef8f98f4e9efe3e7fbefc2697171e630`  
		Last Modified: Thu, 16 Apr 2026 00:06:46 GMT  
		Size: 29.3 MB (29323865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2b31be9ebdd9534c68c8af136a73281cc2b615deb07c59b90658aefda8c9905`  
		Last Modified: Thu, 16 Apr 2026 00:06:45 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83d1efc3de2de4d40390333bcd24ee04a1eba69db839c75f7e8701ccc40bace`  
		Last Modified: Thu, 16 Apr 2026 00:06:45 GMT  
		Size: 1.8 KB (1769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba268957670aba58904a66393f0aafa553cfc077c6d6375cab8aa9582ca75111`  
		Last Modified: Thu, 16 Apr 2026 00:06:45 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-7.0-php8.5-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:6f54bfd998de299e1fbae94e91668bf6831c62881e0776f166def96ca28941b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1167404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49d11c82f1a53b7c7d16f8820e4c27eac6d68be7d17c032620fb076a7c98c021`

```dockerfile
```

-	Layers:
	-	`sha256:5b177a5067d765f3588e31e2dc26e4af1724323cae45643e50dd5015eecdd50f`  
		Last Modified: Thu, 16 Apr 2026 00:06:45 GMT  
		Size: 1.1 MB (1117004 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80738246892da965b50f5d1e50baaa1c2a20ea05d219773904c31b4c6292ba8d`  
		Last Modified: Thu, 16 Apr 2026 00:06:45 GMT  
		Size: 50.4 KB (50400 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-7.0-php8.5-fpm-alpine` - linux; riscv64

```console
$ docker pull wordpress@sha256:19cef2ca58a0a5a0868de0274864b56c79e6c8e31c7350c431d77289b91b1725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.7 MB (106697271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16a20050e2a0554acca10ab9df06775542f763fc4aecfb977d083e361c4b3859`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 09:13:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 28 Jan 2026 09:13:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 28 Jan 2026 09:13:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 28 Jan 2026 09:13:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 28 Jan 2026 09:13:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 28 Jan 2026 09:13:07 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_VERSION=8.5.5
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Fri, 10 Apr 2026 09:29:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 10 Apr 2026 09:29:21 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 11:29:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 10 Apr 2026 11:29:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 10 Apr 2026 11:29:35 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 10 Apr 2026 11:29:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Apr 2026 11:29:36 GMT
WORKDIR /var/www/html
# Fri, 10 Apr 2026 11:29:36 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 10 Apr 2026 11:29:36 GMT
STOPSIGNAL SIGQUIT
# Fri, 10 Apr 2026 11:29:36 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 10 Apr 2026 11:29:36 GMT
CMD ["php-fpm"]
# Sun, 12 Apr 2026 06:14:07 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Sun, 12 Apr 2026 06:37:50 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Sun, 12 Apr 2026 06:37:50 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Sun, 12 Apr 2026 06:37:51 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Sun, 12 Apr 2026 07:51:08 GMT
RUN set -eux; 	version='7.0-RC2'; 	sha1='829cd48a30fd8458902f19d5f35361ec6e335341'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Sun, 12 Apr 2026 07:51:09 GMT
VOLUME [/var/www/html]
# Sun, 12 Apr 2026 07:51:09 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Sun, 12 Apr 2026 07:51:09 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sun, 12 Apr 2026 07:51:09 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Sun, 12 Apr 2026 07:51:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 12 Apr 2026 07:51:09 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d64a68485fdb9ab2ec4159ac3e04e0bb79d9f1d037e580e928ca2b9604180f`  
		Last Modified: Wed, 28 Jan 2026 10:13:59 GMT  
		Size: 3.7 MB (3741000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b030c1b113432578231e8fe7c8a1bc913f2dc5dcba512e805fa9ab07768c9bd4`  
		Last Modified: Wed, 28 Jan 2026 10:13:58 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32a0e9bcb36b34307b4eada1f50c1cd4244d43d19ee57d962818dcb0ff0b110`  
		Last Modified: Wed, 28 Jan 2026 10:13:58 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20501e9e3d17b72af47b7d522d0c369998be222ed66ed9070ed2cbc45e500ca7`  
		Last Modified: Fri, 10 Apr 2026 10:29:42 GMT  
		Size: 14.4 MB (14379290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7fa0bbe8ea35a7aeededb6a1c62d4e192d88a3cbaa6a9ac613390cef5f797e`  
		Last Modified: Fri, 10 Apr 2026 10:29:38 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec67c2ac63fe7bbb0c28ea3262405d3e05e0dddcaacef0ae0dc70b301d1987c6`  
		Last Modified: Fri, 10 Apr 2026 11:30:33 GMT  
		Size: 15.4 MB (15437417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f2f28c97f0f660fbf457176ef0bf0f3e68dc725d14453c0fb86ffc13bae588`  
		Last Modified: Fri, 10 Apr 2026 11:30:30 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2523c4fe3aed7470277613db8e9ab519ae4523e42b5da7f18574f0758b61bcae`  
		Last Modified: Fri, 10 Apr 2026 11:30:30 GMT  
		Size: 23.4 KB (23355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef532bdf1bd4a78f6dbcc4af2103ecfb10d474cc5a120ccf4eb84f38e8c99e8e`  
		Last Modified: Fri, 10 Apr 2026 11:30:30 GMT  
		Size: 9.3 KB (9262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f322daf33fdf8c9bc301d4b70b6bc246922f27f989208069fa73fcb831c2f49`  
		Last Modified: Sun, 12 Apr 2026 06:40:04 GMT  
		Size: 32.7 MB (32652816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6756b31c87719236aabccd4a3268a85832aeb0789aa063895e7e55fa2b4672ac`  
		Last Modified: Sun, 12 Apr 2026 06:39:56 GMT  
		Size: 7.5 MB (7535726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebb4af270cc1463138c404d658cfd1e4215f5b98efa4f7338960cf80922d5c3`  
		Last Modified: Sun, 12 Apr 2026 06:39:54 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff616aca347fe17a89a16470bf9768b33c69a3e01a7d4317f7924d2cfd8fc55e`  
		Last Modified: Sun, 12 Apr 2026 06:39:54 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91de5d9d1733ffb0c2ae79f3403611eb003f8ca90d2072c504d24dc938110bf9`  
		Last Modified: Sun, 12 Apr 2026 07:53:04 GMT  
		Size: 29.3 MB (29323875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b43b40eb8fd60ebd8e95610d243fd4084161cbe9ae2970c30d86b9a1b50886b`  
		Last Modified: Sun, 12 Apr 2026 07:52:59 GMT  
		Size: 2.4 KB (2441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c5539fa7237e5f439ac3e15a086008f899329cde5d9fa341351fcb03c9596f`  
		Last Modified: Sun, 12 Apr 2026 07:52:59 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e5b1e058cc870a02fdca98f9709a12cc0c12f2f94d66449b1a8490a6049ee5d`  
		Last Modified: Sun, 12 Apr 2026 07:52:59 GMT  
		Size: 198.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-7.0-php8.5-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:e9b3671a2443b1313b8fce130fdd251b7f8e5db45cae0f0d604b4a388dd40e6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1170379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86cc16c7b1d46d8fce42918be21958f4ca78d1e1943d0f2299c6690947168de8`

```dockerfile
```

-	Layers:
	-	`sha256:73ec55f16d00680bfdaa4f159cbc4abb46a40962d04b8c9ae8fca77aa172ce2d`  
		Last Modified: Sun, 12 Apr 2026 07:52:59 GMT  
		Size: 1.1 MB (1119978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed474b8bebe102b33640bb0cb395afdd6c2453b9c4e9067e2cbe13b796b3ff1e`  
		Last Modified: Sun, 12 Apr 2026 07:52:58 GMT  
		Size: 50.4 KB (50401 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-7.0-php8.5-fpm-alpine` - linux; s390x

```console
$ docker pull wordpress@sha256:f7fd9eb805889dbcbc2d1aeda7b55f262fb2973c2738bbff2ce6587fc25aaa36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **110.4 MB (110365543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:521784f07f0454faafc596f7d76e86a93dea763c4b7284b62b1ad741240a26cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Mar 2026 23:37:17 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Mar 2026 23:37:17 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Mar 2026 23:37:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Mar 2026 23:37:17 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_VERSION=8.5.5
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Thu, 09 Apr 2026 22:21:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 09 Apr 2026 22:21:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:27:04 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 09 Apr 2026 22:27:04 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 22:27:05 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 09 Apr 2026 22:27:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Apr 2026 22:27:05 GMT
WORKDIR /var/www/html
# Thu, 09 Apr 2026 22:27:05 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 09 Apr 2026 22:27:05 GMT
STOPSIGNAL SIGQUIT
# Thu, 09 Apr 2026 22:27:05 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 09 Apr 2026 22:27:05 GMT
CMD ["php-fpm"]
# Thu, 09 Apr 2026 23:16:27 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Thu, 09 Apr 2026 23:17:59 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 09 Apr 2026 23:17:59 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Thu, 09 Apr 2026 23:17:59 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 09 Apr 2026 23:18:01 GMT
RUN set -eux; 	version='7.0-RC2'; 	sha1='829cd48a30fd8458902f19d5f35361ec6e335341'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 09 Apr 2026 23:18:01 GMT
VOLUME [/var/www/html]
# Thu, 09 Apr 2026 23:18:01 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 09 Apr 2026 23:18:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 09 Apr 2026 23:18:01 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Thu, 09 Apr 2026 23:18:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 09 Apr 2026 23:18:01 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4348d21358ef752a357c33976b85357317bfb623a79cb91ec462b4e5128b82d5`  
		Last Modified: Thu, 12 Mar 2026 23:43:03 GMT  
		Size: 3.8 MB (3795119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a169c2de4deea9b877eb224ec8f2d4f4502dd0bb4e22037516ea41c23c8c1e6`  
		Last Modified: Thu, 12 Mar 2026 23:43:02 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f88a80dfabed7faa02e1bbe28dd4e26c817c26d54bb3411b27cc398ea997ef8`  
		Last Modified: Thu, 12 Mar 2026 23:43:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f5e7662fcf96af1dfae3edab12e535e5dbb2bd9336314490ac9484222315cc0`  
		Last Modified: Thu, 09 Apr 2026 22:27:14 GMT  
		Size: 14.4 MB (14379286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b2bd611f10e897bc78163d788b300458c71f27af849508076d219371619381`  
		Last Modified: Thu, 09 Apr 2026 22:27:14 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75bbbb1baae2fbf2bedd4c3bb0435491f6f0267b7191e5eb40e2660528cb3c6`  
		Last Modified: Thu, 09 Apr 2026 22:27:17 GMT  
		Size: 16.4 MB (16403239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df982ef1a4905e6b8978d449941a2e81108fe80be5f77d2a257a16917c2aac6`  
		Last Modified: Thu, 09 Apr 2026 22:27:16 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a03f2cd7d9e1efbf2f858143cfcdac24d487cd37e4e1c7e511366d5c540fad`  
		Last Modified: Thu, 09 Apr 2026 22:27:16 GMT  
		Size: 23.4 KB (23428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fedb2b6a2f584706db3490eb3500f0c32d8d85cdde7c42375868e1ac25cafca`  
		Last Modified: Thu, 09 Apr 2026 22:27:17 GMT  
		Size: 9.3 KB (9261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3136cf23dc19b4309dd412688a064892229aeb731a4f224bc4b5e5f440cb910`  
		Last Modified: Thu, 09 Apr 2026 23:18:18 GMT  
		Size: 34.0 MB (34010705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d90bfab1ffc659d98e6f96bd593ddc75f9438e53f5d0d983d7f3f03c813eab`  
		Last Modified: Thu, 09 Apr 2026 23:18:18 GMT  
		Size: 8.7 MB (8686111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:887b72da724a56cc8d370bfbc426e0126273b42b67d2d2c5318fa62a6a439086`  
		Last Modified: Thu, 09 Apr 2026 23:18:17 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e15e061baef3e93b89b19c12a1f4cdb1ad13c7a596a8d653027110e787bc67e`  
		Last Modified: Thu, 09 Apr 2026 23:18:17 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7c3ab880b48dab1009b151f6b395a90497cdf59634555728aaf1c25593f213`  
		Last Modified: Thu, 09 Apr 2026 23:18:19 GMT  
		Size: 29.3 MB (29323845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed45e3df84e4e9ca453020a0e7a7157cf361ade57cfe3e081970faad3c978968`  
		Last Modified: Thu, 09 Apr 2026 23:18:18 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45248843b257bf09d323a937f105879d518db7bca3bd4e711365f76ef6d65fdb`  
		Last Modified: Thu, 09 Apr 2026 23:18:19 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0bf3b9b11fba1a9fc7ef338e370991c2df15658b43e26b2de7432516c6271a1`  
		Last Modified: Thu, 09 Apr 2026 23:18:19 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-7.0-php8.5-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:162aa73394ae09f498932b287a2a43e947336316a2645adad61886fb61aa9bde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1170295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6752edc692bf0ec89f985881f035e5276f79626204973eb8e0080841ebef17cf`

```dockerfile
```

-	Layers:
	-	`sha256:fa7122a5f57ab7f4204a7dda9bf306aab158551a7731b22acd38f87f41e5c915`  
		Last Modified: Thu, 09 Apr 2026 23:18:17 GMT  
		Size: 1.1 MB (1119948 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a44e072fe1a7073319e2c5a79d21e3d4cb20dc45a2dda707bec98ba55e61806`  
		Last Modified: Thu, 09 Apr 2026 23:18:17 GMT  
		Size: 50.3 KB (50347 bytes)  
		MIME: application/vnd.in-toto+json
