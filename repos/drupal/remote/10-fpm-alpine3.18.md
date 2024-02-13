## `drupal:10-fpm-alpine3.18`

```console
$ docker pull drupal@sha256:0ec6760e10ddddc1c26628d08faf0cb6f22f3c93c14214821dc96d61335b406b
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

### `drupal:10-fpm-alpine3.18` - linux; amd64

```console
$ docker pull drupal@sha256:66c08a8e006a47660eefe9a932b7fab12b6e8856cf9f721438a13a14c722aa04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53276913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08e5210443a914e697b9cfcb77dcd86792d2d7325faca748f829bf7d03b6d78e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 04:35:36 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 27 Jan 2024 04:35:37 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 27 Jan 2024 04:35:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 27 Jan 2024 04:35:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 27 Jan 2024 04:35:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 27 Jan 2024 04:35:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 04:35:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 04:35:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 27 Jan 2024 04:59:04 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 27 Jan 2024 04:59:04 GMT
ENV PHP_VERSION=8.2.15
# Sat, 27 Jan 2024 04:59:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Sat, 27 Jan 2024 04:59:04 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Sat, 27 Jan 2024 04:59:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 27 Jan 2024 04:59:11 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 27 Jan 2024 05:06:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 27 Jan 2024 05:06:32 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 27 Jan 2024 05:06:33 GMT
RUN docker-php-ext-enable sodium
# Sat, 27 Jan 2024 05:06:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 27 Jan 2024 05:06:33 GMT
WORKDIR /var/www/html
# Sat, 27 Jan 2024 05:06:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 27 Jan 2024 05:06:34 GMT
STOPSIGNAL SIGQUIT
# Sat, 27 Jan 2024 05:06:34 GMT
EXPOSE 9000
# Sat, 27 Jan 2024 05:06:34 GMT
CMD ["php-fpm"]
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
ENV DRUPAL_VERSION=10.2.3
# Thu, 08 Feb 2024 04:27:17 GMT
WORKDIR /opt/drupal
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cdd08544f3979add7a1135032c708137f3a42762bb48446a036a80d16a9c796`  
		Last Modified: Sat, 27 Jan 2024 05:37:35 GMT  
		Size: 2.7 MB (2682495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6f2d92bc3b905b7db953512ceb84266e42e19d498f9d6c4c91170b5360cf3b2`  
		Last Modified: Sat, 27 Jan 2024 05:37:35 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7427b71a5dd639a1a4b6123f46f2d5c6e6f8bd6d7bb8f8ca879516220b330d9`  
		Last Modified: Sat, 27 Jan 2024 05:37:35 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f801e38cc453bae80e9cee6235db4f008f1447b650afbf9346f56884edcf744`  
		Last Modified: Sat, 27 Jan 2024 05:39:48 GMT  
		Size: 12.1 MB (12096231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026b629301171723dcd4799947ae6722f19224c87ecb510f72b154728161dc69`  
		Last Modified: Sat, 27 Jan 2024 05:39:47 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82bf9f6108fab233120fa1cf96324353639e10fa5796394d046cd2b0014dc44e`  
		Last Modified: Sat, 27 Jan 2024 05:40:05 GMT  
		Size: 12.7 MB (12667249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d43bc1a4680fa531af4c04d4acf145dd98c410572df19ca98fa4b464d3a8b3d`  
		Last Modified: Sat, 27 Jan 2024 05:40:03 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c22ea3fca13fe9fc6fb4fabfc88775d453575f9b3e60fe868c3c5952337b09`  
		Last Modified: Sat, 27 Jan 2024 05:40:03 GMT  
		Size: 18.9 KB (18948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819d53d9d8417ab0e2886fd612312e2a55de3b93c04255ae628d3a1d751ce058`  
		Last Modified: Sat, 27 Jan 2024 05:40:03 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93da3428f6a517a7ab2823f4251418d352e9cd41582cf8674a05fc345b02b624`  
		Last Modified: Mon, 12 Feb 2024 21:55:22 GMT  
		Size: 2.4 MB (2439145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3068d4446a417aff1f6d9e3aa1e002a12c37e148cfa1728feb76117e1c09e1`  
		Last Modified: Mon, 12 Feb 2024 21:55:22 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d2355ca8b63b47103bf34f8271756b8ea72a965349a9e41c049e25e359c16b`  
		Last Modified: Mon, 12 Feb 2024 21:55:22 GMT  
		Size: 721.6 KB (721579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d636fce049e464f702d63d5b644be038d8d56345a1f02fce4a0f6726f00fc229`  
		Last Modified: Mon, 12 Feb 2024 21:55:22 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c40132c32535a85f01cdbd9a72f0b54c8ac85d837c1dc704f5b097609b301be`  
		Last Modified: Mon, 12 Feb 2024 21:55:24 GMT  
		Size: 19.2 MB (19234648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.18` - unknown; unknown

```console
$ docker pull drupal@sha256:61bade06223acca1fc6d137a7916fb562c884ee468477284332c7e0ef25d5c67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **845.3 KB (845294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9d110d0b779db9503c02d5fa8aae95df0ded208dfc2d7e8ff06021bdb338b6d`

```dockerfile
```

-	Layers:
	-	`sha256:3f3e00cfe076fccec67f21fb4e1a95d92d7bd3a282ad5d1a23a828dd102748e4`  
		Last Modified: Mon, 12 Feb 2024 21:55:22 GMT  
		Size: 809.5 KB (809467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85ccb0305499d97a5980a5ca92c62cb1ac91ad0fd0c109c6e61dbffc2fa0ebeb`  
		Last Modified: Mon, 12 Feb 2024 21:55:22 GMT  
		Size: 35.8 KB (35827 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.18` - linux; arm variant v6

```console
$ docker pull drupal@sha256:10ac6d4208fc09aab79385a7e57cc5da718625f61cfccb157fe5a3ed55a17260
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51315764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7cae6a4c576a25e5bb98fa012c14e161eed15ef923c3a5b71925b7d3d26ad10`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 05:34:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 27 Jan 2024 05:34:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 27 Jan 2024 05:34:26 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 27 Jan 2024 05:34:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 27 Jan 2024 05:34:27 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 27 Jan 2024 05:34:27 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 05:34:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 05:34:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 27 Jan 2024 06:06:46 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 27 Jan 2024 06:06:46 GMT
ENV PHP_VERSION=8.2.15
# Sat, 27 Jan 2024 06:06:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Sat, 27 Jan 2024 06:06:47 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Sat, 27 Jan 2024 06:06:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 27 Jan 2024 06:06:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 27 Jan 2024 06:17:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 27 Jan 2024 06:17:38 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 27 Jan 2024 06:17:40 GMT
RUN docker-php-ext-enable sodium
# Sat, 27 Jan 2024 06:17:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 27 Jan 2024 06:17:40 GMT
WORKDIR /var/www/html
# Sat, 27 Jan 2024 06:17:42 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 27 Jan 2024 06:17:42 GMT
STOPSIGNAL SIGQUIT
# Sat, 27 Jan 2024 06:17:42 GMT
EXPOSE 9000
# Sat, 27 Jan 2024 06:17:43 GMT
CMD ["php-fpm"]
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
ENV DRUPAL_VERSION=10.2.3
# Thu, 08 Feb 2024 04:27:17 GMT
WORKDIR /opt/drupal
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62daf641b680894f28bde55f9b558dcd71afae65a613d7289839b0ccc1c59935`  
		Last Modified: Sat, 27 Jan 2024 06:45:53 GMT  
		Size: 2.7 MB (2688488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56bbdb0364f95226b0ddc30b86f27a68af4cb1b836ca10db53e713f447ff13bc`  
		Last Modified: Sat, 27 Jan 2024 06:45:52 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72425da7bbe49396c65f29cc1da85be4ba13d8917fa75ad08fd7a48974409d13`  
		Last Modified: Sat, 27 Jan 2024 06:45:52 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74fb304f89cdbc91adf007986f2dd21ddfcc3aecd6e7192b4714bab9309056c4`  
		Last Modified: Sat, 27 Jan 2024 06:47:46 GMT  
		Size: 12.1 MB (12096223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3aee5324cb190c8d4132867fb50bb0ec9717d1038dadb6d5f331a2ef5fb1fb7`  
		Last Modified: Sat, 27 Jan 2024 06:47:45 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95595db2f75ed5879350ad97a58301de45372c27a9c7e1e3c4ad4ce0fa4b593`  
		Last Modified: Sat, 27 Jan 2024 06:48:03 GMT  
		Size: 11.5 MB (11539258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b7e7c81d2a6e86f8de8d779b312f2e1c63746a1f5e649ce8e310129ff9eb73`  
		Last Modified: Sat, 27 Jan 2024 06:48:01 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228f218bbe867f3375674ebfb8d5c18a830b2fc7965a10f14ddfd6a8ee673811`  
		Last Modified: Sat, 27 Jan 2024 06:48:01 GMT  
		Size: 18.8 KB (18774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e73f15ff841bcd0e50a41930d4099311958501e3f07a8111019e8007f3b145fb`  
		Last Modified: Sat, 27 Jan 2024 06:48:01 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c343dcb26d2b31bf767a2f7a96e764ef2df7ff5689146d0a35df21f1e4c7b8a3`  
		Last Modified: Mon, 12 Feb 2024 22:03:35 GMT  
		Size: 1.9 MB (1855479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1cb6138dcaa8314982bef707ef875425c600030d4b6b5a58c749634f8ed946`  
		Last Modified: Mon, 12 Feb 2024 22:03:34 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e14af732d8c20da4f1f7182165afb936a2b63e2cc097c3095a60e4e37b8c4d70`  
		Last Modified: Mon, 12 Feb 2024 22:03:35 GMT  
		Size: 721.6 KB (721580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e03cc7dbe7798fb01e6db753ad93fb28fd86bc03901e1f57f1116587db71d5`  
		Last Modified: Mon, 12 Feb 2024 22:03:34 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c6b709a6bdc91311598f5a6970e1959ba37b19c2cc2b2e1fb6353ab40bc5a54`  
		Last Modified: Mon, 12 Feb 2024 22:03:36 GMT  
		Size: 19.2 MB (19234814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.18` - unknown; unknown

```console
$ docker pull drupal@sha256:84501d8d451fb9153469d5140f2a0d412f1de6f421f019c076ced9bc2a436596
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.5 KB (33483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9551385320fc9576d83081c751769dc100bd8af7109939c1b9929d01411f45e0`

```dockerfile
```

-	Layers:
	-	`sha256:e9ac0c02a1f9e7120185f227b74c9d8dab31ec9998885165b687b029a554a823`  
		Last Modified: Mon, 12 Feb 2024 22:03:34 GMT  
		Size: 33.5 KB (33483 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.18` - linux; arm variant v7

```console
$ docker pull drupal@sha256:a07c975f5466ac1927b4806b9226529eb42890f5b08472b48747a99fdc3823e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50057804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a8daa0d05915cc0b4667e70cadce5c50bcc1cdadacf1145d0d85b3b49d97db`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 06:45:01 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 27 Jan 2024 06:45:02 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 27 Jan 2024 06:45:03 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 27 Jan 2024 06:45:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 27 Jan 2024 06:45:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 27 Jan 2024 06:45:03 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 06:45:03 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 06:45:03 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 27 Jan 2024 07:04:16 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 27 Jan 2024 07:04:16 GMT
ENV PHP_VERSION=8.2.15
# Sat, 27 Jan 2024 07:04:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Sat, 27 Jan 2024 07:04:17 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Sat, 27 Jan 2024 07:04:23 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 27 Jan 2024 07:04:23 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 27 Jan 2024 07:10:10 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 27 Jan 2024 07:10:10 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 27 Jan 2024 07:10:11 GMT
RUN docker-php-ext-enable sodium
# Sat, 27 Jan 2024 07:10:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 27 Jan 2024 07:10:11 GMT
WORKDIR /var/www/html
# Sat, 27 Jan 2024 07:10:12 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 27 Jan 2024 07:10:12 GMT
STOPSIGNAL SIGQUIT
# Sat, 27 Jan 2024 07:10:12 GMT
EXPOSE 9000
# Sat, 27 Jan 2024 07:10:12 GMT
CMD ["php-fpm"]
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
ENV DRUPAL_VERSION=10.2.3
# Thu, 08 Feb 2024 04:27:17 GMT
WORKDIR /opt/drupal
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8c0293e5cb723599572c9030f71f9f0162fdfef255b47fc3f6050ff6fe8df3`  
		Last Modified: Sat, 27 Jan 2024 07:34:33 GMT  
		Size: 2.5 MB (2528495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d8a4e0cfd121c4ed651cbed66fbdb50e920d2af857d4dfb1c5778237f334f0`  
		Last Modified: Sat, 27 Jan 2024 07:34:32 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3061407d5bd08863490376ebb46a63256157ce41f373da5cab4489e9ad19be`  
		Last Modified: Sat, 27 Jan 2024 07:34:32 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d17a02bb37183e5d592d8949629696d28cc0303e0635b5e9239f7ca6916be8f`  
		Last Modified: Sat, 27 Jan 2024 07:36:33 GMT  
		Size: 12.1 MB (12096231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3397fb578f2b024d66c8f9cff501e679402a2e6f429e4d9beb4bb9838e980771`  
		Last Modified: Sat, 27 Jan 2024 07:36:31 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62882933dfcdfd85a025051b7cb2a5eb83138f46000cf91870b21a09a2271f38`  
		Last Modified: Sat, 27 Jan 2024 07:36:48 GMT  
		Size: 10.8 MB (10821082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97ca07f1a9303b1315d5b3b9051236869f249df07b94aebc06592b6ddf9c432`  
		Last Modified: Sat, 27 Jan 2024 07:36:46 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa6997cc9af80494574151704590e3ff73ca203eff0be6dddaafd03134f4c867`  
		Last Modified: Sat, 27 Jan 2024 07:36:46 GMT  
		Size: 18.8 KB (18776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f80fdbaaa9ab81c67842774aca8bc4b97b4985271c164b3defbc95f3534170e`  
		Last Modified: Sat, 27 Jan 2024 07:36:46 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b5157752370ad67776fd9201d6dd10a42ee5941db974f718b1300ab85a7258`  
		Last Modified: Fri, 02 Feb 2024 15:51:08 GMT  
		Size: 1.7 MB (1721465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecc43974f9f6f96880e361847e04b5b69313a2f3ca61ebd299bb802b9e343611`  
		Last Modified: Fri, 02 Feb 2024 15:51:08 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b966586964cfc240c5d1da24df2303567633ea9dd340e1b974e2e240413730`  
		Last Modified: Mon, 12 Feb 2024 22:23:04 GMT  
		Size: 721.6 KB (721589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8792092fd615494a3f4b85a30f73785efc9dc79cd407f67f995b2a3f121850`  
		Last Modified: Mon, 12 Feb 2024 22:23:04 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:293c8e8bfd6996b64426ab546c290e987246270a11c37fc190271a8b29fc15bf`  
		Last Modified: Mon, 12 Feb 2024 22:23:05 GMT  
		Size: 19.2 MB (19234702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.18` - unknown; unknown

```console
$ docker pull drupal@sha256:dbbb15627ac1223722f03e17952b1499ee05aa3d8889709208f0e6350e9b4713
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **839.1 KB (839131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd2a2a655bf5c6327bcf210aa24d49115a6480613be94f2c4d58d3ee13f5a30c`

```dockerfile
```

-	Layers:
	-	`sha256:1d4230d618ba8effcc5f28cac225b5dab4f3f50c1476b25078cd7c1b4e743420`  
		Last Modified: Mon, 12 Feb 2024 22:23:04 GMT  
		Size: 807.1 KB (807059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:233af92766a9fea192d97ae3b376e45706c2e36818f85f2e5c2de9c7c8c2b0e0`  
		Last Modified: Mon, 12 Feb 2024 22:23:04 GMT  
		Size: 32.1 KB (32072 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:97f90473df6e7439b63991d45cd61766993e0109e6dabe50ff1868ceb2789f3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53568407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8cf42ddb55bc33fbb0d61b99a7e2a15ed19eac87829d0f2853bc278977d79dd`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 07:41:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 27 Jan 2024 07:41:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 27 Jan 2024 07:41:35 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 27 Jan 2024 07:41:35 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 27 Jan 2024 07:41:35 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 27 Jan 2024 07:41:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 07:41:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 07:41:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 27 Jan 2024 08:05:06 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 27 Jan 2024 08:05:06 GMT
ENV PHP_VERSION=8.2.15
# Sat, 27 Jan 2024 08:05:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Sat, 27 Jan 2024 08:05:06 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Sat, 27 Jan 2024 08:05:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 27 Jan 2024 08:05:13 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 27 Jan 2024 08:12:04 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 27 Jan 2024 08:12:05 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 27 Jan 2024 08:12:06 GMT
RUN docker-php-ext-enable sodium
# Sat, 27 Jan 2024 08:12:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 27 Jan 2024 08:12:06 GMT
WORKDIR /var/www/html
# Sat, 27 Jan 2024 08:12:06 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 27 Jan 2024 08:12:06 GMT
STOPSIGNAL SIGQUIT
# Sat, 27 Jan 2024 08:12:06 GMT
EXPOSE 9000
# Sat, 27 Jan 2024 08:12:06 GMT
CMD ["php-fpm"]
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
ENV DRUPAL_VERSION=10.2.3
# Thu, 08 Feb 2024 04:27:17 GMT
WORKDIR /opt/drupal
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4eb03fe552f5c8aa36cd79b78aa545592812821d1c3169cfeab7c2a2d2dfdc`  
		Last Modified: Sat, 27 Jan 2024 08:41:45 GMT  
		Size: 2.7 MB (2721116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ecb7467a02f797b3b358a87cd793e73d849cb2dee4668faafaea6ac9037dc7b`  
		Last Modified: Sat, 27 Jan 2024 08:41:44 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbe855ad31e7cd79a1f706abb3a6b77f7e1457b5fb9b89c943ad0e8eb99d6a0`  
		Last Modified: Sat, 27 Jan 2024 08:41:44 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:668e1297a24eb8494667895e01ee28dd6cc44e981089460ea0e662c9462aab42`  
		Last Modified: Sat, 27 Jan 2024 08:43:36 GMT  
		Size: 12.1 MB (12096223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8352cd48d6f5128d38ac5cbc0c30c63dec181d4b6e82e8729a06d0e4da6aac07`  
		Last Modified: Sat, 27 Jan 2024 08:43:35 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93b34edf664727029f0e28359adadc17c1e374090cbac579e5d6c3b120124063`  
		Last Modified: Sat, 27 Jan 2024 08:43:51 GMT  
		Size: 12.7 MB (12722715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a410e0dcbdd51891d07a6f1e38b29551c9713d35cdfc5a03aedda38e5ecb4caa`  
		Last Modified: Sat, 27 Jan 2024 08:43:50 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a849110782c82d3af560a8dd1a21dcf236ae3c7ae6eb9c712ac006bc07e5f276`  
		Last Modified: Sat, 27 Jan 2024 08:43:49 GMT  
		Size: 18.7 KB (18731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b560a4e1c6ec75a53d47e21254444d2f66c9be35d320411dadf7b78666c30d`  
		Last Modified: Sat, 27 Jan 2024 08:43:49 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2510f1bfe1138203109eeb8180419b89d0de9aff90be2b6e6c983ba480bba4a9`  
		Last Modified: Mon, 12 Feb 2024 22:36:56 GMT  
		Size: 2.7 MB (2705601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60c708c46e8e912125091057eedb45ad822e04c4973e2cfa52cd8c1048ff2e6`  
		Last Modified: Mon, 12 Feb 2024 22:36:55 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c88d30a23aa12f84fb6bdae0f8ed4d8aa7a5bec6684fb56bbd753eed2980f559`  
		Last Modified: Mon, 12 Feb 2024 22:36:56 GMT  
		Size: 721.6 KB (721579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b9d68a8c1a795587cdeec6d48a7d47f08e4c8eab4c93cbfb233b90fde627178`  
		Last Modified: Mon, 12 Feb 2024 22:36:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46662586ba20d2c64f824f7e764ad9e9483e477c872e9b702e8bd9710b08cae6`  
		Last Modified: Mon, 12 Feb 2024 22:36:57 GMT  
		Size: 19.2 MB (19235005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.18` - unknown; unknown

```console
$ docker pull drupal@sha256:329aac6a81ec3866e73ce35fb672f7e4bfe9c0eb6101a0d9653c540c6b50afb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **840.6 KB (840582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da42746c8e710e4c22a316405c2ca6e64dd80d73c1d079c78a0d897c52cdb7ed`

```dockerfile
```

-	Layers:
	-	`sha256:8ddb47b756764c835aad6c76d67e67941a4e49ca0d3d92eae36118ebc196c166`  
		Last Modified: Mon, 12 Feb 2024 22:36:56 GMT  
		Size: 807.0 KB (807010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ec1188102b3f93824faad7871572ebd980f3fcf4c5286704849a593847ce256`  
		Last Modified: Mon, 12 Feb 2024 22:36:55 GMT  
		Size: 33.6 KB (33572 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.18` - linux; 386

```console
$ docker pull drupal@sha256:5a3632b3559ebbd68e5326e779480fe483ea16faa7be8c0eb4e50768cd55fff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53346815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11af83bad076193ef5420c4c5fb5cdecbb6c1d2d9e0ca52db8a39cdb98f65c64`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 05:03:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 27 Jan 2024 05:03:36 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 27 Jan 2024 05:03:37 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 27 Jan 2024 05:03:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 27 Jan 2024 05:03:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 27 Jan 2024 05:03:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 05:03:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 05:03:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 27 Jan 2024 05:44:37 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 27 Jan 2024 05:44:37 GMT
ENV PHP_VERSION=8.2.15
# Sat, 27 Jan 2024 05:44:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Sat, 27 Jan 2024 05:44:38 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Sat, 27 Jan 2024 05:44:45 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 27 Jan 2024 05:44:45 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 27 Jan 2024 05:57:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 27 Jan 2024 05:57:18 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 27 Jan 2024 05:57:19 GMT
RUN docker-php-ext-enable sodium
# Sat, 27 Jan 2024 05:57:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 27 Jan 2024 05:57:19 GMT
WORKDIR /var/www/html
# Sat, 27 Jan 2024 05:57:20 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 27 Jan 2024 05:57:20 GMT
STOPSIGNAL SIGQUIT
# Sat, 27 Jan 2024 05:57:20 GMT
EXPOSE 9000
# Sat, 27 Jan 2024 05:57:20 GMT
CMD ["php-fpm"]
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
ENV DRUPAL_VERSION=10.2.3
# Thu, 08 Feb 2024 04:27:17 GMT
WORKDIR /opt/drupal
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d6d2f12df1b19df541851aca59cb3e004d030eea096ff568038497561d6df4`  
		Last Modified: Sat, 27 Jan 2024 06:47:46 GMT  
		Size: 2.7 MB (2727226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7c7b40044db0622103ed0e4a3fa021b8c4579d1677fd27d6e9116d5d8e48c5`  
		Last Modified: Sat, 27 Jan 2024 06:47:45 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0514c3edcfd0f1b5d370eb4eeea4e395ebadba50de6e4f2065e48323f90afaa`  
		Last Modified: Sat, 27 Jan 2024 06:47:45 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e8f8f9aaf2eea4df1b85e4628a54c8b0073bd654b43083f37dcbd87847039f`  
		Last Modified: Sat, 27 Jan 2024 06:50:05 GMT  
		Size: 12.1 MB (12096220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4c39955f5fa546aeba6e680501def51396adb7585e785f1306becc65dcb8bd`  
		Last Modified: Sat, 27 Jan 2024 06:50:04 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7eab1f5f41e9615431ee0397af9711bd6655f69c99466d436b91ee440eb207`  
		Last Modified: Sat, 27 Jan 2024 06:50:25 GMT  
		Size: 12.9 MB (12863923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4095d2395437680b1ba37f776809653f5085af22135e73eb0161f65b2f4d40e`  
		Last Modified: Sat, 27 Jan 2024 06:50:21 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0afc74d55666e6acce63bc2baec23a74feae2d5e5520c6ded6c0f7d5899685c6`  
		Last Modified: Sat, 27 Jan 2024 06:50:21 GMT  
		Size: 18.9 KB (18931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fdfe7d62868549b4e40e09d86b69fc5e9634713f1bcc5bc752fad98790264d5`  
		Last Modified: Sat, 27 Jan 2024 06:50:21 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a1bd5c5b3ad743606393cbf2c57f375926ee5244347e638a136090b86373b6`  
		Last Modified: Mon, 12 Feb 2024 21:55:26 GMT  
		Size: 2.4 MB (2430951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a98590e1c5ce8f7038217e660618b43600738f1b8a25285337bac432e14a3e0`  
		Last Modified: Mon, 12 Feb 2024 21:55:26 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65011b7600713c533c565e24d5274e1557979d8c08b289aab37991f21dfcdb3b`  
		Last Modified: Mon, 12 Feb 2024 21:55:26 GMT  
		Size: 721.6 KB (721582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56de85d9e3430d24618c28a545a1c707a0aa0c3dcffa8bd5ca2f36509145df24`  
		Last Modified: Mon, 12 Feb 2024 21:55:26 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebede5ccdcb092026a63c8bf913607e2b9db581f2ae40089cf411127edcb8c24`  
		Last Modified: Mon, 12 Feb 2024 21:55:28 GMT  
		Size: 19.2 MB (19234843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.18` - unknown; unknown

```console
$ docker pull drupal@sha256:f0afc5bed66f5f3261a24470107b69eab0a85cfa9a96f57e476db5e3fdbcaff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **845.2 KB (845192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:955f9c1d39bfb76c5a9fe1ceac433ccbe33e94055b97d0c828ca0fdedca33094`

```dockerfile
```

-	Layers:
	-	`sha256:ec6479e1bca7d4d6828c476bbc8c3b88a43b8e5ad19596596df300571c6376c9`  
		Last Modified: Mon, 12 Feb 2024 21:55:26 GMT  
		Size: 809.4 KB (809422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6bcea8348ed4b140eaafebecab0170bc14b580042b6e134b54fea6734a5ddd6`  
		Last Modified: Mon, 12 Feb 2024 21:55:26 GMT  
		Size: 35.8 KB (35770 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.18` - linux; ppc64le

```console
$ docker pull drupal@sha256:28701f591210f432c616a221e1a22be35f20d577de954ddc3fc3cf76b137bb64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53540075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca77e7be1b4179545d19ca85c6ed40d7f023cd06c90331ffdbddf36017f61b4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:35:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 27 Jan 2024 03:35:14 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 27 Jan 2024 03:35:16 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 27 Jan 2024 03:35:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 27 Jan 2024 03:35:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 27 Jan 2024 03:35:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 03:35:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 03:35:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 27 Jan 2024 03:53:12 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 27 Jan 2024 03:53:13 GMT
ENV PHP_VERSION=8.2.15
# Sat, 27 Jan 2024 03:53:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Sat, 27 Jan 2024 03:53:13 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Sat, 27 Jan 2024 03:53:21 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 27 Jan 2024 03:53:21 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 27 Jan 2024 03:58:37 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 27 Jan 2024 03:58:38 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 27 Jan 2024 03:58:40 GMT
RUN docker-php-ext-enable sodium
# Sat, 27 Jan 2024 03:58:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 27 Jan 2024 03:58:41 GMT
WORKDIR /var/www/html
# Sat, 27 Jan 2024 03:58:43 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 27 Jan 2024 03:58:43 GMT
STOPSIGNAL SIGQUIT
# Sat, 27 Jan 2024 03:58:44 GMT
EXPOSE 9000
# Sat, 27 Jan 2024 03:58:45 GMT
CMD ["php-fpm"]
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
ENV DRUPAL_VERSION=10.2.3
# Thu, 08 Feb 2024 04:27:17 GMT
WORKDIR /opt/drupal
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6a7a89d73e4ee9a28b90eadd129944afbcac67d80107089f98662fe261ca2da`  
		Last Modified: Sat, 27 Jan 2024 04:23:07 GMT  
		Size: 2.8 MB (2768094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73447972e8407c67ac46260eccde3029f8c096a6bcd6ecfa99d54c3b4f02551`  
		Last Modified: Sat, 27 Jan 2024 04:23:05 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af6a1382346f24ae6f048ea13c81e62a254330bb7b5b1baa18f25dc2245ec31`  
		Last Modified: Sat, 27 Jan 2024 04:23:05 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d26d11095ac7742d44ed5fe6dfc42a85ba37a339d94d00441bd94f10a7c66cea`  
		Last Modified: Sat, 27 Jan 2024 04:25:24 GMT  
		Size: 12.1 MB (12096212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f892a0cfe6d71980bad2d829e5113ca0f37c6c291e311fccd471b56df161b25e`  
		Last Modified: Sat, 27 Jan 2024 04:25:22 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e457523916d5f91210c5326377b36bf7035e81174d2b8464cb0ac996f748554b`  
		Last Modified: Sat, 27 Jan 2024 04:25:41 GMT  
		Size: 13.1 MB (13079700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e220a2585d78fc780ca69f5296ea403879de3ed9ba7bdb2ac4e8c5efe5a90d`  
		Last Modified: Sat, 27 Jan 2024 04:25:39 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd96abfb60ad44c09c51dc0a1a7ebf22777f02fe55fc0062ac8e351ab23fb7e7`  
		Last Modified: Sat, 27 Jan 2024 04:25:39 GMT  
		Size: 18.7 KB (18727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85643b45dd3f176eacab840d0ab964567bbe2adcb43b480d17c637b4523194ad`  
		Last Modified: Sat, 27 Jan 2024 04:25:39 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d2715d5cd0e3068ec9aa03bb717e2c0ddb275ced01defcd5d748769e12b28a`  
		Last Modified: Mon, 12 Feb 2024 21:31:18 GMT  
		Size: 2.3 MB (2258085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c50a17ef3e9ede4ce6a7fe236817180505a7711ec02170c61a6f43b14700ed91`  
		Last Modified: Mon, 12 Feb 2024 21:31:18 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10c0a0536d35a7c41f83fc19ea861af6bf5ca7ff954c3775a5b310e29425293`  
		Last Modified: Mon, 12 Feb 2024 21:31:18 GMT  
		Size: 721.6 KB (721584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e6a0852f0dcc74f649fc1ea85ce73df2e4bb7c815655e1ffc0db696c2c71abd`  
		Last Modified: Mon, 12 Feb 2024 21:31:18 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4037f901340f8f1dff90e33d497f0e889d74132e6aedccd77d8e07388fbc221`  
		Last Modified: Mon, 12 Feb 2024 22:24:47 GMT  
		Size: 19.2 MB (19235110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.18` - unknown; unknown

```console
$ docker pull drupal@sha256:baf1d51e7ac3e9fe93ec4bd60fff68a1dbf516dd1c32e384716007d09ae55b1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **837.4 KB (837412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9eedd93852e6e77a37516ccc5780f4dba56ccc9e064159045c63e0c3a0618e`

```dockerfile
```

-	Layers:
	-	`sha256:790366372430b84d6662a990ec0a8d9e07020c981b248d54f796a91e1ad48dbd`  
		Last Modified: Mon, 12 Feb 2024 22:24:46 GMT  
		Size: 805.4 KB (805413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5eb5fcb6bd184ed23a3425c63e09b5af6f4e1e856ddb5b89a9c01311cb662d21`  
		Last Modified: Mon, 12 Feb 2024 22:24:45 GMT  
		Size: 32.0 KB (31999 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.18` - linux; s390x

```console
$ docker pull drupal@sha256:74b90626bcf648565d55361345d6daeb8f5d15ba5fad03d7c90928e92bdf60cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51922627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e527d9d7cdf614a1f4a9d666bff12fb8705c959e6dfed90b11a2b23c5a2338f6`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 11:11:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 27 Jan 2024 11:11:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 27 Jan 2024 11:11:08 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 27 Jan 2024 11:11:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 27 Jan 2024 11:11:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 27 Jan 2024 11:11:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 11:11:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Jan 2024 11:11:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 27 Jan 2024 11:50:28 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Sat, 27 Jan 2024 11:50:28 GMT
ENV PHP_VERSION=8.2.15
# Sat, 27 Jan 2024 11:50:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Sat, 27 Jan 2024 11:50:29 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Sat, 27 Jan 2024 11:50:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 27 Jan 2024 11:50:34 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 27 Jan 2024 11:57:57 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 27 Jan 2024 11:57:59 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 27 Jan 2024 11:58:00 GMT
RUN docker-php-ext-enable sodium
# Sat, 27 Jan 2024 11:58:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 27 Jan 2024 11:58:01 GMT
WORKDIR /var/www/html
# Sat, 27 Jan 2024 11:58:02 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 27 Jan 2024 11:58:02 GMT
STOPSIGNAL SIGQUIT
# Sat, 27 Jan 2024 11:58:02 GMT
EXPOSE 9000
# Sat, 27 Jan 2024 11:58:02 GMT
CMD ["php-fpm"]
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
ENV DRUPAL_VERSION=10.2.3
# Thu, 08 Feb 2024 04:27:17 GMT
WORKDIR /opt/drupal
# Thu, 08 Feb 2024 04:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 08 Feb 2024 04:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3413052a1d508babdec59ce57cce40835c4c1cc4cd0a76ca57367f5157bfac`  
		Last Modified: Sat, 27 Jan 2024 13:02:31 GMT  
		Size: 2.8 MB (2792799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853cf4113ec71c9f8cf3d722ca3c5c66d434d7d4a34d817fd59a0beacdc2041d`  
		Last Modified: Sat, 27 Jan 2024 13:02:31 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6540cb25a1124aa604da77e43818a829a1aaa3ba794e7dec5929005ae8753aba`  
		Last Modified: Sat, 27 Jan 2024 13:02:30 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cae545b5c455216bd92c1dd5e22ab1ce6f79418e586e933bb7c681d9049ad8e4`  
		Last Modified: Sat, 27 Jan 2024 13:04:27 GMT  
		Size: 12.1 MB (12096223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e2ac28fc214f2f147e70db3464b914791b02484065b1713bd2f4c1a3970713`  
		Last Modified: Sat, 27 Jan 2024 13:04:26 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f6eace639e2ab8cfaafdaaaaecaff6812317010670726b5f06303bab1c9767`  
		Last Modified: Sat, 27 Jan 2024 13:04:44 GMT  
		Size: 11.8 MB (11827293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0386afcc318e4883389f677cf84709b46c42c01a72ab44747df5233dadb581fc`  
		Last Modified: Sat, 27 Jan 2024 13:04:40 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d54d8c049eabc43817bc030e0c730e8cf7ae721154336ef147a5ed507c775cf`  
		Last Modified: Sat, 27 Jan 2024 13:04:40 GMT  
		Size: 18.8 KB (18771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73d169fe4e9f57b6276bbd2c87bc40c6bb19dc8e81a1b6d8bc49b1a09ae083cb`  
		Last Modified: Sat, 27 Jan 2024 13:04:40 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30fdd94e6426c15f1fc05a19e11c684ac92b32777176e58212a8089ab9257081`  
		Last Modified: Tue, 13 Feb 2024 00:16:54 GMT  
		Size: 2.0 MB (1999820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:107e004f0b0daa66d97a150e0745e9213dd0f83a3435c1735da8624c99276f0d`  
		Last Modified: Tue, 13 Feb 2024 00:16:54 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db2360e3e278063cf7cdad928cd9798febc20c8a5af3082b064e283d04cc1a1a`  
		Last Modified: Tue, 13 Feb 2024 00:16:54 GMT  
		Size: 721.6 KB (721579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271035567dcdee05f26890fdb6852e11039ee99852e150e51eb3a9c46d4b2cc1`  
		Last Modified: Tue, 13 Feb 2024 00:16:54 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cbc6c842d9329d117b3fba722cb35698835f34715cd31f80609d60b85dfb6f3`  
		Last Modified: Tue, 13 Feb 2024 00:16:55 GMT  
		Size: 19.2 MB (19234534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.18` - unknown; unknown

```console
$ docker pull drupal@sha256:f92a310983900b95849c993d04cea5b8f15a57b8a1e23fe68902758cea13bd3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **838.9 KB (838909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51951f52955ade6d346a475e5f798ff6589e3c69a77d6df87f1f0a4dd6528298`

```dockerfile
```

-	Layers:
	-	`sha256:1fdf874a92006b4a32d15318255ce9424048d39bfda360a67732ace9fc404e5d`  
		Last Modified: Tue, 13 Feb 2024 00:16:54 GMT  
		Size: 805.4 KB (805355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee9a03bb49d7ef2cc5df13ebf377aa1a080d4da3815162300d9ca14bb086228f`  
		Last Modified: Tue, 13 Feb 2024 00:16:53 GMT  
		Size: 33.6 KB (33554 bytes)  
		MIME: application/vnd.in-toto+json
