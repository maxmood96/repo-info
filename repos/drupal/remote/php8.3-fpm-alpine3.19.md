## `drupal:php8.3-fpm-alpine3.19`

```console
$ docker pull drupal@sha256:4dfceb7fbac026ce8715ec1e4be86f09159a45d064e9c6b1efd9fa0afd5ebf4c
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

### `drupal:php8.3-fpm-alpine3.19` - linux; amd64

```console
$ docker pull drupal@sha256:33fd3ccb691901e8853e38893463d83700e058b12b4bd0f5658177313a5864a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55880707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce326e84e86c5cfc340ed36aa0986cbbccc236a8bb162c5da5b2d1daeeb628a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 04 Jul 2024 15:27:17 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Jul 2024 15:27:17 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Jul 2024 15:27:17 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_VERSION=8.3.9
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.9.tar.xz.asc
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_SHA256=bf4d7b8ea60a356064f88485278bd6f941a230ec16f0fc401574ce1445ad6c77
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 04 Jul 2024 15:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 04 Jul 2024 15:27:17 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 04 Jul 2024 15:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 04 Jul 2024 15:27:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Jul 2024 15:27:17 GMT
EXPOSE 9000
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["php-fpm"]
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV DRUPAL_VERSION=10.3.1
# Thu, 04 Jul 2024 15:27:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /opt/drupal
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f931e8c4ee1eb9216b05b724540ce862c05cd47764c5430b1adcacafe7a0ca`  
		Last Modified: Tue, 23 Jul 2024 03:55:55 GMT  
		Size: 2.8 MB (2775544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7701d11e42f9c63f01acc636a5c0ea3e4f92eda3047d8a1b0a56cd34c4565d1d`  
		Last Modified: Tue, 23 Jul 2024 03:55:54 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980d88e93b06bf737890c4df5068bb324bafc32ad3cbd0f4beced84645e382f2`  
		Last Modified: Tue, 23 Jul 2024 03:55:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b69ceed192f3f9e39063fd60b3fe33e732ee0c1a5b913b01d985c9e0b3d372ac`  
		Last Modified: Tue, 23 Jul 2024 03:59:35 GMT  
		Size: 12.5 MB (12491151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:830aa477fcee136717c0463f47a1af9d605410567e03d926914a90558a56d741`  
		Last Modified: Tue, 23 Jul 2024 03:59:34 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35c12be849541db4c805e69eed964b134479ed630ba878a6cf5c237fffd59ee`  
		Last Modified: Tue, 23 Jul 2024 03:59:58 GMT  
		Size: 13.1 MB (13080278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f452a00a511cf2c4dc8ef0373569561a0e10a494d935ec1b6dcb11b0163ea89`  
		Last Modified: Tue, 23 Jul 2024 03:59:56 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b39b404d3ffb15bd2b68bc83db1668bd6bc9c60ed5b2571c5baac3c6d67c85f`  
		Last Modified: Tue, 23 Jul 2024 03:59:56 GMT  
		Size: 19.6 KB (19552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d987039ef41e839ae7b9cceaed67f2e6ba866682c6905e30557d28e52b889a7e`  
		Last Modified: Tue, 23 Jul 2024 03:59:56 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e59fc8c551697cbd9946c491f38362dfb514aabb7b0d02ba0568522a52c39824`  
		Last Modified: Tue, 23 Jul 2024 07:19:06 GMT  
		Size: 2.3 MB (2285559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc62053fd610246767e3a7085051e9b66d3c50b9ad38a8de6fb153b78c72aff`  
		Last Modified: Tue, 23 Jul 2024 07:19:06 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ea5bf9044b184d0ad28a05cfb12f2c1effa3a316db6a60418c1bedb3e8447c`  
		Last Modified: Tue, 23 Jul 2024 07:19:06 GMT  
		Size: 726.3 KB (726333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca61848ec82436e5f92a7725f18ba8abf529790208e5f44c00d64bb2da415642`  
		Last Modified: Tue, 23 Jul 2024 07:19:06 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf6cdaf1d76c46d583b0c219487887d5836189fc1f56f66a775f758ba7ce015`  
		Last Modified: Tue, 23 Jul 2024 07:19:07 GMT  
		Size: 21.1 MB (21069249 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:6c76b3a4c4d6be1a309b6bcc4508cfcecb248532f8be8369b7a9597231a55191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.4 KB (381418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf8dad5f6a4ba8bb9fe9cff9bc6f55b1910eb6462a99bbcf9c030b87e9f1194`

```dockerfile
```

-	Layers:
	-	`sha256:0a4a8d13cd3a246af766b8a0050a463f5a61b6b53e37b9237f2cb9401be1718d`  
		Last Modified: Tue, 23 Jul 2024 07:19:06 GMT  
		Size: 350.1 KB (350075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47e530786a0c4c1b9eaae9948a3186e8d7f065b407bce8ce246c0af00ff644d8`  
		Last Modified: Tue, 23 Jul 2024 07:19:06 GMT  
		Size: 31.3 KB (31343 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-alpine3.19` - linux; arm variant v6

```console
$ docker pull drupal@sha256:12156b9536649209d357fdf8e205452ed486c495c931339031c445ece01c01a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56141994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31891ced8cf6a2bb124edbe8229755a2d2612ee287c8a108d6de964d37eb5455`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:18 GMT
ADD file:8a9a8699eda49e02bf479cd01e71af80d721e91898a1c053620f39f99069de0a in / 
# Thu, 20 Jun 2024 17:49:18 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 22:14:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 22:14:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 22:14:51 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 22:14:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 22:14:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 22:14:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 22:14:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 22:14:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 22:14:53 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_VERSION=8.3.9
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.9.tar.xz.asc
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_SHA256=bf4d7b8ea60a356064f88485278bd6f941a230ec16f0fc401574ce1445ad6c77
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 04 Jul 2024 15:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 04 Jul 2024 15:27:17 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 04 Jul 2024 15:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 04 Jul 2024 15:27:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Jul 2024 15:27:17 GMT
EXPOSE 9000
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["php-fpm"]
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV DRUPAL_VERSION=10.3.1
# Thu, 04 Jul 2024 15:27:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /opt/drupal
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:217d5fa2bafb793ad47d21c0abaeeca94f1d39763a4cd3d178069467c1c42712`  
		Last Modified: Thu, 20 Jun 2024 17:49:48 GMT  
		Size: 3.2 MB (3173908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0fe3503923312700d0ad215db61ad54d143feac25bfc14ba0b4eb2cd554730`  
		Last Modified: Thu, 20 Jun 2024 23:11:30 GMT  
		Size: 2.8 MB (2782199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e727f9d3c5208e6085f44fcc1802704b726a7b2b884ee795f8ceeb3594b9e6`  
		Last Modified: Thu, 20 Jun 2024 23:11:29 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a49ddfbb89fe4110ef4b151edfe03948f99fe5bf8d637ef0657bd9bb46d10c9`  
		Last Modified: Thu, 20 Jun 2024 23:11:29 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f9d0e4e5a1143ffc77de1d341d167ad83ef23780f53790399f141e899909442`  
		Last Modified: Sat, 06 Jul 2024 01:48:35 GMT  
		Size: 12.5 MB (12491170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4896c7577097e29fe3899956fb6c2126a154f8fe3d969459d4b699b44b3790cd`  
		Last Modified: Sat, 06 Jul 2024 01:48:33 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333b6665845a22af8ad7c465cb38af69ef04448495c3a163b753dae2887bd856`  
		Last Modified: Sat, 06 Jul 2024 01:49:03 GMT  
		Size: 14.1 MB (14123162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff0320f916945de89962360eca0bd40e73dd3f3cf42d60ee20972ab1693929d`  
		Last Modified: Sat, 06 Jul 2024 01:49:00 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:509cfedb7a14f07f5c12462e8326544325474346b577ebb214e6d8f31961f89e`  
		Last Modified: Sat, 06 Jul 2024 01:49:00 GMT  
		Size: 19.4 KB (19407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff396cf0db44fec9725308cdeeecf9b3e042eefa4553e985d06b6e03abfe05ba`  
		Last Modified: Sat, 06 Jul 2024 01:49:00 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe63d58c1c77c37ced99a9c6acddc5384752dd19098042b33ee2e3719d7bd55`  
		Last Modified: Sat, 06 Jul 2024 03:52:22 GMT  
		Size: 1.7 MB (1742605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a79731f277c70a3005f4ad3b213f92301578dc4f3452bcef5d7ed6e53165983`  
		Last Modified: Sat, 06 Jul 2024 03:52:22 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514f5c6fe6434c996511631c1d4c352b1b666ac3f72a198e3496111dff6be32e`  
		Last Modified: Sat, 06 Jul 2024 03:52:22 GMT  
		Size: 726.3 KB (726328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2853784ee7f4b769bae12e54a0923d639769f9a4d649ccefac4bc8ab963d231b`  
		Last Modified: Sat, 06 Jul 2024 03:52:22 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff81f9167051bcf5f7a11b9c5b32600d2f83762c05a2d5a8e1acca22a90a425`  
		Last Modified: Sat, 06 Jul 2024 03:54:43 GMT  
		Size: 21.1 MB (21069216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:74f0df86c34957526d3d1824494b49b1d36123586be03221a25dde280a2d397b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.3 KB (31296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438b9c486919c7ba0e232a625dfa3a5a7090e04e371fe83836c4f34a7c79833e`

```dockerfile
```

-	Layers:
	-	`sha256:0429c50457856222a7ce9cded10722ba21f948b09cb69c38965f38a9753fb4d7`  
		Last Modified: Sat, 06 Jul 2024 03:54:41 GMT  
		Size: 31.3 KB (31296 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-alpine3.19` - linux; arm variant v7

```console
$ docker pull drupal@sha256:f538afee5703989ce1ba79b10577c66d4d95141047d5f5e24ef387cd7bb24477
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54716450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff6c147eb7b5de0effa5388355522fdfcb27b1b9dd93a9c7a986c933ba0ff4f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 20 Jun 2024 18:00:32 GMT
ADD file:a79253a22e927307fa2edd1752e7945fd88afbb97c73bbbe771cc99947c0517a in / 
# Thu, 20 Jun 2024 18:00:32 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 18:36:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 18:36:10 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 18:36:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 18:36:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 18:36:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 18:36:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 18:36:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 18:36:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 18:36:15 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_VERSION=8.3.9
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.9.tar.xz.asc
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_SHA256=bf4d7b8ea60a356064f88485278bd6f941a230ec16f0fc401574ce1445ad6c77
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 04 Jul 2024 15:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 04 Jul 2024 15:27:17 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 04 Jul 2024 15:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 04 Jul 2024 15:27:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Jul 2024 15:27:17 GMT
EXPOSE 9000
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["php-fpm"]
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV DRUPAL_VERSION=10.3.1
# Thu, 04 Jul 2024 15:27:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /opt/drupal
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:4007367bb0cf596fd27d2207989b3864272eb2e5caf7429c07e68abc3bd47b0c`  
		Last Modified: Thu, 20 Jun 2024 18:01:06 GMT  
		Size: 2.9 MB (2926498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06fd2f7314fb5a1bddd9717973873845b50c0071affc1e794041d120c75898de`  
		Last Modified: Thu, 20 Jun 2024 20:09:38 GMT  
		Size: 2.6 MB (2624592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f23dd8be0ad44d730123eaa34961b21523892832d003182b0254c0a46ac650`  
		Last Modified: Thu, 20 Jun 2024 20:09:37 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd5cf20011ab84a0de7e85853e1003271ddd0a307016623fddf7d0a902750d5`  
		Last Modified: Thu, 20 Jun 2024 20:09:37 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19362bad7cc19e04a0523bb08756ffdba351c6e92d517a400f4d5bfc85a8bc40`  
		Last Modified: Sat, 06 Jul 2024 02:48:26 GMT  
		Size: 12.5 MB (12491158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d04f4059ff4b9e12db3a2211afbb268fcec4e850379d275ea352164f65230abf`  
		Last Modified: Sat, 06 Jul 2024 02:48:25 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a3714475b7db27147ab36d8712b213607173c7d2870f0126914cfbe79ec7b54`  
		Last Modified: Sat, 06 Jul 2024 02:48:51 GMT  
		Size: 13.2 MB (13238679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14f148826808d4d9dc9fa4123048278a5b68f66ec36a685db661ec9a949713c`  
		Last Modified: Sat, 06 Jul 2024 02:48:48 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fedf7dbe002c27170941b43fc8776c0a4606316e24494948edc65e20e3239a8`  
		Last Modified: Sat, 06 Jul 2024 02:48:48 GMT  
		Size: 19.4 KB (19375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f526c22306d4ae86a94b167bf8f481d1fee8b790912c43afdef6524daf84695`  
		Last Modified: Sat, 06 Jul 2024 02:48:48 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df2f03439587431859dbc9a8c29ef5e39342191127c34b481cb75bd423c3552`  
		Last Modified: Sat, 06 Jul 2024 06:01:53 GMT  
		Size: 1.6 MB (1606941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6e2cbc62c81f0dc26685f81968576f8218830097edeb3dfaf9e45cdbf200898`  
		Last Modified: Sat, 06 Jul 2024 06:01:53 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b786d99296ba0ce62d64c6e840f98b6ceb9e34cb900849b033b6d4dfbcc3c2f1`  
		Last Modified: Sat, 06 Jul 2024 06:01:53 GMT  
		Size: 726.3 KB (726333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5fd3ea2cd335068906cc9c7b3b73e7b245225420338d4304feaab4030707760`  
		Last Modified: Sat, 06 Jul 2024 06:01:53 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478a9cd5090a175bdc1779dfba16d97ce2bf0557df7e78412eb5d89546f57cfc`  
		Last Modified: Sat, 06 Jul 2024 06:11:49 GMT  
		Size: 21.1 MB (21068866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:dd7f54c2c3a5ea9a959fe11b671c7a69d1b1bfc20df84d5c9a524658bd62782b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.5 KB (360516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb0354944dadab4e0f115df2dea95fa030cbb8201bf520b549552ef0fa4f670`

```dockerfile
```

-	Layers:
	-	`sha256:c0019d53a3b0cf129c0bb0f074d7ca1d655784fde221c8f41908d1c0d31107e6`  
		Last Modified: Sat, 06 Jul 2024 06:11:48 GMT  
		Size: 329.0 KB (329001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b8fed2fb065d5bbea53c45d62adc3cfaf229077ab97a3fe280743edf6316234`  
		Last Modified: Sat, 06 Jul 2024 06:11:48 GMT  
		Size: 31.5 KB (31515 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:cd5bde7c437e794cc9526fde1b950a8b2925fc8fe79d0eed4cce7540aefb98db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58618146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36f1723939a7a65d4b631229e16995b4ee2728f144e589ba9aba06a1358eff18`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:38 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 20 Jun 2024 17:40:38 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 22:51:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 22:51:20 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 22:51:21 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 22:51:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 22:51:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 22:51:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 22:51:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 22:51:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 22:51:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_VERSION=8.3.9
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.9.tar.xz.asc
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_SHA256=bf4d7b8ea60a356064f88485278bd6f941a230ec16f0fc401574ce1445ad6c77
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 04 Jul 2024 15:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 04 Jul 2024 15:27:17 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 04 Jul 2024 15:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 04 Jul 2024 15:27:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Jul 2024 15:27:17 GMT
EXPOSE 9000
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["php-fpm"]
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV DRUPAL_VERSION=10.3.1
# Thu, 04 Jul 2024 15:27:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /opt/drupal
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01446ea5918cdf1fe1b865bb8d7330b56410ce93061441cfcbd2f22e4a75c328`  
		Last Modified: Thu, 20 Jun 2024 23:58:51 GMT  
		Size: 2.8 MB (2829133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121d7c7e80736da27a924b7bbc4c7d347f8de1e1e5d1227f2732342fd44df0a3`  
		Last Modified: Thu, 20 Jun 2024 23:58:51 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7858568419b94cae9ac32ee0afc3ecfeb070d2bf79da8598e2e9e20e51a82578`  
		Last Modified: Thu, 20 Jun 2024 23:58:51 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d860118487fc77e45eeb6986498527de6299385dae5b6d1e1a08fcf91d2932`  
		Last Modified: Sat, 06 Jul 2024 02:33:01 GMT  
		Size: 12.5 MB (12491159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662c50702444937e5cf68965dec371a9164393be760e1208d835822260a9e266`  
		Last Modified: Sat, 06 Jul 2024 02:33:00 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895614d4544ea2fa73548abe1fd3ef97b650166163ce18222e393a083984c061`  
		Last Modified: Sat, 06 Jul 2024 02:33:24 GMT  
		Size: 15.6 MB (15552574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de39a3ab1810a78149c3d514a290968529c26402f508530de0d66a49afcbf1d`  
		Last Modified: Sat, 06 Jul 2024 02:33:22 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4880fbb025d8c9405baa177ea6029377b7ee794090d190cb2ca4cac27cf1be6`  
		Last Modified: Sat, 06 Jul 2024 02:33:23 GMT  
		Size: 19.4 KB (19382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbe72160c726258fe608a3366cb84982f1a88f0f072c41122e437916e7e2aece`  
		Last Modified: Sat, 06 Jul 2024 02:33:22 GMT  
		Size: 9.2 KB (9175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad161cce7e3d32b367e4eaf265525c753c59f7b21efddc69047bb07a3b19cc67`  
		Last Modified: Sat, 06 Jul 2024 06:05:26 GMT  
		Size: 2.6 MB (2559448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf150352e9daffb7a217233a88c77ef52b33b317ef0442eec4a33404b926438`  
		Last Modified: Sat, 06 Jul 2024 06:05:26 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69eeb59239765b84c7f20fd06ab1ee4defe13f1322bedf71f10d59f142b666e3`  
		Last Modified: Sat, 06 Jul 2024 06:05:27 GMT  
		Size: 726.3 KB (726333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10011bcb799bc54e435730f3f28d3d47627965f7ea68788c4a1cef38a000f6c7`  
		Last Modified: Sat, 06 Jul 2024 06:05:26 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04942fede20c8e8ed6b0ca99077b39d1f1046df5a1e8af50c8058f9f4ff435dd`  
		Last Modified: Sat, 06 Jul 2024 06:13:08 GMT  
		Size: 21.1 MB (21068915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:278120467c6f53897d0da8d3238b2de7e736a12243cc04510e457f8de755c0d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.1 KB (361051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dd42a9d09e8e405d063e3e8a44cd09b093f2c24722352ad6f6bb8c6767805b7`

```dockerfile
```

-	Layers:
	-	`sha256:ddd85bc93d84960a014423bc7ccba872efe700f31106abaff196cdcbca54c7f2`  
		Last Modified: Sat, 06 Jul 2024 06:13:07 GMT  
		Size: 329.0 KB (329021 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:046db3afb0f1600610635825bc00211bfc4ab018b144f546e38870e5f856a21e`  
		Last Modified: Sat, 06 Jul 2024 06:13:06 GMT  
		Size: 32.0 KB (32030 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-alpine3.19` - linux; 386

```console
$ docker pull drupal@sha256:7bd788e34e08afcb97dbf35a669c4e0fd5ef7d623fb50b1011b148bcfdb38db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.1 MB (56140985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df692b0b2ccb956f2fe9e7c455dbaff7d32316dadb80b06510f6a2b345733b81`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 04 Jul 2024 15:27:17 GMT
ADD file:0ea09fe32763883fe12b23d858a03245191055e9ab130ba28dc77053fcea5d77 in / 
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Jul 2024 15:27:17 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Jul 2024 15:27:17 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_VERSION=8.3.9
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.9.tar.xz.asc
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_SHA256=bf4d7b8ea60a356064f88485278bd6f941a230ec16f0fc401574ce1445ad6c77
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 04 Jul 2024 15:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 04 Jul 2024 15:27:17 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 04 Jul 2024 15:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 04 Jul 2024 15:27:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Jul 2024 15:27:17 GMT
EXPOSE 9000
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["php-fpm"]
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV DRUPAL_VERSION=10.3.1
# Thu, 04 Jul 2024 15:27:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /opt/drupal
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:158aa28c117a606c22b37b6edf36cfaa99cea0485a39ac8469a3074b48a67534`  
		Last Modified: Mon, 22 Jul 2024 21:39:06 GMT  
		Size: 3.3 MB (3252602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f83dfc65354b38d786dbce66dcc54fce8dc00fb50911d5f0b25891bac00d890f`  
		Last Modified: Tue, 23 Jul 2024 02:15:24 GMT  
		Size: 2.8 MB (2839257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:569cc315ba4cbde39caf33a3761351d59d8268a4887485cce7f6d1e3a0cc8af1`  
		Last Modified: Tue, 23 Jul 2024 02:15:23 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99b201215f8e0acb32ec7e5e0ea5f3a5935a73bbc1d96de15b4bc81e8fe59575`  
		Last Modified: Tue, 23 Jul 2024 02:15:24 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea53b64283b6d706a18fdace167b988b46de7396fa375bb0fac20c898108732`  
		Last Modified: Tue, 23 Jul 2024 02:19:28 GMT  
		Size: 12.5 MB (12491163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a81da6da36dffd8942cc0fd0f104f1f05a0aa84f1175d94f765b9bc7a95764de`  
		Last Modified: Tue, 23 Jul 2024 02:19:27 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcc4e9adf537a13f64cadeb4aa23e393b48269a87337f2da06b3f74a66d673ee`  
		Last Modified: Tue, 23 Jul 2024 02:19:54 GMT  
		Size: 13.4 MB (13408030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fff6e664998557d327bb179d0ed3862bd588d4773c1f89d908e1a0ea108973`  
		Last Modified: Tue, 23 Jul 2024 02:19:51 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4cb24a9236cc93e15f2bc2c6d8aa8502805ce152b15a3b7cdda003a647d530`  
		Last Modified: Tue, 23 Jul 2024 02:19:51 GMT  
		Size: 19.6 KB (19561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2449fea1920c9c0bb9607151402f7ae8f883a280ec3d8bd3190c63dcca07b5b4`  
		Last Modified: Tue, 23 Jul 2024 02:19:51 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d653c9e77eda5138556ddd4a6f8e91b7ae09dea550d5d1e645ae804c6db5e2e5`  
		Last Modified: Tue, 23 Jul 2024 06:09:58 GMT  
		Size: 2.3 MB (2320799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135f85203df0b49717dc3d898271203b67b625d889dcacbc73fe1c27b32af3e1`  
		Last Modified: Tue, 23 Jul 2024 06:09:58 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eced2f251bf56df8300e85cee26b44749acb5c84a56e6352ea0966b165ab1995`  
		Last Modified: Tue, 23 Jul 2024 06:09:58 GMT  
		Size: 726.3 KB (726335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f8367865e19b2028adb50f31304d470044b88e9b2d076aa8353bf26af75283`  
		Last Modified: Tue, 23 Jul 2024 06:09:58 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a1a9c99b59bd5faf2e0833507764fdbb82c44babca958f840d944a70828def`  
		Last Modified: Tue, 23 Jul 2024 06:10:00 GMT  
		Size: 21.1 MB (21069238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:4740948872fd95e70d855ef4d17ef42eabe676447a31659bce14ee9de6a08ead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.4 KB (381353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c19357ac87c67fa053c0e9f2ee95f736a46d0d41d25f0dd0a840de9b2234f4c9`

```dockerfile
```

-	Layers:
	-	`sha256:59257fcb2c61eb6c167622bcf1bd9c87a23e3dcec3444c0f8df3f4f906ce4728`  
		Last Modified: Tue, 23 Jul 2024 06:09:58 GMT  
		Size: 350.1 KB (350050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6113f476a145b838f1376fa49f7b7435c10ebda8f37199c06345af00d60e6579`  
		Last Modified: Tue, 23 Jul 2024 06:09:58 GMT  
		Size: 31.3 KB (31303 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-alpine3.19` - linux; ppc64le

```console
$ docker pull drupal@sha256:a2a354d7309b1745d0c1533ad52d74815310c16b229b8f971b876cf4b07dfa1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58605796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc700473ea185cc73486ed5bca7e6c058b457626202ad66abf4895efb1feead1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 20 Jun 2024 18:18:27 GMT
ADD file:2bbc16bd313a28bd824794768ca122cd630e13eb133abbc1945768f5fadb6afb in / 
# Thu, 20 Jun 2024 18:18:28 GMT
CMD ["/bin/sh"]
# Thu, 20 Jun 2024 18:51:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 20 Jun 2024 18:51:58 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 20 Jun 2024 18:51:59 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 20 Jun 2024 18:52:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 18:52:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 18:52:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 18:52:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 18:52:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 18:52:02 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_VERSION=8.3.9
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.9.tar.xz.asc
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_SHA256=bf4d7b8ea60a356064f88485278bd6f941a230ec16f0fc401574ce1445ad6c77
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 04 Jul 2024 15:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 04 Jul 2024 15:27:17 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 04 Jul 2024 15:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 04 Jul 2024 15:27:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Jul 2024 15:27:17 GMT
EXPOSE 9000
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["php-fpm"]
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV DRUPAL_VERSION=10.3.1
# Thu, 04 Jul 2024 15:27:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /opt/drupal
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:a87ce480a1e6b2a211e539793eb8993daec4a7b45a3b284a63476a172be632c2`  
		Last Modified: Thu, 20 Jun 2024 18:19:08 GMT  
		Size: 3.4 MB (3360635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39eb9ede040a8629a36c19a1019af3a33bdcab0e9b16dd4e50894df992e2bc57`  
		Last Modified: Thu, 20 Jun 2024 19:40:08 GMT  
		Size: 2.9 MB (2858706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1732b6eaedabe72854b318d620f62ca5985f9320a089bd90b6c760234d0c540`  
		Last Modified: Thu, 20 Jun 2024 19:40:07 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4078b4ab583744a8a16db200a1b0a44450c6b122867ead7a14b2a395921cd4`  
		Last Modified: Thu, 20 Jun 2024 19:40:07 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0744354ea16c3e8a147873157a62ee6609622fa14b95c2b5a015be88b6bbdbf9`  
		Last Modified: Sat, 06 Jul 2024 01:45:13 GMT  
		Size: 12.5 MB (12491160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d961e5a67da7d41ea9c79fbc8d3ec8b8ebebd122ca3e09fec99aeadaca49f4`  
		Last Modified: Sat, 06 Jul 2024 01:45:12 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c3d75bca6c40b0ee00ee571ce67c5883c47bcabda9d06eda4d4117a9481130`  
		Last Modified: Sat, 06 Jul 2024 01:45:40 GMT  
		Size: 16.0 MB (15960459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83653f77b36e88fa0f91bcdd646c51032014c92c225aea72f6f439c10066a8e9`  
		Last Modified: Sat, 06 Jul 2024 01:45:37 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42f423aecefd56a1ab13deb1d4c11e41735116093da14818c86d733b365d95c`  
		Last Modified: Sat, 06 Jul 2024 01:45:37 GMT  
		Size: 19.4 KB (19384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce014d3d75a0c50caa04a0ec87b61e845906a60a04b4d2c3205074b33cdebba`  
		Last Modified: Sat, 06 Jul 2024 01:45:37 GMT  
		Size: 9.2 KB (9175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f2d4b703a809e0adc65269c3b212c82ef46020387112757175390307dd8d64`  
		Last Modified: Sat, 06 Jul 2024 08:44:55 GMT  
		Size: 2.1 MB (2105718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeb204df883ae596afc75ed8fd8d41825c3246863b67c3289e2154a26041078a`  
		Last Modified: Sat, 06 Jul 2024 08:44:55 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e1d7fd01bf4870725fa8a6dcfd0b63f2f0c5a4f4e7079b13d301558aaa4397`  
		Last Modified: Sat, 06 Jul 2024 08:44:55 GMT  
		Size: 726.3 KB (726335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0371a04772a944b3a4fc38f2ef27569b0ae14d94a2fb1a7525045fd98330e71f`  
		Last Modified: Sat, 06 Jul 2024 08:44:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b80d046960671930602ebf9f30212fb7ede3706270e41bfd829333ff400e76`  
		Last Modified: Sat, 06 Jul 2024 08:57:57 GMT  
		Size: 21.1 MB (21069395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:951302d14e2e3b4c2582d2c545a21845a1200d5413442697071b7f59824ab526
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.5 KB (358494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de6d8d70b39186d9e26a1598b9615c67498292901c275307cbf6455727149ec`

```dockerfile
```

-	Layers:
	-	`sha256:0b9cf8c626083d97390cf21e3cec6157b94e19169fa00362b650a0d6a834af47`  
		Last Modified: Sat, 06 Jul 2024 08:57:56 GMT  
		Size: 327.0 KB (327045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d760aaa5aa81fd4db898b6827e41d5e16a120bd2cbf0a97993227c3336ad22cf`  
		Last Modified: Sat, 06 Jul 2024 08:57:56 GMT  
		Size: 31.4 KB (31449 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-alpine3.19` - linux; s390x

```console
$ docker pull drupal@sha256:a7a9ae816c217a6b0230d85132205d0c596ac9420d6d96c09401fa2cbde44e00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.9 MB (57880390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b12dc12163af504de8204e4837ef190417cba69a04beb80e0c8b9095f07de466`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 20 Jun 2024 17:42:12 GMT
ADD file:4aa205db6913ec3fd53a65bd281586a5f6abde77d41f1ffab554706c04822982 in / 
# Thu, 20 Jun 2024 17:42:12 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 00:57:35 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 21 Jun 2024 00:57:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 21 Jun 2024 00:57:39 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 21 Jun 2024 00:57:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 21 Jun 2024 00:57:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 21 Jun 2024 00:57:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 21 Jun 2024 00:57:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 21 Jun 2024 00:57:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 21 Jun 2024 00:57:42 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_VERSION=8.3.9
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.9.tar.xz.asc
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_SHA256=bf4d7b8ea60a356064f88485278bd6f941a230ec16f0fc401574ce1445ad6c77
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 04 Jul 2024 15:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 04 Jul 2024 15:27:17 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 04 Jul 2024 15:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 04 Jul 2024 15:27:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Jul 2024 15:27:17 GMT
EXPOSE 9000
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["php-fpm"]
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV DRUPAL_VERSION=10.3.1
# Thu, 04 Jul 2024 15:27:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /opt/drupal
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:71c2dde42aad09035a9686e376c7507b6e8e2a8ada2c409775f1c1bfb8d928ea`  
		Last Modified: Thu, 20 Jun 2024 17:43:16 GMT  
		Size: 3.3 MB (3252491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc7206a1bfab077fd781ea2f1bff4245da6a985c14e5ac529be337f2a603bfe2`  
		Last Modified: Fri, 21 Jun 2024 02:03:40 GMT  
		Size: 3.0 MB (2956393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127507485549677fb9d01f808d1e93e9bd9c50738e97f7d5f24eb6c5c0177d39`  
		Last Modified: Fri, 21 Jun 2024 02:03:39 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0d9ac49dc0992d0026684046dc69d1afde3acf6907aaf78e13654907905c8b7`  
		Last Modified: Fri, 21 Jun 2024 02:03:39 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f77bccf35b75a9d9d41a7d08f77e0b4d8b073dfe43dbf9ae10cb792c01d307`  
		Last Modified: Sat, 06 Jul 2024 02:09:54 GMT  
		Size: 12.5 MB (12491164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38595de477e6e5404b172b314ec6c428b0cf0315001706e78cb1f5690972c393`  
		Last Modified: Sat, 06 Jul 2024 02:09:54 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c884ff20c52a3a25f3a10d943e5a4832a1e3bb0a0a786e3dc34606e24e2a02f`  
		Last Modified: Sat, 06 Jul 2024 02:10:14 GMT  
		Size: 15.4 MB (15351089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf167cf726608231018c26031184fcbae29a34e6f1d180e523a10704162b125`  
		Last Modified: Sat, 06 Jul 2024 02:10:11 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681fef10ac0014bcc58d79e789a50c0631314e41080c1f6283a0c1920ad813a1`  
		Last Modified: Sat, 06 Jul 2024 02:10:11 GMT  
		Size: 19.4 KB (19368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4712063cdcc0a496d8624ccba610a1bab1b24b37be534a9ee916db6f443a766c`  
		Last Modified: Sat, 06 Jul 2024 02:10:12 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e62959cdeed0e45dd9d66a9ead52ab0aff35d6888cdedac6747920bcedfd839a`  
		Last Modified: Sat, 06 Jul 2024 06:01:02 GMT  
		Size: 2.0 MB (2000391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6dce2f3fcf081f679e2ad36580d355be32d1ef95268ef1f919692222f7fb08`  
		Last Modified: Sat, 06 Jul 2024 06:01:01 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b496c9f1d8160b09ea74a0fd14c5e62f126da1bf96a4d9f8696441a707c9bf`  
		Last Modified: Sat, 06 Jul 2024 06:01:02 GMT  
		Size: 726.3 KB (726335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ead2f2615d81b84ddd344f96235f18358e525e40c7d032b588b8d951344090`  
		Last Modified: Sat, 06 Jul 2024 06:01:02 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4544202ed8385f4331dc4a6327eeeba20191a613a92e062a382528b6c606b5c2`  
		Last Modified: Sat, 06 Jul 2024 06:11:02 GMT  
		Size: 21.1 MB (21069157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:90b749f59e632b35fb5b18babb45c080d37f7c91796c1871d4b410b1a1a2f7af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.4 KB (358408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a59098a4654b9f90de3be3a5061fcb3e4511705c1718af9d8a6e166fcd1c247f`

```dockerfile
```

-	Layers:
	-	`sha256:3cc240c39e80d226f04e30fb098410193facf24f7b7702a35d30c5fdfcd243f3`  
		Last Modified: Sat, 06 Jul 2024 06:11:00 GMT  
		Size: 327.0 KB (327011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d257e43fbed5c9257abc94005c96c806afd56e9337feaf3ba4757b5ab6ea42f`  
		Last Modified: Sat, 06 Jul 2024 06:11:00 GMT  
		Size: 31.4 KB (31397 bytes)  
		MIME: application/vnd.in-toto+json
