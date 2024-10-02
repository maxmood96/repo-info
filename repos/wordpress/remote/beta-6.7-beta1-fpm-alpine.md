## `wordpress:beta-6.7-beta1-fpm-alpine`

```console
$ docker pull wordpress@sha256:cb0a5d0d3f13d3ea79589cac1beb69f7cde785f8ecf94aa192a7ff56c701e54b
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

### `wordpress:beta-6.7-beta1-fpm-alpine` - linux; amd64

```console
$ docker pull wordpress@sha256:0ef023c0d4d571436ed9963fd77281b28954d6f51cc6aa522e0da5f3d1dc8247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.5 MB (104452068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a854478a65ddeb36769a5d67c30a3b7b0acdc6fdf8a5ad9b28390451e86583`
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
# Sat, 07 Sep 2024 01:23:30 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 26 Sep 2024 23:34:37 GMT
ENV PHP_VERSION=8.2.24
# Thu, 26 Sep 2024 23:34:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.24.tar.xz.asc
# Thu, 26 Sep 2024 23:34:38 GMT
ENV PHP_SHA256=80a5225746a9eb484475b312d4c626c63a88a037d8e56d214f30205e1ba1411a
# Thu, 26 Sep 2024 23:34:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Sep 2024 23:34:44 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Sep 2024 23:43:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 26 Sep 2024 23:43:13 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 26 Sep 2024 23:43:14 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Sep 2024 23:43:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Sep 2024 23:43:14 GMT
WORKDIR /var/www/html
# Thu, 26 Sep 2024 23:43:15 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 26 Sep 2024 23:43:15 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Sep 2024 23:43:15 GMT
EXPOSE 9000
# Thu, 26 Sep 2024 23:43:15 GMT
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
	-	`sha256:14b6974b37323387584ee3677fc2200fb09e101404c8487e78f90844edcf3950`  
		Last Modified: Fri, 27 Sep 2024 01:06:41 GMT  
		Size: 12.1 MB (12131299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20aee302f78733f29a1aab06e21f568de268649dce468803fe3893f86778817`  
		Last Modified: Fri, 27 Sep 2024 01:06:40 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9138929e2943f3244dc2833bcabbd35cefa32186bd2c120c7149f716b3796cd`  
		Last Modified: Fri, 27 Sep 2024 01:07:04 GMT  
		Size: 13.3 MB (13335864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8c16e8aa640b3d649b29a25fd79fb978f7ee4c3f5d730e57fea207daa2f5d8e`  
		Last Modified: Fri, 27 Sep 2024 01:07:02 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428c6165a2655930c22d5d69643c6c6698b48b70fdb07145feff35dff2d246fc`  
		Last Modified: Fri, 27 Sep 2024 01:07:02 GMT  
		Size: 19.7 KB (19707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41e53bcf0d0aedaf210a6db1bacb20e0e6e874fca729a1ea7db5315d5e420a4`  
		Last Modified: Fri, 27 Sep 2024 01:07:02 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1fd83824b3f8597ecdca9bc51d17d66dbe5991972a6cb2de98553dd5b99c4c3`  
		Last Modified: Tue, 01 Oct 2024 22:20:38 GMT  
		Size: 27.7 MB (27743974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:694b098dc381fa4b520762fa95f517f5c473ffe95ab3f4e9f81618db3d7e50db`  
		Last Modified: Tue, 01 Oct 2024 22:20:37 GMT  
		Size: 7.6 MB (7589572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e50bd20ed8ddbe8a74f60d2abe35b6ca732962947ba1952cf385381cf6b7407d`  
		Last Modified: Tue, 01 Oct 2024 22:20:37 GMT  
		Size: 60.7 KB (60652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12674b0a3d7ade0c359d941451a119046c082cd7cd20020382e313235c678518`  
		Last Modified: Tue, 01 Oct 2024 22:20:37 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1218974ae61a1eeb9154cb569220940cbefe4acc83f35102ad9e1bb9bc3963`  
		Last Modified: Tue, 01 Oct 2024 22:20:39 GMT  
		Size: 36.6 MB (36646675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09f4b41773469c4034a8ce33b50b2224421fc02dd932e2aa9f0c564ccaff08fd`  
		Last Modified: Tue, 01 Oct 2024 22:20:38 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f2d3a3a809e31888c6f136d76206b422338e84feba782a8198f587c52e1bc05`  
		Last Modified: Tue, 01 Oct 2024 22:20:38 GMT  
		Size: 1.7 KB (1727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.7-beta1-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:aa03fa269d0209ef914207244330bf2e753f6568921b319c72adf01db4d84d04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1087416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:707b869bb11f14aad50eb2ce70f0de2706b0868644359430ace37bdb8205c32f`

```dockerfile
```

-	Layers:
	-	`sha256:a590abfe38d5eafa2ec08121564810259fde55feb5bf2c67c61609e64ab254cf`  
		Last Modified: Tue, 01 Oct 2024 22:20:37 GMT  
		Size: 1.0 MB (1039099 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8be8a28ccdc0c5c8c1c631884a5403955e4fbfd8c63092c385282e4235f7d57b`  
		Last Modified: Tue, 01 Oct 2024 22:20:37 GMT  
		Size: 48.3 KB (48317 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.7-beta1-fpm-alpine` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:a5fce7e22dfb1dba6194cf0a7f4e29aad2882fc5af1aae383e8b55c334fd17b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.2 MB (98218237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062dc383ce59c9687e25b821b0cccc8d0c9c542834ca6fa76f47678f68464f94`
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
# Sat, 07 Sep 2024 00:10:58 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 26 Sep 2024 22:21:35 GMT
ENV PHP_VERSION=8.2.24
# Thu, 26 Sep 2024 22:21:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.24.tar.xz.asc
# Thu, 26 Sep 2024 22:21:35 GMT
ENV PHP_SHA256=80a5225746a9eb484475b312d4c626c63a88a037d8e56d214f30205e1ba1411a
# Thu, 26 Sep 2024 22:21:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Sep 2024 22:21:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Sep 2024 22:30:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 26 Sep 2024 22:30:34 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 26 Sep 2024 22:30:35 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Sep 2024 22:30:36 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Sep 2024 22:30:36 GMT
WORKDIR /var/www/html
# Thu, 26 Sep 2024 22:30:37 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 26 Sep 2024 22:30:37 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Sep 2024 22:30:38 GMT
EXPOSE 9000
# Thu, 26 Sep 2024 22:30:38 GMT
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
	-	`sha256:1626f58189cedc9e9de32f1ecfc64ce30005dc5ba226f4c3195f2610b885b3b5`  
		Last Modified: Thu, 26 Sep 2024 23:23:13 GMT  
		Size: 12.1 MB (12131291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2597795e00baa246783e513d801b1c15969d19a3dcb4e6fb83917ba185d45b45`  
		Last Modified: Thu, 26 Sep 2024 23:23:11 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c6731c3567a6020937fd93edbbb9d8d29a9c95514dc3dceede8c666e4db85b5`  
		Last Modified: Thu, 26 Sep 2024 23:23:39 GMT  
		Size: 12.2 MB (12181394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d0d2bfd8b4368d65477c552dba866c7407bddb2e7f477c18a2e267dc0660c2f`  
		Last Modified: Thu, 26 Sep 2024 23:23:36 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f56942133deaba5985ea20304e45c57fb1a65588c1c04c9fc9be3190403a4b`  
		Last Modified: Thu, 26 Sep 2024 23:23:36 GMT  
		Size: 19.5 KB (19495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928d51222fd81cf9d22d2b71ad575921e4d1f84fc734cc2a8552773a3395e766`  
		Last Modified: Thu, 26 Sep 2024 23:23:36 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4299f3f36b8514bdbd04be5cfc17f70f08466da889a8911a5fc257dd509212c8`  
		Last Modified: Fri, 27 Sep 2024 00:57:53 GMT  
		Size: 24.0 MB (23953272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffae62eee71d2a698a5a96bd744b9bcf379cdf65ce5a6f0347f48c0db5f80ee6`  
		Last Modified: Fri, 27 Sep 2024 00:57:53 GMT  
		Size: 6.6 MB (6571420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb32cd71836b27264919b8696464dc3bc82c512f625aa276cd32d06e91a614e3`  
		Last Modified: Fri, 27 Sep 2024 00:57:52 GMT  
		Size: 60.6 KB (60612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb0dd69c1ed3087f89d2bfcf8158a42ad042fdd18669a7a0479efca625d8f88`  
		Last Modified: Fri, 27 Sep 2024 00:57:52 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075f8a46a9f1fff0b3dd64a0cde3838a318f9e63a8ee719c1bea81f5751b5442`  
		Last Modified: Tue, 01 Oct 2024 23:45:22 GMT  
		Size: 36.6 MB (36646618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ecba082c539d38e4a17c6d456c8acbdaac204be36798f42545d72f2fe88af5`  
		Last Modified: Tue, 01 Oct 2024 23:45:21 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ef73424292d0aceb1175aa9a10e37a78cea0d8fb9830279033309bc9b401de`  
		Last Modified: Tue, 01 Oct 2024 23:45:21 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.7-beta1-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:c3b84da4ecabf6e4d906f6e1d4843783fa578312afc36cba26558218bf2f9dd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 KB (48252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da13f2290376e07aa0edb75761b50b8ad61c4a6fbbed76848492dfe0322a9053`

```dockerfile
```

-	Layers:
	-	`sha256:06ac0d5b8eaa65146fdf19121b8f18af761361c04180eceea689ea0bc4187c53`  
		Last Modified: Tue, 01 Oct 2024 23:45:20 GMT  
		Size: 48.3 KB (48252 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.7-beta1-fpm-alpine` - linux; 386

```console
$ docker pull wordpress@sha256:c185784fd32b5a0764e2663ef3025c34267d063739a3292e787f68e517a3ce89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103868164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57db13e7fceee831864891eb465d2871b878c242fe880f644ebe959425985c13`
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
# Sat, 07 Sep 2024 00:24:55 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 27 Sep 2024 01:08:34 GMT
ENV PHP_VERSION=8.2.24
# Fri, 27 Sep 2024 01:08:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.24.tar.xz.asc
# Fri, 27 Sep 2024 01:08:34 GMT
ENV PHP_SHA256=80a5225746a9eb484475b312d4c626c63a88a037d8e56d214f30205e1ba1411a
# Fri, 27 Sep 2024 01:08:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 27 Sep 2024 01:08:39 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 27 Sep 2024 01:22:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 27 Sep 2024 01:22:02 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 27 Sep 2024 01:22:04 GMT
RUN docker-php-ext-enable sodium
# Fri, 27 Sep 2024 01:22:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Sep 2024 01:22:04 GMT
WORKDIR /var/www/html
# Fri, 27 Sep 2024 01:22:04 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 27 Sep 2024 01:22:05 GMT
STOPSIGNAL SIGQUIT
# Fri, 27 Sep 2024 01:22:05 GMT
EXPOSE 9000
# Fri, 27 Sep 2024 01:22:05 GMT
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
	-	`sha256:a95bbce46d856900c2d09cc8e6936792aa2c16a0168152eec91c75cda5546b5e`  
		Last Modified: Fri, 27 Sep 2024 03:31:40 GMT  
		Size: 12.1 MB (12131291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3864122d099e9cb75bc64aead88b2e2d5afbf9a8c073d0fb24ecf32d8c08e410`  
		Last Modified: Fri, 27 Sep 2024 03:31:38 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7da61f4d3b4a6947f992ff1f0d90185183849e3282b30cee8af6952abbb7a1`  
		Last Modified: Fri, 27 Sep 2024 03:32:06 GMT  
		Size: 13.7 MB (13704148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ac95cef2fe8eacc55f50353da0820404b4823ea27a9f35be8de937688a3b25`  
		Last Modified: Fri, 27 Sep 2024 03:32:03 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:086d4bdfffdbe33c51f5380ca6049ea34d552cacc542123f8e202ac7f12f7c80`  
		Last Modified: Fri, 27 Sep 2024 03:32:03 GMT  
		Size: 19.7 KB (19700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:124e14b8183cae7591f1457a38c5f3ac6b5f9b6e9134c86a2f27990068ad3856`  
		Last Modified: Fri, 27 Sep 2024 03:32:03 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754c386d28f9c226be37cdc73f569a7ca52561a00aa5aa951b857d8cacabd715`  
		Last Modified: Tue, 01 Oct 2024 22:20:49 GMT  
		Size: 28.0 MB (28002362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f835731f02f774abbe4dbc6c10d1baa4d7a526e1759372409088acf8576277`  
		Last Modified: Tue, 01 Oct 2024 22:20:48 GMT  
		Size: 6.5 MB (6484412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec2e97e9b0ed6435a0f34dfdd8c8842ce766c127ce00973fd12e7ddeaf0129f6`  
		Last Modified: Tue, 01 Oct 2024 22:20:48 GMT  
		Size: 60.6 KB (60624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0120a788aae4dc37afd051731e586a028594254acfff2243583d47133d77b285`  
		Last Modified: Tue, 01 Oct 2024 22:20:48 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeaf0ec53e8856c2a4dcbbd83d5242adfa2dde985fd4b54c82a8097610d2be8c`  
		Last Modified: Tue, 01 Oct 2024 22:20:50 GMT  
		Size: 36.6 MB (36646654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c6242f76e63dc0edeb29fa5e40af4326336a7067799beb2fef6b38610b9dde`  
		Last Modified: Tue, 01 Oct 2024 22:20:49 GMT  
		Size: 2.4 KB (2429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4276d7a11c0de8680907fb057b49f883be6412b9fb745701e29765a8fec2e114`  
		Last Modified: Tue, 01 Oct 2024 22:20:49 GMT  
		Size: 1.7 KB (1724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.7-beta1-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:59d0419bdd1cba33fcc724ddd366fdffaf103f9ede65acb9314a9c1d3a454320
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1087314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec778e9e5c8ee82b5d8f4eac428260872d9ea246daad808957776b46ffe824e3`

```dockerfile
```

-	Layers:
	-	`sha256:69328567df9f49c323c41289c666b5d74bee4b468105ec30eef6b53977ea66c3`  
		Last Modified: Tue, 01 Oct 2024 22:20:48 GMT  
		Size: 1.0 MB (1039054 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af6d36b04ba6efbb7fae36d92f689af64e0079d5659856e615658f1eb875ff48`  
		Last Modified: Tue, 01 Oct 2024 22:20:48 GMT  
		Size: 48.3 KB (48260 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.7-beta1-fpm-alpine` - linux; riscv64

```console
$ docker pull wordpress@sha256:026814bec938b74e6fda3a624af19c859a4d86d670c85f7398e0e5207c25929b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.2 MB (102198764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2176c2e9da34cf9b393b70baa7e16965479510341967f4c1c28051ed97a8348d`
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
# Sat, 07 Sep 2024 04:48:01 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 27 Sep 2024 02:44:52 GMT
ENV PHP_VERSION=8.2.24
# Fri, 27 Sep 2024 02:44:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.24.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.24.tar.xz.asc
# Fri, 27 Sep 2024 02:44:53 GMT
ENV PHP_SHA256=80a5225746a9eb484475b312d4c626c63a88a037d8e56d214f30205e1ba1411a
# Fri, 27 Sep 2024 02:45:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 27 Sep 2024 02:45:26 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 27 Sep 2024 04:18:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 27 Sep 2024 04:18:39 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 27 Sep 2024 04:18:47 GMT
RUN docker-php-ext-enable sodium
# Fri, 27 Sep 2024 04:18:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 27 Sep 2024 04:18:48 GMT
WORKDIR /var/www/html
# Fri, 27 Sep 2024 04:18:50 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 27 Sep 2024 04:18:51 GMT
STOPSIGNAL SIGQUIT
# Fri, 27 Sep 2024 04:18:51 GMT
EXPOSE 9000
# Fri, 27 Sep 2024 04:18:52 GMT
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
	-	`sha256:dddeec9876ec898927bc3afdb800ee78fef13e9e2b6cc82c4305fbafc9417cdf`  
		Last Modified: Fri, 27 Sep 2024 07:27:03 GMT  
		Size: 12.1 MB (12131300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b8c5dfda73c315519017670d748c1b87f5e2c02a4c243e9981225a6c78d80cd`  
		Last Modified: Fri, 27 Sep 2024 07:26:57 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deea25e51a274843175a36c2cc2c00256c840fd17b1d82f8a54fd70f989e45a9`  
		Last Modified: Fri, 27 Sep 2024 07:27:51 GMT  
		Size: 12.7 MB (12703558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bfaa03a30655a8149c1142c3c6b7bce5d104b340fc98c1592edb20b149d8f2`  
		Last Modified: Fri, 27 Sep 2024 07:27:40 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6a3ed3379bcd4edca48edc947ab395ddbf2bafb6e95df16f421790f1c12d73`  
		Last Modified: Fri, 27 Sep 2024 07:27:40 GMT  
		Size: 19.5 KB (19503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c49a62fc31791ca5d0df6e5bca80f3d1eeff981f8b0f04c66d6457fd523094d`  
		Last Modified: Fri, 27 Sep 2024 07:27:40 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc517761452701136dc8dbfb9229c29116cda969da7b6a4789bb5432e5e633e5`  
		Last Modified: Fri, 27 Sep 2024 16:17:28 GMT  
		Size: 27.8 MB (27788314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a39311daf62b5364a06abcfbb3af7ad21ada3e8c377698ffabadf9979ad393bd`  
		Last Modified: Fri, 27 Sep 2024 16:17:25 GMT  
		Size: 6.1 MB (6054299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df7a951d09ebd72371def7899fe156ab5bff77ab401f96cde24c2e2f4026c53`  
		Last Modified: Fri, 27 Sep 2024 16:17:24 GMT  
		Size: 60.7 KB (60653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac63c09c8b90dce4c009c3f9787a7cc7f6afcdec2e9a89537519c8178116002`  
		Last Modified: Fri, 27 Sep 2024 16:17:24 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e47822aa78e53f2352462b68be61628cbf07077e560dcafdc8a074b9d65c0b6`  
		Last Modified: Tue, 01 Oct 2024 22:51:26 GMT  
		Size: 36.6 MB (36646611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:128c82b1a0f3d189fa62a5532450c258c4c25b021d3ff97871a96a50579d1373`  
		Last Modified: Tue, 01 Oct 2024 22:51:21 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee64820be446aec24077ebc5ecfddc81208315bd3ca9a9746766d25aec3673db`  
		Last Modified: Tue, 01 Oct 2024 22:51:21 GMT  
		Size: 1.7 KB (1731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.7-beta1-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:120e5ec7d6c5f9d20580541a925c6060620298cb8d0d6e72bbe43471d802754d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1085586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d54955f29cc792e00a01f5da6cf08d1e0480e9dc37e82645a2c9a34945750e`

```dockerfile
```

-	Layers:
	-	`sha256:7cabd6dbe0d6c5c15e4b51fcb25d1c37d85afbc68c7d729619031726c85d14c3`  
		Last Modified: Tue, 01 Oct 2024 22:51:21 GMT  
		Size: 1.0 MB (1037199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:108b3c479cfb816485b1314a9952b6dc36b62dcd9d3ae21395a7c97a9537169e`  
		Last Modified: Tue, 01 Oct 2024 22:51:21 GMT  
		Size: 48.4 KB (48387 bytes)  
		MIME: application/vnd.in-toto+json
