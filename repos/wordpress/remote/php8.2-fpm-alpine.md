## `wordpress:php8.2-fpm-alpine`

```console
$ docker pull wordpress@sha256:f76096e409d0cc1aa8b993355f16e2854357338812e2a12037baa621e2d446e6
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

### `wordpress:php8.2-fpm-alpine` - linux; amd64

```console
$ docker pull wordpress@sha256:c90aeeccd3b63dcbfe677b496a4121889a0b9f6f1843bce188e0dc9347cf0f41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107189632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7787446944c2dedfd6a2dc8ecafe7375e34fbfb2c093822ff8703a4187a60900`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:31 GMT
ADD alpine-minirootfs-3.24.0-x86_64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:31 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:53:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 10 Jun 2026 20:53:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 10 Jun 2026 20:53:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 10 Jun 2026 20:53:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Jun 2026 20:53:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 10 Jun 2026 20:53:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 20:53:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 20:53:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Jun 2026 20:53:38 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 10 Jun 2026 20:53:38 GMT
ENV PHP_VERSION=8.2.31
# Wed, 10 Jun 2026 20:53:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.31.tar.xz.asc
# Wed, 10 Jun 2026 20:53:38 GMT
ENV PHP_SHA256=95eae411d594fe6f6e5678b76645dc13ae47d3c0a5325c1d969b58dea56ee45a
# Wed, 10 Jun 2026 20:57:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 10 Jun 2026 20:57:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:00:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 10 Jun 2026 21:00:17 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:00:18 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 10 Jun 2026 21:00:18 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 10 Jun 2026 21:00:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Jun 2026 21:00:18 GMT
WORKDIR /var/www/html
# Wed, 10 Jun 2026 21:00:18 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 10 Jun 2026 21:00:18 GMT
STOPSIGNAL SIGQUIT
# Wed, 10 Jun 2026 21:00:18 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 10 Jun 2026 21:00:18 GMT
CMD ["php-fpm"]
# Wed, 10 Jun 2026 21:12:25 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 10 Jun 2026 21:13:16 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 10 Jun 2026 21:13:16 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Wed, 10 Jun 2026 21:13:16 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 10 Jun 2026 21:13:18 GMT
RUN set -eux; 	version='7.0'; 	sha1='e50bb75667ecaa0eac0694fb3c7b024afc96fde0'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 10 Jun 2026 21:13:18 GMT
VOLUME [/var/www/html]
# Wed, 10 Jun 2026 21:13:18 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 10 Jun 2026 21:13:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:13:18 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Wed, 10 Jun 2026 21:13:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 21:13:18 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9b70e313681f44d32991ec943f89228bc91d7431d4a84feafc269a76e3f96a63`  
		Last Modified: Tue, 09 Jun 2026 20:11:36 GMT  
		Size: 3.9 MB (3866755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eec522a523cd8996ce78e3a99e19af531a6e82199d7b3d922ea42dc16bbf6ab`  
		Last Modified: Wed, 10 Jun 2026 20:57:12 GMT  
		Size: 6.0 MB (5975963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03b878ed4b0c32142a9debaf795074fcfb7f97bada684da3d7970499ec8250c`  
		Last Modified: Wed, 10 Jun 2026 20:57:12 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9306d8986c54d88716638e932c65895c9da939b93ab385534c278e380995edd`  
		Last Modified: Wed, 10 Jun 2026 20:57:12 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee32a29f3c0e40693a777e3adb9b33102cc6d110fef20fdeb0262547e7b419a`  
		Last Modified: Wed, 10 Jun 2026 21:00:26 GMT  
		Size: 12.2 MB (12184203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcefe1c06761b147b66eb5bb0dfdda69b727b1ccefa1dd013f17753ad5ad0ad`  
		Last Modified: Wed, 10 Jun 2026 21:00:25 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a83ee945b108523059ce27a4f3f1055b759d2969dd7e193e61dadcf4b08661`  
		Last Modified: Wed, 10 Jun 2026 21:00:25 GMT  
		Size: 13.2 MB (13172772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c510b160c76e69e1be3eb21fe1506413f9d3f4f16f9022152168b77733ed15`  
		Last Modified: Wed, 10 Jun 2026 21:00:25 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f596012ff9927c7c8c7b8afcb818de120591ecd5cc39b5e92f3f66eda4a05d3f`  
		Last Modified: Wed, 10 Jun 2026 21:00:26 GMT  
		Size: 23.2 KB (23249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1aff0c199cbcae3ac6793fa0fd44d1aadaac14242096237b6cf7efd36c6ec64`  
		Last Modified: Wed, 10 Jun 2026 21:00:26 GMT  
		Size: 23.3 KB (23267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0e01d2044ff507741d512a586ac716e1ef128ed35693b0ec76c1d7616a9ff3`  
		Last Modified: Wed, 10 Jun 2026 21:00:27 GMT  
		Size: 9.2 KB (9247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1cff2511e1b43cc59794b685479926b8f59f67edfc952c5963c01e105e6af0`  
		Last Modified: Wed, 10 Jun 2026 21:13:29 GMT  
		Size: 32.8 MB (32808668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3944ae6f7a70d0002117423ebc3aad25a0f7bae42e806bd00ccc13c79dfebdee`  
		Last Modified: Wed, 10 Jun 2026 21:13:28 GMT  
		Size: 9.5 MB (9466997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3bb4117ea3861e5dba889e444bf7062423f9fea4898c95e0be4527742a78be`  
		Last Modified: Wed, 10 Jun 2026 21:13:28 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a177bf304ed4e6acd529915f07d3ad78c3af05bb00cdbc3cb2ddc7e0d3d3d0ae`  
		Last Modified: Wed, 10 Jun 2026 21:13:28 GMT  
		Size: 384.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb714fceb9bb21658ba94f2bbbf7d9d0654bd9d8ec9ad4050be8e68fbe595992`  
		Last Modified: Wed, 10 Jun 2026 21:13:30 GMT  
		Size: 29.6 MB (29649299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d643d924d1bcc1693724f135d4dec53ea4ab044f95154234e212110dc69993`  
		Last Modified: Wed, 10 Jun 2026 21:13:29 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add75cf79698f7bdf60439f86ea1527dec50469b9162267394e76349be5e2fd9`  
		Last Modified: Wed, 10 Jun 2026 21:13:30 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb1e57a4436824f6914f52b6b282975ff49085661da44347400f2ae6b20f790f`  
		Last Modified: Wed, 10 Jun 2026 21:13:31 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:b37c5b35a12a187f0a588a496119f28dfd9474e4de26dd71ba9be6c01054dcf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1171356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1798c139d07272da276a331b70707dd01cddd8a65fd6deabdf5c689b4721b5d`

```dockerfile
```

-	Layers:
	-	`sha256:ae4fb35097b6212e6975ee57bf4b48222980b15bda796986fbaccc2ddcab9287`  
		Last Modified: Wed, 10 Jun 2026 21:13:27 GMT  
		Size: 1.1 MB (1119633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e844e282471650eb9a4370c666be94723cc88e224913163bb822c81bf4a85efa`  
		Last Modified: Wed, 10 Jun 2026 21:13:27 GMT  
		Size: 51.7 KB (51723 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.2-fpm-alpine` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:46dd824649104fcf909482fecd889a49071bbc7607c24b071c0a54186065e6e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.6 MB (99566941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:945665553efe89d64a3448f50e9a4c9ce9d216a2554f8cb2a1ef8c76501fd9af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:25 GMT
ADD alpine-minirootfs-3.24.0-armhf.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:25 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:41:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 10 Jun 2026 20:41:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 10 Jun 2026 20:41:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 10 Jun 2026 20:41:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Jun 2026 20:41:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 10 Jun 2026 20:41:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 20:41:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 20:41:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Jun 2026 20:41:34 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 10 Jun 2026 20:41:34 GMT
ENV PHP_VERSION=8.2.31
# Wed, 10 Jun 2026 20:41:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.31.tar.xz.asc
# Wed, 10 Jun 2026 20:41:34 GMT
ENV PHP_SHA256=95eae411d594fe6f6e5678b76645dc13ae47d3c0a5325c1d969b58dea56ee45a
# Wed, 10 Jun 2026 20:51:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 10 Jun 2026 20:51:51 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 20:54:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 10 Jun 2026 20:54:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 20:54:39 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 10 Jun 2026 20:54:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 10 Jun 2026 20:54:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Jun 2026 20:54:40 GMT
WORKDIR /var/www/html
# Wed, 10 Jun 2026 20:54:40 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 10 Jun 2026 20:54:40 GMT
STOPSIGNAL SIGQUIT
# Wed, 10 Jun 2026 20:54:40 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 10 Jun 2026 20:54:40 GMT
CMD ["php-fpm"]
# Wed, 10 Jun 2026 21:34:48 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 10 Jun 2026 21:35:53 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 10 Jun 2026 21:35:53 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Wed, 10 Jun 2026 21:35:53 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 10 Jun 2026 21:35:55 GMT
RUN set -eux; 	version='7.0'; 	sha1='e50bb75667ecaa0eac0694fb3c7b024afc96fde0'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 10 Jun 2026 21:35:56 GMT
VOLUME [/var/www/html]
# Wed, 10 Jun 2026 21:35:56 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 10 Jun 2026 21:35:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:35:56 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Wed, 10 Jun 2026 21:35:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 21:35:56 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d44d12cd5c9ecc8e4b75201d67412f77b79157eaffaaed75c3b717bcd42f61e1`  
		Last Modified: Tue, 09 Jun 2026 20:11:29 GMT  
		Size: 3.6 MB (3575314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63958e40f8fe47265f80138ae6d5289666a596a8c5006829db8dc972fd2c50f2`  
		Last Modified: Wed, 10 Jun 2026 20:45:01 GMT  
		Size: 5.6 MB (5569135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820b083e64a778e1fe1b4837260b4689f2e2c6430787238b50f70c8419f6303b`  
		Last Modified: Wed, 10 Jun 2026 20:45:01 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20067b58aaf1e0a1e54d51a8526f71ee55103512ee1714518f48dd59c256c140`  
		Last Modified: Wed, 10 Jun 2026 20:45:01 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095d42bf9d43edc51653c4cc5b0ddebb6fe596e93595dfcacf9ab6d0d37d8abe`  
		Last Modified: Wed, 10 Jun 2026 20:54:46 GMT  
		Size: 12.2 MB (12184224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2072d79b383a4ee237a8b51655830c339083ae34f6a38a1591bdc115b817a04`  
		Last Modified: Wed, 10 Jun 2026 20:54:45 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be726c23aba4c3daef5a7f775da48e3b16396cbf25194c97e5e968c6b3d7b649`  
		Last Modified: Wed, 10 Jun 2026 20:54:46 GMT  
		Size: 11.9 MB (11922483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19350c95aebdc6b73517c29a18f93db85bc6ea752e0b801eec7735ebe81b5b05`  
		Last Modified: Wed, 10 Jun 2026 20:54:45 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf71801f991384754f7d9f2a003b2953863ede22ba1747c27ac598f17edfbc1`  
		Last Modified: Wed, 10 Jun 2026 20:54:46 GMT  
		Size: 23.1 KB (23066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0dc3820346a088e8370e852b04ba21b5ad5699229c85be5bbe0da12fbc76b74`  
		Last Modified: Wed, 10 Jun 2026 20:54:46 GMT  
		Size: 23.1 KB (23090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ec395191f171bbedd74f5da477e6f6bad430a50425cdcd240917a4bdb4169d`  
		Last Modified: Wed, 10 Jun 2026 20:54:47 GMT  
		Size: 9.3 KB (9251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44619fb5e7909241a61d078d3e6a1af7ce112d9ceed9a7d4a3374760b68c5c05`  
		Last Modified: Wed, 10 Jun 2026 21:36:04 GMT  
		Size: 28.8 MB (28768905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa19ea8b1042b3ff48814b78c134e88acb7beae309df1d26125708d701774c7`  
		Last Modified: Wed, 10 Jun 2026 21:36:03 GMT  
		Size: 7.8 MB (7832944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dcf3125c6107f3474a5eea67d52b7698d5ce269c6832d9262ae47821b08d36f`  
		Last Modified: Wed, 10 Jun 2026 21:36:02 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfdc7d5a3432d6953138699578f6b9f00ecb6e7ccd26bfc06827ed3f717f8848`  
		Last Modified: Wed, 10 Jun 2026 21:36:02 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58fd52eff556a3c3f33eaac63b2b71813eed0792bab6f02606a3c2c92588e02`  
		Last Modified: Wed, 10 Jun 2026 21:36:04 GMT  
		Size: 29.6 MB (29649311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ab9a86af5454d00572e63eb6bcf0d89016cd91249327d33276d50d2a5da7e3`  
		Last Modified: Wed, 10 Jun 2026 21:36:04 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6864c0493fc7f07393711422ee6af6b8c76e65d97c391286398a0a01c2176210`  
		Last Modified: Wed, 10 Jun 2026 21:36:05 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa1bd80546e724278170fb341c301f62dc98f08b2fb76237982bf0e77c70c5a8`  
		Last Modified: Wed, 10 Jun 2026 21:36:05 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:fc8a690bb76fc8c6aa496c01ce47c7aa1a5560e77a20c97644ddf137c9fa8bbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 KB (51653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9110b55f146361685f71d5aee9919714155653943a8a946247653dd0f4344682`

```dockerfile
```

-	Layers:
	-	`sha256:14e945353758da0c5483a10fd46ab71aab8ac634dcf4e41a0629fe952ef6eb55`  
		Last Modified: Wed, 10 Jun 2026 21:36:02 GMT  
		Size: 51.7 KB (51653 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.2-fpm-alpine` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:de59c77330c8daf35979222c5d098b6e11dc433cf3c45c5a715546ee23c43a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97570017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e05f5f3692870f7078eb4627f12e79d836a2cef7c0fefb693eab73feb8dff72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 Jun 2026 20:14:38 GMT
ADD alpine-minirootfs-3.24.0-armv7.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:14:38 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 21:00:39 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 10 Jun 2026 21:00:39 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 10 Jun 2026 21:00:39 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 10 Jun 2026 21:00:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Jun 2026 21:00:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 10 Jun 2026 21:00:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 21:00:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 21:00:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Jun 2026 21:00:39 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 10 Jun 2026 21:00:39 GMT
ENV PHP_VERSION=8.2.31
# Wed, 10 Jun 2026 21:00:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.31.tar.xz.asc
# Wed, 10 Jun 2026 21:00:39 GMT
ENV PHP_SHA256=95eae411d594fe6f6e5678b76645dc13ae47d3c0a5325c1d969b58dea56ee45a
# Wed, 10 Jun 2026 21:04:35 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 10 Jun 2026 21:04:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:07:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 10 Jun 2026 21:07:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:07:16 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 10 Jun 2026 21:07:16 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 10 Jun 2026 21:07:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Jun 2026 21:07:16 GMT
WORKDIR /var/www/html
# Wed, 10 Jun 2026 21:07:17 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 10 Jun 2026 21:07:17 GMT
STOPSIGNAL SIGQUIT
# Wed, 10 Jun 2026 21:07:17 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 10 Jun 2026 21:07:17 GMT
CMD ["php-fpm"]
# Wed, 10 Jun 2026 21:32:47 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 10 Jun 2026 21:33:58 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 10 Jun 2026 21:33:58 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Wed, 10 Jun 2026 21:33:59 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 10 Jun 2026 21:34:01 GMT
RUN set -eux; 	version='7.0'; 	sha1='e50bb75667ecaa0eac0694fb3c7b024afc96fde0'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 10 Jun 2026 21:34:01 GMT
VOLUME [/var/www/html]
# Wed, 10 Jun 2026 21:34:01 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 10 Jun 2026 21:34:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:34:01 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Wed, 10 Jun 2026 21:34:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 21:34:01 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:bce674d5697a824549061f4985dfd06a60c018b96ba50b18b7bc1f9ad6143570`  
		Last Modified: Tue, 09 Jun 2026 20:14:43 GMT  
		Size: 3.3 MB (3286160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3182becb74782c15379093b45361c86e1795405b93be5ba2eee61237f4cecbcd`  
		Last Modified: Wed, 10 Jun 2026 21:03:52 GMT  
		Size: 5.2 MB (5223404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267af6d78469945cc336bddea0b298aa96111cfc372805e6b9815092badc7ad0`  
		Last Modified: Wed, 10 Jun 2026 21:03:51 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1d4433db524fea760ab32201e1fe69aa2e9b33629a5276bba4253a35ac27c14`  
		Last Modified: Wed, 10 Jun 2026 21:03:51 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c00e3e193c2f46d87dfdd64d4e6b3b12bc9f3bbbe38f484046776da0083eb2`  
		Last Modified: Wed, 10 Jun 2026 21:07:23 GMT  
		Size: 12.2 MB (12184232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd033055c63a3684c53ce050ff4330221c44a7d35c951d5843f16a6c3e2ad5d4`  
		Last Modified: Wed, 10 Jun 2026 21:07:23 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a3ea40c197a260e2833be4d4aae0372bfbafa911bd90f932c04c5d79173a119`  
		Last Modified: Wed, 10 Jun 2026 21:07:23 GMT  
		Size: 11.2 MB (11223601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d2ad77d529a5f48cf99fa0c626c3538f87b78ad194e517ceb31e32e05a020d`  
		Last Modified: Wed, 10 Jun 2026 21:07:23 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd078c596b6be10c5a95b8ede6ec61a98fe9c61fd56058ecd46b53b85248f24f`  
		Last Modified: Wed, 10 Jun 2026 21:07:24 GMT  
		Size: 23.1 KB (23068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0a3ade8830803f845125053f8a30f1b8ed8c68a98b242d064fa7d03dffd256`  
		Last Modified: Wed, 10 Jun 2026 21:07:24 GMT  
		Size: 23.1 KB (23077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3fac279079da07d59a3f211fc39e8258cbdf339b714882bcb1fd03f03461ae`  
		Last Modified: Wed, 10 Jun 2026 21:07:25 GMT  
		Size: 9.3 KB (9252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe953c1414fe47e304f5bb2772fc305b932ad4f582c1a93a1899410866f62f37`  
		Last Modified: Wed, 10 Jun 2026 21:34:11 GMT  
		Size: 27.1 MB (27091148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f18c432b49ebea5df9c81a4b125cccf7ad2c3b1f325da8e43a107aa2520213`  
		Last Modified: Wed, 10 Jun 2026 21:34:11 GMT  
		Size: 8.8 MB (8847556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28073ac02be8f5cb4ccb8365335d1ae2f8973f2dcb1231f5dee0e66c2afe52ef`  
		Last Modified: Wed, 10 Jun 2026 21:34:10 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1180b0f0f35fd070c39fd6099b5cdefa63d4cd80b4fa0ae1b98455182b4b57f4`  
		Last Modified: Wed, 10 Jun 2026 21:34:10 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e27cf4cf9ae1ac1bfa12a78ad48ca5e121c54a48686ff80f86317ec6cd32ef`  
		Last Modified: Wed, 10 Jun 2026 21:34:12 GMT  
		Size: 29.6 MB (29649301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7a50d3ba8ed95f241cc65406842d33c1d5b478d57bed91399f568587bd4aa4`  
		Last Modified: Wed, 10 Jun 2026 21:34:12 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c94206748fadcd9db1de6edad5cb8d807c4cd9f7131d0570106d0d530c90340`  
		Last Modified: Wed, 10 Jun 2026 21:34:12 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac41947547fb723a95c105f755955b89fd6ab5689a5946fe3ef774a2a7d22f45`  
		Last Modified: Wed, 10 Jun 2026 21:34:13 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:dcd9d7282cfcf96422ea7ba3f418f0c516b7a57b674520bf1736047f4bfef3e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1169641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6d26475a77bca84848f68bb2f6bdf53ccb518ef5a5082962b74a9b8d629ef28`

```dockerfile
```

-	Layers:
	-	`sha256:349b651417d4a55724feb3610d9ba9fbad674a62875a70ce815fb9002a33afb8`  
		Last Modified: Wed, 10 Jun 2026 21:34:10 GMT  
		Size: 1.1 MB (1117775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf4b5760b71dfb774186d2e8325fe722214e369ab039c96c4beba6c7addc8b41`  
		Last Modified: Wed, 10 Jun 2026 21:34:10 GMT  
		Size: 51.9 KB (51866 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.2-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:0c2586efac97eade3b05065fcfc0c60d2e26f2979e6a51d44cd44cac37538dac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.2 MB (107156846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c8a66b67ecf8ec961b4704433251ef7f3f76fb3eb0e5ca0f649df85b04ca9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:09 GMT
ADD alpine-minirootfs-3.24.0-aarch64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:09 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:56:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 10 Jun 2026 20:56:44 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 10 Jun 2026 20:56:44 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 10 Jun 2026 20:56:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Jun 2026 20:56:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 10 Jun 2026 20:56:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 20:56:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 20:56:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Jun 2026 20:56:44 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 10 Jun 2026 20:56:44 GMT
ENV PHP_VERSION=8.2.31
# Wed, 10 Jun 2026 20:56:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.31.tar.xz.asc
# Wed, 10 Jun 2026 20:56:44 GMT
ENV PHP_SHA256=95eae411d594fe6f6e5678b76645dc13ae47d3c0a5325c1d969b58dea56ee45a
# Wed, 10 Jun 2026 21:00:36 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 10 Jun 2026 21:00:36 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:04:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 10 Jun 2026 21:04:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:04:34 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 10 Jun 2026 21:04:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 10 Jun 2026 21:04:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Jun 2026 21:04:34 GMT
WORKDIR /var/www/html
# Wed, 10 Jun 2026 21:04:34 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 10 Jun 2026 21:04:34 GMT
STOPSIGNAL SIGQUIT
# Wed, 10 Jun 2026 21:04:34 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 10 Jun 2026 21:04:34 GMT
CMD ["php-fpm"]
# Wed, 10 Jun 2026 21:10:11 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 10 Jun 2026 21:11:09 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 10 Jun 2026 21:11:10 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Wed, 10 Jun 2026 21:11:10 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 10 Jun 2026 21:11:12 GMT
RUN set -eux; 	version='7.0'; 	sha1='e50bb75667ecaa0eac0694fb3c7b024afc96fde0'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 10 Jun 2026 21:11:12 GMT
VOLUME [/var/www/html]
# Wed, 10 Jun 2026 21:11:12 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 10 Jun 2026 21:11:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:11:12 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Wed, 10 Jun 2026 21:11:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 21:11:12 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c05efffaed614b5ff4e3b9a80136e7c0eed0b47f434802c81baf254c0defca91`  
		Last Modified: Tue, 09 Jun 2026 20:11:14 GMT  
		Size: 4.2 MB (4202330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6ce2b7e213f0f2e1e2f67e3accfc7d3224dc3d6008a413369ab973adeca8c2`  
		Last Modified: Wed, 10 Jun 2026 21:00:22 GMT  
		Size: 6.3 MB (6287195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7f96b81406b28ea7f1d59e53560b5e9a837cb667ae9a14bf540d0374f7e32ac`  
		Last Modified: Wed, 10 Jun 2026 21:00:22 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbee434fed20582875063c2cb0526d9acf87f97642934668a643251c877ce3f1`  
		Last Modified: Wed, 10 Jun 2026 21:00:22 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d9f3be83d6d4afb899321490943b678e55fe923e5dec1ca4814320ff99a9a21`  
		Last Modified: Wed, 10 Jun 2026 21:04:42 GMT  
		Size: 12.2 MB (12184196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d868b27a65e7b9d7fe94297a4f82edf72db15069097582c102cd141f40287116`  
		Last Modified: Wed, 10 Jun 2026 21:04:41 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2203c33c3439607cff5e0fdc070706a26dd9c774e3e1aac517c22f96b18fdf38`  
		Last Modified: Wed, 10 Jun 2026 21:04:42 GMT  
		Size: 13.1 MB (13076562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb87aced58cf8b3515398da81602036fb47d290b6c31e6d4cffb643e8aea760`  
		Last Modified: Wed, 10 Jun 2026 21:04:41 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f242604a567cb2197c3f179c5a3a9994a8f51d1a71b76753161ad3e0663312`  
		Last Modified: Wed, 10 Jun 2026 21:04:42 GMT  
		Size: 23.1 KB (23053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176b4503b10dbab28bfb270c051fd3e42e43e9f5a932ca42902a949290f834b8`  
		Last Modified: Wed, 10 Jun 2026 21:04:42 GMT  
		Size: 23.1 KB (23064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662b8c886eea3c26b5996c5cb394c8fe21d2795b3063d8f4e4dfd81959740478`  
		Last Modified: Wed, 10 Jun 2026 21:04:43 GMT  
		Size: 9.2 KB (9249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4183fd4a44a97fabcbfeebb95d50dd05b7a5c23585f4fc89e6944af23cb2c2a`  
		Last Modified: Wed, 10 Jun 2026 21:11:23 GMT  
		Size: 32.4 MB (32429114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4653627a6ce775b7a499c5cb197fedfb581d62359ee83f6911e22c879c6a08f`  
		Last Modified: Wed, 10 Jun 2026 21:11:22 GMT  
		Size: 9.3 MB (9263578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5552408f2ecaa31e29b929f2ef97c816449e487c8c93172c278b867aace624e4`  
		Last Modified: Wed, 10 Jun 2026 21:11:22 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5a033745d713c4feddda6e94c2d580be4a6cea6637d6603690b4628a6ccb83b`  
		Last Modified: Wed, 10 Jun 2026 21:11:22 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d95e9a05606cb908224be69d58c32bf544ac79d60f36d54add26b82a6b4f7e17`  
		Last Modified: Wed, 10 Jun 2026 21:11:25 GMT  
		Size: 29.6 MB (29649297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f0450f62028562dd4f47d70134c519b049b8b628614a8efd595f2bd827855e6`  
		Last Modified: Wed, 10 Jun 2026 21:11:23 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b5e6ee7c23e4a42960e6a9bd5840eba087d427e2eb77e225254f5406444873a`  
		Last Modified: Wed, 10 Jun 2026 21:11:24 GMT  
		Size: 1.8 KB (1762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42bbc34bbc55718a4971090e2d697da872ee08c011feb5b8f2f6c9d192f5950b`  
		Last Modified: Wed, 10 Jun 2026 21:11:24 GMT  
		Size: 192.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:959318a6b288e13173aa9dab43c786f01b3df143fa1a99b4e6acff4a737df3bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1169697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6ed9007486cd98dd43a610021a2634857a7b5eb9fb5fa2ae0a1f28a9dc80b8`

```dockerfile
```

-	Layers:
	-	`sha256:e93fb715a02e35c053b76b090615bf55d461a9c0445ebefeeeca149c2eff0fcd`  
		Last Modified: Wed, 10 Jun 2026 21:11:21 GMT  
		Size: 1.1 MB (1117795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31d8f7e3c8b5f5c65590a90ec518d78393b47ad51c4881a80ec071920912e28a`  
		Last Modified: Wed, 10 Jun 2026 21:11:22 GMT  
		Size: 51.9 KB (51902 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.2-fpm-alpine` - linux; 386

```console
$ docker pull wordpress@sha256:4939af65d9f6969e1dd2d708a42a58a5f0789b223994e5ca69a943bcae378665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.4 MB (106418006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0a72ed56b5b72ad0ecfc1bf86a17f60770f06434a1a72d6d688650511f3fdf7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 Jun 2026 20:10:54 GMT
ADD alpine-minirootfs-3.24.0-x86.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:10:54 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 21:32:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 10 Jun 2026 21:32:13 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 10 Jun 2026 21:32:13 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 10 Jun 2026 21:32:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Jun 2026 21:32:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 10 Jun 2026 21:32:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 21:32:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 21:32:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Jun 2026 21:32:14 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 10 Jun 2026 21:32:14 GMT
ENV PHP_VERSION=8.2.31
# Wed, 10 Jun 2026 21:32:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.31.tar.xz.asc
# Wed, 10 Jun 2026 21:32:14 GMT
ENV PHP_SHA256=95eae411d594fe6f6e5678b76645dc13ae47d3c0a5325c1d969b58dea56ee45a
# Wed, 10 Jun 2026 21:35:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 10 Jun 2026 21:35:45 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:38:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 10 Jun 2026 21:38:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:38:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 10 Jun 2026 21:38:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 10 Jun 2026 21:38:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Jun 2026 21:38:24 GMT
WORKDIR /var/www/html
# Wed, 10 Jun 2026 21:38:24 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 10 Jun 2026 21:38:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 10 Jun 2026 21:38:24 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 10 Jun 2026 21:38:24 GMT
CMD ["php-fpm"]
# Wed, 10 Jun 2026 23:10:11 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 10 Jun 2026 23:11:02 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 10 Jun 2026 23:11:02 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Wed, 10 Jun 2026 23:11:02 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 10 Jun 2026 23:11:04 GMT
RUN set -eux; 	version='7.0'; 	sha1='e50bb75667ecaa0eac0694fb3c7b024afc96fde0'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 10 Jun 2026 23:11:04 GMT
VOLUME [/var/www/html]
# Wed, 10 Jun 2026 23:11:04 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 10 Jun 2026 23:11:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 23:11:04 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Wed, 10 Jun 2026 23:11:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 23:11:04 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:14b4480cdb6be1a40aafc14c9089d92843794d03fc3115b849ddc49717c25982`  
		Last Modified: Tue, 09 Jun 2026 20:10:59 GMT  
		Size: 3.7 MB (3691754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58ddfeb4bb4e13afa132216ca3d4e09b5774bd6144f850dade79d28eb6c1980`  
		Last Modified: Wed, 10 Jun 2026 21:35:32 GMT  
		Size: 5.8 MB (5823661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015e50921cdc8a590528dbacfa0a674d05f298897b0622bbeafe2291337236aa`  
		Last Modified: Wed, 10 Jun 2026 21:35:32 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110f33450dfd09801a409b585c2e2b4b24f79cfaee89ebcbd4b9fbccdcc9da72`  
		Last Modified: Wed, 10 Jun 2026 21:35:32 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc72c2a010c8ae80dfc7ca720641989fef9007d05cee18a214e527a6e32c7504`  
		Last Modified: Wed, 10 Jun 2026 21:38:31 GMT  
		Size: 12.2 MB (12184196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:679f129b457c490c246c1d02a09283813373c183d6c25116c79c90a7d39f405c`  
		Last Modified: Wed, 10 Jun 2026 21:38:30 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5325b0c9b0272b83a456bd8e204e381e0eef670904f34e6ccad98308504c2ff`  
		Last Modified: Wed, 10 Jun 2026 21:38:31 GMT  
		Size: 13.5 MB (13451786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:344b6d8a99c8d24c5fd37fa3979b2bd2b3e714b1a09231a1ca0062a5e72eb3fd`  
		Last Modified: Wed, 10 Jun 2026 21:38:31 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a58ec1be6023406b5825aad19dd8dfc5fd99a391044d978c99a9c76ea2d4ce9`  
		Last Modified: Wed, 10 Jun 2026 21:38:31 GMT  
		Size: 23.2 KB (23241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c137277ddadb28b8c7d1cf0d77a26040146bb963cec03f618ab27d33ca5f03`  
		Last Modified: Wed, 10 Jun 2026 21:38:32 GMT  
		Size: 23.3 KB (23253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d524950a37b355eea50cd8297139c170281b13ee9a0a5e693ce82fa400ac30b`  
		Last Modified: Wed, 10 Jun 2026 21:38:33 GMT  
		Size: 9.2 KB (9246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e371612d76109c4dffb0d09ccde47b1d01683871659cf6c12bc13c2c36af84`  
		Last Modified: Wed, 10 Jun 2026 23:11:15 GMT  
		Size: 33.2 MB (33220820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d114e2b33576c330034d8ddddceb4e128ce25fe6475beb73581452119ee62008`  
		Last Modified: Wed, 10 Jun 2026 23:11:15 GMT  
		Size: 8.3 MB (8331520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07e48fcc3a92e948dd4422c076241519a31028c6fb55a0fea7927f05959aff2`  
		Last Modified: Wed, 10 Jun 2026 23:11:14 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ecc06e38266ada3bfbd527c80b5db7c04f199d43230d5ff03ce5601df86a809`  
		Last Modified: Wed, 10 Jun 2026 23:11:14 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3350ce235969a5f48beb353f1ef5b63d956192441445d22789ae8e738f018e`  
		Last Modified: Wed, 10 Jun 2026 23:11:17 GMT  
		Size: 29.6 MB (29649309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ded465e9363d9470a2f2254763fe954a9ef07457e67db25ea7533df8992bcb`  
		Last Modified: Wed, 10 Jun 2026 23:11:16 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95832d210e875b5ced04f0081256141b1a02baaa63e72c9c6dd70d6ecb3329f1`  
		Last Modified: Wed, 10 Jun 2026 23:11:16 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cfdb8490ac9b4f3d415907a30353998d6feb909b4b7109e954307384e7640a6`  
		Last Modified: Wed, 10 Jun 2026 23:11:17 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:6497a89f90c0b348ef0ce0dd37b71e1fdd731444a0de3bd944a22bcd3cd9595f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1171289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e145cec67a392240619b00eccabe47b192015f221b0ed06651a25a21fdac7d8d`

```dockerfile
```

-	Layers:
	-	`sha256:20fe4efe842c39e3378a30eeac1d5d6674b48b41d6ff6bdd3312db319716e46e`  
		Last Modified: Wed, 10 Jun 2026 23:11:14 GMT  
		Size: 1.1 MB (1119608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10952503998babd3a9a93420a25e1dc032949874f0efd0f9eb1d714183ef76c3`  
		Last Modified: Wed, 10 Jun 2026 23:11:14 GMT  
		Size: 51.7 KB (51681 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.2-fpm-alpine` - linux; ppc64le

```console
$ docker pull wordpress@sha256:3faa30a08e5fbbed8a14f58a7e2458791c6e77e5c830fceffdaf9f3af2f38e6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.6 MB (108591475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b321ddbb7bde65f2c5d417dba4461d01ded99c7ff5d9e0f25fffe2ac3cc14e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 Jun 2026 20:33:34 GMT
ADD alpine-minirootfs-3.24.0-ppc64le.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:33:34 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:50:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 10 Jun 2026 20:50:57 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 10 Jun 2026 20:50:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 10 Jun 2026 20:50:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Jun 2026 20:50:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 10 Jun 2026 20:50:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 20:50:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 20:50:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Jun 2026 20:50:59 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 10 Jun 2026 20:50:59 GMT
ENV PHP_VERSION=8.2.31
# Wed, 10 Jun 2026 20:50:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.31.tar.xz.asc
# Wed, 10 Jun 2026 20:50:59 GMT
ENV PHP_SHA256=95eae411d594fe6f6e5678b76645dc13ae47d3c0a5325c1d969b58dea56ee45a
# Wed, 10 Jun 2026 21:18:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 10 Jun 2026 21:18:01 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:26:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 10 Jun 2026 21:26:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:26:22 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 10 Jun 2026 21:26:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 10 Jun 2026 21:26:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Jun 2026 21:26:24 GMT
WORKDIR /var/www/html
# Wed, 10 Jun 2026 21:26:25 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 10 Jun 2026 21:26:25 GMT
STOPSIGNAL SIGQUIT
# Wed, 10 Jun 2026 21:26:25 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 10 Jun 2026 21:26:25 GMT
CMD ["php-fpm"]
# Thu, 11 Jun 2026 00:30:57 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Thu, 11 Jun 2026 00:32:33 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 11 Jun 2026 00:32:33 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Thu, 11 Jun 2026 00:32:34 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Thu, 11 Jun 2026 00:32:37 GMT
RUN set -eux; 	version='7.0'; 	sha1='e50bb75667ecaa0eac0694fb3c7b024afc96fde0'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 11 Jun 2026 00:32:38 GMT
VOLUME [/var/www/html]
# Thu, 11 Jun 2026 00:32:38 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 11 Jun 2026 00:32:39 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 00:32:40 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Thu, 11 Jun 2026 00:32:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:32:40 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:73fae309fa62bb67bbe20b40696c81037cf9f77919ce6726a7e535ae9250214e`  
		Last Modified: Tue, 09 Jun 2026 20:33:48 GMT  
		Size: 3.8 MB (3833955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05bf69aa1c55f87e2ef5da703fca33bd334f28f95a4cce0567524060fdf763b7`  
		Last Modified: Wed, 10 Jun 2026 20:55:35 GMT  
		Size: 6.0 MB (6024022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82551215e44da17eb582259647428fdd78b7c59c7221b7a5974f829fc6f1e320`  
		Last Modified: Wed, 10 Jun 2026 20:55:34 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f3d77a4b47a84e644fac42202276c4c43c42eb0ec1975104dc07e396d0f16f`  
		Last Modified: Wed, 10 Jun 2026 20:55:35 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74dc3399354afc298025963321f8fdd3954dc8b1fe9946cf2e40b14f97640afa`  
		Last Modified: Wed, 10 Jun 2026 21:23:15 GMT  
		Size: 12.2 MB (12184235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:363a501d50a58e7220306d50397c916e05c5677b278a0bc46ee6aabe0f2e2ce7`  
		Last Modified: Wed, 10 Jun 2026 21:23:14 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1469e4852efdd2edc6f8bf6803c5dfb4e9c3b3118fbf334ffee89c33c919bddd`  
		Last Modified: Wed, 10 Jun 2026 21:26:39 GMT  
		Size: 13.7 MB (13722944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e56b218d6d569b845470400e2c6e3ca663054aebf6963310861ff4c80a5659b`  
		Last Modified: Wed, 10 Jun 2026 21:26:39 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08b524b5648fd075c857e7eb977f00cfadca3a4b1f23902d64f0221b204d108`  
		Last Modified: Wed, 10 Jun 2026 21:26:38 GMT  
		Size: 23.1 KB (23093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2e19d599a3d1188f41e65a318c10b83acdf1465819f46cc778b04aa2760d09`  
		Last Modified: Wed, 10 Jun 2026 21:26:38 GMT  
		Size: 23.1 KB (23105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3ffac6d2803699c4635c3446ad0348fb26c3934420cd9efefaf0474493ef133`  
		Last Modified: Wed, 10 Jun 2026 21:26:39 GMT  
		Size: 9.3 KB (9251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49240d9e82e67a37330d2416d28d95e780e319fa5213b89a4a8fe40ef3d865c`  
		Last Modified: Thu, 11 Jun 2026 00:33:04 GMT  
		Size: 34.0 MB (34041787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:643df0604694067efd5bd39300e4ae0c9ed8353d5a6b55185e92ec3e4f97d4f3`  
		Last Modified: Thu, 11 Jun 2026 00:33:03 GMT  
		Size: 9.1 MB (9070551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f42f188484160d7f464ae42f40c4641de0bdbeab7bf2b189915ad6c5018f14`  
		Last Modified: Thu, 11 Jun 2026 00:33:02 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa69326f64f4c2bc177a29ca085a93b6fbf8cdde634a81295b4c600cd918b247`  
		Last Modified: Thu, 11 Jun 2026 00:33:02 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99e30ad5fe1948c050bee1787cc22bd1a100a5af5d4808fb47e074303afff1fc`  
		Last Modified: Thu, 11 Jun 2026 00:33:05 GMT  
		Size: 29.6 MB (29649301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49072aaa1299dd40015b99af26994a4ee8759881a20493cb04d6ff2e0d0140e0`  
		Last Modified: Thu, 11 Jun 2026 00:33:04 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67245e59484af084320c8c7f7aff1bec2edc6b574167dcfe65b03bfa083518e0`  
		Last Modified: Thu, 11 Jun 2026 00:33:05 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b3075c824de8eb7a679d4d7ddf9f377ec139cdc989412a3deef59a46424931`  
		Last Modified: Thu, 11 Jun 2026 00:33:06 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:2f765540d03952adb972c66592f6a9ab7b54e7e35be8cb0f6a0611bc2fdf23ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1169549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41f5d2758733ca6c8d96c38a71e34bab06456b2cb675ee106a0f31c7f45ce96`

```dockerfile
```

-	Layers:
	-	`sha256:dc3fe8a30d73c2bde22229e4c78a0fbab2297c802b764e8eda7cdb6972fdc49e`  
		Last Modified: Thu, 11 Jun 2026 00:33:03 GMT  
		Size: 1.1 MB (1117772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4954014a67d2384780e737fa89aeb5e8ac99d7b243b9c6ca2c3a67980b10270c`  
		Last Modified: Thu, 11 Jun 2026 00:33:02 GMT  
		Size: 51.8 KB (51777 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.2-fpm-alpine` - linux; riscv64

```console
$ docker pull wordpress@sha256:2228a93a734d340a368d9fb7d816ddc8f33f121258760991017bd17d3944d795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.4 MB (103420357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6827f192c802731039f579b6574b523d35aeee4be193ffd61e9d33812cbabc79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 10 Jun 2026 00:23:10 GMT
ADD alpine-minirootfs-3.24.0-riscv64.tar.gz / # buildkit
# Wed, 10 Jun 2026 00:23:10 GMT
CMD ["/bin/sh"]
# Thu, 11 Jun 2026 04:52:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 11 Jun 2026 04:52:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 11 Jun 2026 04:52:39 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 11 Jun 2026 04:52:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 11 Jun 2026 04:52:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 11 Jun 2026 04:52:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 04:52:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 11 Jun 2026 04:52:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 11 Jun 2026 04:52:39 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 11 Jun 2026 04:52:39 GMT
ENV PHP_VERSION=8.2.31
# Thu, 11 Jun 2026 04:52:39 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.31.tar.xz.asc
# Thu, 11 Jun 2026 04:52:39 GMT
ENV PHP_SHA256=95eae411d594fe6f6e5678b76645dc13ae47d3c0a5325c1d969b58dea56ee45a
# Thu, 11 Jun 2026 11:23:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 11 Jun 2026 11:23:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 12:59:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 11 Jun 2026 12:59:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 12:59:36 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 11 Jun 2026 12:59:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 11 Jun 2026 12:59:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 11 Jun 2026 12:59:40 GMT
WORKDIR /var/www/html
# Thu, 11 Jun 2026 12:59:41 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 11 Jun 2026 12:59:41 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Jun 2026 12:59:41 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 11 Jun 2026 12:59:41 GMT
CMD ["php-fpm"]
# Sat, 13 Jun 2026 02:44:15 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Sat, 13 Jun 2026 02:57:19 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Sat, 13 Jun 2026 02:57:19 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Sat, 13 Jun 2026 02:57:19 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Sat, 13 Jun 2026 02:57:31 GMT
RUN set -eux; 	version='7.0'; 	sha1='e50bb75667ecaa0eac0694fb3c7b024afc96fde0'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Sat, 13 Jun 2026 02:57:31 GMT
VOLUME [/var/www/html]
# Sat, 13 Jun 2026 02:57:31 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Sat, 13 Jun 2026 02:57:32 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 13 Jun 2026 02:57:32 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Sat, 13 Jun 2026 02:57:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Jun 2026 02:57:32 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3d2f730dbeff3c2e957669de5d586604e82939f67ebfd9142872c9ff56603e07`  
		Last Modified: Wed, 10 Jun 2026 00:23:34 GMT  
		Size: 3.6 MB (3591852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd1dc2b0247d9ffb9aa950846edb9cd66b4f53852a8a9879e3b90eab1e6b59a`  
		Last Modified: Thu, 11 Jun 2026 06:26:26 GMT  
		Size: 5.8 MB (5791702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a6ded20d49de2d129bbc9f97fb6b326363a5b54d9bd6c73e47dee306b314693`  
		Last Modified: Thu, 11 Jun 2026 06:26:24 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f977f288e84989a2379a82f5f4195784dcdf513d90a9d1c0069a2c531162f0d`  
		Last Modified: Thu, 11 Jun 2026 06:26:24 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814c4b0af8e2525763b64e4692db7132b6ca3406951e2d64341d68b35fbaeeb8`  
		Last Modified: Thu, 11 Jun 2026 12:11:52 GMT  
		Size: 12.2 MB (12184215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6791ed6e6cf01e04d2c43368f504018b71b3f9a69290a4ed5a5e5456e1f955fe`  
		Last Modified: Thu, 11 Jun 2026 12:11:49 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf78c839eb5aca60e0f0c97dec5a1bc4a678f39c1225304e1042b80bf2968ad`  
		Last Modified: Thu, 11 Jun 2026 13:00:31 GMT  
		Size: 12.4 MB (12379807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f692b8a80ee9a07ed5ed81e6ba11bfca7ab9ee00dc34b29d140e6f9fc74960`  
		Last Modified: Thu, 11 Jun 2026 13:00:29 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ffe92f6bb297524b77181e0bdeb57f5be6a1be7822da506a91eca5fdb7090fb`  
		Last Modified: Thu, 11 Jun 2026 13:00:29 GMT  
		Size: 23.0 KB (23039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de0ca8a882603904d909a3ff6beead81a1914b2a1fda2d8564ef3b3f5820649`  
		Last Modified: Thu, 11 Jun 2026 13:00:29 GMT  
		Size: 23.1 KB (23058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a2f829a57e4b3d0c5f1e0d5cf7188bd0f60507e5a9aa2de2a333e2c86a0a02`  
		Last Modified: Thu, 11 Jun 2026 13:00:31 GMT  
		Size: 9.3 KB (9254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba3c0be03e24b634da6f5e2e488f67bd9acdfa149e69f0fa4fe630781e97b19`  
		Last Modified: Sat, 13 Jun 2026 02:59:33 GMT  
		Size: 32.6 MB (32602179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df623f4d5e67ebb9b8aaef6d3e21bd48b627d4116d3a9a245d40efa2ee13980`  
		Last Modified: Sat, 13 Jun 2026 02:59:25 GMT  
		Size: 7.2 MB (7156693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70dfefa755df32f14ca2fa6b3c325692756927174515c6ac473a0dfc750ef8ee`  
		Last Modified: Sat, 13 Jun 2026 02:59:23 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10576ff0791d67abec7e99017eb4dc816362eb0767fd4e2bcf134216185d5991`  
		Last Modified: Sat, 13 Jun 2026 02:59:23 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe3fe2d10a360f7b87b9d30a0b592a7e7f07acef0e4d28e3f30bf9e1f69840e`  
		Last Modified: Sat, 13 Jun 2026 02:59:33 GMT  
		Size: 29.6 MB (29649318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5487fe528e254aa1807f136c7e1af0fd56e17cda8be3c61841ade7e2bc893b`  
		Last Modified: Sat, 13 Jun 2026 02:59:25 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2308f565891fa4f6f71efbbf37db2ae1b6cd7ec57f7cb20b9b4a99c0bd3575dd`  
		Last Modified: Sat, 13 Jun 2026 02:59:27 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a79c77055455dd835f5d10d941da5adf2134066bcf0f0e5f2683ec91855950e9`  
		Last Modified: Sat, 13 Jun 2026 02:59:27 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:8afc1631ee15327c059a190645541e4a3e7aee3ec0e35fef1aa2c75f543fbc96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1169545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e08ae017a8f17879d593ef4b38331f2f25bae1f14ea1f44677634d21ed8d5187`

```dockerfile
```

-	Layers:
	-	`sha256:91f8cdbf8b188a8efa9fb07a0f95211fab0299ec695fc3c9ec5887ef100ea62a`  
		Last Modified: Sat, 13 Jun 2026 02:59:23 GMT  
		Size: 1.1 MB (1117768 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2d7a0e379a49bd38ff69a7c563ccd7979cb022c917cef0aed020a23de8e24dc`  
		Last Modified: Sat, 13 Jun 2026 02:59:22 GMT  
		Size: 51.8 KB (51777 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:php8.2-fpm-alpine` - linux; s390x

```console
$ docker pull wordpress@sha256:b571fb1a56673a8e9dbb7cf756facb5d0d6fa8b0ca2f4f990a13b6a699bd64f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107282289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ffe4bb4f04a51f7a5f6055cef23f5ba685a55dc26dfda9c3be58564584088b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 09 Jun 2026 20:18:16 GMT
ADD alpine-minirootfs-3.24.0-s390x.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:18:16 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:59:37 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 10 Jun 2026 20:59:37 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 10 Jun 2026 20:59:37 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 10 Jun 2026 20:59:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 10 Jun 2026 20:59:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 10 Jun 2026 20:59:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 20:59:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 10 Jun 2026 20:59:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 10 Jun 2026 20:59:38 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 10 Jun 2026 20:59:38 GMT
ENV PHP_VERSION=8.2.31
# Wed, 10 Jun 2026 20:59:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.31.tar.xz.asc
# Wed, 10 Jun 2026 20:59:38 GMT
ENV PHP_SHA256=95eae411d594fe6f6e5678b76645dc13ae47d3c0a5325c1d969b58dea56ee45a
# Wed, 10 Jun 2026 21:14:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Wed, 10 Jun 2026 21:14:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:18:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 10 Jun 2026 21:18:02 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 21:18:03 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 10 Jun 2026 21:18:04 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 10 Jun 2026 21:18:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 10 Jun 2026 21:18:04 GMT
WORKDIR /var/www/html
# Wed, 10 Jun 2026 21:18:04 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 10 Jun 2026 21:18:04 GMT
STOPSIGNAL SIGQUIT
# Wed, 10 Jun 2026 21:18:04 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 10 Jun 2026 21:18:04 GMT
CMD ["php-fpm"]
# Wed, 10 Jun 2026 23:09:00 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 10 Jun 2026 23:10:00 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 10 Jun 2026 23:10:00 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Wed, 10 Jun 2026 23:10:00 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Wed, 10 Jun 2026 23:10:02 GMT
RUN set -eux; 	version='7.0'; 	sha1='e50bb75667ecaa0eac0694fb3c7b024afc96fde0'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Wed, 10 Jun 2026 23:10:02 GMT
VOLUME [/var/www/html]
# Wed, 10 Jun 2026 23:10:02 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Wed, 10 Jun 2026 23:10:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 23:10:02 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Wed, 10 Jun 2026 23:10:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Jun 2026 23:10:02 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:4c421b7ac5771added0d41fbc2e1c815472072561366ed82ab9e16b926cb03c6`  
		Last Modified: Tue, 09 Jun 2026 20:18:26 GMT  
		Size: 3.7 MB (3730217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35b3da918cbfec773715cb5c2ba09c98813438f50a50d3430a86242f9c3ace75`  
		Last Modified: Wed, 10 Jun 2026 21:06:04 GMT  
		Size: 5.9 MB (5943440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d360246fb66915c6b8442bb5acd4465ad8e9cb2f0adb4488237ce2913320143`  
		Last Modified: Wed, 10 Jun 2026 21:06:03 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed332689978f619c05676c7b3c891e5c4e1deced85ca5ffcbcf5b048210f92d8`  
		Last Modified: Wed, 10 Jun 2026 21:05:15 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d305ec8be0371a903f127f095c134b0ff99c535d4c89dfc260ab8f48014822eb`  
		Last Modified: Wed, 10 Jun 2026 21:18:15 GMT  
		Size: 12.2 MB (12184204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695a6c26d2e4a1a62604972fec326d1d6adaa57c361fe4dffb0c4e3f9075a2e3`  
		Last Modified: Wed, 10 Jun 2026 21:18:15 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f82357249f4aee01867622f91452882a13909dd3f1ab4a7afefd10d1ecce8a`  
		Last Modified: Wed, 10 Jun 2026 21:18:15 GMT  
		Size: 13.0 MB (13040915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2adc9859713f937f517759c1cb0a46f5cb4f862b7f9443054b6ecc47b8ea64`  
		Last Modified: Wed, 10 Jun 2026 21:18:15 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc2aba4c6f2c882d7710ab5cd60100ad6315fcdcaf9afe9b2a7f89a3048cc96`  
		Last Modified: Wed, 10 Jun 2026 21:18:16 GMT  
		Size: 23.1 KB (23070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e758f6dac5c5312c2be48c2571f89b2f8ba8ef80e472cdb35f9acf60cbdf29d`  
		Last Modified: Wed, 10 Jun 2026 21:18:16 GMT  
		Size: 23.1 KB (23089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8d2401780dd525c37cfb4bd4973ab315e308ef499327abec8f52e499117dce`  
		Last Modified: Wed, 10 Jun 2026 21:18:17 GMT  
		Size: 9.2 KB (9243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fa5654df15f66f7e1a8400a5bd5d64568c23e2ba153dc0f65d5ba0459585141`  
		Last Modified: Wed, 10 Jun 2026 23:10:20 GMT  
		Size: 33.9 MB (33949683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5ebd0135cb2496345534ab8b6fda66db1d1516a04060e5687a401c42810ca9`  
		Last Modified: Wed, 10 Jun 2026 23:10:20 GMT  
		Size: 8.7 MB (8719930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48ad2c28aab0a967272f676182b49a1edb5fe207e5092a412cd3f2916e4f250`  
		Last Modified: Wed, 10 Jun 2026 23:10:19 GMT  
		Size: 307.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c70782182e237f9781c051383d9a62cc764dc11d691dc33f5c26c4403832c2`  
		Last Modified: Wed, 10 Jun 2026 23:10:19 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a730ae2c5bf1a1a994556fdcc2f857379b6818fcc9c97ad03bd7944552b087f8`  
		Last Modified: Wed, 10 Jun 2026 23:10:21 GMT  
		Size: 29.6 MB (29649294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884d242527d30705d4e810847b5d96af1342aa6ea61bc65f12d9eae8b04e51fc`  
		Last Modified: Wed, 10 Jun 2026 23:10:21 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbda9486d2ab62a87839b17859cdeb83944e3a109f9dc23e0995057fb932b0c4`  
		Last Modified: Wed, 10 Jun 2026 23:10:21 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0163f52bab6c33c2ba49e9c929e1fbb09e73b842090eb5b0e8d8602fef524d1b`  
		Last Modified: Wed, 10 Jun 2026 23:10:22 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:67f2a9f644ccf983d99ad4df11bcbe36a253ceea8c807c68b27b1c0f41b5c3fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1169461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7b59c96ca37023651e5a4836bd6c8eca5d56d3bce5b6f781a7d4098d4e734a`

```dockerfile
```

-	Layers:
	-	`sha256:3bf24e1797ad49acd174c4b6aff59ef0f051d7ff633840870aeb656a8510251e`  
		Last Modified: Wed, 10 Jun 2026 23:10:19 GMT  
		Size: 1.1 MB (1117738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d73025012a6fe86bf803c11004cc71ccf356a8276d649ac66194730fafd32a8`  
		Last Modified: Wed, 10 Jun 2026 23:10:19 GMT  
		Size: 51.7 KB (51723 bytes)  
		MIME: application/vnd.in-toto+json
