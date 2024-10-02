## `wordpress:beta-6.7-beta1-php8.1-fpm-alpine`

```console
$ docker pull wordpress@sha256:ea720c1f1553b90530ec58c703103e71ed544d3cb814c68320c7f77b4a725310
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown

### `wordpress:beta-6.7-beta1-php8.1-fpm-alpine` - linux; amd64

```console
$ docker pull wordpress@sha256:149919277d8541b551b02c5fb83b31c1a7b42f453f1cae98973b63a76f21063c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103896014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85326208340421227f468299e016093fbda7d050f761de4427c25296ca23c44`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 00:32:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 07 Sep 2024 00:32:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 07 Sep 2024 00:32:04 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 07 Sep 2024 00:32:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 07 Sep 2024 00:32:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 07 Sep 2024 00:32:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Sep 2024 00:32:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Sep 2024 00:32:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Sep 2024 01:48:44 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 27 Sep 2024 00:28:58 GMT
ENV PHP_VERSION=8.1.30
# Fri, 27 Sep 2024 00:28:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Fri, 27 Sep 2024 00:28:59 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Fri, 27 Sep 2024 00:29:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 27 Sep 2024 00:29:03 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 27 Sep 2024 00:36:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 27 Sep 2024 00:36:59 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 27 Sep 2024 00:37:01 GMT
RUN docker-php-ext-enable sodium
# Fri, 27 Sep 2024 00:37:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Sep 2024 00:37:01 GMT
WORKDIR /var/www/html
# Fri, 27 Sep 2024 00:37:01 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 27 Sep 2024 00:37:02 GMT
STOPSIGNAL SIGQUIT
# Fri, 27 Sep 2024 00:37:02 GMT
EXPOSE 9000
# Fri, 27 Sep 2024 00:37:02 GMT
CMD ["php-fpm"]
# Tue, 01 Oct 2024 07:26:35 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
RUN set -eux; 	version='6.7-beta1'; 	sha1='5425031b02d6917ae8fb357d7453a96c215e6f5a'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
VOLUME [/var/www/html]
# Tue, 01 Oct 2024 07:26:35 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Oct 2024 07:26:35 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb15916673af8229814dcc44164d4616a6141bc5b586ae9362e741d64c6e4c91`  
		Last Modified: Sat, 07 Sep 2024 02:15:12 GMT  
		Size: 3.3 MB (3282678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9feb3258c4c6a46b7e182fa372bfe03ff37fd0fdf7f6894ca97b564fc382d7d4`  
		Last Modified: Sat, 07 Sep 2024 02:15:11 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e436918c34ed4c536bdbaeace5213a8aaeb796ec65951fe681a10758ae2677`  
		Last Modified: Sat, 07 Sep 2024 02:15:11 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3440d557f5fec0a77261c8864955655ea7b3bcea76b60b372a538e2d044e4d85`  
		Last Modified: Fri, 27 Sep 2024 01:10:12 GMT  
		Size: 11.9 MB (11871512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e2c6ac9ac09abf032b6a4db8ab78e5cfc78bcc91fb28c637418533934399fc`  
		Last Modified: Fri, 27 Sep 2024 01:10:12 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416e56822e5a3568ff95be8c0f8dd8bc38e21bf7a70f25f01b8c31df8061c3ab`  
		Last Modified: Fri, 27 Sep 2024 01:10:37 GMT  
		Size: 13.1 MB (13074768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b43c10d4fcfc110c3af91db127e733e147dfacd67ce76497805fe3427840879`  
		Last Modified: Fri, 27 Sep 2024 01:10:35 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2cc61d40baa1193f1e9ada56bb5777723f96b2d474d020a1d83f1f8d2ee7646`  
		Last Modified: Fri, 27 Sep 2024 01:10:35 GMT  
		Size: 19.7 KB (19708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f27434de7095ef1484324762c89e19e8c1fcdba59754fab3c940b227004969`  
		Last Modified: Fri, 27 Sep 2024 01:10:35 GMT  
		Size: 8.9 KB (8880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d28e3390a64031e706b8a008eca6aadfeb4dd9d4d340ae49bc60bcdf4864e08`  
		Last Modified: Tue, 01 Oct 2024 22:24:26 GMT  
		Size: 27.7 MB (27743939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96abc8d270a03a66a8c6324505136d8db75afd633f98de8c20f7b65569fbd069`  
		Last Modified: Tue, 01 Oct 2024 22:24:26 GMT  
		Size: 7.6 MB (7554789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c836e68248dd3ce86a8f487d73f2bbfe4fe3bedbbbb02dde55bab79f6e2e363`  
		Last Modified: Tue, 01 Oct 2024 22:24:26 GMT  
		Size: 60.6 KB (60640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d010998c7d8c5d0934b4b735bbf41fa6769d097abd4ed2c264095e353f95300`  
		Last Modified: Tue, 01 Oct 2024 22:24:26 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d439b711bd740a333b60f2a252f608cc4b392df0d23c3e2387f92b4a19da983`  
		Last Modified: Tue, 01 Oct 2024 22:24:27 GMT  
		Size: 36.6 MB (36646643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3d5892f3a63836b898a415f81fe9fc8ea53e6468a836327605fa0ada9447e5`  
		Last Modified: Tue, 01 Oct 2024 22:24:27 GMT  
		Size: 2.4 KB (2431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d08535abbc47aed44d41af565cab73723dcfa3ac110416ec839b15587be0247`  
		Last Modified: Tue, 01 Oct 2024 22:24:27 GMT  
		Size: 1.7 KB (1723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.7-beta1-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:84bc7e25917a6d395194e9520a66d37303330e1264a0bd7c4c74aafe86de6698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1084776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dba7c0a40297127da49924bd296bd88184fa0375ca8b05fd4c85497e7dd64b6`

```dockerfile
```

-	Layers:
	-	`sha256:d00b8992c292f1a0ecaa857db6b96e44ea4d93e01728dda879291165efa8ab30`  
		Last Modified: Tue, 01 Oct 2024 22:24:26 GMT  
		Size: 1.0 MB (1037779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c0cb4112588f330b05ea0f11fd34b236e931496c41dc7bcab0862b1e349d94e`  
		Last Modified: Tue, 01 Oct 2024 22:24:26 GMT  
		Size: 47.0 KB (46997 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.7-beta1-php8.1-fpm-alpine` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:5cfa3f9a0972d9cf9daeeebcd4f27998e97a852e24847adcf8574e1793fd1a50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97620851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05080a0aa10801c48a1be911d67779c4fda44d63276a8a917c9249e08de0add`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:30:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 23:30:23 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 23:30:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 23:30:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 23:30:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 23:30:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:30:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:30:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Sep 2024 00:29:47 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 26 Sep 2024 22:49:55 GMT
ENV PHP_VERSION=8.1.30
# Thu, 26 Sep 2024 22:49:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Thu, 26 Sep 2024 22:49:55 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Thu, 26 Sep 2024 22:50:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Sep 2024 22:50:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Sep 2024 22:59:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 26 Sep 2024 22:59:18 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 26 Sep 2024 22:59:19 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Sep 2024 22:59:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Sep 2024 22:59:19 GMT
WORKDIR /var/www/html
# Thu, 26 Sep 2024 22:59:20 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 26 Sep 2024 22:59:20 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Sep 2024 22:59:20 GMT
EXPOSE 9000
# Thu, 26 Sep 2024 22:59:20 GMT
CMD ["php-fpm"]
# Tue, 01 Oct 2024 07:26:35 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
RUN set -eux; 	version='6.7-beta1'; 	sha1='5425031b02d6917ae8fb357d7453a96c215e6f5a'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
VOLUME [/var/www/html]
# Tue, 01 Oct 2024 07:26:35 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Oct 2024 07:26:35 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b78c7a9de9941e89cd785fc3ad14f52410d858d2259f5c9b2a852fd144612520`  
		Last Modified: Sat, 07 Sep 2024 00:48:55 GMT  
		Size: 3.3 MB (3269770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddbf8fddbe2a872480c609959838de42e95d1f5d5d3d8daadf7a1e44e5c381a2`  
		Last Modified: Sat, 07 Sep 2024 00:48:54 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfb2d88511b2a3086248129999917d9f1e5928426fda8f08edf40ab5bafa37a9`  
		Last Modified: Sat, 07 Sep 2024 00:48:53 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22a51a5690ee3e375bb21cca8fc4101d68371ce7d3cd60f6fa8ffd9c8416fda`  
		Last Modified: Thu, 26 Sep 2024 23:24:50 GMT  
		Size: 11.9 MB (11871508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c93c13c8521e4b29cf2cfbc0f6d06b9c3a3db95f4206983be97a7ad29d8c873`  
		Last Modified: Thu, 26 Sep 2024 23:24:48 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c293bd87a76ce97c9aa714990b394d3406120a5a91a3686cf8fe07af83a4cd`  
		Last Modified: Thu, 26 Sep 2024 23:25:16 GMT  
		Size: 11.9 MB (11900339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b09ec827d1ea03e674150cbfb81ae461451ce5c7d8a3ecad94dce4cec549bfc`  
		Last Modified: Thu, 26 Sep 2024 23:25:13 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dac47452c89ea0c58cc37ace0896d4deb5d20d0f6986051dcf127dc70bdf6ce`  
		Last Modified: Thu, 26 Sep 2024 23:25:13 GMT  
		Size: 19.5 KB (19496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8a6b6b8dfb1066e610afd2f284b05367306419676098cea350a0976789d7fa`  
		Last Modified: Thu, 26 Sep 2024 23:25:13 GMT  
		Size: 8.9 KB (8881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cead70154006198960f5227b7d0ff5c357a0cdbc667e9dd29ee24df06a657312`  
		Last Modified: Fri, 27 Sep 2024 00:55:43 GMT  
		Size: 24.0 MB (23953281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a732c34fb7035756a1529fc2c4be4c8f94e712149f5be06a7146409806758084`  
		Last Modified: Fri, 27 Sep 2024 00:55:43 GMT  
		Size: 6.5 MB (6515180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b83b044a1f2af0516361a7dd92ad5c4c7e3f033f8e1a7727e4bfc7f1f8088df`  
		Last Modified: Fri, 27 Sep 2024 00:55:42 GMT  
		Size: 60.6 KB (60604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258a41644bf73e03fd9c55cfa8996c985eb37dd6678ddaa118eb289762dcb944`  
		Last Modified: Fri, 27 Sep 2024 00:55:42 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7dd04be69bfd617e7da061f0d7a13a72c47e484866bd852725ce45a53691c3`  
		Last Modified: Tue, 01 Oct 2024 23:44:56 GMT  
		Size: 36.6 MB (36646621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00ba37aded4e2637b8875fe841d7f921b77042ceebbccc19120461fd80c3856`  
		Last Modified: Tue, 01 Oct 2024 23:44:55 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5d8f59db78e9eeb58c014bcbb9fb7ada74bf8e1cb721055ba7693b605bb886`  
		Last Modified: Tue, 01 Oct 2024 23:44:55 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.7-beta1-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:507a0019001a60151a18f235739d626ba68b4273b9ceaf9cb9473a44462e2156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 KB (46900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eb452471055358184da508710245c4e474539bae241f50eab5d54112d1b5585`

```dockerfile
```

-	Layers:
	-	`sha256:1617086c72cfa9939645420caf941a97bd7c6d870a936823edab2f78a08b9e20`  
		Last Modified: Tue, 01 Oct 2024 23:44:54 GMT  
		Size: 46.9 KB (46900 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.7-beta1-php8.1-fpm-alpine` - linux; 386

```console
$ docker pull wordpress@sha256:2d154484dc4ef4fe2d64b83cdce02ae123ebe71b0ef249d06ded78bd4c928bf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.3 MB (103297715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89799d2cd3340cd7125b17e51d5e46c63647751cc7304c3371fc10f7ae6598aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 22:57:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 22:57:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 22:57:52 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 22:57:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 22:57:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 22:57:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 22:57:53 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 22:57:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Sep 2024 01:06:44 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 27 Sep 2024 02:36:15 GMT
ENV PHP_VERSION=8.1.30
# Fri, 27 Sep 2024 02:36:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Fri, 27 Sep 2024 02:36:16 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Fri, 27 Sep 2024 02:36:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 27 Sep 2024 02:36:21 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 27 Sep 2024 02:49:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 27 Sep 2024 02:49:38 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 27 Sep 2024 02:49:39 GMT
RUN docker-php-ext-enable sodium
# Fri, 27 Sep 2024 02:49:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Sep 2024 02:49:39 GMT
WORKDIR /var/www/html
# Fri, 27 Sep 2024 02:49:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 27 Sep 2024 02:49:40 GMT
STOPSIGNAL SIGQUIT
# Fri, 27 Sep 2024 02:49:40 GMT
EXPOSE 9000
# Fri, 27 Sep 2024 02:49:40 GMT
CMD ["php-fpm"]
# Tue, 01 Oct 2024 07:26:35 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
RUN set -eux; 	version='6.7-beta1'; 	sha1='5425031b02d6917ae8fb357d7453a96c215e6f5a'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
VOLUME [/var/www/html]
# Tue, 01 Oct 2024 07:26:35 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Oct 2024 07:26:35 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17866811de1cdb9710f37a522dde62051d068230716118d22b6b987216e037ef`  
		Last Modified: Sat, 07 Sep 2024 01:49:46 GMT  
		Size: 3.3 MB (3331976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9513ca5d3e6e64e8e064f1b178ad39b5d375a65559181a7f4964c9471461ba8f`  
		Last Modified: Sat, 07 Sep 2024 01:49:45 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90338393c7a779c5576927d742c98b6841aa39aa84fe1b137708bd8f4d0ae68e`  
		Last Modified: Sat, 07 Sep 2024 01:49:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072e5477e6d13185d9b6fb1339c895f323e29020712e94b0fbb7033e517f074e`  
		Last Modified: Fri, 27 Sep 2024 03:35:38 GMT  
		Size: 11.9 MB (11871513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06a471f7a5249ee123426ff294236d114e8ab0afe7ebe9e884a865480abca39`  
		Last Modified: Fri, 27 Sep 2024 03:35:37 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1832698cba2ec90202cfd91fb426539e7ba999f938c199fb584af50781b5fd0`  
		Last Modified: Fri, 27 Sep 2024 03:36:05 GMT  
		Size: 13.4 MB (13426953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30f476edcedec53cf5ccda08c5bae84b134d150feb2d3731a34a3b1ba934727`  
		Last Modified: Fri, 27 Sep 2024 03:36:02 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4f9ddd99b01616105682bcde2c3d9e309e98662def1467b9375c642df60c6c`  
		Last Modified: Fri, 27 Sep 2024 03:36:02 GMT  
		Size: 19.7 KB (19705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d59a2c117adda864853c1c0329842d394a352a259d17334f6849aa361707b6c`  
		Last Modified: Fri, 27 Sep 2024 03:36:02 GMT  
		Size: 8.9 KB (8879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394939d3bd219f95335a50d083b997cc7598434375b1fffd6ac204e25cda4419`  
		Last Modified: Tue, 01 Oct 2024 22:20:35 GMT  
		Size: 28.0 MB (28002394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23ca83a9c2740c59092f3f13e2372db2483fdec53a64e34ae5e0d96084f8322`  
		Last Modified: Tue, 01 Oct 2024 22:20:34 GMT  
		Size: 6.5 MB (6451203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bacc1f3fec68895743c235452ec1afb9c54881cf0c1810c1246d17da66347071`  
		Last Modified: Tue, 01 Oct 2024 22:20:34 GMT  
		Size: 60.6 KB (60621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae7ecc6a7f7f700f36488ad20677efb642d4107d8904057cf2f18408555dc9e4`  
		Last Modified: Tue, 01 Oct 2024 22:20:34 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6500b46e5173d99f6e49680a7565577a9d0f54c2cbe51f40100466fb8a054cd9`  
		Last Modified: Tue, 01 Oct 2024 22:20:36 GMT  
		Size: 36.6 MB (36646642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a078ba7202f16fcb9d65d126c4fa785dc42c8d8822cbbe338d23274b5c8ff99`  
		Last Modified: Tue, 01 Oct 2024 22:20:35 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a21fe72655b98152655d78fe4ee80c585afb0145eff8c4d84250c149219968`  
		Last Modified: Tue, 01 Oct 2024 22:20:35 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.7-beta1-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:706aeded6176045dd41c31ec6389f52d227f9cc3954105d41761a51fc392e8a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1084714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eb3b96fce2aadac748ba8179d48697d6379027281dab17f7d93d0a78d94dc94`

```dockerfile
```

-	Layers:
	-	`sha256:b9b48747cd88cec4b441e32bfdbe378705c6019d9afea534507f0a37586610a1`  
		Last Modified: Tue, 01 Oct 2024 22:20:34 GMT  
		Size: 1.0 MB (1037754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be8fa00e57990923b5a717a501e7506d4a6516a387729dcbc2432d75836e473f`  
		Last Modified: Tue, 01 Oct 2024 22:20:34 GMT  
		Size: 47.0 KB (46960 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.7-beta1-php8.1-fpm-alpine` - linux; riscv64

```console
$ docker pull wordpress@sha256:0f52c310310608aebb1bc60ea34afe75fe216b260c7149fff8610a9ff55b5fcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.6 MB (101606559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a43ae3324563ac82b043085d59b9fdd6fa4910df7d40c5163ee2f19f390d6b76`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:03 GMT
ADD file:1f189f0db01ff094ebe1569a5caf278db6965725f4182176ff85dafa711ad524 in / 
# Fri, 06 Sep 2024 22:26:04 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:47:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 23:48:04 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 23:48:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 23:48:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 23:48:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 23:48:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:48:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:48:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Sep 2024 06:54:54 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 27 Sep 2024 05:05:40 GMT
ENV PHP_VERSION=8.1.30
# Fri, 27 Sep 2024 05:05:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.30.tar.xz.asc
# Fri, 27 Sep 2024 05:05:41 GMT
ENV PHP_SHA256=f24a6007f0b25a53cb7fbaee69c85017e0345b62089c2425a0afb7e177192ed1
# Fri, 27 Sep 2024 05:05:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 27 Sep 2024 05:06:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 27 Sep 2024 06:35:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 27 Sep 2024 06:35:19 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 27 Sep 2024 06:35:26 GMT
RUN docker-php-ext-enable sodium
# Fri, 27 Sep 2024 06:35:27 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Sep 2024 06:35:27 GMT
WORKDIR /var/www/html
# Fri, 27 Sep 2024 06:35:29 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 27 Sep 2024 06:35:30 GMT
STOPSIGNAL SIGQUIT
# Fri, 27 Sep 2024 06:35:31 GMT
EXPOSE 9000
# Fri, 27 Sep 2024 06:35:31 GMT
CMD ["php-fpm"]
# Tue, 01 Oct 2024 07:26:35 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
RUN set -eux; 	version='6.7-beta1'; 	sha1='5425031b02d6917ae8fb357d7453a96c215e6f5a'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
VOLUME [/var/www/html]
# Tue, 01 Oct 2024 07:26:35 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Oct 2024 07:26:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Oct 2024 07:26:35 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8c4a05189a5fd2cf629c25ab8d0831be7156d74b336f129a412933ee78af018c`  
		Last Modified: Fri, 06 Sep 2024 22:26:21 GMT  
		Size: 3.4 MB (3371452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160a71fe2c21fa0be03f4ecb3856d46307a8cab34f0749e89c452111c128a28e`  
		Last Modified: Sat, 07 Sep 2024 09:00:45 GMT  
		Size: 3.4 MB (3405216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99de0cdf41fffa764363801fb8a9efbd008b3689317846613f74f55be82ad4ec`  
		Last Modified: Sat, 07 Sep 2024 09:00:41 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f4878284381f1e57d12b980a3d3f2476a10fab26827866948f61cc0a2214a8`  
		Last Modified: Sat, 07 Sep 2024 09:00:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2490885a5a3bef4a4213b349665a3bf844ba1874f27c41c044f685f3d1ac7c96`  
		Last Modified: Fri, 27 Sep 2024 07:28:45 GMT  
		Size: 11.9 MB (11871511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a7f034d94f474e2e6c4359d2793ae8b4c2262d850b6c64fed27581f65061cd`  
		Last Modified: Fri, 27 Sep 2024 07:28:40 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bbed27e701b2a46aee7d8cb9f1d63ad418f1b90a47d0d74774dc7d0b1927111`  
		Last Modified: Fri, 27 Sep 2024 07:29:32 GMT  
		Size: 12.4 MB (12406512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d579c474c45db77db32763ef0c62e4b056a2325bd3b14f4b9c69b8e4b6ba6bbb`  
		Last Modified: Fri, 27 Sep 2024 07:29:22 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e36a3c5462144f54f38a277a99382e658c5bf87825fc1a16bfe01d6b2ac724eb`  
		Last Modified: Fri, 27 Sep 2024 07:29:22 GMT  
		Size: 19.5 KB (19502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba6bc847fedf782dfc85f50e5a16eebc3666da4dd1727f48d1650eb0b7e98ef`  
		Last Modified: Fri, 27 Sep 2024 07:29:22 GMT  
		Size: 8.9 KB (8878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154698bacab8f369193a7371ead3b8384a3b3ae6a63a73f22621f4609388bfa0`  
		Last Modified: Fri, 27 Sep 2024 16:01:30 GMT  
		Size: 27.8 MB (27788258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2422ef96a7179740bbe1a60471c7b1184d3c5d28ba9b277b971c7317eddfc52e`  
		Last Modified: Fri, 27 Sep 2024 16:01:27 GMT  
		Size: 6.0 MB (6019300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f3debc86a901a5763e4afbc55d15b4bd44bff97cc24077b9a90ce00b55654d`  
		Last Modified: Fri, 27 Sep 2024 16:01:26 GMT  
		Size: 60.6 KB (60650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d79aefe55f823148c8a87cda59f3899b51300879f71b92bd12764456e31ba82`  
		Last Modified: Fri, 27 Sep 2024 16:01:26 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49b655ac37a541a43f34af5b731a3b60b83216c93261995a5d40fcc44c4e234`  
		Last Modified: Tue, 01 Oct 2024 22:48:55 GMT  
		Size: 36.6 MB (36646611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dc5c3d35b805f0f9cdc0e423cc2c9374a3cb82baabfac20125f294b7d0d814d`  
		Last Modified: Tue, 01 Oct 2024 22:48:50 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0679e7ac393f84b0fce067045511ef78eb434c452f2db608f6e18a88f0ea4fa`  
		Last Modified: Tue, 01 Oct 2024 22:48:50 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.7-beta1-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:5846d238fd10494b6b74023e9873db8058ecb55e8d66f89706942901d3d2c523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1082898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b535c0ff5f56284e5e3e5df28b051b9bb6138861ba6881ed6902c5e9da031c61`

```dockerfile
```

-	Layers:
	-	`sha256:15ffa5c065d351f03ee813c423543a44b3452ad935737734b46f0f9e970ab000`  
		Last Modified: Tue, 01 Oct 2024 22:48:50 GMT  
		Size: 1.0 MB (1035855 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:395401a0c2dcb29da82eb2384e2790018f587fe1cbcd842671fc8fd59264bc03`  
		Last Modified: Tue, 01 Oct 2024 22:48:49 GMT  
		Size: 47.0 KB (47043 bytes)  
		MIME: application/vnd.in-toto+json
