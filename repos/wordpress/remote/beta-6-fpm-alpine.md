## `wordpress:beta-6-fpm-alpine`

```console
$ docker pull wordpress@sha256:9367cf31494e2341f900b561b04ed7d6282ce19870790e8f4371fce41636ad19
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

### `wordpress:beta-6-fpm-alpine` - linux; amd64

```console
$ docker pull wordpress@sha256:853485e1fa170ed047f6a2edfe7e686734dcc7b42479746cf67f102d08dc6807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 MB (88445313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a39b9766029e5e7779a5ccf7b2d31472f82f083c22ee3bb373fee088765e75ea`
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 18 Jun 2024 19:03:12 GMT
ENV PHP_VERSION=8.2.20
# Tue, 18 Jun 2024 19:03:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.20.tar.xz.asc
# Tue, 18 Jun 2024 19:03:12 GMT
ENV PHP_SHA256=4474cc430febef6de7be958f2c37253e5524d5c5331a7e1765cd2d2234881e50
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 18 Jun 2024 19:03:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
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
	-	`sha256:23cb4b018fda00ed927e30af20f67a15b969c6eebcbc0bd09cebd65705ef0784`  
		Last Modified: Fri, 21 Jun 2024 02:22:55 GMT  
		Size: 12.1 MB (12118886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecb141a5993b567c08250610a6e6fb0e5672b76683d15c8cf67429d79242b82`  
		Last Modified: Fri, 21 Jun 2024 02:22:54 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80274bfe1cc742f40f8d4bc6640531a3cca660cd7c7ca8ff1005cdebed8a0824`  
		Last Modified: Fri, 21 Jun 2024 02:23:18 GMT  
		Size: 12.9 MB (12864131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1417f4d03818b1e2782497242eb3f70148acecbe0d23042dbe3b5adcbf377e`  
		Last Modified: Fri, 21 Jun 2024 02:23:16 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f680cf0245d50edaf480192bec99f99541e3360176452c24451fc3f97beefe16`  
		Last Modified: Fri, 21 Jun 2024 02:23:16 GMT  
		Size: 19.7 KB (19686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c85be5bc15b3d1ef0a2ae889030b99c8d2e859a74658119473bdcccdc19041e`  
		Last Modified: Fri, 21 Jun 2024 02:23:16 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93fd61b67a1a422469cf918b6ec42668fbb1bd288e953e27881b61e15d6a4de`  
		Last Modified: Fri, 21 Jun 2024 02:59:44 GMT  
		Size: 28.3 MB (28264295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49dcd4d6d9adc60a5f25d6e45e9b985b38a40eec15ba94ddf0087240cf52d157`  
		Last Modified: Fri, 21 Jun 2024 02:59:44 GMT  
		Size: 3.8 MB (3753992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0938a9872017a6a38ee6b1148b324a2c024c259f9db99fbdd12b877d207cf842`  
		Last Modified: Fri, 21 Jun 2024 02:59:44 GMT  
		Size: 59.7 KB (59696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55447c0eb19f727d56649f3fcf7c67833b478193facc37f7af106c135078183`  
		Last Modified: Fri, 21 Jun 2024 02:59:44 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4feada8ed06fe2180132189ed49b1f05e06405b15d0bad0c355f035cd074221d`  
		Last Modified: Fri, 21 Jun 2024 02:59:45 GMT  
		Size: 24.5 MB (24455319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f1bf6ca14e1648960ce4d6aa7ab23a88a784cc34e89e9ccc22862c8e50d29c`  
		Last Modified: Fri, 21 Jun 2024 02:59:45 GMT  
		Size: 2.3 KB (2342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974ae0118663ef95436e122339b73ea515d2fda28ab5f6a9de9058855a56215a`  
		Last Modified: Fri, 21 Jun 2024 02:59:45 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:674ee177864f5ea3c084d0256afff19d2aff35e0bafe513a28bb8af9a2d26296
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1062944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b68f081fbcc29e2c78578ec3d5da86ccf36aa1c1507cb7a3961c544e875313b`

```dockerfile
```

-	Layers:
	-	`sha256:fc3b63c1e04edb0ab272f931a075bccf5e0da3019d1a376f1807a8391a146fe5`  
		Last Modified: Fri, 21 Jun 2024 02:59:44 GMT  
		Size: 1.0 MB (1014820 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38cb95f83c17f22412d541f49473967fdf00ed6f3a36e72bb31e3bc13f95362c`  
		Last Modified: Fri, 21 Jun 2024 02:59:44 GMT  
		Size: 48.1 KB (48124 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6-fpm-alpine` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:07e62fe5997ddaf6b5cfa16cf2faefcd8cf808a70d8976b1fd1f9ff4a8c5e390
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86435097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:952593d35c21e8149cbd3027ab3e3c1ad41be8a3716053f56d0cc65d49699462`
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
# Wed, 29 May 2024 22:26:16 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 06 Jun 2024 19:15:53 GMT
ENV PHP_VERSION=8.2.20
# Thu, 06 Jun 2024 19:15:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.20.tar.xz.asc
# Thu, 06 Jun 2024 19:15:53 GMT
ENV PHP_SHA256=4474cc430febef6de7be958f2c37253e5524d5c5331a7e1765cd2d2234881e50
# Thu, 06 Jun 2024 19:15:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 06 Jun 2024 19:15:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 06 Jun 2024 19:25:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 06 Jun 2024 19:25:03 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 06 Jun 2024 19:25:04 GMT
RUN docker-php-ext-enable sodium
# Thu, 06 Jun 2024 19:25:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Jun 2024 19:25:04 GMT
WORKDIR /var/www/html
# Thu, 06 Jun 2024 19:25:05 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 06 Jun 2024 19:25:05 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Jun 2024 19:25:05 GMT
EXPOSE 9000
# Thu, 06 Jun 2024 19:25:05 GMT
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
	-	`sha256:a922e65f3d83ee41fbad3cf5eddf0c301f7c4156f412e4f954e0ecb9b24036fb`  
		Last Modified: Thu, 06 Jun 2024 20:19:45 GMT  
		Size: 12.1 MB (12118899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1e9d56dc15e28920aac538540951170444760842266104ee7e7c514a483f63`  
		Last Modified: Thu, 06 Jun 2024 20:19:44 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a865af112206543d9315d4fe8d37897317c8c6750c34be97ac76fe662dc86efe`  
		Last Modified: Thu, 06 Jun 2024 20:20:12 GMT  
		Size: 11.7 MB (11709119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89dec66560ac355555a040c634b9ea28da9f83b7f84da75a6dfa0080b5195f71`  
		Last Modified: Thu, 06 Jun 2024 20:20:10 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc5d2a4f3dbba489909bab372fb15a6bf9db0aee6a3b359a95afc125c0b1b4a`  
		Last Modified: Thu, 06 Jun 2024 20:20:08 GMT  
		Size: 19.5 KB (19489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4efddc2d4023ab20639839ea7d7eecb9596c33c61bf6d198640f345912971e`  
		Last Modified: Thu, 06 Jun 2024 20:20:08 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74f752002dce7b2d80b59e0f58bcac6e0963be9eac1d5a19847fa6e5bd3f246`  
		Last Modified: Wed, 19 Jun 2024 02:44:23 GMT  
		Size: 27.8 MB (27827325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030b7ab81f5a92be9d7ce7cc1a71be5e109b68d81e63de4d5176b69298e070b7`  
		Last Modified: Wed, 19 Jun 2024 02:44:21 GMT  
		Size: 3.6 MB (3605825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28e1498bb494ffe4688e3d70e9a3c2bb3ce349128a34dca30f091b591b965ac`  
		Last Modified: Wed, 19 Jun 2024 02:44:20 GMT  
		Size: 59.7 KB (59689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a58d49172d1bf83272dbe07ead8269612167700919c20b4acec313d0259e84`  
		Last Modified: Wed, 19 Jun 2024 02:44:20 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab9c6cf7117f2ee5c5c0ec54eb1817d0b2526e590f1e5d932a18163ebc9cce2a`  
		Last Modified: Wed, 19 Jun 2024 02:44:23 GMT  
		Size: 24.5 MB (24455333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae27fe43620ab8bd4cd749404ffb64d1972c5155eca365bbc81fb1e50581dba6`  
		Last Modified: Wed, 19 Jun 2024 02:44:21 GMT  
		Size: 2.3 KB (2347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f90cde8fb365e5f3911904f047805d7392c6c962037c968b06d3121c3890b5`  
		Last Modified: Wed, 19 Jun 2024 02:44:22 GMT  
		Size: 1.7 KB (1730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:7db3eecc6c84fa65df4ce7cf78edf2832eb04247a9b04eae1300cc4a4080344c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 KB (48059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daca51dfd0c2ec65c94f702a97693709ad3f40f5720a453ea345e24af46bc4af`

```dockerfile
```

-	Layers:
	-	`sha256:c532f1c58ec5452d4b671e787742bbb743eb07c9d8948ef95cc6ae06e30ec303`  
		Last Modified: Wed, 19 Jun 2024 02:44:20 GMT  
		Size: 48.1 KB (48059 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6-fpm-alpine` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:058e22076178a5674c6b576330ea9b3a71b01f8b7636e4bbecb7a624fedd102b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.7 MB (83735875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5de3e9d6d606f5079a288e2e6a9b551bbef5f34158230b490af0b65928f8b6b7`
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
# Wed, 29 May 2024 23:12:50 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 06 Jun 2024 20:34:08 GMT
ENV PHP_VERSION=8.2.20
# Thu, 06 Jun 2024 20:34:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.20.tar.xz.asc
# Thu, 06 Jun 2024 20:34:08 GMT
ENV PHP_SHA256=4474cc430febef6de7be958f2c37253e5524d5c5331a7e1765cd2d2234881e50
# Thu, 06 Jun 2024 20:34:14 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 06 Jun 2024 20:34:14 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 06 Jun 2024 20:39:59 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 06 Jun 2024 20:40:00 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 06 Jun 2024 20:40:01 GMT
RUN docker-php-ext-enable sodium
# Thu, 06 Jun 2024 20:40:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Jun 2024 20:40:01 GMT
WORKDIR /var/www/html
# Thu, 06 Jun 2024 20:40:02 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 06 Jun 2024 20:40:02 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Jun 2024 20:40:02 GMT
EXPOSE 9000
# Thu, 06 Jun 2024 20:40:02 GMT
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
	-	`sha256:9c271788df6c086d2e4f2645e068d723aea25e3fc13ddcce11b8eaffb1b62794`  
		Last Modified: Thu, 06 Jun 2024 21:44:59 GMT  
		Size: 12.1 MB (12118907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5c5fe3d9bd9758d56c7f8de838841a02587788fa3ba38d3946dc877e92e61a`  
		Last Modified: Thu, 06 Jun 2024 21:44:58 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade8991594cb805f832c07138ef1882995eb9b1382ef93350d95b984e11b2b82`  
		Last Modified: Thu, 06 Jun 2024 21:45:25 GMT  
		Size: 11.0 MB (10972192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a5c1665cbb8ceccc8b9de800becc2f3842f562b4bbf8dcdef72c95d087093f`  
		Last Modified: Thu, 06 Jun 2024 21:45:23 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f9d13c09ad51351e29fd09b08ad986729db9d1b3300ef1089ca6645a36e5d5`  
		Last Modified: Thu, 06 Jun 2024 21:45:23 GMT  
		Size: 19.5 KB (19483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81c22be8233c21f01f455e327e245c3452c872b85b57048f22c4f1298fbe966`  
		Last Modified: Thu, 06 Jun 2024 21:45:23 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcf069bfeaaf3129e6427f75d23fd8c66838c4d7f0318a1ad110c52f800edc1b`  
		Last Modified: Wed, 12 Jun 2024 18:24:26 GMT  
		Size: 26.3 MB (26288060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7773856761b95c728770c30ec6dff4299a1e70134d4a0102936c0b536885f3`  
		Last Modified: Wed, 12 Jun 2024 18:24:25 GMT  
		Size: 3.6 MB (3640959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6204bdc1f578264c4d5342c6431bcbc019443f5bebb132e4a6af9d2b875589`  
		Last Modified: Wed, 12 Jun 2024 18:24:25 GMT  
		Size: 59.7 KB (59705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca333c47363581dd625c9fc4ee4c1a345646c2255af3c9a4582a87b37360715`  
		Last Modified: Wed, 12 Jun 2024 18:24:25 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:553c76bebacf2fa371d3b4a634aedc117d40f8d8f1a9bacd032ea02d72dd26c4`  
		Last Modified: Wed, 19 Jun 2024 02:47:54 GMT  
		Size: 24.5 MB (24455355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1a84396ec870a31c80cc69852c1d381db925dd502ceaf6bbe4885e9e3843ab`  
		Last Modified: Wed, 19 Jun 2024 02:47:53 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad65a3a38846f85e3c1b0d5fa5019a30f3784c73c262dcaad918ab8b3f3b765b`  
		Last Modified: Wed, 19 Jun 2024 02:47:53 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:356ee8e34d1892b4ad5108c84efcf2072d75a34bff1f4167e45185b870ec4f93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1063165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b200db8d2e71ac9f44af7ace441475e4b353c4db29ae98dfe47e4b3a15d407be`

```dockerfile
```

-	Layers:
	-	`sha256:512283de70e127f3c08b7482cf6cd6920ac254622b4f3494f3106c8f078caf52`  
		Last Modified: Wed, 19 Jun 2024 02:47:53 GMT  
		Size: 1.0 MB (1014887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef5aee447e9d106d29f77733be7d1429301131f2ff1af8acc8e3c2f084457693`  
		Last Modified: Wed, 19 Jun 2024 02:47:53 GMT  
		Size: 48.3 KB (48278 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:cd4239c65a4191c99ee6d6a2e46365401a708b51d781545f2d20230fd5304b4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.2 MB (89225459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6aa8c0556820dcae21aef0978ce9ac02b25e6f8b9e6141ca79c8a9e9a30e596`
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
# Thu, 06 Jun 2024 02:54:01 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 06 Jun 2024 21:00:22 GMT
ENV PHP_VERSION=8.2.20
# Thu, 06 Jun 2024 21:00:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.20.tar.xz.asc
# Thu, 06 Jun 2024 21:00:23 GMT
ENV PHP_SHA256=4474cc430febef6de7be958f2c37253e5524d5c5331a7e1765cd2d2234881e50
# Thu, 06 Jun 2024 21:00:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 06 Jun 2024 21:00:28 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 06 Jun 2024 21:08:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 06 Jun 2024 21:08:23 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 06 Jun 2024 21:08:24 GMT
RUN docker-php-ext-enable sodium
# Thu, 06 Jun 2024 21:08:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Jun 2024 21:08:25 GMT
WORKDIR /var/www/html
# Thu, 06 Jun 2024 21:08:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 06 Jun 2024 21:08:25 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Jun 2024 21:08:25 GMT
EXPOSE 9000
# Thu, 06 Jun 2024 21:08:25 GMT
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
	-	`sha256:a66dbf36537180c0dd888f452ab22a9feb2dff260b8d097058c2b9802857f0f8`  
		Last Modified: Thu, 06 Jun 2024 22:25:30 GMT  
		Size: 12.1 MB (12118892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7242cf95249ee1ba8bbdf4e813aabd15ade8cdf9c7abd9d06ca49d87cd33f9`  
		Last Modified: Thu, 06 Jun 2024 22:25:29 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50d78efa64722006192e621f0b7a33ca5878b2739ebfc6be323c4ad46c5a25d`  
		Last Modified: Thu, 06 Jun 2024 22:25:54 GMT  
		Size: 12.9 MB (12929245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dabb8545c1e2571e4cbe7bfb5da24385d7115f5d38d464c43934458d9fa72c24`  
		Last Modified: Thu, 06 Jun 2024 22:25:52 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f979ec9cf57941e2c2b1fb86e1ed9b77f065d7e834405d1465416f00700e3430`  
		Last Modified: Thu, 06 Jun 2024 22:25:52 GMT  
		Size: 19.5 KB (19479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e4903976168dd7b3518c4c3bf9f3283699af3b91135f360b7bee9a0b98e0a05`  
		Last Modified: Thu, 06 Jun 2024 22:25:52 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1150acc38f3b62cf8a46022d9b71bcffea9c3f692c4330c1266eb5838e42c3f0`  
		Last Modified: Wed, 12 Jun 2024 19:13:39 GMT  
		Size: 28.4 MB (28412216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c67a63ae890c44a87417b88f3450a81e5569957ba657330244736881750aa8`  
		Last Modified: Wed, 12 Jun 2024 19:13:39 GMT  
		Size: 3.8 MB (3804812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04e840e74f4356ab0c461f872fbefb3b6db656d42d36ec457826bd54e0215731`  
		Last Modified: Wed, 12 Jun 2024 19:13:38 GMT  
		Size: 59.6 KB (59646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:245911a7530ef92756478e10e0fe60457fe8e2f09b9ecfdc82817b580566682c`  
		Last Modified: Wed, 12 Jun 2024 19:13:38 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f5bc2d6bc88999956ae261b7e67b153bacce51eedff9ab9433697eb06d8271`  
		Last Modified: Wed, 19 Jun 2024 02:35:22 GMT  
		Size: 24.5 MB (24455361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99053e78059f9df88274e4d315346548d35e6947ae333ee8d779fd55568903d2`  
		Last Modified: Wed, 19 Jun 2024 02:35:21 GMT  
		Size: 2.4 KB (2352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcde71a79cbd2d7dc422bcf2e59751cac438b2f8f933a0d4c6993fe6b42347ba`  
		Last Modified: Wed, 19 Jun 2024 02:35:21 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:e470ae3d0c39fcfe52fca06c09db824d97de15a4d21a305552b0a3e7bd43e9c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1063402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:150bdd5af3f2112383f59dc92bbaa16c81512c8031a6ed030caba91af07379c6`

```dockerfile
```

-	Layers:
	-	`sha256:09b50ff8327d887f57b6d206b5c80b5c3ceba877f490f6dd9151f27439b581ca`  
		Last Modified: Wed, 19 Jun 2024 02:35:21 GMT  
		Size: 1.0 MB (1014923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:380f9af93f25bd89f0d5e3f0638008004a80308a08c98a0fc41c803954ea15a9`  
		Last Modified: Wed, 19 Jun 2024 02:35:21 GMT  
		Size: 48.5 KB (48479 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6-fpm-alpine` - linux; 386

```console
$ docker pull wordpress@sha256:a70104880a3e724190639f39651ef9793723cea6d948446be920e6cf4bb0e79c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.1 MB (89130282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c6f7e0964eede8d5239446234b50d3f7eeeaaadb0fc4d0a288c929b19ad8eb3`
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 18 Jun 2024 19:03:12 GMT
ENV PHP_VERSION=8.2.20
# Tue, 18 Jun 2024 19:03:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.20.tar.xz.asc
# Tue, 18 Jun 2024 19:03:12 GMT
ENV PHP_SHA256=4474cc430febef6de7be958f2c37253e5524d5c5331a7e1765cd2d2234881e50
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 18 Jun 2024 19:03:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
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
	-	`sha256:67357648e8c15655a3c20964c31e3be200c280f7688b81af0645abd24a4d8df5`  
		Last Modified: Thu, 20 Jun 2024 23:02:00 GMT  
		Size: 12.1 MB (12118894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef94528ab1d2a44bb8436d524208210728889d3c312dd3a16c93f58ea0f12a6`  
		Last Modified: Thu, 20 Jun 2024 23:01:59 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61bf0f8f63feb522e9778857554c456e475a5f02892ebda14cc27245c75e329a`  
		Last Modified: Thu, 20 Jun 2024 23:02:26 GMT  
		Size: 13.2 MB (13214883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffce086288dc525250ee9411a8e39dd60e446821a1abaf7211ffc6200a1bc596`  
		Last Modified: Thu, 20 Jun 2024 23:02:23 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cead003357681a099ef625a03a8f05efd5d7d5da69f941ac991644a155fa6765`  
		Last Modified: Thu, 20 Jun 2024 23:02:23 GMT  
		Size: 19.7 KB (19695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28cc6fb2f4dfc3a4033041a73a34e45e1f82501a5b41402552646feaef945d6d`  
		Last Modified: Thu, 20 Jun 2024 23:02:23 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6216c842787207df1c5b387bc3f6cb93d9a212fc6bd80ac3d32b0c2cb1d4ba`  
		Last Modified: Fri, 21 Jun 2024 00:00:59 GMT  
		Size: 28.5 MB (28532943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88827a5a75309ebfda44d082a8c8dd8f6178f80060a71df3cfd01af164f68997`  
		Last Modified: Fri, 21 Jun 2024 00:00:58 GMT  
		Size: 3.9 MB (3922990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cdb60711f72931b6fb38cce0cd3d5290f248f1e46b611a07e1d3bb56b5fd15b`  
		Last Modified: Fri, 21 Jun 2024 00:00:58 GMT  
		Size: 59.7 KB (59672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4058aac59878d04a18c7baf9d736df7f07005bad163f324ea4ee57d9a5698e`  
		Last Modified: Fri, 21 Jun 2024 00:00:58 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8fdc58c6e04ff8df577a7566f590faf5ec0eb55f62bc8f2d94e8ebbe09e8961`  
		Last Modified: Fri, 21 Jun 2024 00:00:59 GMT  
		Size: 24.5 MB (24455335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6b63b644e50f878d16450fc05f7a763945a73c5ae9b481fe3ae68bdeaebc5c`  
		Last Modified: Fri, 21 Jun 2024 00:00:59 GMT  
		Size: 2.3 KB (2344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b4f9d61012ee307c4eb086a86c8bec3dcda44f12a14fe4a66d1a3cb392f59e`  
		Last Modified: Fri, 21 Jun 2024 00:00:59 GMT  
		Size: 1.7 KB (1725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:67c7664b3552b4386553a81f3d91faebeaff5bbf9cbc76c62ad7e5efec523ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1062842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed6898138f9dd5ba31e3715fce77cd6abedc21c9c3d45e2256d57981b79f0c1`

```dockerfile
```

-	Layers:
	-	`sha256:a81ad5a5672dfb365bf3706b1435258135672d227e96928e2e2b5f03f73ea6bb`  
		Last Modified: Fri, 21 Jun 2024 00:00:58 GMT  
		Size: 1.0 MB (1014775 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e26ddb0ed2c3514c10e3eea0a6801b7fe3cd8da657fd620858394411a11f08b`  
		Last Modified: Fri, 21 Jun 2024 00:00:58 GMT  
		Size: 48.1 KB (48067 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6-fpm-alpine` - linux; ppc64le

```console
$ docker pull wordpress@sha256:d8da241fa82c3fa572e423692e5cedf3ba27012e5d16e605295962a7a76e74b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.9 MB (89892894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9a067d72864f348fa116b88316a58d38e35960d67912dd081edca4a5290d9f1`
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 18 Jun 2024 19:03:12 GMT
ENV PHP_VERSION=8.2.20
# Tue, 18 Jun 2024 19:03:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.20.tar.xz.asc
# Tue, 18 Jun 2024 19:03:12 GMT
ENV PHP_SHA256=4474cc430febef6de7be958f2c37253e5524d5c5331a7e1765cd2d2234881e50
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Tue, 18 Jun 2024 19:03:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 18 Jun 2024 19:03:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
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
	-	`sha256:14d8944ae63799ffd8a606cafbaf148e449aefd5a2528a9e123296bfa81f523d`  
		Last Modified: Thu, 20 Jun 2024 19:41:11 GMT  
		Size: 12.1 MB (12118902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fdcefa877cf54e26f705c391e47537545745b02b40f1c9850da6658ca47fd68`  
		Last Modified: Thu, 20 Jun 2024 19:41:10 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7460d94fe1125b941c1e88dd63d453fcaf61f5519e8d6bd8e5ce4f2bc45ca6f`  
		Last Modified: Thu, 20 Jun 2024 19:41:36 GMT  
		Size: 13.4 MB (13359327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6694d8303ff3261b7e807d14075edb46f7a3d85d471bd06bf1a2ebe182f957e5`  
		Last Modified: Thu, 20 Jun 2024 19:41:33 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0b5c825c297fda24dd1e9edb2523cd0fe86a5159a75b85b73442e27e61947e`  
		Last Modified: Thu, 20 Jun 2024 19:41:33 GMT  
		Size: 19.5 KB (19477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d258783f26a2960d92ee1cb5bc0f99f5e4d52d72fa19d1416d8d912dd3a029b`  
		Last Modified: Thu, 20 Jun 2024 19:41:33 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3bf9708ac2ba2da068b0b1b55ba6ec625a25599c9a08d4a86cbc0b1f0f39df`  
		Last Modified: Fri, 21 Jun 2024 05:16:40 GMT  
		Size: 29.0 MB (28979054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbae19bd8d2d532eb6ffe7b6e218c5522e11d13cee1320356e43f4e0fc171ab9`  
		Last Modified: Fri, 21 Jun 2024 05:16:40 GMT  
		Size: 3.9 MB (3916409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e538d8bf7d688e04ce443a5a25a5979a733e37bee42285b45f679eeb538cd7a5`  
		Last Modified: Fri, 21 Jun 2024 05:16:39 GMT  
		Size: 59.7 KB (59677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31aca6d9a67fd373fdd7a00a0e2b50aab0e204ca29d63b222500d8e61c07a9e6`  
		Last Modified: Fri, 21 Jun 2024 05:16:39 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1ed1ea76ed8c8d19678d50ecd13d3301e05894e54cc64a6bbedad681495b6ee`  
		Last Modified: Fri, 21 Jun 2024 05:26:00 GMT  
		Size: 24.5 MB (24455355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb771baf1408e770514791a3c44846fb3f5711afb5b67cf7e3e1467e7fe235ed`  
		Last Modified: Fri, 21 Jun 2024 05:25:58 GMT  
		Size: 2.3 KB (2349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba55da38259110df3d1f493b8043a4e72479d6b64ed49de0ebf1bb373491491b`  
		Last Modified: Fri, 21 Jun 2024 05:25:58 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:5c4d105250c7e5561b1a27fa2a1bb22ea39d778a53536d0c235a3a50f16fa522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1061118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc22b9967cfbee1a7c2bf81467c7f4f80375aeae5aebf3a9556d472be43f99d3`

```dockerfile
```

-	Layers:
	-	`sha256:f837753c3636a4b37a9761ad98a1318288df4ca3a5e835171a03be49b299550d`  
		Last Modified: Fri, 21 Jun 2024 05:25:58 GMT  
		Size: 1.0 MB (1012924 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d246e736c2c48d8f9d9d07d0fc70580dbbe6a8d59a4916801091435e3e14442f`  
		Last Modified: Fri, 21 Jun 2024 05:25:58 GMT  
		Size: 48.2 KB (48194 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6-fpm-alpine` - linux; riscv64

```console
$ docker pull wordpress@sha256:27d2683e913bd1b67d54fa2f92771d971892b623e219ae96adadc1d18650810e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.8 MB (87796970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810aecac077fa6f0071b184cc09a151538cc970055f7e96885e02bbfcdcd731e`
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
# Thu, 06 Jun 2024 16:20:37 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Fri, 07 Jun 2024 01:50:41 GMT
ENV PHP_VERSION=8.2.20
# Fri, 07 Jun 2024 01:50:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.20.tar.xz.asc
# Fri, 07 Jun 2024 01:50:42 GMT
ENV PHP_SHA256=4474cc430febef6de7be958f2c37253e5524d5c5331a7e1765cd2d2234881e50
# Fri, 07 Jun 2024 01:50:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 07 Jun 2024 01:50:57 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 07 Jun 2024 03:12:19 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 07 Jun 2024 03:12:21 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 07 Jun 2024 03:12:28 GMT
RUN docker-php-ext-enable sodium
# Fri, 07 Jun 2024 03:12:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 07 Jun 2024 03:12:29 GMT
WORKDIR /var/www/html
# Fri, 07 Jun 2024 03:12:31 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 07 Jun 2024 03:12:32 GMT
STOPSIGNAL SIGQUIT
# Fri, 07 Jun 2024 03:12:32 GMT
EXPOSE 9000
# Fri, 07 Jun 2024 03:12:33 GMT
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
	-	`sha256:f03f7391cd85f1ad4348726a7ce689c084d7399612d5aaa9569c44272254d34c`  
		Last Modified: Fri, 07 Jun 2024 05:58:59 GMT  
		Size: 12.1 MB (12118902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5daef19673fbaa3d8a4aa1105566e655e3f0f31dcd15d4e85a709e1c4d3480f`  
		Last Modified: Fri, 07 Jun 2024 05:58:54 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ae8d0a88036c98a4b8429d1389ace2355c6ed1ca75e0de822fde25c8ef4c1a`  
		Last Modified: Fri, 07 Jun 2024 05:59:49 GMT  
		Size: 12.2 MB (12224241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389b0463e03fd7dec8300ea37c07c1028fa1ad445b756fc7e0b0c60c21613278`  
		Last Modified: Fri, 07 Jun 2024 05:59:38 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03608acb47729b7785deb959d67a7b759d029b671c97bb81c5a4807dc2cfd4ac`  
		Last Modified: Fri, 07 Jun 2024 05:59:38 GMT  
		Size: 19.5 KB (19482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7106ff3dc070a879369ac4683f6b67dd6d28cfb7ddc5508a62fc965d77ef5859`  
		Last Modified: Fri, 07 Jun 2024 05:59:38 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c71deda041509c4a91b38ced9ac4de341bdcefd9d9265cbfe13770dea74c08`  
		Last Modified: Wed, 12 Jun 2024 22:45:05 GMT  
		Size: 28.4 MB (28353701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99d32f4901c70ded81902f118eb2061d775d5b2790add921e88ae1d78e5923b`  
		Last Modified: Wed, 12 Jun 2024 22:45:01 GMT  
		Size: 3.8 MB (3788931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cacd9346f3429c1edba58f42789da0211e281145ac9fc3bd09328287285c025f`  
		Last Modified: Wed, 12 Jun 2024 22:45:00 GMT  
		Size: 59.7 KB (59694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28124e70d5340321bb8f72bb92ff49e8733671b8d84dbfc5981c5e42aee90ab8`  
		Last Modified: Wed, 12 Jun 2024 22:45:01 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a1e628db6428b73cda8b504aa131696724b38ea6b7c9c5900aea07d69f4ba2`  
		Last Modified: Wed, 19 Jun 2024 06:36:35 GMT  
		Size: 24.5 MB (24455361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022f38262d473a154cd9a05dd41ab69db5a87cc12d9da1350ad11d8508f0ce19`  
		Last Modified: Wed, 19 Jun 2024 06:36:32 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:325034dcc446acb19d41d866e9847411733cb6f43037cc86e5b0f5a39de44139`  
		Last Modified: Wed, 19 Jun 2024 06:36:32 GMT  
		Size: 1.7 KB (1738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:8771fe1608c0650fb19bea4a9019058cef02f60cf1b7556bf3e92809335c6a41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1061113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3003b76e1e99d7e00de738cfbad58111661029b71c4ea587fd5fb11f797f8691`

```dockerfile
```

-	Layers:
	-	`sha256:7a586d8e2a8b50a6cc27495609373ab46287e67b2a187296701cef4dabab5763`  
		Last Modified: Wed, 19 Jun 2024 06:36:31 GMT  
		Size: 1.0 MB (1012919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b8116ef7a60d326c0630f686158a9e4edf6f6717f9946f15676897f28e3f275`  
		Last Modified: Wed, 19 Jun 2024 06:36:30 GMT  
		Size: 48.2 KB (48194 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6-fpm-alpine` - linux; s390x

```console
$ docker pull wordpress@sha256:4a4a0312401526b66a4248248ba963e9a6bd16e4259115a9464c686d956058d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89559894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96bb85358e40ceedb16464a6e37815d14ce627157f059419035021fe83799c58`
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
# Thu, 06 Jun 2024 02:25:46 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 06 Jun 2024 20:55:05 GMT
ENV PHP_VERSION=8.2.20
# Thu, 06 Jun 2024 20:55:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.20.tar.xz.asc
# Thu, 06 Jun 2024 20:55:05 GMT
ENV PHP_SHA256=4474cc430febef6de7be958f2c37253e5524d5c5331a7e1765cd2d2234881e50
# Thu, 06 Jun 2024 20:55:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 06 Jun 2024 20:55:09 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 06 Jun 2024 21:01:39 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 06 Jun 2024 21:01:40 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 06 Jun 2024 21:01:41 GMT
RUN docker-php-ext-enable sodium
# Thu, 06 Jun 2024 21:01:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Jun 2024 21:01:41 GMT
WORKDIR /var/www/html
# Thu, 06 Jun 2024 21:01:42 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 06 Jun 2024 21:01:43 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Jun 2024 21:01:43 GMT
EXPOSE 9000
# Thu, 06 Jun 2024 21:01:43 GMT
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
	-	`sha256:9ce355aafe4ac66d37a8ec2ba8ba7f76d4282d98b76aa3b135d7992437e3f03c`  
		Last Modified: Thu, 06 Jun 2024 22:05:08 GMT  
		Size: 12.1 MB (12118896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4d6d11bf124a1e02422e1a2b379f975de8d23caf963965f37632365e049c1b`  
		Last Modified: Thu, 06 Jun 2024 22:05:07 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313727a92fc3e39d60fa957fc76ddcb47ec127c612f459762b9c5f790466f2a0`  
		Last Modified: Thu, 06 Jun 2024 22:05:28 GMT  
		Size: 12.8 MB (12830083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95caa3c74dcce1c193cc69432d0b9a670d69003ac2ee7ed2e10b221134ea82ae`  
		Last Modified: Thu, 06 Jun 2024 22:05:25 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a60be280299cb6e55a56573f3fe09e1fae0c98f160b59837dd47cebd16b4507`  
		Last Modified: Thu, 06 Jun 2024 22:05:25 GMT  
		Size: 19.5 KB (19481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76021def48f753ac3dbeea5a62bd425d08fc86b8711d55fbc0f54a594acae872`  
		Last Modified: Thu, 06 Jun 2024 22:05:26 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f893fe1b0addd1f3f089dcf14de6bceba84c91d0b251017a94c783ab3df779af`  
		Last Modified: Wed, 12 Jun 2024 18:19:03 GMT  
		Size: 29.2 MB (29237398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ceaa46a1928678a978b5115a8962513a4f6f9a9f108606f29400df2278bade7`  
		Last Modified: Wed, 12 Jun 2024 18:19:01 GMT  
		Size: 3.9 MB (3898250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f57785d23c651df32fb2789ff5bd8d9cd5691d3c7c7ef29359d7a8e1af0400`  
		Last Modified: Wed, 12 Jun 2024 18:19:01 GMT  
		Size: 59.7 KB (59683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f178f6b5862e1bd2fb3a7c14948b8079a80ecabbd66c0e9d626643a96558595b`  
		Last Modified: Wed, 12 Jun 2024 18:19:01 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76580790d80ca34b2b3e42fd3a71a785e42a64f5246b6609cdec8baba226de69`  
		Last Modified: Wed, 19 Jun 2024 02:45:31 GMT  
		Size: 24.5 MB (24455355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a3f627ff12607aceb8e79e8cb6aa8fda700311dd256fbc7a6f910da43507b4b`  
		Last Modified: Wed, 19 Jun 2024 02:45:31 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad25409bfc217367bd4a1e28fb354820f2279f6b1d683bd66964ca406c2a7dcd`  
		Last Modified: Wed, 19 Jun 2024 02:45:30 GMT  
		Size: 1.7 KB (1737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:1df1774ecaf1323d33089affc2d0608991c07979e761220e3114cd3aaefe943a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1060989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aee2ac82f6bc7f2afef859314a8a5c5e9929f817b6215e39af064ca3471fadcc`

```dockerfile
```

-	Layers:
	-	`sha256:c13988064620398aa020782f8e03c88ca45e5a5d194c139b8d75d33a1c13943d`  
		Last Modified: Wed, 19 Jun 2024 02:45:30 GMT  
		Size: 1.0 MB (1012865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d73fa6bfe3507e2c42aa8f122bc46d674cbae895920b52a52260ad4932e097af`  
		Last Modified: Wed, 19 Jun 2024 02:45:30 GMT  
		Size: 48.1 KB (48124 bytes)  
		MIME: application/vnd.in-toto+json
