## `wordpress:beta-php8.4-fpm-alpine`

```console
$ docker pull wordpress@sha256:db1b1c567a5648e699966ad03e9911ba872a413fbf92048a2e296db0f24effa6
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

### `wordpress:beta-php8.4-fpm-alpine` - linux; amd64

```console
$ docker pull wordpress@sha256:d1e83519f66de7478784e1d41921614ff6ce176f629eb5bec126890970875af7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.2 MB (108157585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:812e15189ecac88af62239e728de81a5aa4e0d1018108f03ac1fcf619441fa32`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 12 Mar 2026 23:31:26 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Mar 2026 23:31:26 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Mar 2026 23:31:26 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Mar 2026 23:31:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Mar 2026 23:31:26 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Mar 2026 23:31:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:31:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:31:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Mar 2026 23:31:26 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Mar 2026 23:31:26 GMT
ENV PHP_VERSION=8.4.19
# Thu, 12 Mar 2026 23:31:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.19.tar.xz.asc
# Thu, 12 Mar 2026 23:31:26 GMT
ENV PHP_SHA256=11f7164ab26d356c31f94d3d69cc0e0707d5d2d6494a221aaeae307c08eaaa1c
# Thu, 12 Mar 2026 23:35:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Mar 2026 23:35:10 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:38:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Mar 2026 23:38:18 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:38:19 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 12 Mar 2026 23:38:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Mar 2026 23:38:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Mar 2026 23:38:19 GMT
WORKDIR /var/www/html
# Thu, 12 Mar 2026 23:38:19 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 12 Mar 2026 23:38:19 GMT
STOPSIGNAL SIGQUIT
# Thu, 12 Mar 2026 23:38:19 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 12 Mar 2026 23:38:19 GMT
CMD ["php-fpm"]
# Mon, 23 Mar 2026 17:56:49 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Mon, 23 Mar 2026 17:57:34 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 23 Mar 2026 17:57:34 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Mon, 23 Mar 2026 17:57:34 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Mon, 23 Mar 2026 17:57:36 GMT
RUN set -eux; 	version='7.0-beta6'; 	sha1='40c821fe5ece3fb0feca1fff0ec6fa6a5e066f7d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 23 Mar 2026 17:57:36 GMT
VOLUME [/var/www/html]
# Mon, 23 Mar 2026 17:57:36 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 23 Mar 2026 17:57:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 17:57:36 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Mon, 23 Mar 2026 17:57:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 17:57:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7384bbca651dd1490918b416f82649cefb7274005d5343821078b786e492edbf`  
		Last Modified: Thu, 12 Mar 2026 23:34:59 GMT  
		Size: 3.6 MB (3591767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fadf7ab90915f698316421085b5bc8691f957acf4eadac546575a00ff14fb55b`  
		Last Modified: Thu, 12 Mar 2026 23:34:58 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78eb83af8f22e219516649c8ba76c2b66e7614e8adf2c268b2f1d6e6d657e20`  
		Last Modified: Thu, 12 Mar 2026 23:34:58 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15bc271485aed1cbf486885b168e82a7f05f611597af3cb2a03a1d6ad2bb47ce`  
		Last Modified: Thu, 12 Mar 2026 23:38:27 GMT  
		Size: 13.7 MB (13708137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a777cf0ebaf0eb666ebe2d384083991331dc4602f72ffce8852813fb0313b0`  
		Last Modified: Thu, 12 Mar 2026 23:38:26 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a02f88c8f9a0810fc0edfb2459d8988c63cc278f9454ee1fbd7727354bd2af6`  
		Last Modified: Thu, 12 Mar 2026 23:38:27 GMT  
		Size: 15.3 MB (15254144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c81c5b03d16c0724e354b5890f2b2fd5795f07b224c94383fd589f3d7dc01d`  
		Last Modified: Thu, 12 Mar 2026 23:38:26 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9237f720b82e321dc52d1682c013d6052761f7900359c66cc4d84fdbc9c4e34f`  
		Last Modified: Thu, 12 Mar 2026 23:38:27 GMT  
		Size: 23.5 KB (23528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f49e2be49c8a3a9db40dfff06882b63034cdec156819dc826269035d9662c83c`  
		Last Modified: Thu, 12 Mar 2026 23:38:27 GMT  
		Size: 23.5 KB (23539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727707ce8550a457cd8210b0c5d1dd0a1b7db98bb1ced42e49e977f1f7ff619e`  
		Last Modified: Thu, 12 Mar 2026 23:38:28 GMT  
		Size: 9.3 KB (9265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fd74b8ab4d12b4e900aa6d4b4071aa31b803913420a56401143cc611d8d086`  
		Last Modified: Mon, 23 Mar 2026 17:57:47 GMT  
		Size: 32.8 MB (32839373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aae692acfb701391e332c8282941d4652d940226f21e626d107a6a2a29d928a`  
		Last Modified: Mon, 23 Mar 2026 17:57:46 GMT  
		Size: 9.4 MB (9414069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10cc1754d53627b0221bd9e12fc2b3ae800a2b7abdbdeec8718797534e167730`  
		Last Modified: Mon, 23 Mar 2026 17:57:46 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0ea2762191ed6890171feafdfb649a558f7e2344935d7f3ee392f891de70be`  
		Last Modified: Mon, 23 Mar 2026 17:57:46 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc56959b84f3f2b038418a3c44dc53cb159e7e3916fb987ca38380ed950d065`  
		Last Modified: Mon, 23 Mar 2026 17:57:48 GMT  
		Size: 29.4 MB (29422714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a67a076b5cfcfc4da45071420b828511ebeb56333ed10c812bd0d1c4ada1697`  
		Last Modified: Mon, 23 Mar 2026 17:57:47 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04af49fe87ffd286ff75cb7fd5b01478551679d845f254e2bd3f6300a1ea8ef`  
		Last Modified: Mon, 23 Mar 2026 17:57:48 GMT  
		Size: 1.8 KB (1770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee977d4648f6ac9c031f1c2299b253c0b18d12f52d8c67bd440231beccef1a7`  
		Last Modified: Mon, 23 Mar 2026 17:57:48 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:448d686fb6ce39fb814815180f8764f827bf0f9cdc675ff6fe8a867402b8fc27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1173864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d8e2b1b8cdf7c177e9249abfcabd8c628116b4d627266431c616b30892d8ef1`

```dockerfile
```

-	Layers:
	-	`sha256:f38726fd565f4b12a1cf5ebfa508c7fade0b5148ed7fc90c8e6e98d97d310a53`  
		Last Modified: Mon, 23 Mar 2026 17:57:46 GMT  
		Size: 1.1 MB (1122085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fb20b2b3acc7c1ef3fb1cc1a6c2a8d8ff43e42a36fd8437417ece275d858077`  
		Last Modified: Mon, 23 Mar 2026 17:57:46 GMT  
		Size: 51.8 KB (51779 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.4-fpm-alpine` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:1a006c3473cfe4eb0e42bdc73df2647493815fe24f521b8c5c054b6496b9af1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.3 MB (100315113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13f51de8bdbd9cb3e990c65c238b625d5dd0756e1eff74083e0b0bd245a7aab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Thu, 12 Mar 2026 23:28:35 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Mar 2026 23:28:35 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Mar 2026 23:28:35 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Mar 2026 23:28:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Mar 2026 23:28:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Mar 2026 23:28:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:28:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:28:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Mar 2026 23:28:35 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Mar 2026 23:28:35 GMT
ENV PHP_VERSION=8.4.19
# Thu, 12 Mar 2026 23:28:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.19.tar.xz.asc
# Thu, 12 Mar 2026 23:28:35 GMT
ENV PHP_SHA256=11f7164ab26d356c31f94d3d69cc0e0707d5d2d6494a221aaeae307c08eaaa1c
# Thu, 12 Mar 2026 23:28:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Mar 2026 23:28:39 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:31:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Mar 2026 23:31:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:31:39 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 12 Mar 2026 23:31:39 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Mar 2026 23:31:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Mar 2026 23:31:39 GMT
WORKDIR /var/www/html
# Thu, 12 Mar 2026 23:31:39 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 12 Mar 2026 23:31:39 GMT
STOPSIGNAL SIGQUIT
# Thu, 12 Mar 2026 23:31:39 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 12 Mar 2026 23:31:39 GMT
CMD ["php-fpm"]
# Mon, 23 Mar 2026 17:55:05 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Mon, 23 Mar 2026 17:56:24 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 23 Mar 2026 17:56:24 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Mon, 23 Mar 2026 17:56:25 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Mon, 23 Mar 2026 17:56:27 GMT
RUN set -eux; 	version='7.0-beta6'; 	sha1='40c821fe5ece3fb0feca1fff0ec6fa6a5e066f7d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 23 Mar 2026 17:56:27 GMT
VOLUME [/var/www/html]
# Mon, 23 Mar 2026 17:56:27 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 23 Mar 2026 17:56:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 17:56:27 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Mon, 23 Mar 2026 17:56:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 17:56:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ae39c007bd9155128d5562460e359fa8f6f91807ddb9852ec7aef9d3b155384`  
		Last Modified: Thu, 12 Mar 2026 23:31:45 GMT  
		Size: 3.5 MB (3548642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435c87696ddcf0f76adb55b6d3697803d927c55d2ed7cd9f9138786a5f4383f1`  
		Last Modified: Thu, 12 Mar 2026 23:31:44 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2831c4673a02752f9bb664493e7894f1292f11909d8b83fb5da2b742870843ea`  
		Last Modified: Thu, 12 Mar 2026 23:31:44 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11d473e878d7d04307fcaaaa155289c8e26d997ccd2dd9b5054bd1c6a531b02`  
		Last Modified: Thu, 12 Mar 2026 23:31:45 GMT  
		Size: 13.7 MB (13708139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222ed0cc006386fd036a19601456dab548376a7b7d1ceb0a0ae2fa8effefffca`  
		Last Modified: Thu, 12 Mar 2026 23:31:45 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba02c94eeedc364c76ef0fcb0f3f9ea5fa45269ea750af7102d7660be3769ef3`  
		Last Modified: Thu, 12 Mar 2026 23:31:46 GMT  
		Size: 13.7 MB (13725876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a68cfe00535690967540923493636bd3312e8133ed2c7131bb49ab9bd1137f39`  
		Last Modified: Thu, 12 Mar 2026 23:31:46 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34f8feb4ed41aae9d18b29011f01c91411c700e6bce42622994ac09515c8bc1`  
		Last Modified: Thu, 12 Mar 2026 23:31:46 GMT  
		Size: 23.3 KB (23349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cf7916c3e0900e20698d486a204a2a84b148feaa8f8d8676fad7510978dab2`  
		Last Modified: Thu, 12 Mar 2026 23:31:47 GMT  
		Size: 23.4 KB (23365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b2eddaafcbf9c0e4b2cd77c89d5da9ea2f8719caee6dd15cd44d20c518b825`  
		Last Modified: Thu, 12 Mar 2026 23:31:47 GMT  
		Size: 9.3 KB (9265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec62bc1e304c0c5e3588df37ce4e4b1fa4a42a0859f305308553e26d08cb3f95`  
		Last Modified: Mon, 23 Mar 2026 17:56:35 GMT  
		Size: 28.6 MB (28550028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9087c8272192de26c778631197d0c80b5456090edb77c480d87e439ce8b90b86`  
		Last Modified: Mon, 23 Mar 2026 17:56:34 GMT  
		Size: 7.7 MB (7724693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccceba363b1ff179a7e9472e8873dcd7dbea722f2352de57135d1d17dd5e2e3`  
		Last Modified: Mon, 23 Mar 2026 17:56:34 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9eb9d99672d494e34a6b9420c5c920daaa4ad300bfd5b54b20aa6439718bb5`  
		Last Modified: Mon, 23 Mar 2026 17:56:34 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7e9b267a7cc53fc7f1d1a8c8eef951ee93f00086d0c8b925d611a40546230d`  
		Last Modified: Mon, 23 Mar 2026 17:56:36 GMT  
		Size: 29.4 MB (29422706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aedef7727166e1191ea589a6a5d83d4a4256efc4a3dbc2b2d0eb90ebe7d2e40`  
		Last Modified: Mon, 23 Mar 2026 17:56:35 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93dd9e83218c05fbbb77ff85e0a011006b700f5b25992502009c1ebb05396d84`  
		Last Modified: Mon, 23 Mar 2026 17:56:36 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d060bc14529bf6390332b13f8f1948882f75de31a5202c44f8b2997cef5820`  
		Last Modified: Mon, 23 Mar 2026 17:56:36 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:ec2809017ed4f01b4dc801a8baff4c513e78b86cd7c74f4025027f748de93e5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 KB (51708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:babdb99e5e76f79f4f8aadb5ada81e969fdfafbff6a2aa1a57dd96cd79475d25`

```dockerfile
```

-	Layers:
	-	`sha256:fd9a485e8cd02e464b41a5098116f58c2a1623c7bb1546674e2f3042d7f5c2a7`  
		Last Modified: Mon, 23 Mar 2026 17:56:33 GMT  
		Size: 51.7 KB (51708 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.4-fpm-alpine` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:21ce477913394f9a64c005e17576a99606f527e9ddc60d01b7939df35da28df4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.4 MB (98407278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43310314c892a4c3a701fd951f5d8a53c4630807e63b5684980d7833c196ff5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Thu, 12 Mar 2026 23:44:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Mar 2026 23:44:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Mar 2026 23:44:58 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Mar 2026 23:44:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Mar 2026 23:44:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Mar 2026 23:44:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:44:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:44:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Mar 2026 23:44:58 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Mar 2026 23:44:58 GMT
ENV PHP_VERSION=8.4.19
# Thu, 12 Mar 2026 23:44:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.19.tar.xz.asc
# Thu, 12 Mar 2026 23:44:58 GMT
ENV PHP_SHA256=11f7164ab26d356c31f94d3d69cc0e0707d5d2d6494a221aaeae307c08eaaa1c
# Thu, 12 Mar 2026 23:45:02 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Mar 2026 23:45:02 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:48:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Mar 2026 23:48:08 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:48:09 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 12 Mar 2026 23:48:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Mar 2026 23:48:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Mar 2026 23:48:09 GMT
WORKDIR /var/www/html
# Thu, 12 Mar 2026 23:48:09 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 12 Mar 2026 23:48:09 GMT
STOPSIGNAL SIGQUIT
# Thu, 12 Mar 2026 23:48:09 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 12 Mar 2026 23:48:09 GMT
CMD ["php-fpm"]
# Mon, 23 Mar 2026 17:58:26 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Mon, 23 Mar 2026 17:59:46 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 23 Mar 2026 17:59:46 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Mon, 23 Mar 2026 17:59:46 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Mon, 23 Mar 2026 17:59:49 GMT
RUN set -eux; 	version='7.0-beta6'; 	sha1='40c821fe5ece3fb0feca1fff0ec6fa6a5e066f7d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 23 Mar 2026 17:59:49 GMT
VOLUME [/var/www/html]
# Mon, 23 Mar 2026 17:59:49 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 23 Mar 2026 17:59:49 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 17:59:49 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Mon, 23 Mar 2026 17:59:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 17:59:49 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51387bcb6cc1b283b7affa1a1f6f188bad5edc4bf160b1124df03db3c90bb823`  
		Last Modified: Thu, 12 Mar 2026 23:48:16 GMT  
		Size: 3.3 MB (3347481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d849384c97dea18d310c2f04174673375a08e4cf63777c0e16da8f13cb70c8d`  
		Last Modified: Thu, 12 Mar 2026 23:48:16 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:640fd39d0080142876494f51769aa8e38b9811f5349ad75d6668ec8df61eebcb`  
		Last Modified: Thu, 12 Mar 2026 23:48:16 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d2f1ff0d3b19501a2cdc678155799fb0eaaf509007f2cc2526e45c0a2043d0`  
		Last Modified: Thu, 12 Mar 2026 23:48:16 GMT  
		Size: 13.7 MB (13708140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9431e7c7ecf19db6b576046204cef30973d98bd78f069063904e34051f64895`  
		Last Modified: Thu, 12 Mar 2026 23:48:17 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d2a13c7d2bf7d31d563da86adbe2eecc9b3961aa7fe5ba24a6efb81b79f2b8`  
		Last Modified: Thu, 12 Mar 2026 23:48:17 GMT  
		Size: 13.0 MB (12954206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c647f3d4e13860b7fd091a5cc392403c53b553aa187eba25b8ae61dce10e9e53`  
		Last Modified: Thu, 12 Mar 2026 23:48:17 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7567de3f64be72aeb74b0c2b1b993b98c4db8828d7e1d10875f3d563d0120be1`  
		Last Modified: Thu, 12 Mar 2026 23:48:17 GMT  
		Size: 23.4 KB (23354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d1c4682245ef9f497c5cb92e4454ef4cc0722b37b202d0f3e337357c3625e82`  
		Last Modified: Thu, 12 Mar 2026 23:48:18 GMT  
		Size: 23.4 KB (23363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b030b2d617484e52bf8fe6993c67c5f8ce6e90680eab4ca0575957d45d1bb2`  
		Last Modified: Thu, 12 Mar 2026 23:48:18 GMT  
		Size: 9.3 KB (9266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:802278de15d1931ddf761d1792714f998821f8a0a27a22dd9dbfb511a22b0dbb`  
		Last Modified: Mon, 23 Mar 2026 17:59:59 GMT  
		Size: 26.9 MB (26899956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d2477e5795052e09fd6a15f6a47049b4b5b076e57e911bbc4486333466501c`  
		Last Modified: Mon, 23 Mar 2026 17:59:59 GMT  
		Size: 8.7 MB (8727864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16469178b732a613aed2f70e56b56a5dce7e87331998000c6bae5a5da8ed0547`  
		Last Modified: Mon, 23 Mar 2026 17:59:58 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b02c55646197cd4ae8bff99873750c7c144ee4ceb9fbf08316fac70afc1eca`  
		Last Modified: Mon, 23 Mar 2026 17:59:58 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b5d3288a5f8313e321cf54b73e033cad4a6f58b58f52078199352acb5384ef`  
		Last Modified: Mon, 23 Mar 2026 18:00:00 GMT  
		Size: 29.4 MB (29422708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9618bcae478f985e6dabafdabb62174f5107e13546afb02384b4f1ba0658fb`  
		Last Modified: Mon, 23 Mar 2026 18:00:00 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61b75d275f5f36691b8da5a6563ed5c090612657ec60fdca0b24b937deab013`  
		Last Modified: Mon, 23 Mar 2026 18:00:00 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e062f74abf8b1d623efa9d7732ad60c417de9167042bb27aa767bd70d528304c`  
		Last Modified: Mon, 23 Mar 2026 18:00:01 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:9ab1c78e3e5879f6ad81aaf04e5d9dbc7b5e8634a1abfae8d434bff6a4f4ec6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1172151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:585012d59f61f6a6ffb1979d116459b7f0bf96d1dda34cc5cadea3c2214b8254`

```dockerfile
```

-	Layers:
	-	`sha256:7d8d8465211f2fd34abfc5733c7431435c98214ed9ae5df6f18261b77d3c9525`  
		Last Modified: Mon, 23 Mar 2026 17:59:58 GMT  
		Size: 1.1 MB (1120227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c2ac6e7993110761d8376909e9b855eda8d7c9600b8cceecbc678e7fc02bd7c`  
		Last Modified: Mon, 23 Mar 2026 17:59:58 GMT  
		Size: 51.9 KB (51924 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.4-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:26dad1d4bf8ddb7c66a51acb1d4a91418fb5997df32308dccd25035e3bb7721c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.3 MB (107337439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71aecfa8aa413c35c1f32ae11fb8f4b642493ee7beb17f3b2a2c380305d7f42e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 12 Mar 2026 23:39:35 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Mar 2026 23:39:35 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Mar 2026 23:39:35 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Mar 2026 23:39:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Mar 2026 23:39:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Mar 2026 23:39:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:39:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:39:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Mar 2026 23:39:35 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Mar 2026 23:39:35 GMT
ENV PHP_VERSION=8.4.19
# Thu, 12 Mar 2026 23:39:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.19.tar.xz.asc
# Thu, 12 Mar 2026 23:39:35 GMT
ENV PHP_SHA256=11f7164ab26d356c31f94d3d69cc0e0707d5d2d6494a221aaeae307c08eaaa1c
# Thu, 12 Mar 2026 23:39:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Mar 2026 23:39:39 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:43:00 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Mar 2026 23:43:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:43:01 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 12 Mar 2026 23:43:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Mar 2026 23:43:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Mar 2026 23:43:01 GMT
WORKDIR /var/www/html
# Thu, 12 Mar 2026 23:43:01 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 12 Mar 2026 23:43:01 GMT
STOPSIGNAL SIGQUIT
# Thu, 12 Mar 2026 23:43:01 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 12 Mar 2026 23:43:01 GMT
CMD ["php-fpm"]
# Mon, 23 Mar 2026 17:56:15 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Mon, 23 Mar 2026 17:57:11 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 23 Mar 2026 17:57:11 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Mon, 23 Mar 2026 17:57:11 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Mon, 23 Mar 2026 17:57:13 GMT
RUN set -eux; 	version='7.0-beta6'; 	sha1='40c821fe5ece3fb0feca1fff0ec6fa6a5e066f7d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 23 Mar 2026 17:57:13 GMT
VOLUME [/var/www/html]
# Mon, 23 Mar 2026 17:57:13 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 23 Mar 2026 17:57:13 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 17:57:13 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Mon, 23 Mar 2026 17:57:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 17:57:13 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae15c1aebb5c8b05183f988dfd0638f67996de82a0e60f464ef791724120b67d`  
		Last Modified: Thu, 12 Mar 2026 23:43:08 GMT  
		Size: 3.6 MB (3601812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3289f166ea58ac77272d43a518b3fa4cd42e19a3df9541f8315662bcf5eeee`  
		Last Modified: Thu, 12 Mar 2026 23:43:08 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522d3b125cea588cb670b9efb7635ae636e0ef7073a5398e1a9e8f7bf1728145`  
		Last Modified: Thu, 12 Mar 2026 23:43:08 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e71dab9bbd7ccfe1e99992cfccef4889d39460a3fe1c8c8424d5a8ff762acb`  
		Last Modified: Thu, 12 Mar 2026 23:43:09 GMT  
		Size: 13.7 MB (13708128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e75facab9fae8a38af0b1edf370b8241cb446cbe38cef864710b826d11d54d1`  
		Last Modified: Thu, 12 Mar 2026 23:43:09 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde38664e7d813dc8976659f46320f758894ab3087ead1362ede753cdab3a4ec`  
		Last Modified: Thu, 12 Mar 2026 23:43:10 GMT  
		Size: 14.7 MB (14748601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b885e67129755592fe1f20370c200eda1875b3f56bcee0c3ab8a2fa1ffcce6`  
		Last Modified: Thu, 12 Mar 2026 23:43:10 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f96f1145c17002bef1213496b5a2f13eebd1c5031d770242a2d55f7df912b14d`  
		Last Modified: Thu, 12 Mar 2026 23:43:10 GMT  
		Size: 23.4 KB (23378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bf45551962333ca8896a0da63126e7b88a9a9a308f65c8b368e040c80755d1`  
		Last Modified: Thu, 12 Mar 2026 23:43:10 GMT  
		Size: 23.4 KB (23394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5815d1840fde90e86cfaa551871278e8579778642a08c8979582a94bf93900`  
		Last Modified: Thu, 12 Mar 2026 23:43:11 GMT  
		Size: 9.3 KB (9265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c276c7fc6795873a7e9ea017994b9b245f121619498783aad716cf0c97beda06`  
		Last Modified: Mon, 23 Mar 2026 17:57:25 GMT  
		Size: 32.5 MB (32479231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169b752f22746c07c396a2ccb5a949faf4be4b451bb8abc4b56d8362e492e03a`  
		Last Modified: Mon, 23 Mar 2026 17:57:24 GMT  
		Size: 9.1 MB (9114602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:175421e3585b3023c445952ae4ea82a53bd84cac8fb1f0d41c6cfafc60e7cbcd`  
		Last Modified: Mon, 23 Mar 2026 17:57:24 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70601edf7e469a6c12f1fe801324209600a4be582ba3ab6f4253d9d70386bf83`  
		Last Modified: Mon, 23 Mar 2026 17:57:24 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee3d6a6e0ee107e9c920b1fcfcb1c6b34c4628e4ce312c30af94ed9ed9c86ce7`  
		Last Modified: Mon, 23 Mar 2026 17:57:26 GMT  
		Size: 29.4 MB (29422718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d820f5b600c14c82151179d7df020515e22e76bd270244bbde9688383199e8`  
		Last Modified: Mon, 23 Mar 2026 17:57:25 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9d30af519e756aef38f5a10dd73bd438dc0a47ff8a2c76069cdd33720f8e1b`  
		Last Modified: Mon, 23 Mar 2026 17:57:25 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed1944c73850b5a57bec49722c733a39f58ac2e8c82c821991c729142a5cdf4`  
		Last Modified: Mon, 23 Mar 2026 17:57:26 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:6637a9b6ae25c7b3b0c39816edf17e891716d374e106d0bc26da1289596806fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1172205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbbe1ba2a98fd0b64c002237c3bc85103d6fbab3286346711547552a3f2ecb16`

```dockerfile
```

-	Layers:
	-	`sha256:5376d2561a0077d95ca98d3d3f82621b8bf81361628d245a2f67697bc12709b5`  
		Last Modified: Mon, 23 Mar 2026 17:57:24 GMT  
		Size: 1.1 MB (1120247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:958820197815e71538055c040cf50bd34986e3b000409d74c5238ffa152f5f28`  
		Last Modified: Mon, 23 Mar 2026 17:57:23 GMT  
		Size: 52.0 KB (51958 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.4-fpm-alpine` - linux; 386

```console
$ docker pull wordpress@sha256:ed7301c7002698f2fc6df2d2f61239baa8c49277d236987321422dcd10580118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.6 MB (107635500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8ae0fb2ea4da9459062e9335312273907170141f6ddf9e4a9f3ee76c1f6fd9c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Thu, 12 Mar 2026 23:42:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Mar 2026 23:42:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Mar 2026 23:42:43 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Mar 2026 23:42:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Mar 2026 23:42:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Mar 2026 23:42:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:42:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:42:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Mar 2026 23:42:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Mar 2026 23:42:43 GMT
ENV PHP_VERSION=8.4.19
# Thu, 12 Mar 2026 23:42:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.19.tar.xz.asc
# Thu, 12 Mar 2026 23:42:43 GMT
ENV PHP_SHA256=11f7164ab26d356c31f94d3d69cc0e0707d5d2d6494a221aaeae307c08eaaa1c
# Thu, 12 Mar 2026 23:42:47 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 12 Mar 2026 23:42:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:45:44 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 12 Mar 2026 23:45:44 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 12 Mar 2026 23:45:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 12 Mar 2026 23:45:45 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 12 Mar 2026 23:45:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 12 Mar 2026 23:45:45 GMT
WORKDIR /var/www/html
# Thu, 12 Mar 2026 23:45:45 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 12 Mar 2026 23:45:45 GMT
STOPSIGNAL SIGQUIT
# Thu, 12 Mar 2026 23:45:45 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 12 Mar 2026 23:45:45 GMT
CMD ["php-fpm"]
# Mon, 23 Mar 2026 17:53:27 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Mon, 23 Mar 2026 17:54:19 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 23 Mar 2026 17:54:19 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Mon, 23 Mar 2026 17:54:19 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Mon, 23 Mar 2026 17:54:21 GMT
RUN set -eux; 	version='7.0-beta6'; 	sha1='40c821fe5ece3fb0feca1fff0ec6fa6a5e066f7d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 23 Mar 2026 17:54:21 GMT
VOLUME [/var/www/html]
# Mon, 23 Mar 2026 17:54:21 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 23 Mar 2026 17:54:21 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 17:54:21 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Mon, 23 Mar 2026 17:54:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 17:54:21 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5114df9428bfb4bfe2fc75c32d4d894210f7e878f569600bd357ce4e00e508c6`  
		Last Modified: Thu, 12 Mar 2026 23:45:51 GMT  
		Size: 3.6 MB (3629392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4bae898899bcde9bc22075541d9653172f772fbb580fa90d2622900e7e9b848`  
		Last Modified: Thu, 12 Mar 2026 23:45:51 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9e90fad85fc8d6f087d1dede7e852efb1850f1d88a74f6e3971412f81ac35a`  
		Last Modified: Thu, 12 Mar 2026 23:45:51 GMT  
		Size: 218.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f6fc34ed0c1f7e4d44f3d532472ce86d047cb159a5936d66874c544074955dd`  
		Last Modified: Thu, 12 Mar 2026 23:45:52 GMT  
		Size: 13.7 MB (13708116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be0e6758bc576efae9fd3c96d4185d8b6854dc3c1398ac2ac49131939ce2a347`  
		Last Modified: Thu, 12 Mar 2026 23:45:52 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:331e002dbb065efce86ac826381de283aa31817ced06938de09f75fc75eb8621`  
		Last Modified: Thu, 12 Mar 2026 23:45:53 GMT  
		Size: 15.6 MB (15562467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5712f2d29cf2a8ad1ace52fb36dc1670ad0b3cf44c88adfbc490fdf84f90056`  
		Last Modified: Thu, 12 Mar 2026 23:45:53 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02759c2dbb1c6b28982f7d17a4a83d1d28e10901aadd8e8e2a6f18365f5a2ff9`  
		Last Modified: Thu, 12 Mar 2026 23:45:53 GMT  
		Size: 23.5 KB (23540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c385b72ada0bd4ce696fa75550d50e3932159356ecd1745a29ce3f25facb6000`  
		Last Modified: Thu, 12 Mar 2026 23:45:53 GMT  
		Size: 23.5 KB (23546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80ae4397b21899f5e68b56e49eb92e78217bae3114f1c88fc50febe3c7c5a235`  
		Last Modified: Thu, 12 Mar 2026 23:45:54 GMT  
		Size: 9.3 KB (9264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8d3f81a84c3c30a9d48005250e1f59f9a4e2e1ca889d6b2b62fc2b7700e2aa`  
		Last Modified: Mon, 23 Mar 2026 17:54:33 GMT  
		Size: 33.3 MB (33305126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49949076fea808a067aa8fdf898ca3b0f4645b82c5f73b7f84c1a769c7d4de8`  
		Last Modified: Mon, 23 Mar 2026 17:54:32 GMT  
		Size: 8.3 MB (8255116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b391d3f98fb13a73c7939a22e83b7c2726a05690161689676854737ca41b81f6`  
		Last Modified: Mon, 23 Mar 2026 17:54:32 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2548dd3fccb3681d5a747d0117a5708153360ccdcfe6af6c52e49e2edcbb6d`  
		Last Modified: Mon, 23 Mar 2026 17:54:32 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f767e836c127dc70088ff133e1ed9b0fcb18aacd37511c67a4894fe3240b2b09`  
		Last Modified: Mon, 23 Mar 2026 17:54:34 GMT  
		Size: 29.4 MB (29422713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7432d48ee00d7a01ff0cd87f67ab9c002636a126658d5202afe65abcc66ae11`  
		Last Modified: Mon, 23 Mar 2026 17:54:33 GMT  
		Size: 2.4 KB (2437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1d55f104cf03e4b5f14c04be1e0ea79afa29a2c599a110d0a8ac26396a5e5b`  
		Last Modified: Mon, 23 Mar 2026 17:54:34 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c57c6917a9101117fb33807903b6ed1f19bd77bb3c3d6e82b8a4456b4bc8d94`  
		Last Modified: Mon, 23 Mar 2026 17:54:35 GMT  
		Size: 194.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:7a4d0639fd97715cff514763fc6241ac2dedfd8dd9e90546f697fe62108377b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1173797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:474c79f963b1769542a3ad5cb8fa8370c42b661e1dacd18090b0a42d4a3a8487`

```dockerfile
```

-	Layers:
	-	`sha256:ec8b6af3a67a8d2ffd726f4718b0f52bae500f1dfda970cfb0b7380e755678f3`  
		Last Modified: Mon, 23 Mar 2026 17:54:32 GMT  
		Size: 1.1 MB (1122060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9447957deff3d6ebd0506e2781fff6856b2dbbe12d78748483c3cfeb7b08355a`  
		Last Modified: Mon, 23 Mar 2026 17:54:32 GMT  
		Size: 51.7 KB (51737 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.4-fpm-alpine` - linux; ppc64le

```console
$ docker pull wordpress@sha256:ca7f2cd83fb172a15a0b04545ccbdd56a653a7c5d9d5f2bc633db3109249f289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **109.6 MB (109648512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e11e11ea2217acc65aea6e063ee06d57fa09bb632c84e691739e31e9866beb5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 12 Mar 2026 23:53:02 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 12 Mar 2026 23:53:02 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 12 Mar 2026 23:53:02 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 12 Mar 2026 23:53:02 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_VERSION=8.4.19
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.19.tar.xz.asc
# Thu, 12 Mar 2026 23:53:02 GMT
ENV PHP_SHA256=11f7164ab26d356c31f94d3d69cc0e0707d5d2d6494a221aaeae307c08eaaa1c
# Fri, 13 Mar 2026 00:30:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 13 Mar 2026 00:30:05 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 00:35:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Mar 2026 00:35:22 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 00:35:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 13 Mar 2026 00:35:26 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Mar 2026 00:35:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Mar 2026 00:35:26 GMT
WORKDIR /var/www/html
# Fri, 13 Mar 2026 00:35:27 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 13 Mar 2026 00:35:27 GMT
STOPSIGNAL SIGQUIT
# Fri, 13 Mar 2026 00:35:27 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 13 Mar 2026 00:35:27 GMT
CMD ["php-fpm"]
# Mon, 23 Mar 2026 18:12:10 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Mon, 23 Mar 2026 18:14:01 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 23 Mar 2026 18:14:03 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Mon, 23 Mar 2026 18:14:07 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Mon, 23 Mar 2026 18:14:11 GMT
RUN set -eux; 	version='7.0-beta6'; 	sha1='40c821fe5ece3fb0feca1fff0ec6fa6a5e066f7d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 23 Mar 2026 18:14:11 GMT
VOLUME [/var/www/html]
# Mon, 23 Mar 2026 18:14:11 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 23 Mar 2026 18:14:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 18:14:12 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Mon, 23 Mar 2026 18:14:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 18:14:12 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7db1cc7b26f64d5de44e75f81962c30dead7dbc1dae3ebb93d0dc3d0cea721a`  
		Last Modified: Thu, 12 Mar 2026 23:58:51 GMT  
		Size: 3.8 MB (3768852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4a23ff5963c3f844b77db123769c733318f6ad54386c9f63e356424059470b`  
		Last Modified: Thu, 12 Mar 2026 23:58:51 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a071b7623ea30b2e8950858971a7e7838856db9c469a46b6305dcd619d0531fc`  
		Last Modified: Thu, 12 Mar 2026 23:58:51 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14d2c92d5998b48060c87fc70d0bff77df16c0a76188c808c288d28d5b9fb6fd`  
		Last Modified: Fri, 13 Mar 2026 00:34:25 GMT  
		Size: 13.7 MB (13708158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4118b5edb6de95db8201b5ee55ad2533c5b72350b68762c1484ea31caa5205f4`  
		Last Modified: Fri, 13 Mar 2026 00:34:24 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9706c3df9923641b6eb1768399f41df89d90aad1a3d920602dd948eb9de7f4`  
		Last Modified: Fri, 13 Mar 2026 00:35:43 GMT  
		Size: 15.8 MB (15785443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6b6d7aa2a65943e67c8e3d409977968b28a5f84a4a75888a4d12e4d2a15d56`  
		Last Modified: Fri, 13 Mar 2026 00:35:42 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d533dbee1f169aefed2f8237e055fb3c364843f96ab370c4e0d09dd12440ff4`  
		Last Modified: Fri, 13 Mar 2026 00:35:42 GMT  
		Size: 23.4 KB (23374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0128f031dca74f3f7ac3f5dae89935b1c6059ebd4f9dc56164765f921e7429b0`  
		Last Modified: Fri, 13 Mar 2026 00:35:42 GMT  
		Size: 23.4 KB (23403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f4679c13792307fea270423c67f81ed716d14f94f1214d81309ff23eca4802c`  
		Last Modified: Fri, 13 Mar 2026 00:35:43 GMT  
		Size: 9.3 KB (9268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ce47e6bd9865ce5559c9e897f5976093683dcaeee26e98aa866a0670f8aa31`  
		Last Modified: Mon, 23 Mar 2026 18:14:37 GMT  
		Size: 34.1 MB (34068454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693d76607bc1ce9054015b557a2817e52d7f70ba491fae31e86cf06f39ac7446`  
		Last Modified: Mon, 23 Mar 2026 18:14:36 GMT  
		Size: 9.0 MB (8999968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ed6dadd56a1d5c2128edaacfc74cefc008ef4ef9a6f9d3e5af47a619b3d4b4`  
		Last Modified: Mon, 23 Mar 2026 18:14:36 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eec494f407346d8cd903939f4be5edc31e4e86d8a970f230b209f5e344e923b`  
		Last Modified: Mon, 23 Mar 2026 18:14:36 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb576b12f7647f0a987f49ea7f91ed8ac8417ac7b3b8659c58ff933ceea5f1d`  
		Last Modified: Mon, 23 Mar 2026 18:14:38 GMT  
		Size: 29.4 MB (29422713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b766e64393ddea7e92524682174217e8bfe9c2ccfac93101e6594217917a227`  
		Last Modified: Mon, 23 Mar 2026 18:14:38 GMT  
		Size: 2.4 KB (2438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d8276e694b34e725a303b33332bd5b298b27c85f84eb288fe247daa779ef09`  
		Last Modified: Mon, 23 Mar 2026 18:14:38 GMT  
		Size: 1.8 KB (1766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb313661001894cf16d9a18757f865ed541b797b23ecc1255c434c53571f24d5`  
		Last Modified: Mon, 23 Mar 2026 18:14:39 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:9204bda9d3d352196e839aff91abe3fc88ba582d003568434034e16e69276610
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1172057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d181efd84a58a47c81490c6d770ee4ea249e29cca10beeab9c93bc3e7c54a17`

```dockerfile
```

-	Layers:
	-	`sha256:0876116f48993f3229742af881283e1e64ab7299f612f60a2de15ba6bf49a29c`  
		Last Modified: Mon, 23 Mar 2026 18:14:36 GMT  
		Size: 1.1 MB (1120224 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7207c50c4dd98dcacc726b0f07405260edb83702d5752b72b66aa173fda3faa6`  
		Last Modified: Mon, 23 Mar 2026 18:14:36 GMT  
		Size: 51.8 KB (51833 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.4-fpm-alpine` - linux; riscv64

```console
$ docker pull wordpress@sha256:77acf539dbad13e05d08ff6af2612bce4a0730df7def7b77a40bcec7ee7f5b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.8 MB (104778590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0574809befe1c64027d49d1e8351e5829a9764599196e48d45e2085e50fbba`
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
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_VERSION=8.4.19
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.19.tar.xz.asc
# Wed, 28 Jan 2026 09:13:07 GMT
ENV PHP_SHA256=11f7164ab26d356c31f94d3d69cc0e0707d5d2d6494a221aaeae307c08eaaa1c
# Fri, 13 Mar 2026 14:06:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 13 Mar 2026 14:06:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 16:03:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Mar 2026 16:03:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 16:03:45 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 13 Mar 2026 16:03:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Mar 2026 16:03:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Mar 2026 16:03:50 GMT
WORKDIR /var/www/html
# Fri, 13 Mar 2026 16:03:50 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 13 Mar 2026 16:03:50 GMT
STOPSIGNAL SIGQUIT
# Fri, 13 Mar 2026 16:03:50 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 13 Mar 2026 16:03:50 GMT
CMD ["php-fpm"]
# Tue, 24 Mar 2026 06:28:16 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 24 Mar 2026 06:44:33 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 24 Mar 2026 06:44:33 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Tue, 24 Mar 2026 06:44:34 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Tue, 24 Mar 2026 06:44:44 GMT
RUN set -eux; 	version='7.0-beta6'; 	sha1='40c821fe5ece3fb0feca1fff0ec6fa6a5e066f7d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 24 Mar 2026 06:44:45 GMT
VOLUME [/var/www/html]
# Tue, 24 Mar 2026 06:44:45 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 24 Mar 2026 06:44:45 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 24 Mar 2026 06:44:45 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Tue, 24 Mar 2026 06:44:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 24 Mar 2026 06:44:45 GMT
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
	-	`sha256:3dece99efd4fe1b04d7f121b7e547be9a87171e5416a6355ff5074eb8f0fe905`  
		Last Modified: Fri, 13 Mar 2026 15:05:41 GMT  
		Size: 13.7 MB (13708146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3583b64735302e8083791bc22c7b99e0974026bd44e9f3efad31e8807075d8af`  
		Last Modified: Fri, 13 Mar 2026 15:05:37 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54201815d51489f6bc32178ca2f1fd5e3efb02011bc556c71f64b8c6a4f5eca`  
		Last Modified: Fri, 13 Mar 2026 16:04:43 GMT  
		Size: 14.5 MB (14510642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29a8dfa7e6afe4f3926640db3234337788cbe5cd6d35500f3260645d929c6ed`  
		Last Modified: Fri, 13 Mar 2026 16:04:41 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e744fd1418e5fddb611e14dc691b88b2493c5fb5923a6cac3edd14000dbd3c9`  
		Last Modified: Fri, 13 Mar 2026 16:04:41 GMT  
		Size: 23.4 KB (23356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:deec5fda91a280532138a6b813c7431897348f2f40399b79ea0c0c38e5d99087`  
		Last Modified: Fri, 13 Mar 2026 16:04:41 GMT  
		Size: 23.4 KB (23371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7e4f89f89b0c62b3113dc3353246d04d3fcf2276ce79f6a51c7a2d61cfd1176`  
		Last Modified: Fri, 13 Mar 2026 16:04:42 GMT  
		Size: 9.3 KB (9265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304747c43e1b2bd35b1255ae911faae0dc766737f32922d103610ad1ab50ae95`  
		Last Modified: Tue, 24 Mar 2026 06:46:52 GMT  
		Size: 32.7 MB (32651126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7be7c6cafe7ffd31e0337fe02129eea36b863075750966ecbfa56865af4b9ec`  
		Last Modified: Tue, 24 Mar 2026 06:46:45 GMT  
		Size: 7.1 MB (7094440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2edb017074c4693e3e23fe8dca6aea123475b3709f69222ddb169c83e6b610`  
		Last Modified: Tue, 24 Mar 2026 06:46:42 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0625ce5e1162b536bd8f96f2fc53075233d263d0f54311a249f6dd4319f3c8f5`  
		Last Modified: Tue, 24 Mar 2026 06:46:42 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f565e2c54db4b6558aa33867fb2886668617e988e2e5f6170d044f685f90754`  
		Last Modified: Tue, 24 Mar 2026 06:46:53 GMT  
		Size: 29.4 MB (29422716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321f5bf8a6c9e64ea976c5c86d2efff38bfdb7758f6e4a28150aa55a68b1219a`  
		Last Modified: Tue, 24 Mar 2026 06:46:45 GMT  
		Size: 2.4 KB (2439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487aa39a2fe0dbbad44f6ed6a201ac8d48151326b2f30258e3f96eaa74ca08de`  
		Last Modified: Tue, 24 Mar 2026 06:46:47 GMT  
		Size: 1.8 KB (1768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b472d74577833067874b8f8dbef4eb4b2e1b0a0d78d61e127ec2de91f2e5871`  
		Last Modified: Tue, 24 Mar 2026 06:46:47 GMT  
		Size: 195.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:4784c5aba3c9d7cd3cd94efc3c75ee69f9036d23e4e2bd0834bb1fdc48115790
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1172052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94740d369bd53df05b0a9d66194ec8df30b5b106730a22d374d25882229d8017`

```dockerfile
```

-	Layers:
	-	`sha256:6a8fb068d21f614cfa2689b90cafd90521e6bd90bded0969a468c0f9390167f6`  
		Last Modified: Tue, 24 Mar 2026 06:46:42 GMT  
		Size: 1.1 MB (1120220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83d2fdd06da36082e030ca69bdafcc4459ec985fc1fde38273b321b49d4175c4`  
		Last Modified: Tue, 24 Mar 2026 06:46:42 GMT  
		Size: 51.8 KB (51832 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-php8.4-fpm-alpine` - linux; s390x

```console
$ docker pull wordpress@sha256:c3d3efdddf016b68d0f06278503c4c2ff53d2c64cbef338ed304366ac621cb67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.4 MB (108405538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:299a8b4b07cbd52403c29a31b796aaf3debaa101681bb9fcf46f3d582e605f4f`
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
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_VERSION=8.4.19
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.19.tar.xz.asc
# Thu, 12 Mar 2026 23:37:17 GMT
ENV PHP_SHA256=11f7164ab26d356c31f94d3d69cc0e0707d5d2d6494a221aaeae307c08eaaa1c
# Fri, 13 Mar 2026 00:16:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 13 Mar 2026 00:16:53 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 00:20:48 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 13 Mar 2026 00:20:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 13 Mar 2026 00:20:49 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 13 Mar 2026 00:20:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 13 Mar 2026 00:20:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 13 Mar 2026 00:20:49 GMT
WORKDIR /var/www/html
# Fri, 13 Mar 2026 00:20:49 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 13 Mar 2026 00:20:49 GMT
STOPSIGNAL SIGQUIT
# Fri, 13 Mar 2026 00:20:49 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 13 Mar 2026 00:20:49 GMT
CMD ["php-fpm"]
# Mon, 23 Mar 2026 17:55:09 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Mon, 23 Mar 2026 17:56:14 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev libheif-dev 		libavif-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-avif 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	pecl install imagick-3.8.1; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Mon, 23 Mar 2026 17:56:14 GMT
RUN set -eux; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Mon, 23 Mar 2026 17:56:14 GMT
RUN set -eux; 	{ 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > "$PHP_INI_DIR/conf.d/error-logging.ini" # buildkit
# Mon, 23 Mar 2026 17:56:16 GMT
RUN set -eux; 	version='7.0-beta6'; 	sha1='40c821fe5ece3fb0feca1fff0ec6fa6a5e066f7d'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Mon, 23 Mar 2026 17:56:16 GMT
VOLUME [/var/www/html]
# Mon, 23 Mar 2026 17:56:16 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Mon, 23 Mar 2026 17:56:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 23 Mar 2026 17:56:16 GMT
RUN ln -svfT docker-entrypoint.sh /usr/local/bin/docker-ensure-installed.sh # buildkit
# Mon, 23 Mar 2026 17:56:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 Mar 2026 17:56:16 GMT
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
	-	`sha256:0d264192f889237740934f148edbc4408ca88fefa36f9d47a48e46da10ef0b17`  
		Last Modified: Fri, 13 Mar 2026 00:21:01 GMT  
		Size: 13.7 MB (13708135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0dadac1e53dd32e14397d563846137a88d236a48f06bde595fd6ad6512764b`  
		Last Modified: Fri, 13 Mar 2026 00:21:00 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d539d68fce581c34089ad065f34dd2f9598639ae5c5dce2c610dc00ff3f21f`  
		Last Modified: Fri, 13 Mar 2026 00:21:01 GMT  
		Size: 15.0 MB (15000525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb2e5688048a50da4c04f35f3cc88053100b762fdad9e731a2384875ccafbdc`  
		Last Modified: Fri, 13 Mar 2026 00:21:01 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5938fda4acb1544bab69abf1e7cadc385acd3516dcf43e525b8da6f74fe3da3f`  
		Last Modified: Fri, 13 Mar 2026 00:21:01 GMT  
		Size: 23.4 KB (23355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60255ade78a8ff352c0e3f947c0e40c58d27c13ef6534e33e916332fcc18d181`  
		Last Modified: Fri, 13 Mar 2026 00:21:02 GMT  
		Size: 23.4 KB (23376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31878f0135c1e24a9256d3593134cb724790bf997eeda882ef1f8f9f1365a697`  
		Last Modified: Fri, 13 Mar 2026 00:21:02 GMT  
		Size: 9.3 KB (9265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799b036389fe3a63597daf58729d7d9a1827d7731c930924ef5b90bd6528b6c0`  
		Last Modified: Mon, 23 Mar 2026 17:56:33 GMT  
		Size: 34.0 MB (34010120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08eb4aa0d091ff050485cee32d3a847cd452b1ae2ce390f2add2c9c5138eaa1d`  
		Last Modified: Mon, 23 Mar 2026 17:56:33 GMT  
		Size: 8.7 MB (8678364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18c9a6449a87f98c4571f5a4fd03afed75e48ca64f634e9610afc1ad06145bce`  
		Last Modified: Mon, 23 Mar 2026 17:56:33 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65ca57678f60eea185f2da8eac5d661d4b7456268fa591e735291580cfd08d55`  
		Last Modified: Mon, 23 Mar 2026 17:56:33 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:615493258e0a2dc0e954eca24b941d215b9effea3e3d703b15edd13e3efa2338`  
		Last Modified: Mon, 23 Mar 2026 17:56:34 GMT  
		Size: 29.4 MB (29422712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3e144d314e07d9acce24c01c98b15106cba9b7e568b25b348b09c367971d02`  
		Last Modified: Mon, 23 Mar 2026 17:56:34 GMT  
		Size: 2.4 KB (2436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7951aa530a4a0c0b2f93775224d2789994ba06491f29a7381b852f05b6385d4`  
		Last Modified: Mon, 23 Mar 2026 17:56:34 GMT  
		Size: 1.8 KB (1767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa02d2bf31c69c86dcd6befb5ab52919bebfa7d8f339ed6965cf1e13c520dee`  
		Last Modified: Mon, 23 Mar 2026 17:56:35 GMT  
		Size: 197.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-php8.4-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:7b361e9342bc7b194639156ad9abb84bc122c3c895859830a1dd5abe424f199b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1171969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed4eff557bdc4c4105588eeb7cd563423c63c0b04952be0058114d118acb1a27`

```dockerfile
```

-	Layers:
	-	`sha256:3acc8fdeed742021e0c0957d8865e2ee041474d4032cde628dde310a057d7f0b`  
		Last Modified: Mon, 23 Mar 2026 17:56:33 GMT  
		Size: 1.1 MB (1120190 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f30b54dc4921e9b26b1cedb7f8e026ffdc9aa4bf4f413718ef1922f19720c763`  
		Last Modified: Mon, 23 Mar 2026 17:56:33 GMT  
		Size: 51.8 KB (51779 bytes)  
		MIME: application/vnd.in-toto+json
