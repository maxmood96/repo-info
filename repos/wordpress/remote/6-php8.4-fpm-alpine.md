## `wordpress:6-php8.4-fpm-alpine`

```console
$ docker pull wordpress@sha256:88ede2488febfbccea432a58c13fe32a0510985ca549650c61a2999c1c9ff957
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

### `wordpress:6-php8.4-fpm-alpine` - linux; amd64

```console
$ docker pull wordpress@sha256:5a2679996fd4d8fb634df3b570948abea0799b74ec943a7393bb77ccb0039db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.7 MB (105654095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08bbd7e4f85246ff58c835c68fe8a7227244397360938f73297140f1b365b7e9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 23:17:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 16 Jan 2026 23:17:31 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 16 Jan 2026 23:17:31 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 16 Jan 2026 23:17:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 Jan 2026 23:17:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 Jan 2026 23:17:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:17:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:17:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 Jan 2026 23:17:31 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 16 Jan 2026 23:17:31 GMT
ENV PHP_VERSION=8.4.17
# Fri, 16 Jan 2026 23:17:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.17.tar.xz.asc
# Fri, 16 Jan 2026 23:17:31 GMT
ENV PHP_SHA256=28b234e347286158cae921d61283eb1169d89bc9d2e5f5976567260ff38b0bfa
# Fri, 16 Jan 2026 23:24:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 16 Jan 2026 23:24:37 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:27:27 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 Jan 2026 23:27:27 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:27:28 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 Jan 2026 23:27:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 Jan 2026 23:27:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Jan 2026 23:27:28 GMT
WORKDIR /var/www/html
# Fri, 16 Jan 2026 23:27:28 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 16 Jan 2026 23:27:28 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Jan 2026 23:27:28 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 16 Jan 2026 23:27:28 GMT
CMD ["php-fpm"]
# Fri, 16 Jan 2026 23:52:53 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Fri, 16 Jan 2026 23:53:43 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 16 Jan 2026 23:53:43 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Fri, 16 Jan 2026 23:53:43 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Fri, 16 Jan 2026 23:53:45 GMT
RUN set -eux; 	version='6.9'; 	sha1='256dda5bb6a43aecd806b7a62528f442c06e6c25'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Fri, 16 Jan 2026 23:53:45 GMT
VOLUME [/var/www/html]
# Fri, 16 Jan 2026 23:53:45 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Fri, 16 Jan 2026 23:53:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:53:45 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Fri, 16 Jan 2026 23:53:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:53:45 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d879bd4a499cd3fca061cd2cc459722657c044d974935e3e8a7872715481c87`  
		Last Modified: Fri, 16 Jan 2026 23:20:14 GMT  
		Size: 3.6 MB (3591610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090d95d29cac69ae35b5fa20be7f7192d982e682e60d4270fe4903c0d35bdd04`  
		Last Modified: Fri, 16 Jan 2026 23:28:05 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2fd0333f45274c8f2857f697b47640a446550a1a4fc33892ab755aafba6f58`  
		Last Modified: Fri, 16 Jan 2026 23:20:13 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e5009c66469e8dff340799c45f7d5f6529c915b3d0a70042d63ec9dd1a2cba`  
		Last Modified: Fri, 16 Jan 2026 23:27:46 GMT  
		Size: 13.7 MB (13694309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac4675b5f0f78e997ac3fa5af45ee3b2d7cd94bca03f424c01e9c2c19d3771a`  
		Last Modified: Fri, 16 Jan 2026 23:27:43 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eca59b2f19e837111f159ed571b3df16dd69049e10574c3964ce970dec71dbb`  
		Last Modified: Fri, 16 Jan 2026 23:27:44 GMT  
		Size: 15.2 MB (15183332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3127cadec5237e8a42a534a69b3f1cfbd5c0c3d121614313b412e6a70e3c881b`  
		Last Modified: Fri, 16 Jan 2026 23:27:43 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad7e3c186d6c1a2bcdc7e20d571ab67cd07eea7413f873a24ae15a9c5c05029`  
		Last Modified: Fri, 16 Jan 2026 23:27:50 GMT  
		Size: 23.5 KB (23497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9c11439c81cde32530b0529f9059458590ea378e26696c027ec54d88b9e715b`  
		Last Modified: Fri, 16 Jan 2026 23:27:43 GMT  
		Size: 23.5 KB (23516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cd19bad6322fc3c89d1f47f4983172fe299b14ecf6dda136f833984ac89bd4`  
		Last Modified: Fri, 16 Jan 2026 23:27:37 GMT  
		Size: 9.3 KB (9266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53826c3844298fff65f6a1c80bd7dc463614c1e7e12a2c5689976b5281d40dcc`  
		Last Modified: Fri, 16 Jan 2026 23:53:56 GMT  
		Size: 32.8 MB (32819997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0bc7438f84cf0bd0578e186a6d0d0c9726d6138a555dbd35223cdc535a33c5`  
		Last Modified: Fri, 16 Jan 2026 23:54:05 GMT  
		Size: 9.4 MB (9414037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72147817658b512ce80b6fa269b620e46fe7902dcf0a64ab11c644a1e47fe27e`  
		Last Modified: Fri, 16 Jan 2026 23:54:04 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8384a841f9b22f83a95cd2e442d32982d03dc0d2017491bdca0f5f012c2b69d6`  
		Last Modified: Fri, 16 Jan 2026 23:54:04 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d1cdc37018868b89e32a43e678835991642e5bc2c2bc73d1192442fa81b276`  
		Last Modified: Fri, 16 Jan 2026 23:53:57 GMT  
		Size: 27.0 MB (27025216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796c23b077eec71ce89138d8bc29c3fecfbe6655dbfffbcf4eb58e9a35f6e7eb`  
		Last Modified: Fri, 16 Jan 2026 23:53:57 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40191a288e25ae290f9e486b9137d01def319d2a06ae4b87b91319565aa98fe5`  
		Last Modified: Fri, 16 Jan 2026 23:53:57 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c960a082532d4f10ab6feca9a2a1c3accd60de8509e39a73d796eca1bd626b97`  
		Last Modified: Fri, 16 Jan 2026 23:54:04 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:ce0be4a29c53fd64bf2c68234b320193adbc1b8a8422a99598df9fa1b4d3b1ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1173760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a34cf4edae75d6ca512acffb26b840c57ff14b04cd88cef884e5456e762c4a24`

```dockerfile
```

-	Layers:
	-	`sha256:4d679b75e9f78ad6517d0eef29ebe40c73f23c09e429530082b7cfddd2d5a968`  
		Last Modified: Fri, 16 Jan 2026 23:53:55 GMT  
		Size: 1.1 MB (1122037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33385839e0db186cb2b89016fed7042bfc864301195c374a16c8fb1645bfa60a`  
		Last Modified: Sat, 17 Jan 2026 02:15:33 GMT  
		Size: 51.7 KB (51723 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.4-fpm-alpine` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:4a7b9e1ba59ca72b7c5e490511c1398bdcdceaf1e8b0fdf6fd2331806171913d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.8 MB (97830683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:642e614e48927421561ee798d701dce75b893f401d257fa691b6dc5bbb5ef022`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 23:16:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 16 Jan 2026 23:16:42 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 16 Jan 2026 23:16:42 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 16 Jan 2026 23:16:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 Jan 2026 23:16:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 Jan 2026 23:16:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:16:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:16:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 Jan 2026 23:16:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 16 Jan 2026 23:16:43 GMT
ENV PHP_VERSION=8.4.17
# Fri, 16 Jan 2026 23:16:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.17.tar.xz.asc
# Fri, 16 Jan 2026 23:16:43 GMT
ENV PHP_SHA256=28b234e347286158cae921d61283eb1169d89bc9d2e5f5976567260ff38b0bfa
# Fri, 16 Jan 2026 23:24:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 16 Jan 2026 23:24:59 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:28:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 Jan 2026 23:28:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:28:10 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 Jan 2026 23:28:11 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 Jan 2026 23:28:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Jan 2026 23:28:11 GMT
WORKDIR /var/www/html
# Fri, 16 Jan 2026 23:28:11 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 16 Jan 2026 23:28:11 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Jan 2026 23:28:11 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 16 Jan 2026 23:28:11 GMT
CMD ["php-fpm"]
# Fri, 16 Jan 2026 23:43:37 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Fri, 16 Jan 2026 23:44:59 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 16 Jan 2026 23:44:59 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Fri, 16 Jan 2026 23:44:59 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Fri, 16 Jan 2026 23:45:01 GMT
RUN set -eux; 	version='6.9'; 	sha1='256dda5bb6a43aecd806b7a62528f442c06e6c25'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Fri, 16 Jan 2026 23:45:01 GMT
VOLUME [/var/www/html]
# Fri, 16 Jan 2026 23:45:01 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Fri, 16 Jan 2026 23:45:01 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:45:01 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Fri, 16 Jan 2026 23:45:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:45:01 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:27 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8df8ed2947c4634c4deb205c96657594590a91ad81244ebf749a9bc65e359998`  
		Last Modified: Fri, 16 Jan 2026 23:19:45 GMT  
		Size: 3.5 MB (3548390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebee0b439ad61061926828e6626d74441d7959b21efeacd203eb3c67a13fb74a`  
		Last Modified: Fri, 16 Jan 2026 23:39:25 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad69840482ff6ba4ecc6243c4ce4ca7faa3a8c948a56cd28a2503201c8e95609`  
		Last Modified: Fri, 16 Jan 2026 23:39:28 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:519106bea804086b6e61d1fc7208d4d9153b1870ce8e001ba80d4fa6e6298a1d`  
		Last Modified: Fri, 16 Jan 2026 23:28:25 GMT  
		Size: 13.7 MB (13694327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d011bee1a8013e4de8f017daf121130331eea788c76e72cb02cb6163ad92e65`  
		Last Modified: Fri, 16 Jan 2026 23:28:16 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259f70cef0eea24b2fd54a735d64d12122f15a469f836394ede81fa44625122f`  
		Last Modified: Fri, 16 Jan 2026 23:28:25 GMT  
		Size: 13.7 MB (13667908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb5e8896ed624eaad2c6f68f0cc5a5279652cf00c0e2abdf962d4d1186766fd`  
		Last Modified: Fri, 16 Jan 2026 23:28:16 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d26ced82f6ba0fb08015e382f70ca30678f5e418f43c8fa1752e7aea65aaf30`  
		Last Modified: Fri, 16 Jan 2026 23:28:17 GMT  
		Size: 23.3 KB (23334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb7afa9c5b317018862f629c1b7c6b270638a69c87591db03bdbe6271589a9b6`  
		Last Modified: Fri, 16 Jan 2026 23:28:17 GMT  
		Size: 23.3 KB (23347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd85d23565bc1ec89cda2136e2809c2a6858f793b8cf77c617939c7df6e399f1`  
		Last Modified: Fri, 16 Jan 2026 23:28:23 GMT  
		Size: 9.3 KB (9266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b776bdf32bbf5535f26dc58d18af1494b6192498be67a13140b0842e1f92321`  
		Last Modified: Fri, 16 Jan 2026 23:45:09 GMT  
		Size: 28.5 MB (28536572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e83b4306e26e2b41de25407f3ff89c975ab19a018d1d22ba70d01098c88ed6`  
		Last Modified: Fri, 16 Jan 2026 23:45:15 GMT  
		Size: 7.7 MB (7724662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ad7f447934b5383839a7d24b72092274b265b289da07c6301622a59e5d71f0f`  
		Last Modified: Fri, 16 Jan 2026 23:45:14 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d73e6c89ef98401f74cfafcc3f6a292370d8abef08d717d874ec1378595aae`  
		Last Modified: Fri, 16 Jan 2026 23:45:14 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237b582636730d1c865eb4f829f7cecdb296bdd715a502f0b933d61c83e3e3ca`  
		Last Modified: Fri, 16 Jan 2026 23:45:17 GMT  
		Size: 27.0 MB (27025225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df9ec37787b2eb63b9838da004ce9e978cc33a8b6e76136425fcee3150d513e`  
		Last Modified: Fri, 16 Jan 2026 23:45:09 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f2f773c6a2d7fbf41bb8a193a23c46036246b2e216aaf910cc562e32c227bf`  
		Last Modified: Fri, 16 Jan 2026 23:45:14 GMT  
		Size: 1.8 KB (1764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab6b52c6a902eda6e0649444a1d1098c629c30d71c230d11044a2176532623c1`  
		Last Modified: Fri, 16 Jan 2026 23:45:14 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:b560c379f03d40cd68fc6fb2b52dbceff4383275ce12437497783bb8166d49ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 KB (51653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d984f144779d17cbe80712f7ac01975968c623c96c684513e4010875a8e99b58`

```dockerfile
```

-	Layers:
	-	`sha256:fa8dba901e542d3d0a3af52c3b696641fa46bad28a71e71d9ac99ec02250670e`  
		Last Modified: Fri, 16 Jan 2026 23:45:08 GMT  
		Size: 51.7 KB (51653 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.4-fpm-alpine` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:e18bb7920b67e46d3512276dcac48d54325dc34d419ba05ec6087e78af517487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95932194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec25c357dd9bc1dfc11d18428dccc0718feeea8e5a060df2a9b8ca2b111cddbb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 23:27:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 16 Jan 2026 23:27:50 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 16 Jan 2026 23:27:50 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 16 Jan 2026 23:27:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 Jan 2026 23:27:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 Jan 2026 23:27:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:27:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:27:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 Jan 2026 23:27:50 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 16 Jan 2026 23:27:50 GMT
ENV PHP_VERSION=8.4.17
# Fri, 16 Jan 2026 23:27:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.17.tar.xz.asc
# Fri, 16 Jan 2026 23:27:50 GMT
ENV PHP_SHA256=28b234e347286158cae921d61283eb1169d89bc9d2e5f5976567260ff38b0bfa
# Fri, 16 Jan 2026 23:34:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 16 Jan 2026 23:34:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:37:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 Jan 2026 23:37:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:37:40 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 Jan 2026 23:37:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 Jan 2026 23:37:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Jan 2026 23:37:41 GMT
WORKDIR /var/www/html
# Fri, 16 Jan 2026 23:37:41 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 16 Jan 2026 23:37:41 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Jan 2026 23:37:41 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 16 Jan 2026 23:37:41 GMT
CMD ["php-fpm"]
# Fri, 16 Jan 2026 23:50:34 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Fri, 16 Jan 2026 23:51:56 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 16 Jan 2026 23:51:56 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Fri, 16 Jan 2026 23:51:56 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Fri, 16 Jan 2026 23:51:58 GMT
RUN set -eux; 	version='6.9'; 	sha1='256dda5bb6a43aecd806b7a62528f442c06e6c25'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Fri, 16 Jan 2026 23:51:58 GMT
VOLUME [/var/www/html]
# Fri, 16 Jan 2026 23:51:58 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Fri, 16 Jan 2026 23:51:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:51:58 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Fri, 16 Jan 2026 23:51:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:51:58 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:29 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03244bb8e06c15a141a9809176a3acede73fad3c3725c7516f874233329f9f4`  
		Last Modified: Fri, 16 Jan 2026 23:31:15 GMT  
		Size: 3.3 MB (3347153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6153a9b698a9258dc066a44376293978525f3b8b4216c82e693a3624b28a0b6a`  
		Last Modified: Fri, 16 Jan 2026 23:31:15 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b583ab0f17d8843a0ef6581d98d4b858bbeb4303a6c9c351c91926af5ff5146`  
		Last Modified: Fri, 16 Jan 2026 23:31:15 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acac18f2b7b24c15cbd88728f72facffdff7564196e5150ae39040c06e1b62b4`  
		Last Modified: Fri, 16 Jan 2026 23:37:56 GMT  
		Size: 13.7 MB (13694323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94f3502a7629790977dcac19a4650281c07b7f94506477a3a287ac3d963b33d`  
		Last Modified: Fri, 16 Jan 2026 23:37:47 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d07a9ec91fa0dfea2b34323a920e77ad92e6e06babf8949c0b411d6e00e557a`  
		Last Modified: Fri, 16 Jan 2026 23:37:57 GMT  
		Size: 12.9 MB (12906863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d959adfab783bf85061f0045f3dfea7d51259ffc9edfe6f1ffa6135668efb79e`  
		Last Modified: Fri, 16 Jan 2026 23:37:54 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a84ef97da02e551737d78a0659eb61f7b52aac8c96126b6195c37baa635b664`  
		Last Modified: Fri, 16 Jan 2026 23:37:54 GMT  
		Size: 23.3 KB (23329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65129cc409293188983ea8ba06d3e21ca4be1d1d35b555fab1f35542210b9e1f`  
		Last Modified: Fri, 16 Jan 2026 23:37:48 GMT  
		Size: 23.4 KB (23351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beae67dabe893401cc767d3f570ee0684680b2c880023953902cf76df5efcf0b`  
		Last Modified: Fri, 16 Jan 2026 23:37:54 GMT  
		Size: 9.3 KB (9269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1613735103d8969ef94208d7e5780ca160f71cf31aa4eb270f09c2ca286c45a1`  
		Last Modified: Fri, 16 Jan 2026 23:52:08 GMT  
		Size: 26.9 MB (26886267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdcecd1d7ee921af14206827d8bbc7f3f8c9d5ff872aae71ed6248cdc590d90d`  
		Last Modified: Fri, 16 Jan 2026 23:52:18 GMT  
		Size: 8.7 MB (8727805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc8803c62dedca3eba8e2bbc93139114000563670c502f376eff3dd1ba3ad7c`  
		Last Modified: Fri, 16 Jan 2026 23:52:07 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b05a6d6da47207ee6b32dc0dd1228336ebeb1fb63681ef7c8ea95c9146d94a`  
		Last Modified: Fri, 16 Jan 2026 23:52:15 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f5facf2c821bedf6c462da2806cef481e059ff822655498e6fb0329d0572af`  
		Last Modified: Fri, 16 Jan 2026 23:52:17 GMT  
		Size: 27.0 MB (27025231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02553b424ab6829f37902cafb1c1dfad9a6b62ed9c76045fabe8c1d65cbc22b0`  
		Last Modified: Fri, 16 Jan 2026 23:52:15 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add6aff7787a0de7594d4ba9db89070f10486645ffcf0767132f551568f47de4`  
		Last Modified: Fri, 16 Jan 2026 23:52:15 GMT  
		Size: 1.8 KB (1765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2719bc14be3339081d951319bb0b5c64146473cfa8b28c44df42abadda2e0f`  
		Last Modified: Fri, 16 Jan 2026 23:52:15 GMT  
		Size: 193.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:65fdcdb38c0fb819f8e29c68a89b8e46207caf191b2f940b699d2598a16b9e0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1172047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39d82d1511f9fce2a5f4d1ed7ba95b976f520cd2d3487e6e4dad8d783b241290`

```dockerfile
```

-	Layers:
	-	`sha256:523f6774eb621adee43478e59edb712952734f3052ad107d6561f88e7757a033`  
		Last Modified: Sat, 17 Jan 2026 02:17:58 GMT  
		Size: 1.1 MB (1120179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d29f50ff93bf46bb6c0ebaecca3005dd88793f82d3a6ba172e5f68c4f950c40`  
		Last Modified: Fri, 16 Jan 2026 23:52:07 GMT  
		Size: 51.9 KB (51868 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.4-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:2bb588cf09b2c8d3e7a0c0e1358995ca5bbda5c5668c03d5a23f5f0863b5403c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104839582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06dcfda0465425a1081f3cdd4e3e4fb412e08262087ffa013989ec06f965e841`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 23:18:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 16 Jan 2026 23:18:04 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 16 Jan 2026 23:18:04 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 16 Jan 2026 23:18:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 Jan 2026 23:18:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 Jan 2026 23:18:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:18:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:18:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 Jan 2026 23:18:05 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 16 Jan 2026 23:18:05 GMT
ENV PHP_VERSION=8.4.17
# Fri, 16 Jan 2026 23:18:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.17.tar.xz.asc
# Fri, 16 Jan 2026 23:18:05 GMT
ENV PHP_SHA256=28b234e347286158cae921d61283eb1169d89bc9d2e5f5976567260ff38b0bfa
# Fri, 16 Jan 2026 23:22:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 16 Jan 2026 23:22:23 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:25:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 Jan 2026 23:25:46 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:25:46 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 Jan 2026 23:25:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 Jan 2026 23:25:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Jan 2026 23:25:47 GMT
WORKDIR /var/www/html
# Fri, 16 Jan 2026 23:25:47 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 16 Jan 2026 23:25:47 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Jan 2026 23:25:47 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 16 Jan 2026 23:25:47 GMT
CMD ["php-fpm"]
# Fri, 16 Jan 2026 23:52:41 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Fri, 16 Jan 2026 23:53:40 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 16 Jan 2026 23:53:41 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Fri, 16 Jan 2026 23:53:41 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Fri, 16 Jan 2026 23:53:42 GMT
RUN set -eux; 	version='6.9'; 	sha1='256dda5bb6a43aecd806b7a62528f442c06e6c25'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Fri, 16 Jan 2026 23:53:42 GMT
VOLUME [/var/www/html]
# Fri, 16 Jan 2026 23:53:42 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Fri, 16 Jan 2026 23:53:42 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:53:43 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Fri, 16 Jan 2026 23:53:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:53:43 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4304af56106d7a6c00093d06ad09d46249b8ca9647d02669c4ae749ac69605f`  
		Last Modified: Fri, 16 Jan 2026 23:21:58 GMT  
		Size: 3.6 MB (3601380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4cce304cda318d9bdef4d3028991776ecc74bda2ff352fc5e4b83203235d98`  
		Last Modified: Fri, 16 Jan 2026 23:21:47 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9092a701e099fc9f57cf713ddfca1afd4e1dc10efbf2df4d2454add1870880`  
		Last Modified: Fri, 16 Jan 2026 23:21:47 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d26311efb92b99154e6c03c6a5991e35dd64e40b038698f2e3fbf9f7c32197c`  
		Last Modified: Fri, 16 Jan 2026 23:25:54 GMT  
		Size: 13.7 MB (13694311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1df8d802f118e71a862b31a1b96b4518910b2795c47093e8f29bc9fbb9a3f3`  
		Last Modified: Fri, 16 Jan 2026 23:26:00 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d735da5b51aa9db21dd253ef1ab88c2fc188a17de09a1a46b15abffd878d14bd`  
		Last Modified: Fri, 16 Jan 2026 23:26:05 GMT  
		Size: 14.7 MB (14689114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f4d36cf0a39b4bb46a624843a9404b85f3824f34ee4b71d35ab2148929ada6c`  
		Last Modified: Fri, 16 Jan 2026 23:26:01 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69adf60ca19382d7386b405ee5843e61d6bb052853807d940a9bcfcda8a66b2`  
		Last Modified: Fri, 16 Jan 2026 23:25:55 GMT  
		Size: 23.4 KB (23354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82796106de4d4fc0f72df109115ca7fdfc9451577db66e780dc00b3e61b74604`  
		Last Modified: Fri, 16 Jan 2026 23:25:55 GMT  
		Size: 23.4 KB (23367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368c1411cddf95d6c0303e8af40424fc331382f0d095f42beb2eafe2bf92e4d8`  
		Last Modified: Fri, 16 Jan 2026 23:25:56 GMT  
		Size: 9.3 KB (9264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f02c9954dac765204a5171cc96cfaac36dcf89d13a0bfc65aa20cc4b39ac32`  
		Last Modified: Fri, 16 Jan 2026 23:54:01 GMT  
		Size: 32.5 MB (32454130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca466a3c36ec22b6ba34d045173a044cb78e3477761ca48426696366d4f5392d`  
		Last Modified: Fri, 16 Jan 2026 23:53:53 GMT  
		Size: 9.1 MB (9114490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07e078d34f15126ceec487f2b3462526ec4474d5c3ea3ead7d8f191da615c2b`  
		Last Modified: Fri, 16 Jan 2026 23:53:58 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3728eb3e03c30dba1292a2e2f537f15ed18e0e42a88c34f3a83511c12a309ea7`  
		Last Modified: Fri, 16 Jan 2026 23:53:52 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa9aff6255103f5e0016ee8103a9eeb7f599eb6137ec44316bd82ebb7a3cf35`  
		Last Modified: Fri, 16 Jan 2026 23:53:54 GMT  
		Size: 27.0 MB (27025220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5eb134ccabaae1d61e81b6792827ef3e012b14ec59b1e7422a94bc107be667`  
		Last Modified: Fri, 16 Jan 2026 23:53:58 GMT  
		Size: 2.4 KB (2432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a2f7acac987c443262c40b168c9e76f6f139e2d5d83dc107c54ab820b7c1a2`  
		Last Modified: Fri, 16 Jan 2026 23:53:58 GMT  
		Size: 1.8 KB (1761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c0bf29afddbddd384225fef9794901d4fb0fa89340e3838afcc8d39b4bda33`  
		Last Modified: Fri, 16 Jan 2026 23:53:58 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:5dd9968712d19ad91dc94a49f97065d4912f6780a07d4927e2890af8f9c97398
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1172101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade6a448d8d29faa6b9adde8d045ad9db34fa57429aa4afe4a04d0f797476519`

```dockerfile
```

-	Layers:
	-	`sha256:1dac8237a4fe8c86d7480817af6802f235631233e616e1f41bfb76cd00b03cfc`  
		Last Modified: Sat, 17 Jan 2026 02:18:03 GMT  
		Size: 1.1 MB (1120199 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a4840b03b173741a05c2374e463e4e0cb0aa49cf433045abf92efc3743da4e0`  
		Last Modified: Fri, 16 Jan 2026 23:53:52 GMT  
		Size: 51.9 KB (51902 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.4-fpm-alpine` - linux; 386

```console
$ docker pull wordpress@sha256:80173373ce1bcd83d3196047801b9c5fcfd48b967b89dc5134d8fa6f2c76b6af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105143294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca0fa3d6ea3787d86ccf55ee32fff7d59d3d12f9e6ab5a84f4f4b6ac189e3281`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Fri, 16 Jan 2026 23:14:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 16 Jan 2026 23:14:56 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 16 Jan 2026 23:14:56 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 16 Jan 2026 23:14:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 Jan 2026 23:14:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 Jan 2026 23:14:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:14:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 Jan 2026 23:14:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 Jan 2026 23:14:56 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 16 Jan 2026 23:14:56 GMT
ENV PHP_VERSION=8.4.17
# Fri, 16 Jan 2026 23:14:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.17.tar.xz.asc
# Fri, 16 Jan 2026 23:14:56 GMT
ENV PHP_SHA256=28b234e347286158cae921d61283eb1169d89bc9d2e5f5976567260ff38b0bfa
# Fri, 16 Jan 2026 23:15:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 16 Jan 2026 23:15:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:18:03 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 Jan 2026 23:18:03 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:18:03 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 Jan 2026 23:18:04 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 Jan 2026 23:18:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Jan 2026 23:18:04 GMT
WORKDIR /var/www/html
# Fri, 16 Jan 2026 23:18:04 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 16 Jan 2026 23:18:04 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Jan 2026 23:18:04 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 16 Jan 2026 23:18:04 GMT
CMD ["php-fpm"]
# Fri, 16 Jan 2026 23:30:06 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Fri, 16 Jan 2026 23:31:00 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Fri, 16 Jan 2026 23:31:00 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Fri, 16 Jan 2026 23:31:00 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Fri, 16 Jan 2026 23:31:02 GMT
RUN set -eux; 	version='6.9'; 	sha1='256dda5bb6a43aecd806b7a62528f442c06e6c25'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Fri, 16 Jan 2026 23:31:02 GMT
VOLUME [/var/www/html]
# Fri, 16 Jan 2026 23:31:02 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Fri, 16 Jan 2026 23:31:02 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 23:31:02 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Fri, 16 Jan 2026 23:31:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Jan 2026 23:31:02 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:38 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5b022fa2a8fc7d09b21584cc298a66e536b9a9c66361455dd0446ef5cf4cf3`  
		Last Modified: Fri, 16 Jan 2026 23:29:57 GMT  
		Size: 3.6 MB (3629014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e652f14019bdc441445cc7b9191585528043b5975cb256454a2424fedd2ea1f1`  
		Last Modified: Fri, 16 Jan 2026 23:18:11 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9856489f2fec2375020c4a0a3890895ff742394984c30657d71a2944b3addfb0`  
		Last Modified: Fri, 16 Jan 2026 23:29:56 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e351c48b6685e836d1e2737f340f3bc2c003721d9f574849bd3a2d4628812d20`  
		Last Modified: Fri, 16 Jan 2026 23:18:11 GMT  
		Size: 13.7 MB (13694297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5153f887dca35be21236be74ec2b19babfd3232542b273004bd7fb706995d278`  
		Last Modified: Fri, 16 Jan 2026 23:29:55 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5ca9721fd18abd8e6be3ad7afac60b01f6cc5e59404b933e9d8271cb0dcdf2`  
		Last Modified: Fri, 16 Jan 2026 23:18:27 GMT  
		Size: 15.5 MB (15494582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aee412d0569a2cd45d4e8145c66e1ef1969f108db96740ecbf65f46c9db01f7`  
		Last Modified: Fri, 16 Jan 2026 23:18:26 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4139b30f564f3d8464e945d70beac3cf89c0aff26c63806d031fb046c96fbdca`  
		Last Modified: Fri, 16 Jan 2026 23:18:27 GMT  
		Size: 23.5 KB (23520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33b474c1f49ca5b2f5fdd0afc660359c3e9924a510f870f96d02a8c18b56c1d8`  
		Last Modified: Fri, 16 Jan 2026 23:29:55 GMT  
		Size: 23.5 KB (23537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f1d644be4b138f0013c0c4ff6387043c1564bcfaba68eb64628e44229eaf885`  
		Last Modified: Fri, 16 Jan 2026 23:18:13 GMT  
		Size: 9.3 KB (9267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ab69a623969c2d51db25009ec4285367f8e76993844d94869cb3dace6443f3`  
		Last Modified: Fri, 16 Jan 2026 23:31:22 GMT  
		Size: 33.3 MB (33293450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664a45df81a2c9f4c6c5054acff6457ad3578adfd4eb9f76e31b7e68a7669b08`  
		Last Modified: Fri, 16 Jan 2026 23:31:20 GMT  
		Size: 8.3 MB (8255080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a536e98b59c73296c1921086575a1ca25d53c30d0af1d05bae6cbd274dc7ec8a`  
		Last Modified: Fri, 16 Jan 2026 23:31:12 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8ca98c2f3bd91f310f313e0b2ab3c6d8f12726ce47b64fce06cddc0ce6b916`  
		Last Modified: Fri, 16 Jan 2026 23:31:20 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a4f481e4053bf0a4fff00121e7fae09c30e74155b968aa2bb20f9a205b8610e`  
		Last Modified: Fri, 16 Jan 2026 23:31:25 GMT  
		Size: 27.0 MB (27025234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ef4e322de1ae8a3772da27f5c7247bfea6852be39e41025be1ed9be18a1037`  
		Last Modified: Fri, 16 Jan 2026 23:31:19 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922df704fde5d894fb51d3b3cfe685522f982caf88f7ca00a9723828628d7a04`  
		Last Modified: Fri, 16 Jan 2026 23:31:19 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db3df734ca148e202567fe50e259b3122e1d83838bc63f1231a4efc7939a891`  
		Last Modified: Fri, 16 Jan 2026 23:31:14 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:de67aa4348d1fe4323c9d97835fefab2cce0fbe13c6b398f26be7e4012696c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1173693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f882454b2eaf45f66360d887472f3e36787d3e89fee0679cd342de05b371535a`

```dockerfile
```

-	Layers:
	-	`sha256:000c8daf75fcbf21df92a6b4c8a3778d0c52d8e0282929cdf7236640bea9c327`  
		Last Modified: Fri, 16 Jan 2026 23:31:12 GMT  
		Size: 1.1 MB (1122012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0f53076d30ff225a30c123f458d9609ba5393fbe0befabd08e368a9655386e9`  
		Last Modified: Sat, 17 Jan 2026 02:18:11 GMT  
		Size: 51.7 KB (51681 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.4-fpm-alpine` - linux; ppc64le

```console
$ docker pull wordpress@sha256:c0da441cfcfdf0fb23311bee523ba40acc19f606d34a1b854c6cf083525a1f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.4 MB (107379663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecf88ba42fb23bec5e909beb17c6c0fa6ad9cedcda3af7a8e67c7c9aa71210c3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Sat, 03 Jan 2026 02:13:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 03 Jan 2026 02:13:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 03 Jan 2026 02:13:26 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 03 Jan 2026 02:13:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 03 Jan 2026 02:13:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 03 Jan 2026 02:13:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 03 Jan 2026 02:13:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 03 Jan 2026 02:13:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 03 Jan 2026 02:13:27 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Sat, 03 Jan 2026 02:13:27 GMT
ENV PHP_VERSION=8.4.17
# Sat, 03 Jan 2026 02:13:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.17.tar.xz.asc
# Sat, 03 Jan 2026 02:13:27 GMT
ENV PHP_SHA256=28b234e347286158cae921d61283eb1169d89bc9d2e5f5976567260ff38b0bfa
# Fri, 16 Jan 2026 00:12:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 16 Jan 2026 00:12:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 00:16:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 Jan 2026 00:16:59 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 Jan 2026 00:17:01 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 Jan 2026 00:17:02 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 Jan 2026 00:17:02 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 Jan 2026 00:17:03 GMT
WORKDIR /var/www/html
# Sat, 17 Jan 2026 00:05:41 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 17 Jan 2026 00:05:41 GMT
STOPSIGNAL SIGQUIT
# Sat, 17 Jan 2026 00:05:41 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 17 Jan 2026 00:05:41 GMT
CMD ["php-fpm"]
# Sat, 17 Jan 2026 02:51:26 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Sat, 17 Jan 2026 02:53:31 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Sat, 17 Jan 2026 02:53:32 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Sat, 17 Jan 2026 02:53:33 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Sat, 17 Jan 2026 02:53:39 GMT
RUN set -eux; 	version='6.9'; 	sha1='256dda5bb6a43aecd806b7a62528f442c06e6c25'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Sat, 17 Jan 2026 02:53:40 GMT
VOLUME [/var/www/html]
# Sat, 17 Jan 2026 02:53:40 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Sat, 17 Jan 2026 02:53:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 17 Jan 2026 02:53:42 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Sat, 17 Jan 2026 02:53:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 17 Jan 2026 02:53:42 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:42 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e772e0a90d4aa4f209aab27b75a49043c6df83f144ec29ba8e6c8e964a8a165a`  
		Last Modified: Sat, 03 Jan 2026 02:17:36 GMT  
		Size: 3.8 MB (3768859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edb9c8b89ecca8688bdf852690f34dbf7da2dc90d2e06d7221c85ff1070c08b`  
		Last Modified: Sat, 03 Jan 2026 02:17:36 GMT  
		Size: 928.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ce8460d16487c23dd44b0afef57a49c4aeca53309e968b330dc8c9044d5e51`  
		Last Modified: Sat, 03 Jan 2026 02:17:28 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635f2b3f69e5b5cc8308fa39069e1dc5b69d344006bb70780e36be0078b758f1`  
		Last Modified: Fri, 16 Jan 2026 00:16:21 GMT  
		Size: 13.7 MB (13694341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57646fbf28999a726342d7622036b3cfe4859a4aacc500fbceae9cb0b7edda7`  
		Last Modified: Fri, 16 Jan 2026 00:16:12 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389777609f0a5a520d93f10e09375ccacca524e1fbd38635f111505e33e2c60a`  
		Last Modified: Fri, 16 Jan 2026 00:17:31 GMT  
		Size: 15.7 MB (15723714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de4975b5bccd2e83e8bdd87a443d484539ad91a8125ee74b753ba5ce81befe1a`  
		Last Modified: Fri, 16 Jan 2026 00:17:29 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7054eb905ed82e496fabf24c0fe796a0f9b58ab9d29f4cc62a8fe4ee45fd3714`  
		Last Modified: Fri, 16 Jan 2026 00:17:29 GMT  
		Size: 23.4 KB (23351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf8749d03c4b8da0fb97f3b232f5c44117c1c4b8401c2ffc6591942474ad9a4`  
		Last Modified: Fri, 16 Jan 2026 00:17:29 GMT  
		Size: 23.4 KB (23372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:126d55071f3e42cdb59d4191e7626842d232a1f1945dd3d33b718705079f2bf4`  
		Last Modified: Sat, 17 Jan 2026 00:06:05 GMT  
		Size: 9.3 KB (9272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60342f4c26558b3e135e7e46a6a6571baaa66c9a1dc79c1c723fb0ed8bf6bdb6`  
		Last Modified: Sat, 17 Jan 2026 02:54:36 GMT  
		Size: 34.1 MB (34057144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05a51c3e27b9b21208637f7da6e311ff0b651104835c412b04c7677629f4837`  
		Last Modified: Sat, 17 Jan 2026 02:54:19 GMT  
		Size: 9.2 MB (9217403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3581a339dcad933a1e41c315e4e57943749b0ed12b4a0d78ef60f762eab6980f`  
		Last Modified: Sat, 17 Jan 2026 02:54:31 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2c58bc67829de5a6dde761f96b700342c521098d55cfc02d4f30d466e0ed03`  
		Last Modified: Sat, 17 Jan 2026 02:54:31 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57d98c017fa24c20fbe8d7f6219a8e6796a51f5ddffbb8deb3df16d9296b954`  
		Last Modified: Sat, 17 Jan 2026 02:54:35 GMT  
		Size: 27.0 MB (27025220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97fe7b6180fe692bbb560a9d6a851a634328ee73ad5589283ade62aa86664d7`  
		Last Modified: Sat, 17 Jan 2026 02:54:20 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b481dafaa3bbb0268c15257b6574b0668e0f5073de98908c91d547167cfdf744`  
		Last Modified: Sat, 17 Jan 2026 02:54:32 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2360a196b23b3908b3aef10c6a702e27c2cf2dda0ff87ebbdce84d5b1c498113`  
		Last Modified: Sat, 17 Jan 2026 02:54:21 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:5855d30f2c8031a0a2598049df9c629191e1e3221e5a1065d5cd9704d31c65c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1171952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956c16eb8babe74372094ce20d63a6831530af9276edc847a5fe99c8576d3626`

```dockerfile
```

-	Layers:
	-	`sha256:7b653fc9073d8241a8a940b4d6c9f68ea11378f5d521884240b76e90d1d424ed`  
		Last Modified: Sat, 17 Jan 2026 02:54:18 GMT  
		Size: 1.1 MB (1120176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b625e1aa14109363a501e1cf687b2769d8301cb8c2feea3bf19daba051ac3108`  
		Last Modified: Sat, 17 Jan 2026 05:14:35 GMT  
		Size: 51.8 KB (51776 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.4-fpm-alpine` - linux; riscv64

```console
$ docker pull wordpress@sha256:9174c37b2f3f446488f0fe0d3d6e90a73b649cdd6eb4e4b0fd52923930865103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.5 MB (102487842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b0721da552405e55b310bce0680b62e4d1c64e708db63a1eb9ed103e5aa0e89`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 07:08:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Dec 2025 07:08:04 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Dec 2025 07:08:05 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Dec 2025 07:08:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Dec 2025 07:08:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Dec 2025 07:08:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 07:08:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 07:08:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Dec 2025 07:08:05 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 18 Dec 2025 07:08:05 GMT
ENV PHP_VERSION=8.4.17
# Thu, 18 Dec 2025 07:08:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.17.tar.xz.asc
# Thu, 18 Dec 2025 07:08:05 GMT
ENV PHP_SHA256=28b234e347286158cae921d61283eb1169d89bc9d2e5f5976567260ff38b0bfa
# Sun, 18 Jan 2026 04:44:00 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Sun, 18 Jan 2026 04:44:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sun, 18 Jan 2026 06:39:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sun, 18 Jan 2026 06:39:06 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sun, 18 Jan 2026 06:39:11 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sun, 18 Jan 2026 06:39:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sun, 18 Jan 2026 06:39:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sun, 18 Jan 2026 06:39:15 GMT
WORKDIR /var/www/html
# Sun, 18 Jan 2026 06:39:16 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sun, 18 Jan 2026 06:39:16 GMT
STOPSIGNAL SIGQUIT
# Sun, 18 Jan 2026 06:39:16 GMT
EXPOSE map[9000/tcp:{}]
# Sun, 18 Jan 2026 06:39:16 GMT
CMD ["php-fpm"]
# Mon, 19 Jan 2026 14:41:27 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Mon, 19 Jan 2026 14:57:17 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 19 Jan 2026 14:57:17 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Mon, 19 Jan 2026 14:57:18 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Mon, 19 Jan 2026 14:57:27 GMT
RUN set -eux; 	version='6.9'; 	sha1='256dda5bb6a43aecd806b7a62528f442c06e6c25'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 19 Jan 2026 14:57:28 GMT
VOLUME [/var/www/html]
# Mon, 19 Jan 2026 14:57:28 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 19 Jan 2026 14:57:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 19 Jan 2026 14:57:28 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Mon, 19 Jan 2026 14:57:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 19 Jan 2026 14:57:28 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:28 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b530e2aa9b2657de1d52e221d1841cf1970adc8a19d28df2a836438ca82d59`  
		Last Modified: Thu, 18 Dec 2025 08:10:14 GMT  
		Size: 3.7 MB (3740208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f161979011df79f0935c37e8044239316a16a481a51548ff3d1420fa2b71d7b`  
		Last Modified: Thu, 18 Dec 2025 08:10:14 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f8e47306a76921db05f6fca6bbff42051f7da8662b35dfc0b3cc197f7cc2ee`  
		Last Modified: Thu, 18 Dec 2025 08:10:14 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbf0b22e7f711d7a73eeeca6cf324b7c89075066b43de770508d227e2a46509`  
		Last Modified: Sun, 18 Jan 2026 05:41:51 GMT  
		Size: 13.7 MB (13694324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617b1a5f09a97344003260afa6b2f030a26eaf82ef2283415da091a63a24ea1f`  
		Last Modified: Sun, 18 Jan 2026 05:41:47 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2c684c606b9c6a9f44b4e65b71c85bab2552d54b3584d482bf1f49ed69703f2`  
		Last Modified: Sun, 18 Jan 2026 06:40:21 GMT  
		Size: 14.6 MB (14642619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a118ff07a8a3877927b91877b3e0e5d361726488624c662537c39defaf389a67`  
		Last Modified: Sun, 18 Jan 2026 06:40:21 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c8cf7cbf7e2bf86787c6814295352e35086b5c265515607d5a485b482e15f8c`  
		Last Modified: Sun, 18 Jan 2026 06:40:21 GMT  
		Size: 23.4 KB (23376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc46c23eb42039a98b9e4949f2bf9d0c1f1b488f58aa45faa5701806c1b6124`  
		Last Modified: Sun, 18 Jan 2026 06:40:07 GMT  
		Size: 23.4 KB (23393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc2a8d0b688698ac7c885980ef05e371bbde142ec629707bc1eb7544e75349a`  
		Last Modified: Sun, 18 Jan 2026 06:40:20 GMT  
		Size: 9.3 KB (9275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:114187294e5dc0f52484e44145f666ef12424fb1fe63c8dd90413881fb367f71`  
		Last Modified: Mon, 19 Jan 2026 14:59:29 GMT  
		Size: 32.6 MB (32641797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3637c8a7cc45d96cf24c1c24a945a302db6bda39f5b2355281a4027a17e81d30`  
		Last Modified: Mon, 19 Jan 2026 14:59:54 GMT  
		Size: 7.1 MB (7094430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9307061dc86c67f2e4abb27c67bddd0e110eb2244a5e6f7ed6aec88a6091dff4`  
		Last Modified: Mon, 19 Jan 2026 14:59:19 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d1dfa74d7e94438e37b6a80d7ff4a26f00c06200ebda40ee44e0c69dcb0a5e`  
		Last Modified: Mon, 19 Jan 2026 22:17:10 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0a267eba632dc7631220fb0d62e8cbaf7efa2fc64c563e235367ccb587d80f`  
		Last Modified: Mon, 19 Jan 2026 14:59:59 GMT  
		Size: 27.0 MB (27025237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71abcacc9b004157ffa87b4899b0b5d92335f1406a54af22df7d7d0d1c7a27ed`  
		Last Modified: Mon, 19 Jan 2026 14:59:22 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ba1137e140d0e47c1da3a89739cc7095b5c42f4c0e9fa6328b552d492c3940`  
		Last Modified: Mon, 19 Jan 2026 14:59:23 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:379e1c3de8dc3017bcc5765a73748d88c63b8db924ab4ebd4046e57bc782eeb0`  
		Last Modified: Mon, 19 Jan 2026 22:17:11 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:cf8bd71fbf77376292e10166ea694aacc85640d6e6c56dea3b08a7722b6e92a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1171949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:894666c9e04cabd35ce8da1ee0a944cf63f842ee02c70e84926c4047e81ef3a6`

```dockerfile
```

-	Layers:
	-	`sha256:c37eea4f3c4132f792d6389831406ea711b45c8a58389660fa50498bfcaf2855`  
		Last Modified: Mon, 19 Jan 2026 17:13:19 GMT  
		Size: 1.1 MB (1120172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c8f90b5dbb018448a09c236040e8605be4867b8364a81a56fa911711965756f`  
		Last Modified: Mon, 19 Jan 2026 14:59:19 GMT  
		Size: 51.8 KB (51777 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:6-php8.4-fpm-alpine` - linux; s390x

```console
$ docker pull wordpress@sha256:2652528a38d5b71b29192eb7633eaad9c0d7db43e1daef040652ea18f9aea976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **106.1 MB (106106149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdbcc11b703180041c5fc80dd003a8e9e2d1a2dcd371ac933fba44d891c57513`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 18 Dec 2025 00:30:49 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 18 Dec 2025 00:30:49 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 18 Dec 2025 00:30:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Dec 2025 00:30:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Dec 2025 00:30:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 00:30:50 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Dec 2025 00:30:50 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Dec 2025 00:30:50 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 18 Dec 2025 00:30:50 GMT
ENV PHP_VERSION=8.4.17
# Thu, 18 Dec 2025 00:30:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.17.tar.xz.asc
# Thu, 18 Dec 2025 00:30:50 GMT
ENV PHP_SHA256=28b234e347286158cae921d61283eb1169d89bc9d2e5f5976567260ff38b0bfa
# Thu, 15 Jan 2026 22:38:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 15 Jan 2026 22:38:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:43:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 15 Jan 2026 22:43:17 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 15 Jan 2026 22:43:18 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 15 Jan 2026 22:43:18 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 15 Jan 2026 22:43:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 15 Jan 2026 22:43:18 GMT
WORKDIR /var/www/html
# Fri, 16 Jan 2026 23:32:07 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen adddress for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 16 Jan 2026 23:32:07 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 Jan 2026 23:32:07 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 16 Jan 2026 23:32:07 GMT
CMD ["php-fpm"]
# Fri, 16 Jan 2026 23:58:53 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Sat, 17 Jan 2026 00:00:05 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Sat, 17 Jan 2026 00:00:05 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Sat, 17 Jan 2026 00:00:05 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Sat, 17 Jan 2026 00:00:07 GMT
RUN set -eux; 	version='6.9'; 	sha1='256dda5bb6a43aecd806b7a62528f442c06e6c25'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Sat, 17 Jan 2026 00:00:07 GMT
VOLUME [/var/www/html]
# Sat, 17 Jan 2026 00:00:07 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Sat, 17 Jan 2026 00:00:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 17 Jan 2026 00:00:07 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Sat, 17 Jan 2026 00:00:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 17 Jan 2026 00:00:07 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:18 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9af672712b2dab3c8a68ddbd40990098668c349a31bf4fe54360519012d2e9`  
		Last Modified: Thu, 18 Dec 2025 00:34:55 GMT  
		Size: 3.8 MB (3794529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e82f0b184abfa92d79d92b03514acd8b9f92c2ca083f9fa2e62587fde8871a2`  
		Last Modified: Thu, 18 Dec 2025 00:35:02 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b827f069b40835efda3a88ba34853291bec4baedd59564b9d33abc39667950f2`  
		Last Modified: Thu, 18 Dec 2025 00:34:55 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9915ee6e7bc986c6bc00ae2c7377c4d1c1da6dbf61e114f2c04afb7dc64a0bce`  
		Last Modified: Thu, 15 Jan 2026 22:42:44 GMT  
		Size: 13.7 MB (13694323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f9ccec429d4e1a40b769a08c6f8d17f5bff7a5d62fd841f4289153c436a1ec`  
		Last Modified: Thu, 15 Jan 2026 22:42:43 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a407f2c328e5a18805d337d681f17b642de3d8c9212011c3ff2429a6a60c0bb4`  
		Last Modified: Thu, 15 Jan 2026 22:43:30 GMT  
		Size: 14.9 MB (14937420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c362a94da127124552fae11ffa50cb8d55fad52ab275beae95b230e31b2f8ac8`  
		Last Modified: Thu, 15 Jan 2026 22:43:37 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f1f65cd6a194f15031fda4d062aee532f193b26a35b25d2497bc4303580e62`  
		Last Modified: Thu, 15 Jan 2026 22:43:29 GMT  
		Size: 23.3 KB (23345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f7c47560b39f708a2870f22295445625d58b38c19d51f4f3393fc135d2863d`  
		Last Modified: Thu, 15 Jan 2026 22:43:37 GMT  
		Size: 23.4 KB (23358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866bb04931b21adfc2ed246065cb490322210d34b2e27d622f4617ac0b9c24ef`  
		Last Modified: Fri, 16 Jan 2026 23:32:21 GMT  
		Size: 9.3 KB (9272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1428297c04eb88b79b03e8fe8534ad8fc2ce55f6ac89623e528efc6ee28f62c0`  
		Last Modified: Sat, 17 Jan 2026 00:00:47 GMT  
		Size: 34.0 MB (33987246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71c32a89ddfb2fc70fa71db3f68868afc0fc542089ef0d6ab00c239467792c2d`  
		Last Modified: Sat, 17 Jan 2026 00:00:44 GMT  
		Size: 8.9 MB (8877879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa1c572877012187f06e77e227b6f71289584de1dc66820f2d4562c023609d9`  
		Last Modified: Sat, 17 Jan 2026 00:00:43 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50dc0999dad9adff020e420692d855b5a8a6dd17e62b94973af7f4bfba06d03`  
		Last Modified: Sat, 17 Jan 2026 00:00:53 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6b34b37cccad0904fc19d9c6a615198a7ab17923fe6276318a4ea582b8cbba`  
		Last Modified: Sat, 17 Jan 2026 00:00:29 GMT  
		Size: 27.0 MB (27025237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3b69595779db7bd57595c98f739aee8fad191f903ad7f2da1e2ae2e902460c`  
		Last Modified: Sat, 17 Jan 2026 00:00:43 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ede58d2334e95ee8ea9d5f3a1384889f062f058ddd6873ce635dfa4fa6d6f0`  
		Last Modified: Sat, 17 Jan 2026 00:00:43 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2b92baefbd5eafbcef487052ff1a41c8a911fe1e538847970a5ccac25781f3`  
		Last Modified: Sat, 17 Jan 2026 00:00:30 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:6-php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:4820b9c2d3fe6576f07ce46f419fd28ca7e3f19ccd35298a4bd4b01ce8603e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1171865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45393201903377efbb276175e77c1f16de4152745343e2f4692ae3830391c17`

```dockerfile
```

-	Layers:
	-	`sha256:8dc9c399000c9f4dffde22713450527311a30f2c23983c549faf08643ad0bd89`  
		Last Modified: Sat, 17 Jan 2026 02:18:20 GMT  
		Size: 1.1 MB (1120142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f93fb806e000ee5c6bdf95aea66064e4d0bdab37ba3e07b51264c44bde89b9b3`  
		Last Modified: Sat, 17 Jan 2026 00:00:25 GMT  
		Size: 51.7 KB (51723 bytes)  
		MIME: application/vnd.in-toto+json
