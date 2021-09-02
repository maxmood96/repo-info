## `wordpress:beta-5.8.1-RC1-fpm-alpine`

```console
$ docker pull wordpress@sha256:e649437dba46833f6204292d3afba1e102a83efd29cf492677cdc2ba7accb4c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm variant v6

### `wordpress:beta-5.8.1-RC1-fpm-alpine` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:13511fd82e380df65ded8d10400dbbf0e8dc6a83b0b50b3727270c9f6276f501
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81749144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80bfca91e063503f6649f54f46c4be977e3f2101c3312a8be36414f0e45e87db`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Fri, 27 Aug 2021 20:48:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 27 Aug 2021 20:48:04 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Fri, 27 Aug 2021 20:48:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 27 Aug 2021 20:48:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 27 Aug 2021 20:48:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 27 Aug 2021 20:53:20 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 27 Aug 2021 20:53:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 20:53:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 27 Aug 2021 20:53:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 27 Aug 2021 21:14:36 GMT
ENV GPG_KEYS=42670A7FE4D0441C8E4632349E4FDC074A4EF02D 5A52880781F755608BF815FC910DEB46F53EA312
# Fri, 27 Aug 2021 21:14:36 GMT
ENV PHP_VERSION=7.4.23
# Fri, 27 Aug 2021 21:14:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.4.23.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.4.23.tar.xz.asc
# Fri, 27 Aug 2021 21:14:37 GMT
ENV PHP_SHA256=cea52313fcffe56343bcd3c66dbb23cd5507dc559cc2e3547cf8f5452e88a05d
# Fri, 27 Aug 2021 21:14:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 27 Aug 2021 21:14:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 27 Aug 2021 21:19:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -perm +0111 -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 27 Aug 2021 21:19:20 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 27 Aug 2021 21:19:22 GMT
RUN docker-php-ext-enable sodium
# Fri, 27 Aug 2021 21:19:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Aug 2021 21:19:23 GMT
WORKDIR /var/www/html
# Fri, 27 Aug 2021 21:19:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 27 Aug 2021 21:19:25 GMT
STOPSIGNAL SIGQUIT
# Fri, 27 Aug 2021 21:19:26 GMT
EXPOSE 9000
# Fri, 27 Aug 2021 21:19:26 GMT
CMD ["php-fpm"]
# Sat, 28 Aug 2021 02:53:06 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	;
# Sat, 28 Aug 2021 02:54:54 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		mysqli 		zip 	; 	pecl install imagick-3.5.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps
# Sat, 28 Aug 2021 02:54:56 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Sat, 28 Aug 2021 02:54:58 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 02 Sep 2021 19:56:53 GMT
RUN set -eux; 	version='5.8.1-RC1'; 	sha1='a88cb0846d1385958d88b8fb93d36585c985e916'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 777 wp-content
# Thu, 02 Sep 2021 19:56:54 GMT
VOLUME [/var/www/html]
# Thu, 02 Sep 2021 19:56:55 GMT
COPY --chown=www-data:www-datafile:2708a2c2ddd7102be41b667427e2ff8a8f87e2fe99f16c5d6508102164a04563 in /usr/src/wordpress/ 
# Thu, 02 Sep 2021 19:56:55 GMT
COPY file:5be6bcc31206cb827f037769d89fd092037ed61a1e10d6cae7939a37055beb4c in /usr/local/bin/ 
# Thu, 02 Sep 2021 19:56:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 02 Sep 2021 19:56:56 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05720bf4927bb754d842782fff2d045d42b804759e30b8312cbf75272e200af`  
		Last Modified: Fri, 27 Aug 2021 21:55:19 GMT  
		Size: 1.7 MB (1696736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c9951b98a5bb83a868efe164832e7d1a35e9a078a82219f95634454a864a332`  
		Last Modified: Fri, 27 Aug 2021 21:55:18 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6baa29c72aee654b7205fcfbde95333a6e9a5dfadc1a99d94e64c957f543ac`  
		Last Modified: Fri, 27 Aug 2021 21:55:18 GMT  
		Size: 267.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0dc849da240ee519899d1f19c5306738aa04bddb40d04a3f17a5c4c91c471fb`  
		Last Modified: Fri, 27 Aug 2021 22:00:25 GMT  
		Size: 10.4 MB (10390794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae7e4f462145d9cd373b97ba5eb1bf03e212e3fd826e5a90c1966a8761d28df`  
		Last Modified: Fri, 27 Aug 2021 22:00:21 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:940c41cded5fc0e07123d3d0d999ac25d73a4d171605b499ca330acdbfadc485`  
		Last Modified: Fri, 27 Aug 2021 22:00:27 GMT  
		Size: 13.4 MB (13364203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adefaa414e95736ae05cb208dc292442768fdb11031034f7f135c1e19e24cc1f`  
		Last Modified: Fri, 27 Aug 2021 22:00:21 GMT  
		Size: 2.3 KB (2267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5645a069385c52ec6af2a968510100afbeb0f921a4caad78f36e1e7b02db4087`  
		Last Modified: Fri, 27 Aug 2021 22:00:21 GMT  
		Size: 17.8 KB (17811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0630fd51a735fcd89f422255eb1943a4380ab8940ea4128bd8a83f162f124cdf`  
		Last Modified: Fri, 27 Aug 2021 22:00:21 GMT  
		Size: 8.4 KB (8445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19492b6d8aed1370cb8c4e29771e15b793fb200cef6ad9aa3aceb6930e39c047`  
		Last Modified: Sat, 28 Aug 2021 03:10:57 GMT  
		Size: 37.5 MB (37538104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e44da86050a5aba41dac116d9ca83820e5c5253bed43299a23fdc9097f9cf71`  
		Last Modified: Sat, 28 Aug 2021 03:10:33 GMT  
		Size: 1.1 MB (1117828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f92f6fe2beddb9367f98d952f7098913f64de29ec28a2d5b21bdf34bff9e918`  
		Last Modified: Sat, 28 Aug 2021 03:10:30 GMT  
		Size: 63.9 KB (63878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51bc4277f650d6957bcefd90d131375519df932e4bd1f0d28db410b52ce424e`  
		Last Modified: Sat, 28 Aug 2021 03:10:30 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b70f141cef23896771ebfee5d5566e0c83e49617a11a049d9d21c431f979cc`  
		Last Modified: Thu, 02 Sep 2021 20:02:38 GMT  
		Size: 14.9 MB (14915124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928ae95dc38208c11705dbcacaa12d31c98bbb41c298bd749e8342e979c8bbec`  
		Last Modified: Thu, 02 Sep 2021 20:02:26 GMT  
		Size: 2.4 KB (2358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3333809c8854081b02db90776e0ddd920c833f2d9539af36d82dd6965f1ac159`  
		Last Modified: Thu, 02 Sep 2021 20:02:26 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
