## `wordpress:beta-6.2-RC2-php8.2-fpm-alpine`

```console
$ docker pull wordpress@sha256:63dc47442ea0bd72f31724e8aecc1b3dca73b2170c021adaafde718378c394fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm variant v6

### `wordpress:beta-6.2-RC2-php8.2-fpm-alpine` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:20cfe172d029e271524db188f4927282ea9e8c14fd9199644a628b1c23ab96a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.9 MB (96929288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bafa384748d23e20a1c1d731698b9d07deaaaa795991e1bbc303a2a890e081c2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 13 Mar 2023 16:12:44 GMT
ADD file:d825d9aef59df0df23c0140a490998407ee0a62a051699b5c050aef7cb03f042 in / 
# Mon, 13 Mar 2023 16:12:44 GMT
CMD ["/bin/sh"]
# Mon, 13 Mar 2023 21:07:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 13 Mar 2023 21:07:08 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Mon, 13 Mar 2023 21:07:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Mon, 13 Mar 2023 21:07:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 13 Mar 2023 21:07:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Mon, 13 Mar 2023 21:07:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 13 Mar 2023 21:07:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 13 Mar 2023 21:07:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 13 Mar 2023 21:07:10 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Mon, 13 Mar 2023 21:24:18 GMT
ENV PHP_VERSION=8.2.3
# Mon, 13 Mar 2023 21:24:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.3.tar.xz.asc
# Mon, 13 Mar 2023 21:24:19 GMT
ENV PHP_SHA256=b9b566686e351125d67568a33291650eb8dfa26614d205d70d82e6e92613d457
# Mon, 13 Mar 2023 21:24:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Mon, 13 Mar 2023 21:24:26 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Mon, 13 Mar 2023 21:29:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Mon, 13 Mar 2023 21:29:27 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Mon, 13 Mar 2023 21:29:28 GMT
RUN docker-php-ext-enable sodium
# Mon, 13 Mar 2023 21:29:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 13 Mar 2023 21:29:28 GMT
WORKDIR /var/www/html
# Mon, 13 Mar 2023 21:29:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Mon, 13 Mar 2023 21:29:29 GMT
STOPSIGNAL SIGQUIT
# Mon, 13 Mar 2023 21:29:29 GMT
EXPOSE 9000
# Mon, 13 Mar 2023 21:29:29 GMT
CMD ["php-fpm"]
# Tue, 14 Mar 2023 02:54:14 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	;
# Tue, 14 Mar 2023 02:55:11 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.6.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]
# Tue, 14 Mar 2023 02:55:12 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Tue, 14 Mar 2023 02:55:12 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini
# Thu, 16 Mar 2023 00:08:04 GMT
RUN set -eux; 	version='6.2-RC2'; 	sha1='275008d535aa34e840dd8f6913cdb64b6006a9a5'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 777 wp-content
# Thu, 16 Mar 2023 00:08:04 GMT
VOLUME [/var/www/html]
# Thu, 16 Mar 2023 00:08:04 GMT
COPY --chown=www-data:www-datafile:d38fd3c0db552e13465e83c5d7bbd85c7c3d036bf1285495988cc4ab2ffaf7f5 in /usr/src/wordpress/ 
# Thu, 16 Mar 2023 00:08:04 GMT
COPY file:5be6bcc31206cb827f037769d89fd092037ed61a1e10d6cae7939a37055beb4c in /usr/local/bin/ 
# Thu, 16 Mar 2023 00:08:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Mar 2023 00:08:05 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6a6e4ab63e54442e16400f69d37f662d60cbd67565631eff6bf59b4176e482c3`  
		Last Modified: Fri, 10 Feb 2023 20:50:22 GMT  
		Size: 3.1 MB (3110885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b525ba211658332771b8d1e1e6274a63819ca62cce4ae60af48bd6ea6de2e81e`  
		Last Modified: Mon, 13 Mar 2023 22:29:45 GMT  
		Size: 1.9 MB (1865508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8f3139761283dde8c51dccb6f9887eedcebb955cb74f916390ef170c7f432c`  
		Last Modified: Mon, 13 Mar 2023 22:29:45 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d473bc0ad5e16dc9e7a8b062b4d46e1bc4c325a792b684246fdf4710b85a59`  
		Last Modified: Mon, 13 Mar 2023 22:29:45 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8597bb2febebb8d97845f8f7fca8e5250eeca2dae9764264d442c13512b37828`  
		Last Modified: Mon, 13 Mar 2023 22:31:42 GMT  
		Size: 12.1 MB (12058794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9124282b1dd0809bb3d98a8b3ae21604d032a80424eca04de7c504bbe5b91775`  
		Last Modified: Mon, 13 Mar 2023 22:31:41 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9cd5821050aba6bd7c6a788ea0aeb25c5c45cf0eee65f8aef23cece7ebacca6`  
		Last Modified: Mon, 13 Mar 2023 22:32:40 GMT  
		Size: 11.6 MB (11576571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aadf981cb111d5d440e17a4b1747e01b64ac588ab41c4882e89763d7fd2107c8`  
		Last Modified: Mon, 13 Mar 2023 22:32:38 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cdbc7a42d2b1d3ed7b5647d56a2e12f73b670a218625985a26fdf2014a723fc`  
		Last Modified: Mon, 13 Mar 2023 22:32:38 GMT  
		Size: 18.7 KB (18732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc973bed292454cace731ae3f47809bfb4af372677c19d324a58fab3ab7b30c4`  
		Last Modified: Mon, 13 Mar 2023 22:32:38 GMT  
		Size: 9.2 KB (9175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:618dd1c879958eaada06d454db46937ee87365c8ecd15951873a1c013ba3cd6e`  
		Last Modified: Tue, 14 Mar 2023 03:03:30 GMT  
		Size: 41.2 MB (41218318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df0239986fd8b54b2f3fdaab08db83f07a2bf6c0354062a8e9e765ce72246d7`  
		Last Modified: Tue, 14 Mar 2023 03:03:24 GMT  
		Size: 4.1 MB (4149679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ccbf28b7fac7a409b34df2f058c6fcd1d277beb056e4b12a2b35503dd68c66`  
		Last Modified: Tue, 14 Mar 2023 03:03:21 GMT  
		Size: 66.4 KB (66423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4c2431298bef0123544ba36dfd246ba2d057e90d49e191e82480ab2bc592ee`  
		Last Modified: Tue, 14 Mar 2023 03:03:21 GMT  
		Size: 392.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b2fa6fe2ac44b8bfabe5b77026a2ef5d139f561402bad65836385208867c5b`  
		Last Modified: Thu, 16 Mar 2023 00:12:32 GMT  
		Size: 22.8 MB (22846253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b48693c3908124985259d5d215f74f8438513ece8c9d03a9f3c7015d3cfe821c`  
		Last Modified: Thu, 16 Mar 2023 00:12:29 GMT  
		Size: 2.3 KB (2349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8942fbb163d2f0f30ae8eeab7dda9b32401f72358509c890015350d156bc09e8`  
		Last Modified: Thu, 16 Mar 2023 00:12:28 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
