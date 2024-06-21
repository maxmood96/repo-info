## `wordpress:beta-6.6-php8.1-fpm-alpine`

```console
$ docker pull wordpress@sha256:b651748eb9c181fdaa021d214f62927601a8889e0e36ed1c2810728079960fe8
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

### `wordpress:beta-6.6-php8.1-fpm-alpine` - linux; amd64

```console
$ docker pull wordpress@sha256:1ff29ffd4d88fcd7f64b677f4f401fa310fbe89e7e6e77b73092c69dec078ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.9 MB (87892839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e60ec812d29fe9a18044f19fb3fc5801d174d0c6660855cce1ca9676d520fa97`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 18 Jun 2024 19:03:12 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Tue, 18 Jun 2024 19:03:12 GMT
CMD ["/bin/sh"]
# Tue, 18 Jun 2024 19:03:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 18 Jun 2024 19:03:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 18 Jun 2024 19:03:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 18 Jun 2024 19:03:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Jun 2024 19:03:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Jun 2024 19:03:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 18 Jun 2024 19:03:12 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 18 Jun 2024 19:03:12 GMT
ENV PHP_VERSION=8.1.29
# Tue, 18 Jun 2024 19:03:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Tue, 18 Jun 2024 19:03:12 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 18 Jun 2024 19:03:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 18 Jun 2024 19:03:12 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 18 Jun 2024 19:03:12 GMT
RUN docker-php-ext-enable sodium
# Tue, 18 Jun 2024 19:03:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 18 Jun 2024 19:03:12 GMT
WORKDIR /var/www/html
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Tue, 18 Jun 2024 19:03:12 GMT
STOPSIGNAL SIGQUIT
# Tue, 18 Jun 2024 19:03:12 GMT
EXPOSE 9000
# Tue, 18 Jun 2024 19:03:12 GMT
CMD ["php-fpm"]
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 	version='6.6-beta3'; 	sha1='ff959b1b4f2985ae69ee5df97a0f58838ec977c9'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
VOLUME [/var/www/html]
# Tue, 18 Jun 2024 19:03:12 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 19:03:12 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ed43a8165048a0688eda4741a1c89e730a72a7647897adef61a18b9017f2fc`  
		Last Modified: Fri, 21 Jun 2024 02:20:31 GMT  
		Size: 3.3 MB (3267719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82333a17c7c21e5bb46fbe4c79ef67474e6b016204698b266e09dc1477d55f18`  
		Last Modified: Fri, 21 Jun 2024 02:20:31 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6bc217d680f55bf9778238a32a4aa5b811c1e9199fbee493c57c487d7f0adf2`  
		Last Modified: Fri, 21 Jun 2024 02:20:30 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de4329585f0aef0f4af24b02275e7b56cae2ba47ebbc071312816405545aa70`  
		Last Modified: Fri, 21 Jun 2024 02:24:29 GMT  
		Size: 11.8 MB (11847372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d65a36b880af95f37c1b61f6a3b75c6aa13591821a02b73aae550211109dcab`  
		Last Modified: Fri, 21 Jun 2024 02:24:28 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d21933c044839bbe371f504c7116acb1c25f26538b60d00ec408e0315a0de1d`  
		Last Modified: Fri, 21 Jun 2024 02:24:51 GMT  
		Size: 12.6 MB (12612099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f711e48c0234ea0453071de5ade3299d2d35cb6ce2ee157bc269e134ba592ad`  
		Last Modified: Fri, 21 Jun 2024 02:24:49 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8b497d2c01415bfae1d9a354650723084ece3bee53d1b3b4d8c96c63a39067`  
		Last Modified: Fri, 21 Jun 2024 02:24:49 GMT  
		Size: 19.7 KB (19685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01613a17045206cdf8150bf28618fb87dc1e832303633a9cd2c2e80376ece8b0`  
		Last Modified: Fri, 21 Jun 2024 02:24:49 GMT  
		Size: 8.9 KB (8877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b47fe438c16403093ab74392be7527b92f0623c84035ccfbb8996c578b1d283`  
		Last Modified: Fri, 21 Jun 2024 02:59:49 GMT  
		Size: 28.3 MB (28264249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b57d003f06e3fbc7547639f9577233800c0ce7f37c256889508c938d589b0c8b`  
		Last Modified: Fri, 21 Jun 2024 02:59:48 GMT  
		Size: 3.7 MB (3725390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c7b38d7112f029ad5c0c557de4cc0268b812726070c524042c78c827676c0ad`  
		Last Modified: Fri, 21 Jun 2024 02:59:48 GMT  
		Size: 59.7 KB (59695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de52c4393be0fde76a2f12b2ddad9c4a81462b8a2994dd3edb3131cc766a7ff1`  
		Last Modified: Fri, 21 Jun 2024 02:59:48 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a707498249f37e821d2df0d55bba8c9c8c490005b510b7d5ec878526d43e5e`  
		Last Modified: Fri, 21 Jun 2024 02:59:50 GMT  
		Size: 24.5 MB (24455344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490c2ad29298dc967f8077c7bb7a2f0740b20ce73d3221b3efc6ea6edbb336bf`  
		Last Modified: Fri, 21 Jun 2024 02:59:49 GMT  
		Size: 2.3 KB (2346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6049c4739ac0dc1f47180d1587f5c0fea920117db7662f1304e8e93e927f97a9`  
		Last Modified: Fri, 21 Jun 2024 02:59:49 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.6-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:1c7d33cf60b527f9a5717836d0a3473a05fc60f544790a32c924409ca9cc84d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1060304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7d2db78cf5ea687964356aacb809cf48f7cebc7eb300128e9cd25a8b27fa869`

```dockerfile
```

-	Layers:
	-	`sha256:ad61a3849d595eb0202881fa74b56fc41d6b2a8d5102710939b54a717b359bfc`  
		Last Modified: Fri, 21 Jun 2024 02:59:48 GMT  
		Size: 1.0 MB (1013500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06b032660a5c3bdd41d933c54d809602c1b49bc8bb4e8071d383113cbbccac76`  
		Last Modified: Fri, 21 Jun 2024 02:59:47 GMT  
		Size: 46.8 KB (46804 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.6-php8.1-fpm-alpine` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:31dc872beaf2903c60d0efcf263cc975218d08f02b7872f2565b26610ab1172d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.8 MB (85834853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca76b3ff6246124377696ddda93c8c4f85b985f7878c76bc2992c7775c65fd0a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 21:50:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 29 May 2024 21:50:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 29 May 2024 21:50:44 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 29 May 2024 21:50:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 29 May 2024 21:50:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 29 May 2024 21:50:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 21:50:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 21:50:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 29 May 2024 22:36:16 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 06 Jun 2024 19:45:58 GMT
ENV PHP_VERSION=8.1.29
# Thu, 06 Jun 2024 19:45:58 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Thu, 06 Jun 2024 19:45:58 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Thu, 06 Jun 2024 19:46:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 06 Jun 2024 19:46:04 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 06 Jun 2024 19:55:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 06 Jun 2024 19:55:27 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 06 Jun 2024 19:55:28 GMT
RUN docker-php-ext-enable sodium
# Thu, 06 Jun 2024 19:55:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Jun 2024 19:55:28 GMT
WORKDIR /var/www/html
# Thu, 06 Jun 2024 19:55:29 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 06 Jun 2024 19:55:29 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Jun 2024 19:55:29 GMT
EXPOSE 9000
# Thu, 06 Jun 2024 19:55:29 GMT
CMD ["php-fpm"]
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 	version='6.6-beta3'; 	sha1='ff959b1b4f2985ae69ee5df97a0f58838ec977c9'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
VOLUME [/var/www/html]
# Tue, 18 Jun 2024 19:03:12 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 19:03:12 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fbde2bc87fb1211abfaa9d742eb1626779b6e008e3910fc9e86d002d2c18b4`  
		Last Modified: Wed, 29 May 2024 22:46:54 GMT  
		Size: 3.3 MB (3256537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3d57f281c14652f66f7ed738a118a66f8f9fe01923de337160db44abde6c2e`  
		Last Modified: Wed, 29 May 2024 22:46:53 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df4f95681943fb2de91ae5af31702772ccab2891b4971de5a53ad5b5f06489e`  
		Last Modified: Wed, 29 May 2024 22:46:53 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a62386b935f4953e9d375fff7740b3edfe5273307b96d307eaf8c6a42b9e3a`  
		Last Modified: Thu, 06 Jun 2024 20:21:29 GMT  
		Size: 11.8 MB (11847381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0c47714ac3dbaf81c544cc9f59212cca1197b06ec0bd5f2002c282fcb72f6b6`  
		Last Modified: Thu, 06 Jun 2024 20:21:27 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cf28e072ecc1f0583b7453a974bfcc8ddb87e45bb2b2fcf0bc7d244f3f6a3e7`  
		Last Modified: Thu, 06 Jun 2024 20:22:04 GMT  
		Size: 11.4 MB (11437265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8697ce0f7c7c5ff8f6310eac7f3165d6ec9554499349c4091d90d4103e68ee18`  
		Last Modified: Thu, 06 Jun 2024 20:22:01 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805d254e1977f4d940bab0030e8ef9a74ef6151d3f1301f75bd515cc7bfcb380`  
		Last Modified: Thu, 06 Jun 2024 20:22:01 GMT  
		Size: 19.5 KB (19489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13fce7b4bbe8d81c139b9e6c428d2c30c372181e1366de475cb24a6fdd208b9b`  
		Last Modified: Thu, 06 Jun 2024 20:22:01 GMT  
		Size: 8.9 KB (8875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b005e5e24edf215a95dd34b00190cdfc50e12b32ea58f01415944253bd19c2`  
		Last Modified: Wed, 19 Jun 2024 02:42:44 GMT  
		Size: 27.8 MB (27827224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3d08fdce4c148b6dd8aea8073490447977a85e802803a649b895b38584bb9c`  
		Last Modified: Wed, 19 Jun 2024 02:42:41 GMT  
		Size: 3.5 MB (3549357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2013b5551825ba48312e3404e547f5038af7359bea7077e27f567634c7d037c6`  
		Last Modified: Wed, 19 Jun 2024 02:42:41 GMT  
		Size: 59.7 KB (59684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43b6f860a461de4f55eae9549fd06e8093fb3572e6101dd8d73c41d87f311db0`  
		Last Modified: Wed, 19 Jun 2024 02:42:40 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d4bdd53a720ffaf71094a35524c91d59a028488472f92777ceebfd7c2dc1f21`  
		Last Modified: Wed, 19 Jun 2024 02:42:43 GMT  
		Size: 24.5 MB (24455338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc686d33ccd72ba216b297b6121218d0449baa791d618df611f6debe7afa86b2`  
		Last Modified: Wed, 19 Jun 2024 02:42:42 GMT  
		Size: 2.3 KB (2345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a0cdd17e60b3e30e482a73ff2c43bbc520c41af3c27a3414f66762f9ae5fb4`  
		Last Modified: Wed, 19 Jun 2024 02:42:43 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.6-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:b9829b3c3f7150fff01d6d165f8e7999485ed77c75c64092415863087d589074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 KB (46707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b584bca0cf7dac3610ca7e228d0562c66efc353c0055583cf28a522b37bbe995`

```dockerfile
```

-	Layers:
	-	`sha256:b3d108e79e23a2b1d980b6db3b77bb7de6da653ab5a485fb4a63d670e7a8f1bb`  
		Last Modified: Wed, 19 Jun 2024 02:42:40 GMT  
		Size: 46.7 KB (46707 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.6-php8.1-fpm-alpine` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:b938a995c37407319f778fd18f5cc866c5b7bb9fa6271ae71d95c2a39d8145ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.2 MB (83163512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c0587ed2af25d90662d77e9f57bcbaa12960c8422ee69318cedbc2561b6f2a8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 22:44:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 29 May 2024 22:44:07 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 29 May 2024 22:44:08 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 29 May 2024 22:44:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 29 May 2024 22:44:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 29 May 2024 22:44:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 22:44:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 22:44:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 29 May 2024 23:23:53 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 06 Jun 2024 21:16:03 GMT
ENV PHP_VERSION=8.1.29
# Thu, 06 Jun 2024 21:16:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Thu, 06 Jun 2024 21:16:03 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Thu, 06 Jun 2024 21:16:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 06 Jun 2024 21:16:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 06 Jun 2024 21:22:14 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 06 Jun 2024 21:22:14 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 06 Jun 2024 21:22:16 GMT
RUN docker-php-ext-enable sodium
# Thu, 06 Jun 2024 21:22:16 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Jun 2024 21:22:16 GMT
WORKDIR /var/www/html
# Thu, 06 Jun 2024 21:22:16 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 06 Jun 2024 21:22:16 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Jun 2024 21:22:17 GMT
EXPOSE 9000
# Thu, 06 Jun 2024 21:22:17 GMT
CMD ["php-fpm"]
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 	version='6.6-beta3'; 	sha1='ff959b1b4f2985ae69ee5df97a0f58838ec977c9'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
VOLUME [/var/www/html]
# Tue, 18 Jun 2024 19:03:12 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 19:03:12 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b726d2ea6325cbe2918171017f17d1d12ab778e5c1d68d663b22b061790803e5`  
		Last Modified: Wed, 29 May 2024 23:37:27 GMT  
		Size: 3.1 MB (3069336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2825cd15ae946086782a856b1d53fadaac330d395b11caf35413766a5903ab25`  
		Last Modified: Wed, 29 May 2024 23:37:26 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ea0ff5951f7688d6fc2e3212eae4ff67224a3150942bba64e271e0e6878353`  
		Last Modified: Wed, 29 May 2024 23:37:25 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0b37250f2349f080437e2e15d40485f22e26743b041c9500d97693e6910793a`  
		Last Modified: Thu, 06 Jun 2024 21:48:50 GMT  
		Size: 11.8 MB (11847384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5797282cc2ae458c7b84b1a14568e3f13df2c032eec5ed2a4c9f2569e55e8a36`  
		Last Modified: Thu, 06 Jun 2024 21:48:49 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a4894ec2d572a147a93f96237c172ed068e115445a3f518a7b2fd1e27af3a60`  
		Last Modified: Thu, 06 Jun 2024 21:49:15 GMT  
		Size: 10.7 MB (10722684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c74bf01ffa62ca43d4555772b4a4962df65805f1cd0f9ab1cf4177f25310145`  
		Last Modified: Thu, 06 Jun 2024 21:49:12 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a38f24b3a8f1eb28b1dc1279779bc9ad16cb2a7832ba2f25a6d04f72be61fb3`  
		Last Modified: Thu, 06 Jun 2024 21:49:12 GMT  
		Size: 19.5 KB (19484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:261ae1f4840e62130998d2fd7241d372e1c3b8da12c9cb7d31bf227e106d257b`  
		Last Modified: Thu, 06 Jun 2024 21:49:12 GMT  
		Size: 8.9 KB (8879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1381b5b98107b2344682f911061d5e1a465743e92c2f634b3ac213e842d13af6`  
		Last Modified: Wed, 12 Jun 2024 18:21:12 GMT  
		Size: 26.3 MB (26287992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a11ddfbfd7997be4397bb98ff7016b485cdc671a6c286317b6838788409f1d8d`  
		Last Modified: Wed, 12 Jun 2024 18:21:11 GMT  
		Size: 3.6 MB (3590000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283c7fb0bd77f429f68bdb21b61352eafeeb6c69c263cb7ccb53f3a7bc38f3d6`  
		Last Modified: Wed, 12 Jun 2024 18:21:10 GMT  
		Size: 59.7 KB (59702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fbf6faf699c90e462f5db37e9bedbca1971d230b833f2fad8c760235ee8a5d3`  
		Last Modified: Wed, 12 Jun 2024 18:21:10 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27293b3bd440e12441e3f29636e348bf97636e42d3a8dfc7f25aa827d1bdfc5f`  
		Last Modified: Wed, 19 Jun 2024 02:45:51 GMT  
		Size: 24.5 MB (24455358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc0152298ad0dae5edfce8cdbd89ecbccd05f25a04e44f0678c8802858100b0`  
		Last Modified: Wed, 19 Jun 2024 02:45:50 GMT  
		Size: 2.3 KB (2349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7723ac21e49d0dd1876f6058b41dc096eb7e361267fff589841ae7a44cc9186e`  
		Last Modified: Wed, 19 Jun 2024 02:45:50 GMT  
		Size: 1.7 KB (1733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.6-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:4b3e738e261965a74d97dcb7b4d10be0b443b7d2ab3cc24af4675b40f7c3fa2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1060461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db403d41d2cd450cd3e0723ca14f08b4f5e65a90ce5af402409e65abe2f48cae`

```dockerfile
```

-	Layers:
	-	`sha256:ec6fedb6434affd5a6eb278b7962aaa679f546638788829809453eb56f5f2938`  
		Last Modified: Wed, 19 Jun 2024 02:45:50 GMT  
		Size: 1.0 MB (1013535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:46ba5b8fcf744df900926fe61bdcb7462556f4c3e941c6694794c034e71f7fce`  
		Last Modified: Wed, 19 Jun 2024 02:45:49 GMT  
		Size: 46.9 KB (46926 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.6-php8.1-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:be239eeba1dff4c7d292d27bfd7733b566cc8367cda5b0390f1f20cd222a0f3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.6 MB (88649344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd602bb69caf0019451ca36d3c43ad9fba0a51dd1f1bd0aac4663bb22cd99b8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 22:24:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 29 May 2024 22:24:50 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 29 May 2024 22:24:51 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 29 May 2024 22:24:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 29 May 2024 22:24:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 29 May 2024 22:24:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 22:24:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 22:24:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 06 Jun 2024 03:44:56 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 06 Jun 2024 21:51:17 GMT
ENV PHP_VERSION=8.1.29
# Thu, 06 Jun 2024 21:51:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Thu, 06 Jun 2024 21:51:17 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Thu, 06 Jun 2024 21:51:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 06 Jun 2024 21:51:22 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 06 Jun 2024 21:59:18 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 06 Jun 2024 21:59:18 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 06 Jun 2024 21:59:19 GMT
RUN docker-php-ext-enable sodium
# Thu, 06 Jun 2024 21:59:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Jun 2024 21:59:19 GMT
WORKDIR /var/www/html
# Thu, 06 Jun 2024 21:59:20 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 06 Jun 2024 21:59:20 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Jun 2024 21:59:20 GMT
EXPOSE 9000
# Thu, 06 Jun 2024 21:59:20 GMT
CMD ["php-fpm"]
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 	version='6.6-beta3'; 	sha1='ff959b1b4f2985ae69ee5df97a0f58838ec977c9'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
VOLUME [/var/www/html]
# Tue, 18 Jun 2024 19:03:12 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 19:03:12 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499c233d91e0b285ef0ee55a1f0788e53ee03c80e7d609f44dfb93d39b760d4b`  
		Last Modified: Wed, 29 May 2024 22:56:13 GMT  
		Size: 3.3 MB (3321187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d2271fbac7611742e70ef3cf276070acf7876e4bcb10f6841029eb4f88f0f9`  
		Last Modified: Wed, 29 May 2024 22:56:12 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9701985de31ecc58dfb2496e5353c355dc9587a81cddc0dc9043524261c37c5`  
		Last Modified: Wed, 29 May 2024 22:56:12 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edb2c45859cc0636e77d53ba8d50480fa594a2e5fd5a9e61ccc7697cc0bf5579`  
		Last Modified: Thu, 06 Jun 2024 22:29:02 GMT  
		Size: 11.8 MB (11847373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a24fe39a58e8cb41f0b9de8c61820386b743f8f7d6771472e5fb8c4d35e1d7`  
		Last Modified: Thu, 06 Jun 2024 22:29:01 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d5d9e004d255235b4fa5ad5dcfa0578af8beea08a533030020391271327e012`  
		Last Modified: Thu, 06 Jun 2024 22:29:27 GMT  
		Size: 12.7 MB (12662443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629549bba3de3e2188974022f30a0733f8fe9d81ca5b7b481b624a6746d35d3b`  
		Last Modified: Thu, 06 Jun 2024 22:29:24 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:925c8849e890a3491e7f1b6e01f99e9f62bcde6876bdada69fd704be9ab66c93`  
		Last Modified: Thu, 06 Jun 2024 22:29:24 GMT  
		Size: 19.5 KB (19475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e8d93d121cb020fd51a37e6682c464d4061f990ed7f914709055da41fad1f7`  
		Last Modified: Thu, 06 Jun 2024 22:29:24 GMT  
		Size: 8.9 KB (8880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ce5406a9f92d1be0e73bff20c54470a06b8e05912fca2ea2534d8065bea7a96`  
		Last Modified: Wed, 12 Jun 2024 19:11:09 GMT  
		Size: 28.4 MB (28412216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b03553b6cae7fa3e0295789cdc50a507e066b87e479d468b7a545061f04b0ca`  
		Last Modified: Wed, 12 Jun 2024 19:11:08 GMT  
		Size: 3.8 MB (3767324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5d6c99d69382fda1962bcc3879cff9ea39a7345b83dd2f7bc4441315a46dc7`  
		Last Modified: Wed, 12 Jun 2024 19:11:07 GMT  
		Size: 59.6 KB (59646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b76cf9a8a7141c8e5203c9a972a1e6524a850bc72c0ad172ce5b59d6efe3975`  
		Last Modified: Wed, 12 Jun 2024 19:11:07 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05b9d8909d3228924c50bbf42f5d744c5052fe0ed2eaeb897dfa85b79689d31c`  
		Last Modified: Wed, 19 Jun 2024 02:33:45 GMT  
		Size: 24.5 MB (24455361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63e4ac3ddeec68179b758fe7c46707bfc3c473e94925aa1d7bd39ba222ebf0d9`  
		Last Modified: Wed, 19 Jun 2024 02:33:44 GMT  
		Size: 2.4 KB (2350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db5615fb372f51a94850defa3ffc365e153eec114694d60ac8eb556f500b633`  
		Last Modified: Wed, 19 Jun 2024 02:33:44 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.6-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:194e3316bffeafd3309c15a346317ac4c0d12909210656a3c0cb044348a02dd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1060666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d8c4b82f707a9292f351538e56f05f6b885ad3dee6b15ee23bc730d436af0a0`

```dockerfile
```

-	Layers:
	-	`sha256:f72e37f2dd015d88c4e9bee48d793055425e30e5551bcaa075578d447eff5052`  
		Last Modified: Wed, 19 Jun 2024 02:33:44 GMT  
		Size: 1.0 MB (1013555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df34e207cb4202951eeaea32bc4dc515fc65fece8304db506f95ba0f88caa4f4`  
		Last Modified: Wed, 19 Jun 2024 02:33:44 GMT  
		Size: 47.1 KB (47111 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.6-php8.1-fpm-alpine` - linux; 386

```console
$ docker pull wordpress@sha256:1e8156d35245e54ebd5576bece897053d1a1374a0bdf3bca851fb9f0dfad933d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.5 MB (88546638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4d7d124255c8ace0081ae4ebda6ee93234606f3120935bdbbe3b7974e3bf2c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 18 Jun 2024 19:03:12 GMT
ADD file:cd0e8f9dc9e579bd0c884d2c92e4773391bd73d8302d6f4a9bca0796e7ff9a77 in / 
# Tue, 18 Jun 2024 19:03:12 GMT
CMD ["/bin/sh"]
# Tue, 18 Jun 2024 19:03:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 18 Jun 2024 19:03:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 18 Jun 2024 19:03:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 18 Jun 2024 19:03:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Jun 2024 19:03:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Jun 2024 19:03:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 18 Jun 2024 19:03:12 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 18 Jun 2024 19:03:12 GMT
ENV PHP_VERSION=8.1.29
# Tue, 18 Jun 2024 19:03:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Tue, 18 Jun 2024 19:03:12 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 18 Jun 2024 19:03:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 18 Jun 2024 19:03:12 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 18 Jun 2024 19:03:12 GMT
RUN docker-php-ext-enable sodium
# Tue, 18 Jun 2024 19:03:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 18 Jun 2024 19:03:12 GMT
WORKDIR /var/www/html
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Tue, 18 Jun 2024 19:03:12 GMT
STOPSIGNAL SIGQUIT
# Tue, 18 Jun 2024 19:03:12 GMT
EXPOSE 9000
# Tue, 18 Jun 2024 19:03:12 GMT
CMD ["php-fpm"]
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 	version='6.6-beta3'; 	sha1='ff959b1b4f2985ae69ee5df97a0f58838ec977c9'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
VOLUME [/var/www/html]
# Tue, 18 Jun 2024 19:03:12 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 19:03:12 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:354eb832d25d95145569d0a3a573fb95b8350ee897d5b90a2f67ec1157706ec2`  
		Last Modified: Thu, 20 Jun 2024 17:38:50 GMT  
		Size: 3.5 MB (3469470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2323366a64c9696e4b985a0b5c338075544e5c4feec46f2d10d51a7b595e29`  
		Last Modified: Thu, 20 Jun 2024 22:59:30 GMT  
		Size: 3.3 MB (3318654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ed21a4a2f5c9deb46389e5d3a9c39b9a42ef686b0202b042c9f8e3658a211b2`  
		Last Modified: Thu, 20 Jun 2024 22:59:29 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff4dc126214224f26071d0bbfbff76af0e96a93d7e261c5c921b22224b77f616`  
		Last Modified: Thu, 20 Jun 2024 22:59:29 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bae74f93c2693db0566ca173d2c4c32dd7f1879e50278b520d1c53bfd3eb7a7`  
		Last Modified: Thu, 20 Jun 2024 23:03:44 GMT  
		Size: 11.8 MB (11847376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf0b2bcc0ccd56ea80a4a969bb51a998337f32ee84d10f678f2151b6a095bfc`  
		Last Modified: Thu, 20 Jun 2024 23:03:43 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe0287451895bbbd2d987687489d07fd49557f824ffef898898dbf2c9480316`  
		Last Modified: Thu, 20 Jun 2024 23:04:09 GMT  
		Size: 12.9 MB (12939595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:466895fdbe45874d7541c9ec03df33b29092a9c8127f99917ad957dae91d685a`  
		Last Modified: Thu, 20 Jun 2024 23:04:06 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e292508f8b2b53cdbb359eaa4e3ed544ec8c59ca4d6c9f11d0b895cb601287e`  
		Last Modified: Thu, 20 Jun 2024 23:04:06 GMT  
		Size: 19.7 KB (19694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395bf09b66d4c20ddc1dc731d9a06d01f8a07f27f6cb778561b8909e46300a4f`  
		Last Modified: Thu, 20 Jun 2024 23:04:06 GMT  
		Size: 8.9 KB (8879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bce43506876a2a5762c1cada6eface2170970b5888e2b671c936220f76399c4`  
		Last Modified: Fri, 21 Jun 2024 00:00:53 GMT  
		Size: 28.5 MB (28532914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc68e7f356359cdeb9401c7f2e6e80338a0e4900e02685805359d71793a4af76`  
		Last Modified: Fri, 21 Jun 2024 00:00:52 GMT  
		Size: 3.9 MB (3886489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4d40dc8fded53219682251078f991a4634830ebbde653826726f361dccd9ae`  
		Last Modified: Fri, 21 Jun 2024 00:00:52 GMT  
		Size: 59.7 KB (59670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5799d648cabd23d0146c89ab62fe8f214f8ca1d2f034e5d9671300b417eb32`  
		Last Modified: Fri, 21 Jun 2024 00:00:52 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0772a680af3ce63fa0ec269f68042a9b356a00eddad2160f1e4154f3c67212e2`  
		Last Modified: Fri, 21 Jun 2024 00:00:53 GMT  
		Size: 24.5 MB (24455328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b45b7cceb9d36252b035ddc8fd03a81803230715a17a8b65bee78503e95cf8`  
		Last Modified: Fri, 21 Jun 2024 00:00:53 GMT  
		Size: 2.3 KB (2345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36be18922cc735daa203d3a51d406fce3f6febb6520158cea1bf558bf51081f9`  
		Last Modified: Fri, 21 Jun 2024 00:00:53 GMT  
		Size: 1.7 KB (1729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.6-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:0a6840cfd6d0a2e97ef95ffe781c62700e424cf864414889215a07deb0c7505f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1060242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec5b9a48bf1b00ed7f95742fd11072b49fc1c7ab9b2819ab0388f587b04da9d9`

```dockerfile
```

-	Layers:
	-	`sha256:9b0de40ee1d742c470b4ce682e88fc336a9f358b357083f78ba02de4922e9ea3`  
		Last Modified: Fri, 21 Jun 2024 00:00:52 GMT  
		Size: 1.0 MB (1013475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa9bcc97d22f48b936c070a08daa3f5a54b7323cdee8f4479947a090004fbb37`  
		Last Modified: Fri, 21 Jun 2024 00:00:52 GMT  
		Size: 46.8 KB (46767 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.6-php8.1-fpm-alpine` - linux; ppc64le

```console
$ docker pull wordpress@sha256:29aec5e6b52beb407aef8f9a9f924266ccedb2f59568ab5d8e11c4324d6ab1b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.3 MB (89281787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfd2699be3ab1f63fc42c223742d5e084e79688b5449b7a1e7b7ecaf81ba9b45`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 18 Jun 2024 19:03:12 GMT
ADD file:c98fdd4075ec8eb66a469bd36f2d1369030638ad4b76778b5ad9c787b9f63c8b in / 
# Tue, 18 Jun 2024 19:03:12 GMT
CMD ["/bin/sh"]
# Tue, 18 Jun 2024 19:03:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 18 Jun 2024 19:03:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Tue, 18 Jun 2024 19:03:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 18 Jun 2024 19:03:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Jun 2024 19:03:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 18 Jun 2024 19:03:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 18 Jun 2024 19:03:12 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 18 Jun 2024 19:03:12 GMT
ENV PHP_VERSION=8.1.29
# Tue, 18 Jun 2024 19:03:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Tue, 18 Jun 2024 19:03:12 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 18 Jun 2024 19:03:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 18 Jun 2024 19:03:12 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 18 Jun 2024 19:03:12 GMT
RUN docker-php-ext-enable sodium
# Tue, 18 Jun 2024 19:03:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 18 Jun 2024 19:03:12 GMT
WORKDIR /var/www/html
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Tue, 18 Jun 2024 19:03:12 GMT
STOPSIGNAL SIGQUIT
# Tue, 18 Jun 2024 19:03:12 GMT
EXPOSE 9000
# Tue, 18 Jun 2024 19:03:12 GMT
CMD ["php-fpm"]
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 	version='6.6-beta3'; 	sha1='ff959b1b4f2985ae69ee5df97a0f58838ec977c9'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
VOLUME [/var/www/html]
# Tue, 18 Jun 2024 19:03:12 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 19:03:12 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b02dcd5eb44e382ea711bca074a007403db63dacf55f888b3a87214d1052dd50`  
		Last Modified: Thu, 20 Jun 2024 18:18:55 GMT  
		Size: 3.6 MB (3571699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6a26704de1bf6248f6df44727e1e01ae48fec7917e229bc3e343c672804b51`  
		Last Modified: Thu, 20 Jun 2024 19:38:43 GMT  
		Size: 3.4 MB (3395236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ee9c5937bf5aa444d1623e38c7154bb2971a8bd3cbd2f3b736c22ed6c73927`  
		Last Modified: Thu, 20 Jun 2024 19:38:41 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e84c1b8ee2969afc28f29a4447dc6ee6dbe5a916abb033890d01ce72b9e98d79`  
		Last Modified: Thu, 20 Jun 2024 19:38:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6786cdf2ba2e763d7f565ac08054ef090fad8282fbd84e0ee79a540b97c1ad10`  
		Last Modified: Thu, 20 Jun 2024 19:42:49 GMT  
		Size: 11.8 MB (11847387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2116f97c8303d9103f65f33c9b8abb47d99118cfbe66b98fbdfc0162291f6d15`  
		Last Modified: Thu, 20 Jun 2024 19:42:48 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d936d4daca873b501c2a9accc5119a661c7f9c3797c2a58f1e8e2eb0c1f0a0d1`  
		Last Modified: Thu, 20 Jun 2024 19:43:14 GMT  
		Size: 13.1 MB (13055958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8e3fe7448a5983d1f14bc11b0a79c38a96111c25d73114cb76c6e893d29a43`  
		Last Modified: Thu, 20 Jun 2024 19:43:12 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373a6eba41633add7fb208c0cefcb8ea0ed19b27dee965706d0f9cbf5c8558fa`  
		Last Modified: Thu, 20 Jun 2024 19:43:12 GMT  
		Size: 19.5 KB (19477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56528d0b1572c17e90b62e84891146b83cb292e2efb45c1d5b4b64254fb44e9b`  
		Last Modified: Thu, 20 Jun 2024 19:43:11 GMT  
		Size: 8.9 KB (8877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e328329580b025984147909cc671427ac4bec3cbe55c9720c7cb285abbf1b5`  
		Last Modified: Fri, 21 Jun 2024 05:14:42 GMT  
		Size: 29.0 MB (28979096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3490d63ea14c4981e34a094941c62bb257bdae7745651a2df28163295b469f70`  
		Last Modified: Fri, 21 Jun 2024 05:14:41 GMT  
		Size: 3.9 MB (3880438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55755314ab2f6c9c98db3e8389a692d1f2d872fc501f59f8ecc7ffffda177483`  
		Last Modified: Fri, 21 Jun 2024 05:14:40 GMT  
		Size: 59.7 KB (59678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c65d273c1322a62d99f26fb66958f3d13496c438267951a96348e2360b4e372`  
		Last Modified: Fri, 21 Jun 2024 05:14:40 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b5fabb478f194b22539b3f8368737f285eacc09b363840f7aa23093be039e3`  
		Last Modified: Fri, 21 Jun 2024 05:25:16 GMT  
		Size: 24.5 MB (24455358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2b4b95602e8ca736a9ae4b81c87f99f0f3004dbac25affd4c058c6ce680bd0`  
		Last Modified: Fri, 21 Jun 2024 05:25:14 GMT  
		Size: 2.3 KB (2349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34289b9a69bbd8fcd190feec7b358ba5e4bb025ff3a99a5b16f94359b319c80c`  
		Last Modified: Fri, 21 Jun 2024 05:25:14 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.6-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:03cd3341bce4a9c20a692149e85747933d41e3bc0a2e877f1c721c118d8d2425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1058430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54725c40030ee689564dd58bb394f31dbc23454071c5b21deb716f22ef4cd080`

```dockerfile
```

-	Layers:
	-	`sha256:5a2808e1283beb5bbce59a3b69268e8a60357da1dceff4d605803db0d44ca0d9`  
		Last Modified: Fri, 21 Jun 2024 05:25:14 GMT  
		Size: 1.0 MB (1011580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac3292e9ea498c5aab7aa24db098cacf239b336f15941b6b606a9a8cf754b19c`  
		Last Modified: Fri, 21 Jun 2024 05:25:14 GMT  
		Size: 46.9 KB (46850 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.6-php8.1-fpm-alpine` - linux; riscv64

```console
$ docker pull wordpress@sha256:3987520b84e40d8ac162f17c41a6675c740dd954ffc38c341a75b28830c968f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.2 MB (87195852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69727a208c3f2334497f2db3562446ed52169c14d618290eca9e327b2c1999f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 22 May 2024 17:57:29 GMT
ADD file:adedc612a3543e3a541be8e74c994fc3782e0f4a762ca77a1e29e6abfc81d7d8 in / 
# Wed, 22 May 2024 17:57:29 GMT
CMD ["/bin/sh"]
# Sat, 25 May 2024 09:09:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 25 May 2024 09:09:36 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 25 May 2024 09:09:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 25 May 2024 09:09:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 25 May 2024 09:09:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 25 May 2024 09:09:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 25 May 2024 09:09:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 25 May 2024 09:09:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 06 Jun 2024 18:24:11 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 07 Jun 2024 03:54:14 GMT
ENV PHP_VERSION=8.1.29
# Fri, 07 Jun 2024 03:54:15 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Fri, 07 Jun 2024 03:54:16 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Fri, 07 Jun 2024 03:54:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 07 Jun 2024 03:54:31 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 07 Jun 2024 05:14:19 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 07 Jun 2024 05:14:21 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 07 Jun 2024 05:14:28 GMT
RUN docker-php-ext-enable sodium
# Fri, 07 Jun 2024 05:14:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 07 Jun 2024 05:14:29 GMT
WORKDIR /var/www/html
# Fri, 07 Jun 2024 05:14:31 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 07 Jun 2024 05:14:32 GMT
STOPSIGNAL SIGQUIT
# Fri, 07 Jun 2024 05:14:32 GMT
EXPOSE 9000
# Fri, 07 Jun 2024 05:14:33 GMT
CMD ["php-fpm"]
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 	version='6.6-beta3'; 	sha1='ff959b1b4f2985ae69ee5df97a0f58838ec977c9'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
VOLUME [/var/www/html]
# Tue, 18 Jun 2024 19:03:12 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 19:03:12 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f280e85d15153a8f10f3fa47dd9d639e7a8fc6c1c8795d7123a32a0c36f16f55`  
		Last Modified: Wed, 22 May 2024 17:57:48 GMT  
		Size: 3.4 MB (3368560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94bc223ff0b5f41f6ce851397abb4ff3c5d40c6ae806a2a42975273c8e50ffb2`  
		Last Modified: Sat, 25 May 2024 16:19:49 GMT  
		Size: 3.4 MB (3390317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ee99391317e1ba305efd5739eca0a05c476c03d0e1c0cd7e0b5853e0cefe31`  
		Last Modified: Sat, 25 May 2024 16:19:44 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:159c26fc593ab14c52f09d8353c5ee82552b12bce63d672558073cd574642917`  
		Last Modified: Sat, 25 May 2024 16:19:44 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218046fd843dc5ab4b527959db5befec009656fe505f661261d165671bc61de6`  
		Last Modified: Fri, 07 Jun 2024 06:00:47 GMT  
		Size: 11.8 MB (11847386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0749ff9e66910765d6985d750f96fa94bae798d281e15dfce92c87768d13872`  
		Last Modified: Fri, 07 Jun 2024 06:00:42 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6636eefbbb966f9680c7d85d27696828f0735116a6499397faed22ca2553da56`  
		Last Modified: Fri, 07 Jun 2024 06:01:36 GMT  
		Size: 11.9 MB (11934117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72608ad408a07ad9d1bcddbbc2bdd1c622f4ff8837961918a548811f457004be`  
		Last Modified: Fri, 07 Jun 2024 06:01:25 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5af19bba77c96c33a639795b0c644ffc08f8c7a5bfa3a559c55ea06d45febb1`  
		Last Modified: Fri, 07 Jun 2024 06:01:25 GMT  
		Size: 19.5 KB (19480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e931f1e728506a819692ff7e46410bf685f006fa321a7067f65400c642c4ca2f`  
		Last Modified: Fri, 07 Jun 2024 06:01:25 GMT  
		Size: 8.9 KB (8877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2b6b67df84eb85835279daedfdcd347644dc2623dad2114a1c9a1fd06d25b31`  
		Last Modified: Wed, 12 Jun 2024 22:00:02 GMT  
		Size: 28.4 MB (28353629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4970adb8164e8f324b19896b364b8c836394963f0d8e23070ee6f9f043644897`  
		Last Modified: Wed, 12 Jun 2024 21:59:57 GMT  
		Size: 3.7 MB (3749839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8a7337674ee76afc2cc5dfe3b11f652d052da746ae58af2485426546fe8c37`  
		Last Modified: Wed, 12 Jun 2024 21:59:56 GMT  
		Size: 59.7 KB (59693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af80d5be41fc997b5521c926db707a05416a20fb88e313bab01cccfcb488d645`  
		Last Modified: Wed, 12 Jun 2024 21:59:56 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be9d0993004b3106c471fa266cd9263b0af59026ad86ab355d0bfa0c3a240b50`  
		Last Modified: Wed, 19 Jun 2024 06:34:19 GMT  
		Size: 24.5 MB (24455354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4cb5f98faa1509210c4e9201cdc55f6c67e8e317cbada17a05067d8203e3e92`  
		Last Modified: Wed, 19 Jun 2024 06:34:16 GMT  
		Size: 2.4 KB (2353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fe04557bca7d87eac7569e1b9534d55e547939dc6aa5bdfd955492b0b3c26e`  
		Last Modified: Wed, 19 Jun 2024 06:34:16 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.6-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:1c4db671f742c93ed853d47f7e09b876da84a1080129ba31b1fb895cd859c3c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1058425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fb012f28e85e4da3a5282b60d56aee6e1fb6a814cebeb2ec0706d289de2642e`

```dockerfile
```

-	Layers:
	-	`sha256:5da0e091f9252a12a59c84a2ea18ca214b6bca00fa0e75000aaabb02bab1cd4e`  
		Last Modified: Wed, 19 Jun 2024 06:34:15 GMT  
		Size: 1.0 MB (1011575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7588f3eea79019787acff1a520d68d49c50fec52505f163f73e1eac3ddf71cf8`  
		Last Modified: Wed, 19 Jun 2024 06:34:15 GMT  
		Size: 46.9 KB (46850 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.6-php8.1-fpm-alpine` - linux; s390x

```console
$ docker pull wordpress@sha256:84cd990af03f2a505f0330a6333a85cba1011338318278874af9acf0642ec97a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.0 MB (88962598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d87bfc5a96039b7ca94bfdc55cff84c4f154ea2f7f2df4aa4ed84bb77b4638fc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 22:13:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 29 May 2024 22:13:57 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 29 May 2024 22:13:57 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 29 May 2024 22:13:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 29 May 2024 22:13:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 29 May 2024 22:13:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 22:13:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 22:13:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 06 Jun 2024 03:04:55 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 06 Jun 2024 21:37:12 GMT
ENV PHP_VERSION=8.1.29
# Thu, 06 Jun 2024 21:37:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.29.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.29.tar.xz.asc
# Thu, 06 Jun 2024 21:37:12 GMT
ENV PHP_SHA256=288884af60581d4284baba2ace9ca6d646f72facbd3e3c2dd2acc7fe6f903536
# Thu, 06 Jun 2024 21:37:16 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 06 Jun 2024 21:37:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 06 Jun 2024 21:43:20 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 06 Jun 2024 21:43:20 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 06 Jun 2024 21:43:21 GMT
RUN docker-php-ext-enable sodium
# Thu, 06 Jun 2024 21:43:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Jun 2024 21:43:22 GMT
WORKDIR /var/www/html
# Thu, 06 Jun 2024 21:43:22 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 06 Jun 2024 21:43:22 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Jun 2024 21:43:22 GMT
EXPOSE 9000
# Thu, 06 Jun 2024 21:43:22 GMT
CMD ["php-fpm"]
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 	version='6.6-beta3'; 	sha1='ff959b1b4f2985ae69ee5df97a0f58838ec977c9'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
VOLUME [/var/www/html]
# Tue, 18 Jun 2024 19:03:12 GMT
COPY --chown=www-data:www-data wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 18 Jun 2024 19:03:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 18 Jun 2024 19:03:12 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e59aaf3957408d79830703dc723f179ea56d5e09b1b2358d2a1714ad397bd5f`  
		Last Modified: Wed, 29 May 2024 22:44:35 GMT  
		Size: 3.5 MB (3462557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4bd92d81aa824eaaf12fe4dc2b23834b92dfcb5f95ef3f980bbb78e812f400`  
		Last Modified: Wed, 29 May 2024 22:44:34 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4444860820a15536e66bf9ebb5b9ad505955c852e9a02a4a2aa1afae631eb1`  
		Last Modified: Wed, 29 May 2024 22:44:34 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc05801b5122b90d3e0b134020a71cb03192eac0d615eb286622869c0f1f0f01`  
		Last Modified: Thu, 06 Jun 2024 22:08:01 GMT  
		Size: 11.8 MB (11847379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819ad46a34688372cf3c9789057d8cc5206a1ca83ff71a8af1202af4fafa6dec`  
		Last Modified: Thu, 06 Jun 2024 22:08:00 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c9e71fa9509c1cd5552f27be22712c2d536064ed7a84f9087458e24ba0479b`  
		Last Modified: Thu, 06 Jun 2024 22:08:21 GMT  
		Size: 12.5 MB (12547493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02e049b5ae60a22160c00bb307e915203e5e0bc8cbdd402bf746d9de91227982`  
		Last Modified: Thu, 06 Jun 2024 22:08:19 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641278a0c5896f193830c0d4aeaa36fa636e43e2c22fc69ad6afe2623a0ff4f6`  
		Last Modified: Thu, 06 Jun 2024 22:08:19 GMT  
		Size: 19.5 KB (19483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69b8e045f608c388369d4aa0c29ec51b587a0877b306ae01b2c5e17e3209697c`  
		Last Modified: Thu, 06 Jun 2024 22:08:19 GMT  
		Size: 8.9 KB (8876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:968a7f944b2fd220d4d7b09c2da8dc51cec9672b782b504f69a955d7e4ed14dd`  
		Last Modified: Wed, 12 Jun 2024 18:15:53 GMT  
		Size: 29.2 MB (29237378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043b469fd447f6088b01c803e0c620179ded1043703f076a508526df4ab73951`  
		Last Modified: Wed, 12 Jun 2024 18:15:52 GMT  
		Size: 3.9 MB (3855387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0193bd012692f4af1bf97b4b3fcdeb1489ca12590eee877aa3917925780629d`  
		Last Modified: Wed, 12 Jun 2024 18:15:52 GMT  
		Size: 59.7 KB (59685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61511bcc886c0d556e8e56be59921f61905ab9e5c76177adba77e072d271bb39`  
		Last Modified: Wed, 12 Jun 2024 18:15:52 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b389e5a1b81f3ff9b4266e7eb9b76c0352b6564b08171e33c3b2fa434a5eb9`  
		Last Modified: Wed, 19 Jun 2024 02:43:13 GMT  
		Size: 24.5 MB (24455359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9687c1fce6b9bd26d85fa92d8cc76fc1409e677fa02d3fa25bf65fe93e4ea8f7`  
		Last Modified: Wed, 19 Jun 2024 02:43:13 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8dc3668ed278b9db83315798dba8fb6fd60430c3e0d7a1d43bea6f8b63dca6`  
		Last Modified: Wed, 19 Jun 2024 02:43:13 GMT  
		Size: 1.7 KB (1736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.6-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:560be2aeb101a79761806945eb599003c815cd593cd4c57bbfb648c37613abfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1058349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:323fea4f363a9d47b33242a6706d8348a4ad98ef83666ed9c2a48320b31c436a`

```dockerfile
```

-	Layers:
	-	`sha256:0feab78df63f55efc82d22b5b2cd67a0a807622bf4a0038f5d267c37fc2e675c`  
		Last Modified: Wed, 19 Jun 2024 02:43:12 GMT  
		Size: 1.0 MB (1011545 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:740e4a14bd2024ff8913f0d5dff6264c359d718538adb4b4d8260316abb2a807`  
		Last Modified: Wed, 19 Jun 2024 02:43:12 GMT  
		Size: 46.8 KB (46804 bytes)  
		MIME: application/vnd.in-toto+json
