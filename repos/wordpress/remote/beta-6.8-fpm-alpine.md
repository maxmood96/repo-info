## `wordpress:beta-6.8-fpm-alpine`

```console
$ docker pull wordpress@sha256:2a37f6d65f6a457c8a3e5d9afe13d07b3f3eccb5e19308a3607bbac6dbdf22ae
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

### `wordpress:beta-6.8-fpm-alpine` - linux; amd64

```console
$ docker pull wordpress@sha256:d63557b7722f9fc0c9cc204d9e3fe64d267bd228e5a277dd38f0855d1e64ebc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.5 MB (99461705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b82a4e10eda68a1df8b45ebee6341f69d0f6b425874e5c56e42440a4c975186`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 03 Jul 2025 12:46:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Jul 2025 12:46:24 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_VERSION=8.2.29
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Jul 2025 12:46:24 GMT
WORKDIR /var/www/html
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 03 Jul 2025 12:46:24 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 03 Jul 2025 12:46:24 GMT
CMD ["php-fpm"]
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	version='6.8.2-RC1'; 	sha1='62102972957c99a42274e719fc537960f4ed346a'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
VOLUME [/var/www/html]
# Tue, 08 Jul 2025 19:03:14 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Jul 2025 19:03:14 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1444feebcb001cc3453cf82ff8d9e42f085f514c697981bac875105fc84c31d`  
		Last Modified: Thu, 03 Jul 2025 23:10:05 GMT  
		Size: 5.9 MB (5944372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d39aea9fc169357634f20e88ddc270c24b21ddfcad15f3cebc21313968df4b`  
		Last Modified: Thu, 03 Jul 2025 23:10:04 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fb2ef086286738dfeaea5f0e1248d9bfe60b196566a1b751525c937d7138d6`  
		Last Modified: Thu, 03 Jul 2025 23:10:04 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b8d56306b2dad5d51a253b353d7ea80289208d15d4ffc3946cbfef875cff9a`  
		Last Modified: Thu, 03 Jul 2025 23:10:06 GMT  
		Size: 12.2 MB (12183860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a0a78ac0c7e2c313c633279708d3db4243151f72eb35bac0ad2273ef1fd82b`  
		Last Modified: Thu, 03 Jul 2025 23:10:05 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d4aebcd8ed6c397ec2db83f17841ba9da698fb9531f6cfc153c0cd2f265052a`  
		Last Modified: Thu, 03 Jul 2025 23:10:08 GMT  
		Size: 13.0 MB (13024636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4903d38749a46f6eea0eeb8d2b120170084ff38075b533dbc981870def7491f3`  
		Last Modified: Thu, 03 Jul 2025 23:10:05 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc50016fddc15ce0a40a8a11855a1e739c64f3493b47328792c608989765341`  
		Last Modified: Thu, 03 Jul 2025 23:10:05 GMT  
		Size: 20.2 KB (20209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58846a3abfe3533ed5fd33a1f2e3ce3a8bc1c5d3d1b04e9c58410f57f869cbf9`  
		Last Modified: Thu, 03 Jul 2025 23:10:05 GMT  
		Size: 20.2 KB (20204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0a5d652965a38b554e9ef4616d2d8f6f5b0c87c1059185c3ae478f97a3b525d`  
		Last Modified: Thu, 03 Jul 2025 23:10:05 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa9c981ede344164afbeee762e53189ecf18b969091476fa6bbf564778c1105`  
		Last Modified: Wed, 09 Jul 2025 15:27:44 GMT  
		Size: 28.3 MB (28272556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41b0f353752dd943492da2296e3f6cbb775d7daa837ee69e13b85d0ed9e6ff0`  
		Last Modified: Wed, 09 Jul 2025 15:27:34 GMT  
		Size: 9.2 MB (9219293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fda9147f058e4f54f4ad7f294163c2ad18c278886216523c32caab70589a1ae4`  
		Last Modified: Wed, 09 Jul 2025 15:27:30 GMT  
		Size: 62.6 KB (62571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da9bc1e852ab0a7db06b5c046d523393f384b37f49dd7ef5d052e11cbe206fa`  
		Last Modified: Wed, 09 Jul 2025 15:27:30 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9034f8f1dd06421a96dd8f1a0342156c38dd64c3d32384cb50f1ae3c417136`  
		Last Modified: Wed, 09 Jul 2025 15:27:36 GMT  
		Size: 26.9 MB (26899071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37688142f731d986b691ff1fb2dc200bb9903a51e9b288a2ad1da29fa8a2641b`  
		Last Modified: Wed, 09 Jul 2025 15:27:30 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ba50180eeb57afec212aa10aec40a19909289fe1c5f72eb37cd4002e225ea92`  
		Last Modified: Wed, 09 Jul 2025 15:27:32 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:273de3b1bf68606d549069c2d7b8fa46c75c2c6a60db65c911324981bf0e6c75`  
		Last Modified: Wed, 09 Jul 2025 15:27:30 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.8-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:66629ca6928a21987232cdafd80cd2f58198af1d79ef10d192348b1531a3e91f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1136805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:302cff9f5b5eddce268c57c1e60aac4601db33c44a065e68d6d04168b1f6d3e1`

```dockerfile
```

-	Layers:
	-	`sha256:778af353fd76a4bfd40bc07bdabfe0e7e88d1985e228e1d4d6043e6222532b52`  
		Last Modified: Tue, 08 Jul 2025 22:15:29 GMT  
		Size: 1.1 MB (1083026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:200e37976cbf4c6384ec0bce19f8006031c3314355def7444be547478306867f`  
		Last Modified: Tue, 08 Jul 2025 22:15:30 GMT  
		Size: 53.8 KB (53779 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.8-fpm-alpine` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:2b5449f6faeeefd5bff934e419ac2d52c9a1b9b70cfe22b26475d259b2a17788
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.0 MB (93029557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118e0200e727bd393b28c625fe419969e12bbc177e4cfe3b293d5338b9b35bc6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 03 Jul 2025 12:46:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Jul 2025 12:46:24 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_VERSION=8.2.29
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Jul 2025 12:46:24 GMT
WORKDIR /var/www/html
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 03 Jul 2025 12:46:24 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 03 Jul 2025 12:46:24 GMT
CMD ["php-fpm"]
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	version='6.8.2-RC1'; 	sha1='62102972957c99a42274e719fc537960f4ed346a'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
VOLUME [/var/www/html]
# Tue, 08 Jul 2025 19:03:14 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Jul 2025 19:03:14 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b2fddcddb67f07dabc88b449999588f7b51998c1114a9e3f0ae4ad9519b41e`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 3.4 MB (3432459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f159e81bd801861164e94e01093125bcc7ed5b9fb65bed9a9f3ce4d3a707c8c`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045dfb1ee98b64d4099b6b9d91bdb57fab7a640182f195075c814d3071429a5b`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4ee62282ba45798eee9dfb091af41d630a8873a7e39fc99ca0dc4c7b645c5d`  
		Last Modified: Fri, 04 Jul 2025 00:01:14 GMT  
		Size: 12.2 MB (12183814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbfde8895d2000b76b62727c74d397d749171b40510989774c2704b02550bcaa`  
		Last Modified: Fri, 04 Jul 2025 00:01:13 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7dc73dc886f8bf0463f361620135af1fb46eaac72e50393319512466949bb1c`  
		Last Modified: Fri, 04 Jul 2025 00:06:37 GMT  
		Size: 14.9 MB (14879416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c8371dcf60b925ec0d0ec3b5a6b9dbaadc3de09f4e191dbdaab0dd73080f4ed`  
		Last Modified: Fri, 04 Jul 2025 00:06:35 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a19db4eba543c66462d6cf9803d8a377ebe2b40ce2bd48850a563a8a8beeeb`  
		Last Modified: Fri, 04 Jul 2025 00:06:35 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea076f0a1aa107abed1dfb2a085c9e37f4e7e346aaee04bb4e1a473b950a48a`  
		Last Modified: Fri, 04 Jul 2025 00:06:35 GMT  
		Size: 20.0 KB (19993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a851feb0f737918b0f10ea146245486be4b8dcda5753ca7572fb9405ff6a5e97`  
		Last Modified: Fri, 04 Jul 2025 00:06:35 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86cf7a1f14992ebfcc44df6ffbf739cd2d71ee7dcb37abbf31dd3c2a2dc2097f`  
		Last Modified: Fri, 04 Jul 2025 01:40:19 GMT  
		Size: 24.4 MB (24359696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9ecab0a2fe7c4c031c7631fec18b89c6826b17aea02e693460a684b71e3c819`  
		Last Modified: Fri, 04 Jul 2025 01:40:15 GMT  
		Size: 7.7 MB (7653504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06e3550c57b09af7b28ac9eb2ec87280ae59d47e8fde8f0a02914b1a780866e`  
		Last Modified: Fri, 04 Jul 2025 01:40:14 GMT  
		Size: 62.6 KB (62552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6623c29c7ab538a9b22901d7193b0355d0fe49dcf2f20979c132a1a760b7c5a4`  
		Last Modified: Fri, 04 Jul 2025 01:40:14 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93881f0eddad714609c308b13c757c7139a96d72cf3b89577724857db8f3c300`  
		Last Modified: Tue, 08 Jul 2025 22:16:17 GMT  
		Size: 26.9 MB (26899092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:779cce9f8d5fc11c7ca6657b3ac2af7597934d52e19fe50e4403e21650eb7688`  
		Last Modified: Tue, 08 Jul 2025 22:16:16 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a38d52dab754e0031d773f2598908ab43dff7ac6142b389d620d980c112ff94`  
		Last Modified: Tue, 08 Jul 2025 22:16:16 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c242c81807201fe87e98c46d86dcb59aab32d857a793a214161ce1b3e6fd171b`  
		Last Modified: Tue, 08 Jul 2025 22:16:16 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.8-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:d59ccae7188a57406af68fd4b06a747da089f834fb8646bef494e4bc7973e6a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 KB (53752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cd30080d53b83d069617001a26da7b0762b66e21d47351b5076a661efb39ba1`

```dockerfile
```

-	Layers:
	-	`sha256:d01d46d599793ad4ed4ecfa5dd3e9ae4f3bbf2d6d5b7c8a03c1a71eca7a54c5d`  
		Last Modified: Tue, 08 Jul 2025 22:15:33 GMT  
		Size: 53.8 KB (53752 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.8-fpm-alpine` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:3c3b8ae67235df347d0b7b99777c98454020a4146f9f375d7868fcde021be699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91528829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54b19fe9e81c4d8e1d852f8d156d639b8cf1a43ae7a03c4642135934a0aa761`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 03 Jul 2025 12:46:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Jul 2025 12:46:24 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_VERSION=8.2.29
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Jul 2025 12:46:24 GMT
WORKDIR /var/www/html
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 03 Jul 2025 12:46:24 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 03 Jul 2025 12:46:24 GMT
CMD ["php-fpm"]
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	version='6.8.2-RC1'; 	sha1='62102972957c99a42274e719fc537960f4ed346a'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
VOLUME [/var/www/html]
# Tue, 08 Jul 2025 19:03:14 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Jul 2025 19:03:14 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec113fe1f048c8128d671c69cfadec1876ed37d14a445b7755326cbfa9acee36`  
		Last Modified: Wed, 11 Jun 2025 11:39:14 GMT  
		Size: 3.2 MB (3247470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3d974efcf5fd7ed95cd66bd2537770b4f31b8d7af064ae6e9119868bac3309`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29a62342af1e9fd2e1392885a9e1a9439cdee5d849c8f557fb8693b5650363b`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4850115fc99ef58d39ccdb152543870aa3fb14704b172d3fe472cccc1bff3e63`  
		Last Modified: Fri, 04 Jul 2025 01:46:01 GMT  
		Size: 12.2 MB (12183844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c82773d0467f11623ac0b360c9c4c5d03baa46594c5e11a459225ee229583b5`  
		Last Modified: Fri, 04 Jul 2025 01:46:00 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bbeb6f569a37ad1855ca3ceef04786898b1384c17ede4aeec5862578aa6c9ca`  
		Last Modified: Fri, 04 Jul 2025 01:49:37 GMT  
		Size: 14.0 MB (13964732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2427bf7fa4611ed8ccdc623dc67fac0c65e6e3e2b7ab29a5e3b377a6f931895e`  
		Last Modified: Fri, 04 Jul 2025 01:49:37 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c96fbaac6f81fcf92a044c1ecebb177d9e150e017339ae6a5347b734d486e9`  
		Last Modified: Fri, 04 Jul 2025 01:49:37 GMT  
		Size: 20.0 KB (19993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9552668e8e665846cb5444b72a75ef5c0d8ba4a616f06ff85a6d1820a5edb022`  
		Last Modified: Fri, 04 Jul 2025 01:49:36 GMT  
		Size: 20.0 KB (19992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f65f516eb09dd3f7f2c6a5b31f1bc1409224610e4a7d0caf801d5f1f4bb0daa6`  
		Last Modified: Fri, 04 Jul 2025 01:49:36 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0e04f352534982b2e97756575b5b2fdef0c6d1b65ddb26c1b4021b9aafec19`  
		Last Modified: Fri, 04 Jul 2025 03:02:40 GMT  
		Size: 23.1 MB (23137800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8079587b961a0bb95d0f96d8de89be8600233be5e43316537cb6d42b63d7e959`  
		Last Modified: Fri, 04 Jul 2025 03:02:39 GMT  
		Size: 8.8 MB (8756106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bdfe1a380c9e54acec46266a56ec07aa25002e9a942b773269175b41021d867`  
		Last Modified: Fri, 04 Jul 2025 03:02:38 GMT  
		Size: 62.5 KB (62523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfddb4512e95ae9cfbe76d28ac26fd1406cdfd869f72aea5d17bcc9d7725bee8`  
		Last Modified: Fri, 04 Jul 2025 03:02:37 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7599f072af755db76e179a2a7553bb940bfc77d95810133a388b66b20e8f28e`  
		Last Modified: Wed, 09 Jul 2025 20:31:01 GMT  
		Size: 26.9 MB (26899094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56083b4eb3fa5007f0dcece51d7dd76c00effcc5379b4acf29a0b48198f62c6`  
		Last Modified: Wed, 09 Jul 2025 20:31:00 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5f03fa1003d242a4ea20ee8a19373e93a61a5503834f13674ef3bebd2ae98f`  
		Last Modified: Wed, 09 Jul 2025 20:31:02 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c9df3ea74f426d4ef6d0149e6d941a6ea4c4bf43ed2d68b35312994ff4f9e7d`  
		Last Modified: Wed, 09 Jul 2025 20:31:02 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.8-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:9f5f9a427fb2d21cd2bbd2ef7142eb208c13b45040e119efa794d13e211a5210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1135834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3142df863f94819ffee36f55358e70bd8411056af88c21f711411772cab3e191`

```dockerfile
```

-	Layers:
	-	`sha256:fd6cc46b89bd31a7d7e837c8ced57957753e6db3e6746d9e503c5b3be9dbe061`  
		Last Modified: Tue, 08 Jul 2025 22:15:37 GMT  
		Size: 1.1 MB (1081866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f55d066117d01fe8a5be1377be6b67224ecacc4912fdbe20a4e0cad59fa6ed53`  
		Last Modified: Tue, 08 Jul 2025 22:15:37 GMT  
		Size: 54.0 KB (53968 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.8-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:2a5f702ef8698fbcf46cf17ec16bf6837c30c7ae6bcb51aae9d3cdc9ca208f04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.1 MB (100075904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6e98d7abc1e9ee6d91ad86e91932af0b9eec596b2455972147f136fd7c3003f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 03 Jul 2025 12:46:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Jul 2025 12:46:24 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_VERSION=8.2.29
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Jul 2025 12:46:24 GMT
WORKDIR /var/www/html
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 03 Jul 2025 12:46:24 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 03 Jul 2025 12:46:24 GMT
CMD ["php-fpm"]
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	version='6.8.2-RC1'; 	sha1='62102972957c99a42274e719fc537960f4ed346a'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
VOLUME [/var/www/html]
# Tue, 08 Jul 2025 19:03:14 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Jul 2025 19:03:14 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f73985aec8f2b878dbb559825b96bc42ecedc3f93d14e5f1b9a6ca2e1816299c`  
		Last Modified: Thu, 03 Jul 2025 23:26:01 GMT  
		Size: 6.2 MB (6231904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2edf112b2c5bea025053bf307e764ef87252d3b53a912374edb00c6b9cda47`  
		Last Modified: Thu, 03 Jul 2025 23:26:00 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106cb39859ac9004e783043bb75563ecfc6db5970ab2b1965a10cfec3c797d10`  
		Last Modified: Thu, 03 Jul 2025 23:26:00 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c85fad52315a324b6bcfa1bdfec74689faea510d6e706671c4d567af30b341d7`  
		Last Modified: Fri, 04 Jul 2025 01:22:47 GMT  
		Size: 12.2 MB (12183852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec4e6f8300e0c16a72f565392f4be992fa53deabe8bde22f3ed0f7a10f5242c`  
		Last Modified: Fri, 04 Jul 2025 01:22:45 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c03d6e7b65831f4e9eae015ace12e9aea4c2548114b005a74f2a71532aaf23`  
		Last Modified: Fri, 04 Jul 2025 01:27:25 GMT  
		Size: 13.0 MB (13023342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40f45e71980e2648702c530d39340056ef06d832493b289e5b3e0dfd00e95bd`  
		Last Modified: Fri, 04 Jul 2025 01:27:25 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b762ba494c6f7496ef2609bc1c9610adcc34ba0165980a26cec0f5856836090b`  
		Last Modified: Fri, 04 Jul 2025 01:27:25 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f4261346444131438235e92506ce9fda3316eb34a831d3ed4237f90ee38a35`  
		Last Modified: Fri, 04 Jul 2025 01:27:25 GMT  
		Size: 20.0 KB (20000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01fc71071a0c74b685e5c12952da71ae0f9aa9440e9a7a2cae9e9cc3cb170ab9`  
		Last Modified: Fri, 04 Jul 2025 01:27:25 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fffb413c97fb6b976ecb392110c5991bb13a5ee49ce0ec440a0b47a7b9510c`  
		Last Modified: Fri, 04 Jul 2025 03:40:14 GMT  
		Size: 28.1 MB (28082072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61eff06f0c6f4297b9ac4351805be09ab7e760ce4a1601f9b83cad584e9c5aa8`  
		Last Modified: Fri, 04 Jul 2025 03:40:13 GMT  
		Size: 9.4 MB (9399064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1cad7e28f6a04c0955c3e4fb750423a16f91341eb580706624b31b8f7b2e6d`  
		Last Modified: Fri, 04 Jul 2025 03:40:12 GMT  
		Size: 62.6 KB (62562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7740111b7c81cbbccc811bf171d0f0291ecd6b7e0c794ca7c45b4b1b6b34f1`  
		Last Modified: Fri, 04 Jul 2025 03:40:12 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a65c2425fc10a4cb329b2d378c40f549b0f5f105dc5c4fe7bb15aa17b83bf8`  
		Last Modified: Wed, 09 Jul 2025 20:23:25 GMT  
		Size: 26.9 MB (26899078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334ce19e5b9934958405ca20ca9d3ff26b0a54acfa1a845781a1e7a47dba6a8d`  
		Last Modified: Wed, 09 Jul 2025 20:23:23 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb27b7604352e6e6e34f2262e6a33addbe6b498508fdab29e63a508f1c85c70`  
		Last Modified: Wed, 09 Jul 2025 20:23:24 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4d5bde6c2e7145c2eeb23baa83bb59fc4e161ff21a9732352c203bf6789b750`  
		Last Modified: Wed, 09 Jul 2025 20:23:26 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.8-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:3f4bbb499cd9ee773986b92d35a972465064e9fc003e84fd9a825db93ac8cd53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1135940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c860ef2e1d23419f0e503e07044b5a34ad9d8b47b85cf4360682199c7b8f88c`

```dockerfile
```

-	Layers:
	-	`sha256:32f473a63a8e9522d3c14e497697ab3626236acd5a87cd4694a4cebfd17883ff`  
		Last Modified: Tue, 08 Jul 2025 22:15:41 GMT  
		Size: 1.1 MB (1081910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:654476c76d317d6dd14e32553f3c4e975f832f91fa5c116710bcceaf9ec160ad`  
		Last Modified: Tue, 08 Jul 2025 22:15:42 GMT  
		Size: 54.0 KB (54030 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.8-fpm-alpine` - linux; 386

```console
$ docker pull wordpress@sha256:e4e001696dd0be1ec5ad12cc7e549870d23589f5cc7555bdab5e54008685816c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.5 MB (98518468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eea79c5bd40db52777ae840aeb64e34af2448e94c6146003d2a2654a82b1c48b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 03 Jul 2025 12:46:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Jul 2025 12:46:24 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_VERSION=8.2.29
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Jul 2025 12:46:24 GMT
WORKDIR /var/www/html
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 03 Jul 2025 12:46:24 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 03 Jul 2025 12:46:24 GMT
CMD ["php-fpm"]
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	version='6.8.2-RC1'; 	sha1='62102972957c99a42274e719fc537960f4ed346a'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
VOLUME [/var/www/html]
# Tue, 08 Jul 2025 19:03:14 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Jul 2025 19:03:14 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1d96b5628f8670659289bf3bee6fb7c62d215846bc489213b8426851261582b`  
		Last Modified: Thu, 03 Jul 2025 23:10:39 GMT  
		Size: 5.8 MB (5806969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f59eb77e5d261968a192f5e738de61adbf415c63dfe15f2de6c1f98ec5d26e0`  
		Last Modified: Thu, 03 Jul 2025 23:10:38 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:568d3e15cb321228076e5668c824f9c68329ba34249abca4ffc741b3d6610893`  
		Last Modified: Thu, 03 Jul 2025 23:10:38 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8378afa5486d25e3db193e564343d695a12381eb657c0e11063e7b1e9c1876fc`  
		Last Modified: Thu, 03 Jul 2025 23:10:38 GMT  
		Size: 12.2 MB (12183833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b06e99a9b08b2b714510c519d0385826e3796db018801b5361486a6b3fb5d69`  
		Last Modified: Thu, 03 Jul 2025 23:10:38 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060ca2e22f52b7bfc37a84124f6e827a37c1cc820d0dbac2f4cf5a642e50f420`  
		Last Modified: Thu, 03 Jul 2025 23:10:40 GMT  
		Size: 13.3 MB (13348163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11043e4c378cc5c454a12709fb33257930e38a23ff7920502a4c1d5ac5861766`  
		Last Modified: Thu, 03 Jul 2025 23:10:37 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d18a33705482953496da8a9acd8c964b2bb128e45c9606cc3c87a17b031056`  
		Last Modified: Thu, 03 Jul 2025 23:10:39 GMT  
		Size: 20.2 KB (20190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5c09e74b632a6dcd06c39b44490ab9c9ca29d2c835b9a384dce0d6968ffcb3`  
		Last Modified: Thu, 03 Jul 2025 23:10:38 GMT  
		Size: 20.2 KB (20187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca70701271854a137f3a67943331eab64c777816324caeb151e5d738251c749d`  
		Last Modified: Thu, 03 Jul 2025 23:10:39 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f87d0c794366f0de86992908f52794c7b34601c0722ebe15e65ebccce37cef`  
		Last Modified: Wed, 09 Jul 2025 20:31:43 GMT  
		Size: 28.5 MB (28487021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c09047944da9c0630c6fe89a5bb41c086b0b3b181a96d0835465c04c09d30482`  
		Last Modified: Wed, 09 Jul 2025 20:31:41 GMT  
		Size: 8.1 MB (8056401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89bde066155b5c029c9cd04d512b0c7ea1622e99c61474cdde06de67c76ff630`  
		Last Modified: Wed, 09 Jul 2025 20:31:40 GMT  
		Size: 62.5 KB (62521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4186e5af8793b0a6521586a701c1dcecb48daa048933b1a5f16b60150034d845`  
		Last Modified: Wed, 09 Jul 2025 20:31:41 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde5b6d2ffd3da487294ef0a226f8369065e71dd2fc0c2ec662d68774590322a`  
		Last Modified: Wed, 09 Jul 2025 20:31:42 GMT  
		Size: 26.9 MB (26899066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c00127d54da8533aeb939dfccd7ed000670ad2ab3e8d665b8c913badb391cb3`  
		Last Modified: Wed, 09 Jul 2025 20:31:43 GMT  
		Size: 2.4 KB (2435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29947e5f6ffe6422fcc29990707e45da1d29276797df767da23df80b18ff9d89`  
		Last Modified: Wed, 09 Jul 2025 20:31:43 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7399db2f5d0e5fdc1aa188ac1c7cbbd04cec7b8a17def98a4027b25a82bb151`  
		Last Modified: Wed, 09 Jul 2025 20:31:44 GMT  
		Size: 196.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.8-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:a4dcf8fcbd6f63375181b6f9533c2350e0452d8d574230961f50b9347adcd604
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1136678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8a95a1887bdfc86df677eccc1e256610d3474b5cfabd50e89ffaff4a443d982`

```dockerfile
```

-	Layers:
	-	`sha256:6583f2a80fe0664d96458dd0119b7a2187ad01bea50139e0e881a1951cf3bbfc`  
		Last Modified: Tue, 08 Jul 2025 22:15:45 GMT  
		Size: 1.1 MB (1082971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc0469edcc524195bdedf2b66f8aa9f24062a41d968e41e8b6830fe1333ab9e0`  
		Last Modified: Tue, 08 Jul 2025 22:15:46 GMT  
		Size: 53.7 KB (53707 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.8-fpm-alpine` - linux; ppc64le

```console
$ docker pull wordpress@sha256:2fa69b77e48a6cacd9ee7fb556e82bb48794e7dbb30a2160633b2255e02e26eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.3 MB (100254578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0daa6a69379a3b0deadb47eac3a75ead4e4c59d9d3b3172a0c51cdb367e9ca09`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 03 Jul 2025 12:46:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Jul 2025 12:46:24 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_VERSION=8.2.29
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Jul 2025 12:46:24 GMT
WORKDIR /var/www/html
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 03 Jul 2025 12:46:24 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 03 Jul 2025 12:46:24 GMT
CMD ["php-fpm"]
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	version='6.8.2-RC1'; 	sha1='62102972957c99a42274e719fc537960f4ed346a'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
VOLUME [/var/www/html]
# Tue, 08 Jul 2025 19:03:14 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Jul 2025 19:03:14 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7db3af28cc31124a8bce98c13cd1b2512963d13f437d0d67f9918df0d57d2b`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 5.9 MB (5946924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ec39d79edfa484fac002ed8c640f17ae8077df4dce88811d8d186865593a6b`  
		Last Modified: Thu, 03 Jul 2025 23:15:36 GMT  
		Size: 939.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2995d4272705fc452f2b3ea9e2d118681efbad9f858c7743f6f69364d73a50`  
		Last Modified: Thu, 03 Jul 2025 23:15:35 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:790bf6906a4b16496902e6eba7e88ec69093d118faf89d335c5a519a51ddfab6`  
		Last Modified: Fri, 04 Jul 2025 00:32:28 GMT  
		Size: 12.2 MB (12183838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ac38a5597c0dc1fb42cdffbb60a8ce5c075565d6be2c890245e0f08ad7c0af`  
		Last Modified: Fri, 04 Jul 2025 00:32:27 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3113925438bd415e99bc1294471b466c84d7f6b34a5eaefa35279c8c15697115`  
		Last Modified: Fri, 04 Jul 2025 00:35:55 GMT  
		Size: 13.5 MB (13493710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e22e9b016d5e85c39ddce5fc57bff7028e928dbcfb7f5f1aea222a16e554033`  
		Last Modified: Fri, 04 Jul 2025 00:35:54 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f7984cc31bf2a130ffb2e3b4880cacb2dde0217d149ddbb63ca92c39d63646`  
		Last Modified: Fri, 04 Jul 2025 00:35:55 GMT  
		Size: 20.0 KB (20005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:911b401700272d2a1af471f40f4326f9c9ad7030bce9a7eb9a8faa1aefb9cce4`  
		Last Modified: Fri, 04 Jul 2025 00:35:56 GMT  
		Size: 20.0 KB (19998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54b7f7d31da75c5d38cde92483e4768c54a142da49922117f1ba03b12a738b5`  
		Last Modified: Fri, 04 Jul 2025 00:35:56 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f98224d41b3bc6310c39faadaaeb2479db411fdfe07719bb4583bb6c5a6362`  
		Last Modified: Fri, 04 Jul 2025 01:53:25 GMT  
		Size: 28.9 MB (28916025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c78f15d7e34141960463d00da3e42108494fa1b7e98cf7e1d70a79a9cd9ec5`  
		Last Modified: Fri, 04 Jul 2025 01:53:24 GMT  
		Size: 9.0 MB (8964171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f930d11295a972c8c59373db7d67e582c146698ff670bbbc7561ac84e3fce1c`  
		Last Modified: Fri, 04 Jul 2025 01:53:23 GMT  
		Size: 62.6 KB (62556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6fc3eda9c052d54090af28dfc237937ac00434509920c820a387ab92c230429`  
		Last Modified: Fri, 04 Jul 2025 01:53:23 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fcd828512df4b28bc5844716ed9e0857904c7ccfd1c1d1a5a8ac5ba21e0e46d`  
		Last Modified: Wed, 09 Jul 2025 20:32:06 GMT  
		Size: 26.9 MB (26899064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad71e5b388f7577cde081c65ebaf9c137f667dcf3b1cb25123a9c8c0978b5aa8`  
		Last Modified: Wed, 09 Jul 2025 20:32:04 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca7726b75802964cf6be1c6fa46df56d2c6d1e752b7046d6d0c4ad26d5193601`  
		Last Modified: Wed, 09 Jul 2025 20:32:06 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d1f1fef39d71e32582736a7194310e42894511d924cc9560ec53dd05d2052b5`  
		Last Modified: Wed, 09 Jul 2025 20:32:07 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.8-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:90c16f066a33036c0b3e2fa8c0f75dab22c844585d259a4d60f7161e15f012f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1133770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47914bff243e96b4d9577109859a63259dc8ee7d0c398acff95db11046c47987`

```dockerfile
```

-	Layers:
	-	`sha256:05d068bd22ad7095903674c128eea11b12657d4ce706f35953dca660d247672a`  
		Last Modified: Tue, 08 Jul 2025 22:15:50 GMT  
		Size: 1.1 MB (1079901 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b23c3cb4c8481da52789c3983939bcb9a0737198f228bb0e2468c830b55dcb5a`  
		Last Modified: Tue, 08 Jul 2025 22:15:50 GMT  
		Size: 53.9 KB (53869 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.8-fpm-alpine` - linux; riscv64

```console
$ docker pull wordpress@sha256:20171d2cff25cfb4bb92e847d56eaf0b47c75970e17e4adb0f14c7ac14d6cf96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.8 MB (96843629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cc99f8ea6c5598bc6e029c8928c6a966c7d2f2dec69040b6167958025aceb9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 03 Jul 2025 12:46:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Jul 2025 12:46:24 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_VERSION=8.2.29
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Jul 2025 12:46:24 GMT
WORKDIR /var/www/html
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 03 Jul 2025 12:46:24 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 03 Jul 2025 12:46:24 GMT
CMD ["php-fpm"]
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	version='6.8.2-RC1'; 	sha1='62102972957c99a42274e719fc537960f4ed346a'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
VOLUME [/var/www/html]
# Tue, 08 Jul 2025 19:03:14 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Jul 2025 19:03:14 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc9c1f5ef55f1b2ff3a6b36284b619ab1578de78bc84c439b1898065ffdd4f1`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 3.6 MB (3603347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799ef8c3b461dc47d68354281bf2ae2d00422c181fa7d8f8084c1489e4f74b7c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6faf4f4cbdf1dd7a77faca53bd9b20a1a4be9c74973d2b4d795fed979f275c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c7222bbb28334b2afe139d1d92397d4be65c490f9bee5e6fcbf9d97d6279d3`  
		Last Modified: Fri, 04 Jul 2025 10:35:06 GMT  
		Size: 12.2 MB (12183843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0557410c9f7cf55cb21958cba80b21371ef0cf8a6cb3dcf740205adf22747e07`  
		Last Modified: Fri, 04 Jul 2025 10:35:04 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b668a3d45f2b932701f32320596bc6890c3bfb8ee3884c021f7d3be3eb2287df`  
		Last Modified: Fri, 04 Jul 2025 11:23:05 GMT  
		Size: 15.4 MB (15441741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43406042cd0ba23b6761b2a24a543e859d21c1ca8e064aa16d12d184e929b72d`  
		Last Modified: Fri, 04 Jul 2025 11:23:03 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e00e07e60f69b4d6539149588344d988e77d12d47c2ddbfc870467d22edc894`  
		Last Modified: Fri, 04 Jul 2025 11:23:03 GMT  
		Size: 20.0 KB (19993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8d69a6122ecf84a73e338d3f42a2e241cba3168aecc2218494f532e1c0aa31`  
		Last Modified: Fri, 04 Jul 2025 11:23:03 GMT  
		Size: 20.0 KB (19995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6d02f1659c1708a9966cbe7166e61d762500229b098e948f1cc82475c68299`  
		Last Modified: Fri, 04 Jul 2025 11:23:04 GMT  
		Size: 9.2 KB (9175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af5aa3b711fa1b169ad614e3de5ff99bb2ee332dba032a186b8610224385faa4`  
		Last Modified: Fri, 04 Jul 2025 20:04:13 GMT  
		Size: 28.1 MB (28067873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1630351e2256d59a7c0d74e3fdc486a79513fee477a15378d6ea3fd8a5ca7e5d`  
		Last Modified: Fri, 04 Jul 2025 20:04:13 GMT  
		Size: 7.0 MB (7013259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b56bfbb9d3f593511e172290136b96355617467a235612e3394844c13ed221`  
		Last Modified: Fri, 04 Jul 2025 20:04:12 GMT  
		Size: 62.6 KB (62557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec68bba60db94ffc37fbca791fdb9c57edb0f2c4d41c5304fcfa258d6556dda`  
		Last Modified: Fri, 04 Jul 2025 20:04:11 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f544d6916a13939bec35bcc64afbabe31b0aed544889136560e8943f3080d487`  
		Last Modified: Wed, 09 Jul 2025 21:22:27 GMT  
		Size: 26.9 MB (26899103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:852ae4436c64feeab92fb9d15be3d5b0e0c621f18275b9d8bba972c850e48d39`  
		Last Modified: Wed, 09 Jul 2025 21:22:26 GMT  
		Size: 2.4 KB (2440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ffaab977ffc6d8b1354a25cd29c140a2880d050c81ed3b870ff2ed6adbe71d`  
		Last Modified: Wed, 09 Jul 2025 21:22:28 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439f614f978f7c7b792f2606010a2959cd6ce1066ee30964a010409aa71db410`  
		Last Modified: Wed, 09 Jul 2025 21:22:28 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.8-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:9a2dedf250d542065a27bda04191ce7efe1756f2dfc3f42b1f47bec102d280ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1133766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3f4e809330ea7b900d509d8aab48a482f68271ea7bc61a4608a2a9885fc2846`

```dockerfile
```

-	Layers:
	-	`sha256:9d41fbea323e417db50768c078d0175dc2428a9c0a23c6bcfc47f6fb8ac66210`  
		Last Modified: Tue, 08 Jul 2025 22:15:54 GMT  
		Size: 1.1 MB (1079897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0ef64c2b4122c7d24bc15c79faf6e9b8ed9e0b28aa42cb8ef9e3b752fe709a7`  
		Last Modified: Tue, 08 Jul 2025 22:15:55 GMT  
		Size: 53.9 KB (53869 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.8-fpm-alpine` - linux; s390x

```console
$ docker pull wordpress@sha256:277b49ac2f2e69cb455ab988f9079896aad6bb3ea8a2da844f9191422ad1d385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.6 MB (99648191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b23bc368a1b5d57c7f1d7f7c64078121f69f98d407bc2c42ccaa385fbcade1d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 03 Jul 2025 12:46:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 03 Jul 2025 12:46:24 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_VERSION=8.2.29
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.29.tar.xz.asc
# Thu, 03 Jul 2025 12:46:24 GMT
ENV PHP_SHA256=475f991afd2d5b901fb410be407d929bc00c46285d3f439a02c59e8b6fe3589c
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 03 Jul 2025 12:46:24 GMT
WORKDIR /var/www/html
# Thu, 03 Jul 2025 12:46:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 03 Jul 2025 12:46:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 03 Jul 2025 12:46:24 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 03 Jul 2025 12:46:24 GMT
CMD ["php-fpm"]
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN set -eux; 	version='6.8.2-RC1'; 	sha1='62102972957c99a42274e719fc537960f4ed346a'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
VOLUME [/var/www/html]
# Tue, 08 Jul 2025 19:03:14 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 08 Jul 2025 19:03:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Jul 2025 19:03:14 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7abd3e67b018bcd8c0aa4d0434d7ec04dcdb3a3cfbf444a313e2be49d0524ec2`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 5.9 MB (5932552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f41e4866617495859c5133b898f769b3867a6a3ae061aa9561da765981c5ad`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9335ac6e22dd0c0b2e07f4a5406c437168067a987662ebd8bcd3b269496018`  
		Last Modified: Thu, 03 Jul 2025 23:16:22 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617af236d5ad95f5074829e2b22833cf0dbb14e4f4f1c63d84d242cbeedbd52f`  
		Last Modified: Fri, 04 Jul 2025 00:34:26 GMT  
		Size: 12.2 MB (12183857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f00a9fd00815af9531706206a2f7d257a42885f8596f83748f7f19f6f2b8b902`  
		Last Modified: Fri, 04 Jul 2025 00:34:24 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60e58700966d78b5a3c6a99e195c824b1e611f16d332d2c16f5fb1e029a6ac6`  
		Last Modified: Fri, 04 Jul 2025 00:38:07 GMT  
		Size: 13.0 MB (12979815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15f04e980d6879eebc28e270d275e45cd15b5796106ee17f0e1edc1e07bb87f`  
		Last Modified: Fri, 04 Jul 2025 00:38:05 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df49ea7c7e24de52ec97616f36f3357ef4d6008551bf085fd0e77612beab4a0c`  
		Last Modified: Fri, 04 Jul 2025 00:38:05 GMT  
		Size: 20.0 KB (20003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a8aeba77960627b2597fdaea47bafe9d1168243ba10d620968e73080393c63b`  
		Last Modified: Fri, 04 Jul 2025 00:38:05 GMT  
		Size: 20.0 KB (19994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aff6a908eaf438e6287d37188a6594f6f3521f9b4f4bf57bb023e1ae7fc3554e`  
		Last Modified: Fri, 04 Jul 2025 00:38:05 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35098fac81df818d9856460501ea283c47d63b2d2e431bebf9651dfd8bd329d0`  
		Last Modified: Fri, 04 Jul 2025 01:42:40 GMT  
		Size: 29.3 MB (29250145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7588420723c8ff05744a75cd7f592746cc41635f120166b2eb0e2e94ebb9b0cb`  
		Last Modified: Fri, 04 Jul 2025 01:42:39 GMT  
		Size: 8.6 MB (8634582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76b357ea317aba300372f1ae615275ed25344d949432385e439716cd744245e`  
		Last Modified: Fri, 04 Jul 2025 01:42:38 GMT  
		Size: 62.5 KB (62544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7a357419c23786047f4a877770b79d3c89055671e68cb52ad43c33009a3ab9`  
		Last Modified: Fri, 04 Jul 2025 01:42:38 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9690d3b85eac8b6e5879965d7f2ce9c886341303723cf477c838b8f30d2872b`  
		Last Modified: Wed, 09 Jul 2025 21:22:51 GMT  
		Size: 26.9 MB (26899075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c829a2782682c4a4ae5f6d91fba0a76e8b86ad3f35073ba558977d621abf7a`  
		Last Modified: Wed, 09 Jul 2025 21:22:49 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:311b6bc2f2afe424c1c1bdc07e97d9108df0dd60d484a0a22b591ac2307c8e5f`  
		Last Modified: Wed, 09 Jul 2025 21:22:51 GMT  
		Size: 1.8 KB (1763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9b6fd29d1d3d3b3827825c0ab96e25c1ee9331bbf4dd4e27dde1089406cf0d1`  
		Last Modified: Wed, 09 Jul 2025 21:22:52 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.8-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:2c103a5d2519ee84e64e98812f3d40af74a8e0b85a241e1b46a233ce43966274
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1133609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:552de23d3aa808e35b11b8f6abe88fbc650ac8e34ada3e242d1bc6e291507ce7`

```dockerfile
```

-	Layers:
	-	`sha256:72b6c8af8f32447e4b60b2f098aa060080d3a4d114799119f6a03a36afe2f93d`  
		Last Modified: Tue, 08 Jul 2025 22:15:59 GMT  
		Size: 1.1 MB (1079831 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d0c9d37a600de090ab2ac0d5e0c80f8ec146bf93fd2324412d9009d44750cc0`  
		Last Modified: Tue, 08 Jul 2025 22:15:59 GMT  
		Size: 53.8 KB (53778 bytes)  
		MIME: application/vnd.in-toto+json
