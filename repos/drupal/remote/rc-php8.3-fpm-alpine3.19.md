## `drupal:rc-php8.3-fpm-alpine3.19`

```console
$ docker pull drupal@sha256:9daff5bcb43e56e3932ceb7926e28fa8c2c37d4ceedf36778c6bb03903d665ae
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

### `drupal:rc-php8.3-fpm-alpine3.19` - linux; amd64

```console
$ docker pull drupal@sha256:ce87533309a5b580ef194cebd325918e1464c564cbe463ea1fa57e08db374bc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (54013311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3556c2939dfffd8e31edf450c51ea24e3b088ccfd2ce719bf02edf7a9328c709`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 12 Jul 2024 03:27:25 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Fri, 12 Jul 2024 03:27:25 GMT
CMD ["/bin/sh"]
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 12 Jul 2024 03:27:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 12 Jul 2024 03:27:25 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_VERSION=8.3.9
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.9.tar.xz.asc
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_SHA256=bf4d7b8ea60a356064f88485278bd6f941a230ec16f0fc401574ce1445ad6c77
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 12 Jul 2024 03:27:25 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 12 Jul 2024 03:27:25 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 12 Jul 2024 03:27:25 GMT
RUN docker-php-ext-enable sodium
# Fri, 12 Jul 2024 03:27:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /var/www/html
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 12 Jul 2024 03:27:25 GMT
STOPSIGNAL SIGQUIT
# Fri, 12 Jul 2024 03:27:25 GMT
EXPOSE 9000
# Fri, 12 Jul 2024 03:27:25 GMT
CMD ["php-fpm"]
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV DRUPAL_VERSION=11.0.0-rc1
# Fri, 12 Jul 2024 03:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /opt/drupal
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
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
	-	`sha256:50e0debcd287dd4c1a6ccfae6a3ecb6949d8491acbcbb32470d17a927e5dccbe`  
		Last Modified: Tue, 23 Jul 2024 07:17:25 GMT  
		Size: 2.3 MB (2285534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da1517fcc4e7501390d62fed245cf0970e4717b0207e8b037a56a6891521fab`  
		Last Modified: Tue, 23 Jul 2024 07:17:25 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b72139b3dbae3d71668b4655dd88db836a435ef56b920b68311fd8d52bb4d34`  
		Last Modified: Tue, 23 Jul 2024 07:17:26 GMT  
		Size: 726.3 KB (726333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9253e2fd75778463271346d6fb1f96d698c9e33fcd76a5303020219ae0e1f22a`  
		Last Modified: Tue, 23 Jul 2024 07:17:26 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b35a37de5947010fa46c6ec9fd05ceeeb2fda10019f61050d25c61d3bf5440d`  
		Last Modified: Tue, 23 Jul 2024 07:17:26 GMT  
		Size: 19.2 MB (19201878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:41c31e9f1ab16a10a9dccf7b948388779ea762b5b4e259c03f8f742b64b12439
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.8 KB (380842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aca93d46642691681fa47e3ecc2be97716e0ff994270b4b4a95e1df4b477cb1`

```dockerfile
```

-	Layers:
	-	`sha256:eecfd14fc2c1539d951561e88df584930fb2728fddaed68ba4bb62ce5fe0f1db`  
		Last Modified: Tue, 23 Jul 2024 07:17:24 GMT  
		Size: 349.8 KB (349791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09df76cfa956b3e2bf938c6b3b26c02eb8c2b65c656f930e39484651b084f50c`  
		Last Modified: Tue, 23 Jul 2024 07:17:24 GMT  
		Size: 31.1 KB (31051 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.3-fpm-alpine3.19` - linux; arm variant v6

```console
$ docker pull drupal@sha256:cce50218dc9eafb518d7699bec7656ef50b9ffafa95228484a910e7a560fb6db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56491970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6856d0bb0365a97d393238cb863fe927e8aa8384ab8d592a6cefbdedaaac0b88`
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
# Sat, 06 Jul 2024 01:02:08 GMT
ENV PHP_VERSION=8.3.9
# Sat, 06 Jul 2024 01:02:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.9.tar.xz.asc
# Sat, 06 Jul 2024 01:02:09 GMT
ENV PHP_SHA256=bf4d7b8ea60a356064f88485278bd6f941a230ec16f0fc401574ce1445ad6c77
# Sat, 06 Jul 2024 01:02:15 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 06 Jul 2024 01:02:15 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 06 Jul 2024 01:11:15 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 06 Jul 2024 01:11:16 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 06 Jul 2024 01:11:18 GMT
RUN docker-php-ext-enable sodium
# Sat, 06 Jul 2024 01:11:18 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 06 Jul 2024 01:11:18 GMT
WORKDIR /var/www/html
# Sat, 06 Jul 2024 01:11:19 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 06 Jul 2024 01:11:19 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Jul 2024 01:11:19 GMT
EXPOSE 9000
# Sat, 06 Jul 2024 01:11:19 GMT
CMD ["php-fpm"]
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV DRUPAL_VERSION=11.0.0-rc1
# Fri, 12 Jul 2024 03:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /opt/drupal
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
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
	-	`sha256:e5d807f91b68f9de641f1ca62042acd1f58c55b6e814e64d1b3a5ce77a7b757b`  
		Last Modified: Fri, 12 Jul 2024 21:58:38 GMT  
		Size: 4.0 MB (3960606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c15d945c3133181d25d4140b320d5772005a953d850469a1ee13b9164c667d5`  
		Last Modified: Fri, 12 Jul 2024 21:58:38 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ac9fc53a4f215f8dabbaac643894a31fab9f2c23627bc628d624e6f1dd71d4`  
		Last Modified: Fri, 12 Jul 2024 21:58:38 GMT  
		Size: 726.3 KB (726334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368cdbd58112f4523b5ad152f165be4aa9c9dc877c5608147ef9b82965835830`  
		Last Modified: Fri, 12 Jul 2024 21:58:38 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7477a15b545e4bae81b8bf24437e3b4926225f41749e22ccc11c411bf7337a01`  
		Last Modified: Fri, 12 Jul 2024 21:58:40 GMT  
		Size: 19.2 MB (19201183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:8140f3df5fa1e64d8f76f6e75ea1819ec6343b3e3306e67fb8f30d01c444d8a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 KB (30978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f57796e198346c2a2c0dd18a81071b445920ae17cb3235f04549b63d69cfb2`

```dockerfile
```

-	Layers:
	-	`sha256:a5b4548016344155515233a649d631a2c9f48d2af96750917041bededb40301a`  
		Last Modified: Fri, 12 Jul 2024 21:58:38 GMT  
		Size: 31.0 KB (30978 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.3-fpm-alpine3.19` - linux; arm variant v7

```console
$ docker pull drupal@sha256:02a6d7d555f6b39b9b08afb79b7c4de044724749535a197da54af0286e2f0482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52849526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e474112823847671eabee80cc8fa0ddc20b6881fbb99d0414346b1245356daae`
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
# Sat, 06 Jul 2024 01:46:47 GMT
ENV PHP_VERSION=8.3.9
# Sat, 06 Jul 2024 01:46:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.9.tar.xz.asc
# Sat, 06 Jul 2024 01:46:47 GMT
ENV PHP_SHA256=bf4d7b8ea60a356064f88485278bd6f941a230ec16f0fc401574ce1445ad6c77
# Sat, 06 Jul 2024 01:46:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 06 Jul 2024 01:46:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 06 Jul 2024 01:54:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 06 Jul 2024 01:54:25 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 06 Jul 2024 01:54:28 GMT
RUN docker-php-ext-enable sodium
# Sat, 06 Jul 2024 01:54:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 06 Jul 2024 01:54:28 GMT
WORKDIR /var/www/html
# Sat, 06 Jul 2024 01:54:29 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 06 Jul 2024 01:54:29 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Jul 2024 01:54:29 GMT
EXPOSE 9000
# Sat, 06 Jul 2024 01:54:29 GMT
CMD ["php-fpm"]
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV DRUPAL_VERSION=11.0.0-rc1
# Fri, 12 Jul 2024 03:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /opt/drupal
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
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
	-	`sha256:64d5d05b46f546d8b662ba5841145e4d024a73d096a2ce48ca782b1c9839897c`  
		Last Modified: Fri, 12 Jul 2024 22:01:24 GMT  
		Size: 19.2 MB (19201942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:3a3833b1437dd7043bb0d1f91f50f4ce0d475bf34d288e7f778353769fc2cab6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.9 KB (359923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7e13df1d728c8622531246e8e3704f0a16824c9801f6484305a531b6c065131`

```dockerfile
```

-	Layers:
	-	`sha256:e6887f703645a6cda4d0567231284d0ac98e6c0f0142a11d17cd359c519d13d0`  
		Last Modified: Fri, 12 Jul 2024 22:01:23 GMT  
		Size: 328.7 KB (328709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3adf02b56e42c84971ed40ad27d57c144e2060c79e61cb695c3fb43ea8c1c462`  
		Last Modified: Fri, 12 Jul 2024 22:01:22 GMT  
		Size: 31.2 KB (31214 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.3-fpm-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:af24025d760c72143e3068808232aa6e498c700c310c162eff84abcb0533c879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.8 MB (56751057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:437090e8d3171608110dc80c0fbf5feec3f9511faf0e7d2dbad95a2009f3361b`
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
# Sat, 06 Jul 2024 01:22:03 GMT
ENV PHP_VERSION=8.3.9
# Sat, 06 Jul 2024 01:22:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.9.tar.xz.asc
# Sat, 06 Jul 2024 01:22:03 GMT
ENV PHP_SHA256=bf4d7b8ea60a356064f88485278bd6f941a230ec16f0fc401574ce1445ad6c77
# Sat, 06 Jul 2024 01:22:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 06 Jul 2024 01:22:08 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 06 Jul 2024 01:31:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 06 Jul 2024 01:31:02 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 06 Jul 2024 01:31:03 GMT
RUN docker-php-ext-enable sodium
# Sat, 06 Jul 2024 01:31:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 06 Jul 2024 01:31:03 GMT
WORKDIR /var/www/html
# Sat, 06 Jul 2024 01:31:04 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 06 Jul 2024 01:31:04 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Jul 2024 01:31:04 GMT
EXPOSE 9000
# Sat, 06 Jul 2024 01:31:04 GMT
CMD ["php-fpm"]
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV DRUPAL_VERSION=11.0.0-rc1
# Fri, 12 Jul 2024 03:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /opt/drupal
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
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
	-	`sha256:f4172bea0e37e206a74f8c2afdf3d55fa531bd52b38e5b850085f8747e534faf`  
		Last Modified: Fri, 12 Jul 2024 22:00:00 GMT  
		Size: 19.2 MB (19201826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:86bf7edf3cbd4b7c3d1e8e52495e6494130a710bcf49ba7daa4b7cc19532c1c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.5 KB (360451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c146933accdcb44fc78f6d062325f85d95733b23edac949a2f6eab2bc4d408`

```dockerfile
```

-	Layers:
	-	`sha256:6382eab9c6b38635b7a3fb78ad98ed539cb83bd7b20c002be9c494a144dc4193`  
		Last Modified: Fri, 12 Jul 2024 21:59:59 GMT  
		Size: 328.7 KB (328725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2557cf6ec6afed3ce462129e5d588aeed7497637bec6b3d11a18e5d7cf933d8f`  
		Last Modified: Fri, 12 Jul 2024 21:59:59 GMT  
		Size: 31.7 KB (31726 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.3-fpm-alpine3.19` - linux; 386

```console
$ docker pull drupal@sha256:02fe6ede037331f58514585a4e1cbc9b68ecf88be1a756b7e4e84d08b997c171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 MB (54273665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71941603aef2caae934f90343cbca53d92db0afd2ae15b28ad2aebad6cebe52e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 12 Jul 2024 03:27:25 GMT
ADD file:0ea09fe32763883fe12b23d858a03245191055e9ab130ba28dc77053fcea5d77 in / 
# Fri, 12 Jul 2024 03:27:25 GMT
CMD ["/bin/sh"]
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 12 Jul 2024 03:27:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 12 Jul 2024 03:27:25 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_VERSION=8.3.9
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.9.tar.xz.asc
# Fri, 12 Jul 2024 03:27:25 GMT
ENV PHP_SHA256=bf4d7b8ea60a356064f88485278bd6f941a230ec16f0fc401574ce1445ad6c77
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 12 Jul 2024 03:27:25 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 12 Jul 2024 03:27:25 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 12 Jul 2024 03:27:25 GMT
RUN docker-php-ext-enable sodium
# Fri, 12 Jul 2024 03:27:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /var/www/html
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 12 Jul 2024 03:27:25 GMT
STOPSIGNAL SIGQUIT
# Fri, 12 Jul 2024 03:27:25 GMT
EXPOSE 9000
# Fri, 12 Jul 2024 03:27:25 GMT
CMD ["php-fpm"]
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV DRUPAL_VERSION=11.0.0-rc1
# Fri, 12 Jul 2024 03:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /opt/drupal
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
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
	-	`sha256:1c14f94ca6fdbe9e0ed903232f17eddb418cdb089dd5e09e657cd8d013308cdb`  
		Last Modified: Tue, 23 Jul 2024 06:09:39 GMT  
		Size: 2.3 MB (2320794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9830eeddf27df8512925b8fd2558c9509043a76bcd6463cfd66d8b6f5490ff36`  
		Last Modified: Tue, 23 Jul 2024 06:09:39 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b4e5b9df184ad775df5ed1decc716309bd8c8a1546df1cfb7cd8a337ee2221`  
		Last Modified: Tue, 23 Jul 2024 06:09:39 GMT  
		Size: 726.3 KB (726328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be8501ab27ed1c3a29faf26c661871a2b71475c3b10387ac8b69b82f51385b4`  
		Last Modified: Tue, 23 Jul 2024 06:09:39 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77f0bde2a24933fd12ed83d8a115131c08ea765d4d6a73384d05ec5ec14e103`  
		Last Modified: Tue, 23 Jul 2024 06:09:40 GMT  
		Size: 19.2 MB (19201929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:217ebca97bbe5d9ac667f33122fb776397279eceeecc67592db3e89c39c2a03e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.8 KB (380787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d754c32863a44d4e870fefce72c232f8daad989aa1cebe5a842ed07596c2a757`

```dockerfile
```

-	Layers:
	-	`sha256:05e1d7d13b1f10881347f354a2ec4cbd8f34e72cbf0aba6db54508aaad766685`  
		Last Modified: Tue, 23 Jul 2024 06:09:38 GMT  
		Size: 349.8 KB (349771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59187b23adf77120a1b400c74c1a40bf8f1efb0d0fb16a25e18d345719af42df`  
		Last Modified: Tue, 23 Jul 2024 06:09:38 GMT  
		Size: 31.0 KB (31016 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.3-fpm-alpine3.19` - linux; ppc64le

```console
$ docker pull drupal@sha256:7c5f675028548b51ea4900cc5e676111781806504c3cbe108385c8bb26116ce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56738192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df09890d10337872b2540565f54502fcb2ea73ca4213b82225e2fb5c1f35b5e3`
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
# Sat, 06 Jul 2024 00:49:38 GMT
ENV PHP_VERSION=8.3.9
# Sat, 06 Jul 2024 00:49:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.9.tar.xz.asc
# Sat, 06 Jul 2024 00:49:38 GMT
ENV PHP_SHA256=bf4d7b8ea60a356064f88485278bd6f941a230ec16f0fc401574ce1445ad6c77
# Sat, 06 Jul 2024 00:49:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 06 Jul 2024 00:49:45 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 06 Jul 2024 00:55:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 06 Jul 2024 00:55:03 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 06 Jul 2024 00:55:05 GMT
RUN docker-php-ext-enable sodium
# Sat, 06 Jul 2024 00:55:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 06 Jul 2024 00:55:06 GMT
WORKDIR /var/www/html
# Sat, 06 Jul 2024 00:55:07 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 06 Jul 2024 00:55:07 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Jul 2024 00:55:07 GMT
EXPOSE 9000
# Sat, 06 Jul 2024 00:55:07 GMT
CMD ["php-fpm"]
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV DRUPAL_VERSION=11.0.0-rc1
# Fri, 12 Jul 2024 03:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /opt/drupal
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
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
	-	`sha256:5eb9666d6fe65c7f8fb6789f9bc960718b81bf054aeb33f30bc2f1a2a9d363f6`  
		Last Modified: Fri, 12 Jul 2024 22:03:43 GMT  
		Size: 19.2 MB (19201791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:433f2f0d63054c3040ac5ce9cbd88408e601702e56cb288e6d15259896662b94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.9 KB (357906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40450fbda51739adde9721fd4cc18eb530947b515ec9d5ee80fc90479317f0c2`

```dockerfile
```

-	Layers:
	-	`sha256:87ee3a1312cba7f1c82abfdce22c7ebbe23a663a5f41270c45f037e26ab86eb7`  
		Last Modified: Fri, 12 Jul 2024 22:03:41 GMT  
		Size: 326.8 KB (326755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83ba10cfe4a96b0e2589e3a2f4efd849d0a86c58334108226834f4b7e01ae99f`  
		Last Modified: Fri, 12 Jul 2024 22:03:41 GMT  
		Size: 31.2 KB (31151 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:rc-php8.3-fpm-alpine3.19` - linux; s390x

```console
$ docker pull drupal@sha256:929565a3ebe56d1f5a42979a3b93e8ab9af7623b50fad51f0f6dc6bcbe01537c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56012957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55025007ce283c7f4d9ee9c9f569608561b7ae6479039e964e40fdf6b45fe8d8`
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
# Sat, 06 Jul 2024 01:14:29 GMT
ENV PHP_VERSION=8.3.9
# Sat, 06 Jul 2024 01:14:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.9.tar.xz.asc
# Sat, 06 Jul 2024 01:14:29 GMT
ENV PHP_SHA256=bf4d7b8ea60a356064f88485278bd6f941a230ec16f0fc401574ce1445ad6c77
# Sat, 06 Jul 2024 01:14:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Sat, 06 Jul 2024 01:14:34 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 06 Jul 2024 01:20:49 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 06 Jul 2024 01:20:50 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Sat, 06 Jul 2024 01:20:51 GMT
RUN docker-php-ext-enable sodium
# Sat, 06 Jul 2024 01:20:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 06 Jul 2024 01:20:52 GMT
WORKDIR /var/www/html
# Sat, 06 Jul 2024 01:20:52 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Sat, 06 Jul 2024 01:20:52 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Jul 2024 01:20:52 GMT
EXPOSE 9000
# Sat, 06 Jul 2024 01:20:52 GMT
CMD ["php-fpm"]
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
ENV DRUPAL_VERSION=11.0.0-rc1
# Fri, 12 Jul 2024 03:27:25 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Fri, 12 Jul 2024 03:27:25 GMT
WORKDIR /opt/drupal
# Fri, 12 Jul 2024 03:27:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Fri, 12 Jul 2024 03:27:25 GMT
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
	-	`sha256:54c5533f4942f37e0b74f681c28abad275bbbce2b8fdeb7efb59195b08515f16`  
		Last Modified: Fri, 12 Jul 2024 22:03:43 GMT  
		Size: 19.2 MB (19201724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:rc-php8.3-fpm-alpine3.19` - unknown; unknown

```console
$ docker pull drupal@sha256:e8b2dfb772912553db6b4a83e4524db1bf1731a74f27c2a47ca8afa96406da6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **357.8 KB (357831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9be5129cfca096deeb446371e60fc93d1856b35e8e7a2b7a31518ed3de7e57`

```dockerfile
```

-	Layers:
	-	`sha256:d7ead7ca4881c891389dcf8981b1443c5f3c03c5f6fe59b39b2fd3357d623155`  
		Last Modified: Fri, 12 Jul 2024 22:03:42 GMT  
		Size: 326.7 KB (326727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4df3d71f3162f422a039e6efc46b3ad980c604f9b846c706c76d730a5cd18ed1`  
		Last Modified: Fri, 12 Jul 2024 22:03:42 GMT  
		Size: 31.1 KB (31104 bytes)  
		MIME: application/vnd.in-toto+json
