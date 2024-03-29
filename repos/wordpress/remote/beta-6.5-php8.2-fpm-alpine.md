## `wordpress:beta-6.5-php8.2-fpm-alpine`

```console
$ docker pull wordpress@sha256:44b4054d364734ec0f2b9649efa780a4f62597c53cb30d5699583d5844eba104
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `wordpress:beta-6.5-php8.2-fpm-alpine` - linux; amd64

```console
$ docker pull wordpress@sha256:d8089312663ef6129775c9a63ae7e6f84f544868037d21083996d1ee38daf719
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.2 MB (88157288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e13da5c76de388128c7bad6f94a6905b50aceddb07ef4819d39ea025b7f1953`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 00:32:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 16 Mar 2024 00:32:11 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 16 Mar 2024 00:32:11 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 16 Mar 2024 00:32:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 16 Mar 2024 00:32:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 16 Mar 2024 00:32:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 16 Mar 2024 00:32:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 16 Mar 2024 00:32:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 16 Mar 2024 01:34:46 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 16 Mar 2024 01:34:46 GMT
ENV PHP_VERSION=8.2.17
# Sat, 16 Mar 2024 01:34:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.17.tar.xz.asc
# Sat, 16 Mar 2024 01:34:46 GMT
ENV PHP_SHA256=1cc4ef733ba58f6557db648012471f1916e5bac316303aa165535bedab08ee35
# Sat, 16 Mar 2024 01:34:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 16 Mar 2024 01:34:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 16 Mar 2024 01:43:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 16 Mar 2024 01:43:51 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 16 Mar 2024 01:43:52 GMT
RUN docker-php-ext-enable sodium
# Sat, 16 Mar 2024 01:43:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 16 Mar 2024 01:43:52 GMT
WORKDIR /var/www/html
# Sat, 16 Mar 2024 01:43:53 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 16 Mar 2024 01:43:53 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Mar 2024 01:43:53 GMT
EXPOSE 9000
# Sat, 16 Mar 2024 01:43:53 GMT
CMD ["php-fpm"]
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -eux; 	version='6.5-RC4'; 	sha1='2c93035e42009d5ae37ee5be7e6738e1dfa04102'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
VOLUME [/var/www/html]
# Thu, 28 Mar 2024 19:03:12 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 19:03:12 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b99432ace8a7bcff6a457c1ea616c20b241e4012ebc18ff9b4b9a7ca571de2d`  
		Last Modified: Sat, 16 Mar 2024 02:36:07 GMT  
		Size: 2.8 MB (2761513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a73aae1c86e8e06844a0d6ff516b8d12cc95d745da7005aea6ff3ec71c90ef`  
		Last Modified: Sat, 16 Mar 2024 02:36:07 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9294d9185d898643d89218d8a670313cd2bb59107bf32cb6ac92e7f46839bbc8`  
		Last Modified: Sat, 16 Mar 2024 02:36:07 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d311ade3bc839e5d734fe1b58120f0a3eee2104bcca9c10b8ce0295583bae2d`  
		Last Modified: Sat, 16 Mar 2024 02:40:45 GMT  
		Size: 12.1 MB (12113504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d524b064fceb531683ef03ea0a6a25c77ea8c2ee6960bbb3bc2446df436f7a`  
		Last Modified: Sat, 16 Mar 2024 02:40:44 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f58802ded6673e15958fdcdd089f3ad85e6ed3798e24da7e36928bae047dc4`  
		Last Modified: Sat, 16 Mar 2024 02:41:10 GMT  
		Size: 12.9 MB (12850790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e03c070f9c94f19904e69551286f4f9fec4145cdbbab515406a57d203f50081`  
		Last Modified: Sat, 16 Mar 2024 02:41:07 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc5ce590881c741d374ea4af3942b92e17b51646f7ea0f6426448f8266c62a7`  
		Last Modified: Sat, 16 Mar 2024 02:41:07 GMT  
		Size: 19.3 KB (19291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7ee9ca8bda687201bc0018682e3653c6456cae26448415e52064cb02ceaacc`  
		Last Modified: Sat, 16 Mar 2024 02:41:07 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c098e0463c08e68b4ac3be9d375bfe85229e9124a38ca571c835af5a6dabe771`  
		Last Modified: Fri, 29 Mar 2024 00:53:26 GMT  
		Size: 28.6 MB (28646254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31efbdac3bd6811d54b0fdb2c2dcfd5b91c077fe840de99983246f9f46e66e06`  
		Last Modified: Fri, 29 Mar 2024 00:53:25 GMT  
		Size: 3.8 MB (3754370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7f24e490c25549eb0ca91d9b9f0fd98a39ff2830fe774172895e93d4ec442d`  
		Last Modified: Fri, 29 Mar 2024 00:53:25 GMT  
		Size: 59.4 KB (59395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3b782f15c2b08286475c900285355669031908c870f7c0eb2919c0d113ce4a`  
		Last Modified: Fri, 29 Mar 2024 00:53:25 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64caf89c7df48947f73cb7c5f11d4ab4639131b86c983a7fc9248a7e5154d85`  
		Last Modified: Fri, 29 Mar 2024 00:53:27 GMT  
		Size: 24.5 MB (24525321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b6c0565e58ed867c72e61496416cdd4a10acd2f2e4959bd6355554dd12ae4f1`  
		Last Modified: Fri, 29 Mar 2024 00:53:26 GMT  
		Size: 2.3 KB (2347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623add736534c50efd9fe06d66912cca347ccb0caa73d9639ba29fa107810324`  
		Last Modified: Fri, 29 Mar 2024 00:53:26 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.5-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:f0ca544b58358e32ba0b2118b72512a8201f51286ca3d5ab1940704adf8596f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1062309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a1c1290f3d4552ae91f84f301f05b54ec3e6bd1aac534b1f35501def93c4807`

```dockerfile
```

-	Layers:
	-	`sha256:3591110f35fb09ad79e178d8adf8b724ed173c29a29c20515dbe6258ef7caaa9`  
		Last Modified: Fri, 29 Mar 2024 00:53:25 GMT  
		Size: 1.0 MB (1012619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc68e30ec208d036220bca64729a5441179b727c24ad7caa2c462d4fe85a6e7a`  
		Last Modified: Fri, 29 Mar 2024 00:53:24 GMT  
		Size: 49.7 KB (49690 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.5-php8.2-fpm-alpine` - linux; arm variant v6

```console
$ docker pull wordpress@sha256:78296b0010aec44e0ccbcdbd3e053d3fdd7f34a48f32d86dda190583ed47f512
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.1 MB (86129584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11aa423e89a23b17497f8a84d1ab58698b24453dde918e396a5ea7805939d47a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 23:49:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 15 Mar 2024 23:49:30 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 15 Mar 2024 23:49:31 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 15 Mar 2024 23:49:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 15 Mar 2024 23:49:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 15 Mar 2024 23:49:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Mar 2024 23:49:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 15 Mar 2024 23:49:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 16 Mar 2024 00:12:18 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 16 Mar 2024 00:12:18 GMT
ENV PHP_VERSION=8.2.17
# Sat, 16 Mar 2024 00:12:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.17.tar.xz.asc
# Sat, 16 Mar 2024 00:12:18 GMT
ENV PHP_SHA256=1cc4ef733ba58f6557db648012471f1916e5bac316303aa165535bedab08ee35
# Sat, 16 Mar 2024 00:12:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 16 Mar 2024 00:12:26 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 16 Mar 2024 00:20:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 16 Mar 2024 00:20:52 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 16 Mar 2024 00:20:54 GMT
RUN docker-php-ext-enable sodium
# Sat, 16 Mar 2024 00:20:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 16 Mar 2024 00:20:54 GMT
WORKDIR /var/www/html
# Sat, 16 Mar 2024 00:20:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 16 Mar 2024 00:20:55 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Mar 2024 00:20:55 GMT
EXPOSE 9000
# Sat, 16 Mar 2024 00:20:55 GMT
CMD ["php-fpm"]
# Tue, 19 Mar 2024 19:03:10 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Tue, 19 Mar 2024 19:03:10 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 19 Mar 2024 19:03:10 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Mar 2024 19:03:10 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 19 Mar 2024 19:03:10 GMT
RUN set -eux; 	version='6.5-RC3'; 	sha1='060ffbb620332ad9edcd29659bf087faf84fd916'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Tue, 19 Mar 2024 19:03:10 GMT
VOLUME [/var/www/html]
# Tue, 19 Mar 2024 19:03:10 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Tue, 19 Mar 2024 19:03:10 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Mar 2024 19:03:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 19 Mar 2024 19:03:10 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59be61bd2ba9f18af71b96c422917e0014880c902aa3ccb7f8257383b11b69ac`  
		Last Modified: Sat, 16 Mar 2024 01:01:12 GMT  
		Size: 2.8 MB (2764506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95722804161331c4c8c5fb5c67c2930e7f200746da0b87efc2cc1ca230b2bdf`  
		Last Modified: Sat, 16 Mar 2024 01:01:11 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9405a5b710e6142fb5b24b32edc3d286164167c9a50bc8d571a93dba40d73564`  
		Last Modified: Sat, 16 Mar 2024 01:01:10 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45646c6d55a580de8804880dd38484f1b112aeeea7560821da566c9e96ad52f1`  
		Last Modified: Sat, 16 Mar 2024 01:04:01 GMT  
		Size: 12.1 MB (12113523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb99454390c67e16d757b1a8e46d11332951b7876e9ce13b8bfee79b06745b9`  
		Last Modified: Sat, 16 Mar 2024 01:03:59 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20d5fe9cea9d9dc4235fe32fff4b71dd1f3566de5474c8fbc671e83b1c500b7`  
		Last Modified: Sat, 16 Mar 2024 01:04:31 GMT  
		Size: 11.7 MB (11696761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8cb62f86dca31efb86af0604d75bd46983e890069033dc283ceaac754fe5790`  
		Last Modified: Sat, 16 Mar 2024 01:04:28 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1b9f82ca09f1eeda9d42ccce896de8b16fb2ee22d201a6264975e8ec76f06d`  
		Last Modified: Sat, 16 Mar 2024 01:04:28 GMT  
		Size: 19.1 KB (19145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe30deb3542986389e6c6bc7cef43e8dbda604f2be9ad78a9e037435f28548c`  
		Last Modified: Sat, 16 Mar 2024 01:04:28 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccb6dcaf32b3fbfaf1a01522cac664f07a4e65d9da9558309fbf74fb8a7a3ab`  
		Last Modified: Tue, 19 Mar 2024 15:00:22 GMT  
		Size: 28.2 MB (28163606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45dbaa4e33f559af46f7754d814cb8b4a0c9cbf5844a48fa0bc880a1514ea2c`  
		Last Modified: Tue, 19 Mar 2024 15:00:22 GMT  
		Size: 3.6 MB (3605964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ae4366977a037fde8702ca790a349a88214faba369e565e2a1679c6d5fb3c0`  
		Last Modified: Tue, 19 Mar 2024 15:00:21 GMT  
		Size: 59.4 KB (59427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bd5eecd8bfcc057fbaeb119b6f809ab09dc9d585b7bfe45eef12ecba45d81da`  
		Last Modified: Tue, 19 Mar 2024 15:00:21 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a07bc525a454cabe7643d62c4c7f8fd19add6bb206ffd281e1b06e25a0e4c3df`  
		Last Modified: Wed, 20 Mar 2024 04:00:39 GMT  
		Size: 24.5 MB (24523133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e770a44707a143dc4e17aaf1488654dbea7524869512a82d71e63c1828be51c`  
		Last Modified: Wed, 20 Mar 2024 04:00:38 GMT  
		Size: 2.4 KB (2351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a783d749c08fd4199f2e1fd98e07129dfd8a7dc3548285d9de729e67bf5d41d4`  
		Last Modified: Wed, 20 Mar 2024 04:00:38 GMT  
		Size: 1.7 KB (1728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.5-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:45882af362f083501d54f982c3f47c1dc1bd8d75786c5df04b5ee78dc2fa5742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 KB (48004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739ad04b0b19246c3d1d6431459c42e24906bf7d22578150e03e6adad9f73fd4`

```dockerfile
```

-	Layers:
	-	`sha256:19b3382dfbbf56bc6a8bde3daf6befc270ac00f1ed13fee81d2bdc3c24a7f9ef`  
		Last Modified: Wed, 20 Mar 2024 04:00:38 GMT  
		Size: 48.0 KB (48004 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.5-php8.2-fpm-alpine` - linux; arm variant v7

```console
$ docker pull wordpress@sha256:f5f6f3f95da2247962ce760f15d3904c837f03e13017b7fdf4b5670958381a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.5 MB (83473300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:933de227de1b83f05bbf8f05d23ce27c3a82678aabcb795b3cfdcaabbf5be35d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 09:01:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 16 Mar 2024 09:01:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 16 Mar 2024 09:01:15 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 16 Mar 2024 09:01:15 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 16 Mar 2024 09:01:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 16 Mar 2024 09:01:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 16 Mar 2024 09:01:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 16 Mar 2024 09:01:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 16 Mar 2024 09:39:19 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 16 Mar 2024 09:39:20 GMT
ENV PHP_VERSION=8.2.17
# Sat, 16 Mar 2024 09:39:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.17.tar.xz.asc
# Sat, 16 Mar 2024 09:39:20 GMT
ENV PHP_SHA256=1cc4ef733ba58f6557db648012471f1916e5bac316303aa165535bedab08ee35
# Sat, 16 Mar 2024 09:39:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 16 Mar 2024 09:39:34 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 16 Mar 2024 09:51:13 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 16 Mar 2024 09:51:14 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 16 Mar 2024 09:51:17 GMT
RUN docker-php-ext-enable sodium
# Sat, 16 Mar 2024 09:51:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 16 Mar 2024 09:51:17 GMT
WORKDIR /var/www/html
# Sat, 16 Mar 2024 09:51:18 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 16 Mar 2024 09:51:19 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Mar 2024 09:51:19 GMT
EXPOSE 9000
# Sat, 16 Mar 2024 09:51:19 GMT
CMD ["php-fpm"]
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -eux; 	version='6.5-RC4'; 	sha1='2c93035e42009d5ae37ee5be7e6738e1dfa04102'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
VOLUME [/var/www/html]
# Thu, 28 Mar 2024 19:03:12 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 19:03:12 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c24a3155a604085efaa4c70bd2859739b6141d4fd0670fa3e15fd67cab1a2154`  
		Last Modified: Sat, 16 Mar 2024 11:00:26 GMT  
		Size: 2.6 MB (2612666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91bbcf35c6eddf26fa13dc8c811f2ac147d03bba1af2fa37c43084f218a04ca`  
		Last Modified: Sat, 16 Mar 2024 11:00:25 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb37d0aeb5ad8612608d36edcbe0f65f4004674effbc82dceac7fda7895b9f1`  
		Last Modified: Sat, 16 Mar 2024 11:00:25 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87ddc10b7ac67878aafbed3dece703da464c130bbe12323b2fa18674d935658`  
		Last Modified: Sat, 16 Mar 2024 11:05:32 GMT  
		Size: 12.1 MB (12113510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2f81462e885d1375754d2707a5468e34c1b7cf0c4c954caf45aab60f32b7d4`  
		Last Modified: Sat, 16 Mar 2024 11:05:31 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59af55f935c2fccede8b491d6db7eec3f21e9128761b99d7503f47cf0c549211`  
		Last Modified: Sat, 16 Mar 2024 11:06:00 GMT  
		Size: 11.0 MB (10966958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335a0dfd557536d0da74224cf031cb541cc70dce41cb9e621b4a5e0b4034aa79`  
		Last Modified: Sat, 16 Mar 2024 11:05:57 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf4ddf9ae8da2509ff0355a891f21a59ad87b4ff14308605afcb6605d72ef689`  
		Last Modified: Sat, 16 Mar 2024 11:05:57 GMT  
		Size: 19.1 KB (19119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86307baf2818fa1a83994e734050ee3d37dca26564b5e03fad9913fac9968c61`  
		Last Modified: Sat, 16 Mar 2024 11:05:57 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:453da0d79a10dff603dd16f345973327419d8912b21c7564131d8dd30d3e4706`  
		Last Modified: Sat, 16 Mar 2024 21:20:37 GMT  
		Size: 26.6 MB (26597966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5def54cdb1cdc4247eaf7044bda2cf71b051a52e71d10d9d40268b68c029731`  
		Last Modified: Sat, 16 Mar 2024 21:20:36 GMT  
		Size: 3.6 MB (3641307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d406f8a18f69b1265a52db027b1bba5b58150b80a9073dc28529c157062c0013`  
		Last Modified: Sat, 16 Mar 2024 21:20:36 GMT  
		Size: 59.4 KB (59414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e13e09eecc26cfc7224ccab3598af633baa0649390ab0677f00c3d5fda3e539`  
		Last Modified: Sat, 16 Mar 2024 21:20:36 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c790e9d35ad41dee63cb6911a5d3a5b0a12df0b5e3066df067ff22a60f5311`  
		Last Modified: Fri, 29 Mar 2024 00:57:57 GMT  
		Size: 24.5 MB (24525325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2fd836bf16895dce32220c40a25eccd281e0ed12f1735c7971ee58d1c02e121`  
		Last Modified: Fri, 29 Mar 2024 00:57:56 GMT  
		Size: 2.4 KB (2354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d96023bc304cbc5821e9d5b2f9c1fde4be7f92b0bad8af1e45a16b7e97eb903`  
		Last Modified: Fri, 29 Mar 2024 00:57:56 GMT  
		Size: 1.7 KB (1734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.5-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:bad6e4615cff67aecb4aa1d2f2cd68e22ed7f8ceadedd92ecf50cdca25abfec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1060906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b31ad38dbe8b91376fc9829db10a07101d62163ab8f7b26340648e64cae46e`

```dockerfile
```

-	Layers:
	-	`sha256:fa3786318df7887f882328e61d6368ca47ed73bdc2543b3c33c86dc5e7c4922e`  
		Last Modified: Fri, 29 Mar 2024 00:57:56 GMT  
		Size: 1.0 MB (1012687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bef482ed7a1f3ce6b085af9babc3691d0d04ab8f80491baaf8abb98362f2c10b`  
		Last Modified: Fri, 29 Mar 2024 00:57:55 GMT  
		Size: 48.2 KB (48219 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.5-php8.2-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull wordpress@sha256:46adfd626c22bd8803a8e362b05782b2d8b991c2e6dee1ad9967ec2a0bae1aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.4 MB (88387874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f9f862f84a8e1a883e78c1c09b777a4f032f63a766b6bfe3b5540237cfeb38c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 00:36:31 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 16 Mar 2024 00:36:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 16 Mar 2024 00:36:33 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 16 Mar 2024 00:36:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 16 Mar 2024 00:36:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 16 Mar 2024 00:36:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 16 Mar 2024 00:36:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 16 Mar 2024 00:36:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 16 Mar 2024 01:26:54 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 16 Mar 2024 01:26:54 GMT
ENV PHP_VERSION=8.2.17
# Sat, 16 Mar 2024 01:26:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.17.tar.xz.asc
# Sat, 16 Mar 2024 01:26:54 GMT
ENV PHP_SHA256=1cc4ef733ba58f6557db648012471f1916e5bac316303aa165535bedab08ee35
# Sat, 16 Mar 2024 01:27:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 16 Mar 2024 01:27:01 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 16 Mar 2024 01:34:28 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 16 Mar 2024 01:34:29 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 16 Mar 2024 01:34:30 GMT
RUN docker-php-ext-enable sodium
# Sat, 16 Mar 2024 01:34:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 16 Mar 2024 01:34:30 GMT
WORKDIR /var/www/html
# Sat, 16 Mar 2024 01:34:30 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 16 Mar 2024 01:34:30 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Mar 2024 01:34:30 GMT
EXPOSE 9000
# Sat, 16 Mar 2024 01:34:30 GMT
CMD ["php-fpm"]
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -eux; 	version='6.5-RC4'; 	sha1='2c93035e42009d5ae37ee5be7e6738e1dfa04102'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
VOLUME [/var/www/html]
# Thu, 28 Mar 2024 19:03:12 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 19:03:12 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af252c8885a7ef2b1e85bce006efb30a7c8fb938ae8b50557ac99f551db6347d`  
		Last Modified: Sat, 16 Mar 2024 02:17:26 GMT  
		Size: 2.8 MB (2815736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41380dbb2574885d6efd5d44c03067af395ce0303f74e6aa7a08b639904dfb09`  
		Last Modified: Sat, 16 Mar 2024 02:17:26 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a0a53e1b8079d8de445a7d2739eb1b065a4df2f537d45e8ceaeeb4469bc61a2`  
		Last Modified: Sat, 16 Mar 2024 02:17:26 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1961129304a9e56071b3989396314104deec7f57f4ec58e2de45374508733ffd`  
		Last Modified: Sat, 16 Mar 2024 02:21:55 GMT  
		Size: 12.1 MB (12113513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98f5a93d7cf2072d6ddd072d0c166baa5e29647d2657ed4fd6b50f6354d03999`  
		Last Modified: Sat, 16 Mar 2024 02:21:54 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f3d94b2545fd86a41d944d2eff187b10c5151d5d5b902151083fd3e0f34a872`  
		Last Modified: Sat, 16 Mar 2024 02:22:18 GMT  
		Size: 12.9 MB (12913110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67218c81d7ccaffa5cdcf6f5a5d3c6f2b570ad1ace716a79563bc9599a37660d`  
		Last Modified: Sat, 16 Mar 2024 02:22:16 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff7aaf86ae784c3f102a655411104555cc858e6de4271868aafb2ed57813b644`  
		Last Modified: Sat, 16 Mar 2024 02:22:17 GMT  
		Size: 19.1 KB (19091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1686e682d675c78c25ab78d81c76d6845f30378b3401153dae89d7540da69975`  
		Last Modified: Sat, 16 Mar 2024 02:22:16 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5ce7d853c92a66340baf920d13c1537496cfe3c55a3e21b777f4e000331f5d`  
		Last Modified: Sat, 16 Mar 2024 19:18:50 GMT  
		Size: 28.8 MB (28770893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3fda6792770be4be662223bda515285ef650202e18840445a9a99bcb0079200`  
		Last Modified: Sat, 16 Mar 2024 19:18:50 GMT  
		Size: 3.8 MB (3805003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980d77fa7b69d68f4c04c463a4c146ebc567d1e61ae85959bfb79ea7579ce9e5`  
		Last Modified: Sat, 16 Mar 2024 19:18:49 GMT  
		Size: 59.4 KB (59362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb8ace0a8a524a9938d16b768e3f99d2615791372601502fe21f8fa691f6861`  
		Last Modified: Sat, 16 Mar 2024 19:18:49 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7654c0c3e5fb570b2e726a18df45bab3930de4dd35efc0844b59c873fd02fa72`  
		Last Modified: Fri, 29 Mar 2024 00:55:26 GMT  
		Size: 24.5 MB (24525320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ef5b9d68c7aa6aba20f18d6dd49c617c340855673cb05b8fb7eef8474b0caa`  
		Last Modified: Fri, 29 Mar 2024 00:55:25 GMT  
		Size: 2.4 KB (2352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4575a789ab4945659cecead8ea90b5df556a8c6c43ea97fe629e6d781e22530`  
		Last Modified: Fri, 29 Mar 2024 00:55:25 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.5-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:9572f050e52bb94af3370d641a5ac1f3032a7e6850bf368ec58c8ae682daceb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1060721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73b131dc02a434fde02897ccdda37a18c0da5a91c1a8fb02a25681e5f2b335be`

```dockerfile
```

-	Layers:
	-	`sha256:be881ae0132183a3be5977eaed610d4ab4bd82c1d20d959881b52cda46239734`  
		Last Modified: Fri, 29 Mar 2024 00:55:25 GMT  
		Size: 1.0 MB (1012638 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9ab9f0926fa207ae0c27418c5c65bcc3d95e3c819a69386d05d824d47482148`  
		Last Modified: Fri, 29 Mar 2024 00:55:25 GMT  
		Size: 48.1 KB (48083 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.5-php8.2-fpm-alpine` - linux; 386

```console
$ docker pull wordpress@sha256:946b26d0b6688ea42da236563802c53758c3cf0804ac3e25b1064c071af7969c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88802188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a1f6140b5e666e468fc5747a9aad1e9d4c5a0347bd1e9f3ee2ab3caa5d63fd1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 01:59:39 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 16 Mar 2024 01:59:41 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 16 Mar 2024 01:59:42 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 16 Mar 2024 01:59:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 16 Mar 2024 01:59:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 16 Mar 2024 01:59:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 16 Mar 2024 01:59:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 16 Mar 2024 01:59:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 16 Mar 2024 03:31:37 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 16 Mar 2024 03:31:37 GMT
ENV PHP_VERSION=8.2.17
# Sat, 16 Mar 2024 03:31:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.17.tar.xz.asc
# Sat, 16 Mar 2024 03:31:37 GMT
ENV PHP_SHA256=1cc4ef733ba58f6557db648012471f1916e5bac316303aa165535bedab08ee35
# Sat, 16 Mar 2024 03:31:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 16 Mar 2024 03:31:45 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 16 Mar 2024 03:45:09 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 16 Mar 2024 03:45:10 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 16 Mar 2024 03:45:11 GMT
RUN docker-php-ext-enable sodium
# Sat, 16 Mar 2024 03:45:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 16 Mar 2024 03:45:11 GMT
WORKDIR /var/www/html
# Sat, 16 Mar 2024 03:45:12 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 16 Mar 2024 03:45:12 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Mar 2024 03:45:12 GMT
EXPOSE 9000
# Sat, 16 Mar 2024 03:45:12 GMT
CMD ["php-fpm"]
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -eux; 	version='6.5-RC4'; 	sha1='2c93035e42009d5ae37ee5be7e6738e1dfa04102'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
VOLUME [/var/www/html]
# Thu, 28 Mar 2024 19:03:12 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 19:03:12 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a52b85e4d8e4d0e4048cab06c149fd0b6d64c5a5f04ec3a3f7c0ab4d4a3d8e6`  
		Last Modified: Sat, 16 Mar 2024 04:58:57 GMT  
		Size: 2.8 MB (2825337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d00dcc91f58845575e9487816e58609662888d41b2facfcf6128056ee483579`  
		Last Modified: Sat, 16 Mar 2024 04:58:56 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3264601b4fa42c37a2b6f6e47b5c8cb1c963b67ee7e15c2c18d17f2fd035a3fa`  
		Last Modified: Sat, 16 Mar 2024 04:58:56 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528b6e37950eea9d64eb1d1ae3331b5af80b18a518f6fea7c9878c5d64d17d4e`  
		Last Modified: Sat, 16 Mar 2024 05:04:12 GMT  
		Size: 12.1 MB (12113517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f208142f76d41a0d8efad041368bd0e3c8c1c490b4c79a30cfb843ffcd223a23`  
		Last Modified: Sat, 16 Mar 2024 05:04:11 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37317c0b0f35b125ce18481d91aed0ce0cdde047aef28291312dfffd25484626`  
		Last Modified: Sat, 16 Mar 2024 05:04:41 GMT  
		Size: 13.2 MB (13197042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077bb39dd57aaca27f6900ef3fb8b52e1defe2c8d69885a712d3dcb9a5a5fa5f`  
		Last Modified: Sat, 16 Mar 2024 05:04:37 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c7231106360d90394561e05014d40a62bfacb4e79ee81d75bda20969717e78`  
		Last Modified: Sat, 16 Mar 2024 05:04:38 GMT  
		Size: 19.3 KB (19300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a695ebe9213f955058e7f3243c8fe6aa0312c132f27f596d46027123420625a`  
		Last Modified: Sat, 16 Mar 2024 05:04:38 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c6fc26eb730064e2165bf50430095b072ff9bbfbef0a909419db2e6552f91e`  
		Last Modified: Fri, 29 Mar 2024 00:53:23 GMT  
		Size: 28.9 MB (28877153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7878666ab1f14cde089953ad6853c4637e9cdafc6138fb228036976a082241e9`  
		Last Modified: Fri, 29 Mar 2024 00:53:23 GMT  
		Size: 3.9 MB (3922916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fb6e84264b5ac7458b0aa8275d7cb14b6239c0dac6a30a04140e847f8af90e`  
		Last Modified: Fri, 29 Mar 2024 00:53:22 GMT  
		Size: 59.4 KB (59396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f63c4d3b35fa25241b797049e35dc9195b27d94001e8ee51147a8451d00e83f`  
		Last Modified: Fri, 29 Mar 2024 00:53:22 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65056a75da6e17187d5284ff9f6a8d292584fbeef845ae78423a6a30c0704398`  
		Last Modified: Fri, 29 Mar 2024 00:53:24 GMT  
		Size: 24.5 MB (24525322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66adc349bfc8ee713a143c92d1453cd17a2645791d1b008de3c3fb5f18f0b79e`  
		Last Modified: Fri, 29 Mar 2024 00:53:23 GMT  
		Size: 2.3 KB (2345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:791689526180cffcec49f292253fd21424093319995458aa139ecc06953445e0`  
		Last Modified: Fri, 29 Mar 2024 00:53:24 GMT  
		Size: 1.7 KB (1726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.5-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:8482c793d2c0b2709dc0e2306cba29beb615f6e53ea404a7c3dbcbb2f7f78efe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1062206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4f08704d365da4432c7f97fbb0245dcb1610cc5a6d5d798a622e9bd20b0b1ce`

```dockerfile
```

-	Layers:
	-	`sha256:abbfa3908ac4432c5196a3e2e927fbbf1429888971170b9126750d98aba9a3cf`  
		Last Modified: Fri, 29 Mar 2024 00:53:22 GMT  
		Size: 1.0 MB (1012574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9094444d712b556cdbbca2e5f8b78a9f46f1ea0af1665072d3c277da3cc32659`  
		Last Modified: Fri, 29 Mar 2024 00:53:22 GMT  
		Size: 49.6 KB (49632 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.5-php8.2-fpm-alpine` - linux; ppc64le

```console
$ docker pull wordpress@sha256:a4cca4f4d0bc68bfda3aa7c93355616d66624d24200cfbf9e10c12b35dc6643c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.6 MB (89573185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862201455a75cbff946d3d6d18ad9180ec68ae35e53a03fc0d2a2e02c55d77c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:32:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 16 Mar 2024 05:32:10 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 16 Mar 2024 05:32:11 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 16 Mar 2024 05:32:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 16 Mar 2024 05:32:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 16 Mar 2024 05:32:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 16 Mar 2024 05:32:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 16 Mar 2024 05:32:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 16 Mar 2024 06:15:55 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 16 Mar 2024 06:15:56 GMT
ENV PHP_VERSION=8.2.17
# Sat, 16 Mar 2024 06:15:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.17.tar.xz.asc
# Sat, 16 Mar 2024 06:15:56 GMT
ENV PHP_SHA256=1cc4ef733ba58f6557db648012471f1916e5bac316303aa165535bedab08ee35
# Sat, 16 Mar 2024 06:16:04 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 16 Mar 2024 06:16:05 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 16 Mar 2024 06:21:22 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 16 Mar 2024 06:21:23 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 16 Mar 2024 06:21:25 GMT
RUN docker-php-ext-enable sodium
# Sat, 16 Mar 2024 06:21:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 16 Mar 2024 06:21:26 GMT
WORKDIR /var/www/html
# Sat, 16 Mar 2024 06:21:28 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 16 Mar 2024 06:21:28 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Mar 2024 06:21:29 GMT
EXPOSE 9000
# Sat, 16 Mar 2024 06:21:29 GMT
CMD ["php-fpm"]
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -eux; 	version='6.5-RC4'; 	sha1='2c93035e42009d5ae37ee5be7e6738e1dfa04102'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
VOLUME [/var/www/html]
# Thu, 28 Mar 2024 19:03:12 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 19:03:12 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8351cc51b7233ca6780794a860d1cb9c98abff8e8277d2b87c1fafd5d06239d8`  
		Last Modified: Sat, 16 Mar 2024 06:55:33 GMT  
		Size: 2.8 MB (2842850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83541649479862a60e6e0a63881477379ac3ebccf9b657c4646de7eb1d4dc0f7`  
		Last Modified: Sat, 16 Mar 2024 06:55:32 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b3f7fb8aafed95ce8f9c79f9af65ce6e4439edfd71c1ba169b88443d61e05a`  
		Last Modified: Sat, 16 Mar 2024 06:55:32 GMT  
		Size: 266.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095e8023220b266f01152cf2f07a609f6efea7d540ce1241b802e17169cfbf6e`  
		Last Modified: Sat, 16 Mar 2024 07:01:00 GMT  
		Size: 12.1 MB (12113519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f99c2e90dd3010ebdd1bd0666b5618166f0804822beb402b9e29f7a0d6c573`  
		Last Modified: Sat, 16 Mar 2024 07:00:59 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b932d1477133fb91aa1824fd4a9a98fadf55964c1374912f118d152129a7c2`  
		Last Modified: Sat, 16 Mar 2024 07:01:30 GMT  
		Size: 13.3 MB (13340672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8c26f8c26194524ea482733e6245a47a9251075f4b2a05f875dff2c5c1eab8`  
		Last Modified: Sat, 16 Mar 2024 07:01:27 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e11a9c70051f3f297fd7448021dd50e5c18a4832f4a8f7251e924cea995e054f`  
		Last Modified: Sat, 16 Mar 2024 07:01:27 GMT  
		Size: 19.1 KB (19111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e0a4842e7bc51beaf585e0e8a67f421049d0976f1599eeb212ffd003515aae3`  
		Last Modified: Sat, 16 Mar 2024 07:01:27 GMT  
		Size: 9.2 KB (9175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06a63aec4ad0644573f008fb233157b08141ce82f3eb18cef81270c0db90121`  
		Last Modified: Sat, 16 Mar 2024 15:27:48 GMT  
		Size: 29.4 MB (29379301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a24bcfd51231a9b2ca7163378ae73e37ce2f9214cd7fb1e56d72dd50c754da8`  
		Last Modified: Sat, 16 Mar 2024 15:27:48 GMT  
		Size: 3.9 MB (3916512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ea899cb06d80e4df282f1041d6aeef97dd367eb5e7c45d2b9d0f62a13f9a5d`  
		Last Modified: Sat, 16 Mar 2024 15:27:47 GMT  
		Size: 59.4 KB (59413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce2aac5febc7d3a7fa62817514035af616e239064ed604649e5ea6731f7184b`  
		Last Modified: Sat, 16 Mar 2024 15:27:47 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:701bfe61a7923fce42064080fb1f0470e93cdfd9e4d7e0c32961f11234120271`  
		Last Modified: Fri, 29 Mar 2024 01:17:25 GMT  
		Size: 24.5 MB (24525323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92873fa2d306cefd631da58acf29b9c82c49f185fd4149626e6ef62eb471a3a`  
		Last Modified: Fri, 29 Mar 2024 01:17:24 GMT  
		Size: 2.4 KB (2353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d8fe0473dc326a35ab165398ba032a9e7792d59de7f78566a7b63df065ec78`  
		Last Modified: Fri, 29 Mar 2024 01:17:24 GMT  
		Size: 1.7 KB (1735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.5-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:1990a0e7c8f8d3ac23b628f80040caf2a900e470f7149c457b6467817f11f52d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1058858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:321b273626168ca941e3b23819e4c5dd0824e1e008a1224090dbd0ff3cf72d38`

```dockerfile
```

-	Layers:
	-	`sha256:b0a55c1ff54cc6335e4f76c45dadd3602d599c67cc7d4eefe5149556b4d4db9c`  
		Last Modified: Fri, 29 Mar 2024 01:17:24 GMT  
		Size: 1.0 MB (1010723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86e10f139eaff8e74fe6f1f200998ba9966cdae306e7e4ac09231c12d715c6fa`  
		Last Modified: Fri, 29 Mar 2024 01:17:23 GMT  
		Size: 48.1 KB (48135 bytes)  
		MIME: application/vnd.in-toto+json

### `wordpress:beta-6.5-php8.2-fpm-alpine` - linux; s390x

```console
$ docker pull wordpress@sha256:09a6a9315ec5160c0bad957cd025ad65313874a2df55fb7e29d31c79e0152840
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.0 MB (89041689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecc0f72e78df9786ae5257571ffa212ee9a33db02d66f10dae6c48b4fa4b1afe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 12:14:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 16 Mar 2024 12:14:23 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 16 Mar 2024 12:14:23 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 16 Mar 2024 12:14:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 16 Mar 2024 12:14:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 16 Mar 2024 12:14:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 16 Mar 2024 12:14:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 16 Mar 2024 12:14:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 16 Mar 2024 13:13:41 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 16 Mar 2024 13:13:41 GMT
ENV PHP_VERSION=8.2.17
# Sat, 16 Mar 2024 13:13:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.17.tar.xz.asc
# Sat, 16 Mar 2024 13:13:41 GMT
ENV PHP_SHA256=1cc4ef733ba58f6557db648012471f1916e5bac316303aa165535bedab08ee35
# Sat, 16 Mar 2024 13:13:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 16 Mar 2024 13:13:47 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 16 Mar 2024 13:20:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 16 Mar 2024 13:20:55 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 16 Mar 2024 13:20:56 GMT
RUN docker-php-ext-enable sodium
# Sat, 16 Mar 2024 13:20:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 16 Mar 2024 13:20:57 GMT
WORKDIR /var/www/html
# Sat, 16 Mar 2024 13:20:57 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 16 Mar 2024 13:20:57 GMT
STOPSIGNAL SIGQUIT
# Sat, 16 Mar 2024 13:20:57 GMT
EXPOSE 9000
# Sat, 16 Mar 2024 13:20:57 GMT
CMD ["php-fpm"]
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		freetype-dev 		icu-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-install -j "$(nproc)" 		bcmath 		exif 		gd 		intl 		mysqli 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 	runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .wordpress-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
RUN set -eux; 	version='6.5-RC4'; 	sha1='2c93035e42009d5ae37ee5be7e6738e1dfa04102'; 		curl -o wordpress.tar.gz -fL "https://wordpress.org/wordpress-$version.tar.gz"; 	echo "$sha1 *wordpress.tar.gz" | sha1sum -c -; 		tar -xzf wordpress.tar.gz -C /usr/src/; 	rm wordpress.tar.gz; 		[ ! -e /usr/src/wordpress/.htaccess ]; 	{ 		echo '# BEGIN WordPress'; 		echo ''; 		echo 'RewriteEngine On'; 		echo 'RewriteRule .* - [E=HTTP_AUTHORIZATION:%{HTTP:Authorization}]'; 		echo 'RewriteBase /'; 		echo 'RewriteRule ^index\.php$ - [L]'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-f'; 		echo 'RewriteCond %{REQUEST_FILENAME} !-d'; 		echo 'RewriteRule . /index.php [L]'; 		echo ''; 		echo '# END WordPress'; 	} > /usr/src/wordpress/.htaccess; 		chown -R www-data:www-data /usr/src/wordpress; 	mkdir wp-content; 	for dir in /usr/src/wordpress/wp-content/*/ cache; do 		dir="$(basename "${dir%/}")"; 		mkdir "wp-content/$dir"; 	done; 	chown -R www-data:www-data wp-content; 	chmod -R 1777 wp-content # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
VOLUME [/var/www/html]
# Thu, 28 Mar 2024 19:03:12 GMT
COPY wp-config-docker.php /usr/src/wordpress/ # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 28 Mar 2024 19:03:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 28 Mar 2024 19:03:12 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01acb6f7038172bde2ff1bda8f1d1adcc1ab12d84810d2aa5acf1971fb749a71`  
		Last Modified: Sat, 16 Mar 2024 14:18:54 GMT  
		Size: 2.9 MB (2940586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce621a8f961e9b9055c4dc41216537b964b8ad5eea518ed588f6d169fba2dae`  
		Last Modified: Sat, 16 Mar 2024 14:18:53 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c74ef430cf1ac125831e6082e733c08a93c0954eddcb8ddb042b1c73977b0c9`  
		Last Modified: Sat, 16 Mar 2024 14:18:53 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a13aa0a5ed652d9247960dbd18d7fc355d6f1f1cdd0f86a8d8b67f910140ee48`  
		Last Modified: Sat, 16 Mar 2024 14:23:13 GMT  
		Size: 12.1 MB (12113520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d0dbcdd7e74977eda60ad9c053d773a684dd5c14c5ead4afb9f95b7959d5902`  
		Last Modified: Sat, 16 Mar 2024 14:23:13 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9173902e73aea2f2bea353f0d223b10b01cf9c6d5940a9014c24c2f28ce3bbf`  
		Last Modified: Sat, 16 Mar 2024 14:23:38 GMT  
		Size: 12.6 MB (12600101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a6018479404815c617467b2b0d22a385f8a708b7c3306d64daaf198401db9d`  
		Last Modified: Sat, 16 Mar 2024 14:23:36 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e92a68097d953b2738228e068fdd46cb76a620cee61d9cb105ad4f5f3fc6f770`  
		Last Modified: Sat, 16 Mar 2024 14:23:36 GMT  
		Size: 19.1 KB (19110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3892e593a782b5ae5a9500c5ae13c1a8bd2a80e34638d8ae1ed17064ba08ab9`  
		Last Modified: Sat, 16 Mar 2024 14:23:36 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:808c2ee248b6a8b150a1b876ce341bc50111fa16ac419036d90c8743e398ca07`  
		Last Modified: Sun, 17 Mar 2024 16:16:38 GMT  
		Size: 29.6 MB (29624806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0487d32dc48191f93ee237478a528d3f476f9613a1315fb0421aba948d22f010`  
		Last Modified: Sun, 17 Mar 2024 16:16:37 GMT  
		Size: 3.9 MB (3898074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7092ce9eb97e7d65d51d4ba8c87aa1bbe00df9d57311f6081b87667ba9451b2`  
		Last Modified: Sun, 17 Mar 2024 16:16:37 GMT  
		Size: 59.4 KB (59417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f6dbd065e1957482d34338c753f66ca7fbf9ea5555771c511d82405668efc1e`  
		Last Modified: Sun, 17 Mar 2024 16:16:37 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff44ea410ad2091ae481f8710b61dd2959915e5f3017be9f7cb2d7ea3e88ba80`  
		Last Modified: Fri, 29 Mar 2024 02:04:27 GMT  
		Size: 24.5 MB (24525322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9a2f87f19a6d551aaa5d23833e4c318dd34fcd1a3c11042ab9de9831388bbcd`  
		Last Modified: Fri, 29 Mar 2024 02:04:27 GMT  
		Size: 2.4 KB (2352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f26368af01d6c887df857c99f620673ecc77a464e2ea9df1100b92b4746be5`  
		Last Modified: Fri, 29 Mar 2024 02:04:27 GMT  
		Size: 1.7 KB (1732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `wordpress:beta-6.5-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull wordpress@sha256:a7d2d16963d281097de6444bd9733dea0bec7a9cf53fcd37ff8022928cd78d46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1058727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ed1d12031276eebdd36b2de182e284ad5ecba4cdc2120f4f49c971d23cf97e3`

```dockerfile
```

-	Layers:
	-	`sha256:d583eab346076e789ded85a96380e13e81efd2d09e36fa4ff5f5c7ea5ecf0a1e`  
		Last Modified: Fri, 29 Mar 2024 02:04:26 GMT  
		Size: 1.0 MB (1010665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af1bed78120595a7439bfbf1359dcf7bf7361b2090c6b690b8b18a6e06bdd235`  
		Last Modified: Fri, 29 Mar 2024 02:04:26 GMT  
		Size: 48.1 KB (48062 bytes)  
		MIME: application/vnd.in-toto+json
