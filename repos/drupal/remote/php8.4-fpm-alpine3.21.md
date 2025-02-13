## `drupal:php8.4-fpm-alpine3.21`

```console
$ docker pull drupal@sha256:53d74e948b0c17811bde15258882b76cca2e3b87ddb1173775023abd09007178
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

### `drupal:php8.4-fpm-alpine3.21` - linux; amd64

```console
$ docker pull drupal@sha256:e54670da985fc67779eeac3b0af3cd07f50d8253d43b8d09fe68ab99d73f64b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61813262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab0f02d500ba7204038aef63f9b340483d8c3f30bcb6fbe3bc3ea8f6cf987650`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
WORKDIR /var/www/html
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
STOPSIGNAL SIGQUIT
# Fri, 17 Jan 2025 01:46:40 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["php-fpm"]
# Tue, 11 Feb 2025 00:01:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
ENV DRUPAL_VERSION=11.1.2
# Tue, 11 Feb 2025 00:01:46 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 11 Feb 2025 00:01:46 GMT
WORKDIR /opt/drupal
# Tue, 11 Feb 2025 00:01:46 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e89f75d4f4b27ab12f7c9e979e06153a7cbc6a0646efb933101f3803775dd52`  
		Last Modified: Fri, 17 Jan 2025 21:26:18 GMT  
		Size: 3.3 MB (3333774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a47b8a53b3745947177ce8a23b4f09869cccb419abf0a179415025eeede6e5`  
		Last Modified: Fri, 17 Jan 2025 21:26:17 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbff75b3ca6137e77f94a366274c57f6ef80622a2dba1f799cc36a6e84f250e0`  
		Last Modified: Fri, 17 Jan 2025 21:26:17 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957d706fab0c56be8e505920ccebf9bf01a4774856c6eba70f7aacfad07bf9a5`  
		Last Modified: Fri, 17 Jan 2025 21:26:21 GMT  
		Size: 13.6 MB (13591522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b18822abce55af491ddc5412d421458dc40844154b7348bb9c81d86ffeeeb3`  
		Last Modified: Fri, 17 Jan 2025 21:26:19 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cd2b2329d1ac48acf2e56ac35a03e429ca5beaab1f17aad9e16c999df0a7ce`  
		Last Modified: Fri, 17 Jan 2025 21:26:24 GMT  
		Size: 15.6 MB (15630898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e961734941eca83344d470c08a4528795b7d7596d1d871749b6889b7c4b43a08`  
		Last Modified: Fri, 17 Jan 2025 21:26:21 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce69e88ccc0caf9688c796bb895782ecab7007e575425b489c6dbbed21f9d54e`  
		Last Modified: Fri, 17 Jan 2025 21:26:21 GMT  
		Size: 20.0 KB (20043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3001248bf3d5ba89948afeec1edd54b21e72d2142ac2b870235e221490d70a28`  
		Last Modified: Fri, 17 Jan 2025 21:26:23 GMT  
		Size: 9.2 KB (9191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87cca704bbce8c1e80c5ef6cfd47619aa31128c7dad0b648fa4f112e43606d3`  
		Last Modified: Wed, 12 Feb 2025 22:20:18 GMT  
		Size: 4.8 MB (4793686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:921a1935eadb0f9c5c8e1a51a7bea6215309378250597164cb090df470efd51a`  
		Last Modified: Wed, 12 Feb 2025 21:06:33 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c01f6a5700390e6aa3fecdbdc8fb694d901fb40dcb605b095b46bd7000b2780`  
		Last Modified: Wed, 12 Feb 2025 22:20:18 GMT  
		Size: 740.4 KB (740354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:913a8521268c64f248f1cbd2baf9650744d195dfeb68dd2c8b58e9a3d4ee3919`  
		Last Modified: Wed, 12 Feb 2025 21:08:59 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6d637c7d2e9b4e48afc6c2f96569162a89d0bc3a11e7cd44fb3d8b873db7185`  
		Last Modified: Wed, 12 Feb 2025 21:06:38 GMT  
		Size: 20.0 MB (20047526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:41fef074c0523d22c9cc26ccff3377323f734e8288ff1289aa97d6c201121977
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.7 KB (384663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f9bcd9dbedc5ea0b377d6f915471c658a3bad0be46ec4b9c01629867780894`

```dockerfile
```

-	Layers:
	-	`sha256:f6ea7726dce159926806cc5eddfce782292b2cf54bf267a4da679b4656389b01`  
		Last Modified: Wed, 12 Feb 2025 17:30:51 GMT  
		Size: 351.0 KB (350973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1816097cd69f0fbed7b4bda7c5ac50795d25a31c2e057082247f2917af1d5043`  
		Last Modified: Wed, 12 Feb 2025 17:30:51 GMT  
		Size: 33.7 KB (33690 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine3.21` - linux; arm variant v6

```console
$ docker pull drupal@sha256:b1f61cde4c9e5202a1c902ad6c4957b77e4bff755d3955a48dc371ec15850ce2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59077355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f749ee604c99fc945460f81cb1b37cc6d6f30058ae42478279f76fe0ee7157d8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
WORKDIR /var/www/html
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
STOPSIGNAL SIGQUIT
# Fri, 17 Jan 2025 01:46:40 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["php-fpm"]
# Tue, 11 Feb 2025 00:01:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
ENV DRUPAL_VERSION=11.1.2
# Tue, 11 Feb 2025 00:01:46 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 11 Feb 2025 00:01:46 GMT
WORKDIR /opt/drupal
# Tue, 11 Feb 2025 00:01:46 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27df19b1748e0c5336a2934dab90837cecaea9ecf548f60ec89ced0bb3caa23`  
		Last Modified: Wed, 15 Jan 2025 01:25:26 GMT  
		Size: 3.3 MB (3300488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d8c9d60966ee150dd112939c109e4bdb3925301588315d098c22b807f8a62c`  
		Last Modified: Wed, 15 Jan 2025 08:46:52 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5af0368056bd9d6658ab6d584d82811582bf7d94d14851784fefbce2ac6bd01`  
		Last Modified: Wed, 15 Jan 2025 08:46:53 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c35832122daf4e6cfd46f0be114a1c6d91b28caceb8f9b86ccb0253e0678632`  
		Last Modified: Fri, 17 Jan 2025 21:24:21 GMT  
		Size: 13.6 MB (13591522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abac4d6df3f8471bdecc32831cfc97f2c065ebc58af29566d6e67161775d19e0`  
		Last Modified: Fri, 17 Jan 2025 21:24:17 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5b0533d4e37d067e58ac8098dc274b50e0dcb976261daba3fa73d607804e2d`  
		Last Modified: Fri, 17 Jan 2025 21:26:37 GMT  
		Size: 14.2 MB (14160681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6520bc0e1a5f0d267056c9ff6b0bca353e893e1840622561000079a79941808`  
		Last Modified: Fri, 17 Jan 2025 21:26:35 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d1e71854b13c38cdcdc3d2bfe5494176eb3a3537517e3576b6e07ab64a711ae`  
		Last Modified: Fri, 17 Jan 2025 21:26:35 GMT  
		Size: 19.8 KB (19845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ae57009918872e81a92278159a5094d17a90df90b2fbf4662ccdd5ee435fca`  
		Last Modified: Fri, 17 Jan 2025 21:26:35 GMT  
		Size: 9.2 KB (9188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef5a2433c9cc20773ba75dabc38e3729a02d9b61203d27b69a2f2521fa19505`  
		Last Modified: Thu, 13 Feb 2025 09:05:34 GMT  
		Size: 3.8 MB (3839423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ffbfc779f09507bceefff522fdeb35d7f3d62804ebefba44d6f58729752313`  
		Last Modified: Thu, 13 Feb 2025 09:05:34 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579e4da03c1c5cd4aeeee2e3f2e2761979a4d1b25f64c2b36446fc36dbb86d27`  
		Last Modified: Thu, 13 Feb 2025 09:05:35 GMT  
		Size: 740.4 KB (740351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce12f0b09b89fadab5406bdbc4940bb5db8d04f384e71c51b204ab4f062315f`  
		Last Modified: Thu, 13 Feb 2025 09:05:35 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef46ce57f624f63f375f97cbd3c1be53e90d69fecccaa1ac078d82497fc17d76`  
		Last Modified: Thu, 13 Feb 2025 09:05:38 GMT  
		Size: 20.0 MB (20047426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:55081a571b4f34c09e49b83fd95f54f83818ff91054fa50db7cdcf98679bf5a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.6 KB (33631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdef30d00da5398921c899ad54adf6e975b7e373d0789b45dba779f205d96303`

```dockerfile
```

-	Layers:
	-	`sha256:1626fd16c6dc6e879dad9a87cd9b7d972ee570c74472f1109c6e18e51d7ce8be`  
		Last Modified: Wed, 12 Feb 2025 17:31:14 GMT  
		Size: 33.6 KB (33631 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine3.21` - linux; arm variant v7

```console
$ docker pull drupal@sha256:6d54990df0c254a699ffbd1b2da4445ed0fc1ffa6ef6adc4535e23dc49682a27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57606599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd47986e432e321fff5bf08d1f6dd3526f6c8056f70d1a156e04b9d33a866a22`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
WORKDIR /var/www/html
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
STOPSIGNAL SIGQUIT
# Fri, 17 Jan 2025 01:46:40 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["php-fpm"]
# Tue, 11 Feb 2025 00:01:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
ENV DRUPAL_VERSION=11.1.2
# Tue, 11 Feb 2025 00:01:46 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 11 Feb 2025 00:01:46 GMT
WORKDIR /opt/drupal
# Tue, 11 Feb 2025 00:01:46 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5ceb78f083649061e4b802531e1ff0a876077474242c75cfdca63feceddf42`  
		Last Modified: Wed, 15 Jan 2025 00:11:56 GMT  
		Size: 3.1 MB (3115360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3874d1ba95c5456f76e6eaf3fcad122706769776c7031c7f79e4104de9979281`  
		Last Modified: Wed, 15 Jan 2025 00:28:56 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237b35dc6dca52f50940237e3dd268e0dbbd22216c7d386d5989137c1f820852`  
		Last Modified: Wed, 15 Jan 2025 00:11:56 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fd21ecbb1437ff572027296c81b71ea6bcf753dfcb9fced9a3e4c513608ce85`  
		Last Modified: Fri, 17 Jan 2025 21:24:38 GMT  
		Size: 13.6 MB (13591526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1714aa8068ed2453409143cd56f70e2daac1988bea2f2e8110ff2819aebbd6ff`  
		Last Modified: Fri, 17 Jan 2025 21:24:34 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d56892ed34278e50c50d009cc889860075382dd33ba7fbdf8fc58812a8e71678`  
		Last Modified: Fri, 17 Jan 2025 21:26:50 GMT  
		Size: 13.4 MB (13416268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc1528624c6a93e9d863d69426bcef38bb4f5077651f2b219aa5217bf35b729`  
		Last Modified: Fri, 17 Jan 2025 21:26:48 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3997e6970972fea5f9d4e24454ceb152c88bb4484eb3c4314ff607df478c9aa0`  
		Last Modified: Fri, 17 Jan 2025 21:26:48 GMT  
		Size: 19.9 KB (19852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f68ca33fd3b04bebefa0c557fa870551982a3299636fd1efbdcfe537fa0095`  
		Last Modified: Fri, 17 Jan 2025 21:26:49 GMT  
		Size: 9.2 KB (9192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f322b9644d6e2af84974b5f0ef9eb1f34d8685c4bcaa7050b05217dcaec92830`  
		Last Modified: Wed, 12 Feb 2025 17:38:15 GMT  
		Size: 3.6 MB (3565013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7569f74743a3b6c7a933cab7e3396896885c2d7e3ed3121e41da799dbff45793`  
		Last Modified: Wed, 12 Feb 2025 17:38:15 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28800c374cfe2427bdd59fc508db4208e70e3da7bb739f41db6ef92b561b669a`  
		Last Modified: Wed, 12 Feb 2025 17:38:15 GMT  
		Size: 740.4 KB (740353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02be66b1e337514ddfe497cfffdd90324e24070ea888d4d85003bf57896980ed`  
		Last Modified: Wed, 12 Feb 2025 17:38:15 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bde2fe0fbd487912b0bd9043da593441a7ffc0de4e663fbaf33a53b03eec9e78`  
		Last Modified: Wed, 12 Feb 2025 17:38:17 GMT  
		Size: 20.0 MB (20047371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:62a487e1f28e500828390c54f7c2c20544c0c9c75315c4f2899a10479bd48f72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.4 KB (393372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6332faca8a69a8074d398c0e27febae1ebdc381e31498077fe761167d95aaf4`

```dockerfile
```

-	Layers:
	-	`sha256:39c286dce041b5a13d4abfb1e717f50eb322a6c444cb551d8923cb6e9e3b44ca`  
		Last Modified: Wed, 12 Feb 2025 17:38:15 GMT  
		Size: 359.5 KB (359526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4d8232b609fe59120dd281bb7e4881987beba866688d9e91ffa6847aa96d7fa`  
		Last Modified: Wed, 12 Feb 2025 17:38:15 GMT  
		Size: 33.8 KB (33846 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:de0f4459530b418d2ea819288b9ca636ecf195acc3576d031b73b5e576075644
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62001490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf93cfff5603a082c84b0151b7127c9459e475f0cdf90ddfc4d9a745e1c828ac`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
WORKDIR /var/www/html
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
STOPSIGNAL SIGQUIT
# Fri, 17 Jan 2025 01:46:40 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["php-fpm"]
# Tue, 11 Feb 2025 00:01:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
ENV DRUPAL_VERSION=11.1.2
# Tue, 11 Feb 2025 00:01:46 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 11 Feb 2025 00:01:46 GMT
WORKDIR /opt/drupal
# Tue, 11 Feb 2025 00:01:46 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a259b492a8c3558416dd48f8aad1dda78fda9cef38298295c5e43623b56a18c`  
		Last Modified: Tue, 14 Jan 2025 20:34:52 GMT  
		Size: 3.3 MB (3327674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549c6a796a4d698d720516d98efaded2b858014b8a81418484745626b542df1b`  
		Last Modified: Tue, 14 Jan 2025 20:34:51 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e06c334c2725cc400bba17c21a0380b9f9c970473c4959000a3921b22cdf4a8`  
		Last Modified: Tue, 14 Jan 2025 20:34:37 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759ded2f1970092c503a682b521201d635e8da0ad60d85a3975060091b0f092d`  
		Last Modified: Fri, 17 Jan 2025 21:24:54 GMT  
		Size: 13.6 MB (13591559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12833fff26b4ea2cc381b02e1323f22bd1ac14a4e52a6c8417bbaa55152bd4e`  
		Last Modified: Fri, 17 Jan 2025 21:24:50 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7177dacb9ed8436a2a4552e02cb1238f59ff0109ae9c635f331e8746d9d4456`  
		Last Modified: Fri, 17 Jan 2025 21:27:05 GMT  
		Size: 15.3 MB (15261410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb77eac889ad763c9c9dbb47e90a1ee163cf71a8d6386e2d7eea1e2b55d80412`  
		Last Modified: Fri, 17 Jan 2025 21:27:02 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73601db43478d6d0698b63001a860ed31cc87bdbe0123ae151c2fe2575673279`  
		Last Modified: Fri, 17 Jan 2025 21:27:02 GMT  
		Size: 19.8 KB (19848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96927e4e23f48ff2ffbdfdbe75678b60ace5d1035af6280413a28bdb91fa1550`  
		Last Modified: Fri, 17 Jan 2025 21:27:02 GMT  
		Size: 9.2 KB (9194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1966d36655ac9f965f3b06f219e48abd16672c414e1e05b5131b073af0be70ba`  
		Last Modified: Wed, 12 Feb 2025 21:07:13 GMT  
		Size: 5.0 MB (5007118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e870590c49a19507488440dd0bafe53ca239077254953f3f29e2525521284bf`  
		Last Modified: Wed, 12 Feb 2025 21:07:12 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83077b4436c76d0a5b45ac0e3d0b70be3cba1b55576260480fdbb768b121b3a2`  
		Last Modified: Wed, 12 Feb 2025 21:07:13 GMT  
		Size: 740.4 KB (740350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f39ac0dab57c24ff596d14903d3ce8af2e1207d0a53f73bf5a5b948327fca25`  
		Last Modified: Wed, 12 Feb 2025 21:07:14 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8459d38eb2593e549cca0c67813a0c14c6fee7f523969ef9280066c5d3ded9a0`  
		Last Modified: Wed, 12 Feb 2025 21:07:17 GMT  
		Size: 20.0 MB (20047425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:80fdc6bca374a09924e3b3bd860a0818eabca41bb4dc34f5ea311aa3b3bbfe05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.5 KB (393460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e198a92301da07c6dc6b2e4eea83d756b6e3f4fc31b7057727c8f44e9731726`

```dockerfile
```

-	Layers:
	-	`sha256:488f0e0b0c81a10a3f61d8d1df5627331ab7ad88a1a9f2a27b1ddfd1686820e4`  
		Last Modified: Wed, 12 Feb 2025 17:37:07 GMT  
		Size: 359.6 KB (359562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebea0e5004dd998df113f99c410129dbd156a50a2341c9edf0bee4d69e87bf8e`  
		Last Modified: Wed, 12 Feb 2025 17:37:06 GMT  
		Size: 33.9 KB (33898 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine3.21` - linux; 386

```console
$ docker pull drupal@sha256:ef905f1f5827fde1b527d98942c774c159590bb9eff54ef5fd98f290a6442cfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61978191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb223608009ba8d02a1b7185abde8c12771a86b1227c732532530f852c1309d1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
WORKDIR /var/www/html
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
STOPSIGNAL SIGQUIT
# Fri, 17 Jan 2025 01:46:40 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["php-fpm"]
# Tue, 11 Feb 2025 00:01:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
ENV DRUPAL_VERSION=11.1.2
# Tue, 11 Feb 2025 00:01:46 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 11 Feb 2025 00:01:46 GMT
WORKDIR /opt/drupal
# Tue, 11 Feb 2025 00:01:46 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de7bf241ab457f2dd2e0aaba5d5a871fe606811a040f10372c07a82e855e94e`  
		Last Modified: Fri, 17 Jan 2025 21:27:16 GMT  
		Size: 3.4 MB (3373769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e57ceb5ecd58823d805208beffa7e24ede9029826e4c0f4e340ff7d5777701d9`  
		Last Modified: Fri, 17 Jan 2025 21:27:16 GMT  
		Size: 944.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19cd15cd422cab1c9539c218f233f00bf452964c97f0c96214d7f97740b48c1a`  
		Last Modified: Fri, 17 Jan 2025 21:27:16 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b87594f52eb8d0a491210e96018695f43b97704782f1f5614d476627924aa08`  
		Last Modified: Fri, 17 Jan 2025 21:27:20 GMT  
		Size: 13.6 MB (13591509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844aa4cef37e20ec2872ca4240220914fa3c82b01707ce620e281114e0aee6ab`  
		Last Modified: Fri, 17 Jan 2025 21:27:18 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ede1f9ffb2cc3d6d55bf2d2782840ba94ab92eeaee9d4c1da91b5bc67e38855`  
		Last Modified: Fri, 17 Jan 2025 21:27:24 GMT  
		Size: 16.0 MB (16018690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0228af4e5dba017c736405404b731ec47d36d5570be8ab0737efc7fcc60db0b1`  
		Last Modified: Fri, 17 Jan 2025 21:27:20 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4532e162d4c2cc4df4d5620661c1a33f1c0f24ca81b12ed1d357851f474eb501`  
		Last Modified: Fri, 17 Jan 2025 21:27:20 GMT  
		Size: 20.0 KB (20031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332f4e5a9cf94cb9398bb1b73dbf02b347b0b92ec72e9e6c2cd0bc4a3551f00b`  
		Last Modified: Fri, 17 Jan 2025 21:27:22 GMT  
		Size: 9.2 KB (9189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0de3dc2f93635125e7c6d565caed9904821908e1e5e89c8d3cf6f6b58d76d78`  
		Last Modified: Wed, 12 Feb 2025 17:31:10 GMT  
		Size: 4.7 MB (4709882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c996ed251f9565d05be184f00ea7c1c8e99bf07e2f6b8a4e2d4c964e7bd1c6`  
		Last Modified: Wed, 12 Feb 2025 17:31:10 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de61629ad3e58bdfe9f62bd8aa87e7d67bb9f2b752a5f00c2bfc25081bdc7cd`  
		Last Modified: Wed, 12 Feb 2025 17:31:10 GMT  
		Size: 740.3 KB (740349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffad31843d8d112ee79ba16c9a2403f56b3fd586b53d6ae354c8022d65d0c1d6`  
		Last Modified: Wed, 12 Feb 2025 17:31:10 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac723fc143b7e36b518502988fa52bb36aec1d16e8852c904fc2c7ac994e4674`  
		Last Modified: Wed, 12 Feb 2025 17:31:11 GMT  
		Size: 20.0 MB (20047098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:c88c1d5e4652683b7fead83a849385d816ec916d78d1607a30cdd18e58030b00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.6 KB (384555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e06944911360b955e2fd76b9d4d5e68f288aaac02818b09ac781d3d54ea71b1`

```dockerfile
```

-	Layers:
	-	`sha256:3ef30e14ade74248555687e687cc42b9b9968a61c72eec59fd0a45f1445704c9`  
		Last Modified: Wed, 12 Feb 2025 17:31:09 GMT  
		Size: 350.9 KB (350928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e62ecbbcb0a2fe0d6b360952832c54db7949e4db6cb285436af62fe364229e9`  
		Last Modified: Wed, 12 Feb 2025 17:31:10 GMT  
		Size: 33.6 KB (33627 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine3.21` - linux; ppc64le

```console
$ docker pull drupal@sha256:6821427aa8f2a3815aff48fe29b332de271a402729eebaed739962ea63ae966a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.9 MB (61895573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfcab022f2dac75665df740aeca2b1e342f3c9cba4484c5fa26587fde5124da0`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
WORKDIR /var/www/html
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
STOPSIGNAL SIGQUIT
# Fri, 17 Jan 2025 01:46:40 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["php-fpm"]
# Tue, 11 Feb 2025 00:01:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
ENV DRUPAL_VERSION=11.1.2
# Tue, 11 Feb 2025 00:01:46 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 11 Feb 2025 00:01:46 GMT
WORKDIR /opt/drupal
# Tue, 11 Feb 2025 00:01:46 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Tue, 14 Jan 2025 20:33:45 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e88c0bde0da532d37286f677138c7e480dcb6f566920007e98f5e5eb88d6d4`  
		Last Modified: Wed, 15 Jan 2025 04:47:37 GMT  
		Size: 3.5 MB (3476342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3cc68900042575ac984146d93aef63e5c37b3e8c420156abe75bd0eab7f3e2`  
		Last Modified: Wed, 15 Jan 2025 04:47:36 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bec6f6109cf776dd85e5729606c85d0024f7d6d1ec08e54ddb40c264cc4f45`  
		Last Modified: Wed, 15 Jan 2025 04:47:36 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b4383e34608c265e3fcbc92f32f5b8e945fc93e6ecdaee910fa87b61b91eb7`  
		Last Modified: Fri, 17 Jan 2025 21:25:28 GMT  
		Size: 13.6 MB (13591557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0e98b79c382ca554316b5d1b58a69661a67bd73dd451dd9abba75515417cbf`  
		Last Modified: Fri, 17 Jan 2025 21:25:24 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e1d1f25a109f093c6c2144ed2a9656dfc7b9425cf6debe124b43132a7454a1`  
		Last Modified: Fri, 17 Jan 2025 21:27:38 GMT  
		Size: 16.1 MB (16113529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ab6bd3e18afedbcce6c3309bf3fabc0f74ab1a8ca6b0d721a62cca56c8c2c9`  
		Last Modified: Fri, 17 Jan 2025 21:27:35 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4efce51cee913e64bc23896ae3cf63d21778e33d992a1509c45ee36f77892bc`  
		Last Modified: Fri, 17 Jan 2025 21:27:35 GMT  
		Size: 19.9 KB (19852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f5db3fbfacba64b8a1f3f2038183bc7483b60570f926d5e4fa486977def2704`  
		Last Modified: Fri, 17 Jan 2025 21:27:36 GMT  
		Size: 9.2 KB (9193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb0cf37abe7afa121e6851558fa6cbc6247fd6a72c19a2315eb9d2907b20c0c`  
		Last Modified: Wed, 12 Feb 2025 17:36:47 GMT  
		Size: 4.3 MB (4319347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b900d2f53c4ee45c5d0f22c35997444cc81fb929f41320aac6a777f0068cc3c1`  
		Last Modified: Wed, 12 Feb 2025 17:36:46 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f94fa3f06477afa92ae01aeaf1826e5c439170a6543f39741cae5ee535a1723`  
		Last Modified: Wed, 12 Feb 2025 17:36:47 GMT  
		Size: 740.4 KB (740350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3161316b7305a581d54a822e6e087821eebf33e478958fd33e718e5238a8aa92`  
		Last Modified: Wed, 12 Feb 2025 17:36:46 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59e87db6217d06362dd55b5a39cc6a96d4646d5692a698b909352c540d513aff`  
		Last Modified: Wed, 12 Feb 2025 17:36:48 GMT  
		Size: 20.0 MB (20047244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:684ab1cf3c78e1a405c12ed8b76b66ef6677f318e3c34a3a7d0b701c28ccd936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.3 KB (391337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33f1a4d247a88759d09177388dd724e621f9f2a68fcb6083132ef313a906965c`

```dockerfile
```

-	Layers:
	-	`sha256:17006ae889be1e23aa941ae6cc190f631a00b63277a379a915243139c29ebe1a`  
		Last Modified: Wed, 12 Feb 2025 17:36:46 GMT  
		Size: 357.6 KB (357565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62aa94f2387da139b7b2bd2d2ebe215950b536b30a0309f6ebffc3e8270a43f3`  
		Last Modified: Wed, 12 Feb 2025 17:36:46 GMT  
		Size: 33.8 KB (33772 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine3.21` - linux; riscv64

```console
$ docker pull drupal@sha256:7ef5cb445641963ee34f3cb2405026ce31129f58951154bc90f5ef0a6ce6ca9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.2 MB (60183612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57b04eb845ba2eabca8322f6ffa911fa287e40404ad33804a29ac9ff98548f0b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
WORKDIR /var/www/html
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
STOPSIGNAL SIGQUIT
# Fri, 17 Jan 2025 01:46:40 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["php-fpm"]
# Tue, 11 Feb 2025 00:01:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
ENV DRUPAL_VERSION=11.1.2
# Tue, 11 Feb 2025 00:01:46 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 11 Feb 2025 00:01:46 GMT
WORKDIR /opt/drupal
# Tue, 11 Feb 2025 00:01:46 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Tue, 14 Jan 2025 20:35:37 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743579fbfa9d6a462255cb84fc5b099d3cf542442a9305bc0f96bce81c76e4f3`  
		Last Modified: Wed, 15 Jan 2025 08:47:48 GMT  
		Size: 3.5 MB (3457918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550ac1c09c8b9181323bf079ede440cee01f0fec62e09b75afcae7c35627d0e6`  
		Last Modified: Wed, 15 Jan 2025 03:01:25 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0810a5f710bc8b0a06b441c232e302e968233890edb8bd1ae54afee19878e9f1`  
		Last Modified: Wed, 15 Jan 2025 10:06:18 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e64793aaff3751dd44a42f619b3870dc06bfb2a283e8e4704ed79aa8325e08c`  
		Last Modified: Fri, 17 Jan 2025 21:25:44 GMT  
		Size: 13.6 MB (13591547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cafbd5ca2c5d1d981667732f0d492033946c9800b55728bdad3fa51ea766762`  
		Last Modified: Fri, 17 Jan 2025 21:25:41 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cb9640dd16260f580615a6bb314d03cd2f4cc6a61f1c8a6a567baed8bf9e749`  
		Last Modified: Sat, 18 Jan 2025 21:15:39 GMT  
		Size: 15.0 MB (15049842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d62e41a3eca1bc8e12df4f73dcc603f4bea49907d3b432ab9a1ef96e0aaa489f`  
		Last Modified: Sat, 18 Jan 2025 21:15:35 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4bdfbe6d6ae3b4c7499235f73f39b31848ad1b902dd2deb5c6d64f796f0514b`  
		Last Modified: Sat, 18 Jan 2025 21:15:36 GMT  
		Size: 19.8 KB (19842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5628394cd21957c5eb42ebd924266c5d5650f6e6870f7e59da381cc0e9235e28`  
		Last Modified: Sat, 18 Jan 2025 21:15:36 GMT  
		Size: 9.2 KB (9194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eae2d407fd2265610dbbf8d158a170fb419510f01597a77aa0feba46d822cfc`  
		Last Modified: Wed, 12 Feb 2025 17:39:37 GMT  
		Size: 3.9 MB (3911721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d59f2769779d7c908019a027cf36f02ef1efa26cff51023a17e935c6fdabc498`  
		Last Modified: Wed, 12 Feb 2025 17:39:37 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a8027d904cd36557f9c451ab321621e9ce60032d59d375fff961ba084db92c`  
		Last Modified: Wed, 12 Feb 2025 17:39:37 GMT  
		Size: 740.4 KB (740353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93e1ed39703accfcd2f6913d204398d96decef22584f372552f1ba0157b658b`  
		Last Modified: Wed, 12 Feb 2025 17:39:37 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b68cf2c3b4b123ab8f92056212ab1a04ed7f2b76660e672bce99893a078eaf14`  
		Last Modified: Wed, 12 Feb 2025 17:39:41 GMT  
		Size: 20.0 MB (20048374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:53fa4e177cef2d2a5b4e95d69c255d9273446bd7ce3ad0121bc75bdf273f82de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.3 KB (391333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff44a86a24f58b7051621dad6d05c9e2e3a8f42e7583236c090cc5944f010e34`

```dockerfile
```

-	Layers:
	-	`sha256:3b83a7ee8e791ad11e05dd19cc525a34117ff7dc9550e7c2626543ab3ab17a29`  
		Last Modified: Wed, 12 Feb 2025 17:39:36 GMT  
		Size: 357.6 KB (357561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04445d5e118a94dc630f8b093d4b0e3825c3e443a1df680cb575a3bd5644782b`  
		Last Modified: Wed, 12 Feb 2025 17:39:36 GMT  
		Size: 33.8 KB (33772 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine3.21` - linux; s390x

```console
$ docker pull drupal@sha256:58dc5ec184db760ed1e66ef2de72bf7905bc1f39859cfdbb21c76201349f17a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61431761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a476e4268db7ea618946b7cf4cef738c865bd3bcff759dfab740041ea5160aa`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Jan 2025 12:07:30 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:07:30 GMT
CMD ["/bin/sh"]
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 17 Jan 2025 01:46:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Jan 2025 01:46:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_VERSION=8.4.3
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.3.tar.xz.asc
# Fri, 17 Jan 2025 01:46:40 GMT
ENV PHP_SHA256=5c42173cbde7d0add8249c2e8a0c19ae271f41d8c47d67d72bdf91a88dcc7e4b
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 17 Jan 2025 01:46:40 GMT
WORKDIR /var/www/html
# Fri, 17 Jan 2025 01:46:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 17 Jan 2025 01:46:40 GMT
STOPSIGNAL SIGQUIT
# Fri, 17 Jan 2025 01:46:40 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 17 Jan 2025 01:46:40 GMT
CMD ["php-fpm"]
# Tue, 11 Feb 2025 00:01:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
ENV DRUPAL_VERSION=11.1.2
# Tue, 11 Feb 2025 00:01:46 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Tue, 11 Feb 2025 00:01:46 GMT
WORKDIR /opt/drupal
# Tue, 11 Feb 2025 00:01:46 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Tue, 11 Feb 2025 00:01:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Tue, 14 Jan 2025 20:34:39 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26282a4a0a714cd1f4efa558a9c16c549bcb3d98039f808a2da09f37551fac63`  
		Last Modified: Wed, 15 Jan 2025 04:47:39 GMT  
		Size: 3.6 MB (3561274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82035fdc219157bbb0deab69c2a1382fccf8a51ac5b20be190e26173e8a8be95`  
		Last Modified: Wed, 15 Jan 2025 04:47:36 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c31af6d9d81023b2dbb6d6e14114bb3c0a961f429216de8f8cdfd98fb13c317`  
		Last Modified: Wed, 15 Jan 2025 04:47:34 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0fc7cff5036cf5b5616852253d5d9633415871bca83e115da4d7d0881e1898a`  
		Last Modified: Fri, 17 Jan 2025 21:26:01 GMT  
		Size: 13.6 MB (13591550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d05694c633358a0136f7d794f58e3cae9a7757dcd871f7deb226edc14ca8286`  
		Last Modified: Fri, 17 Jan 2025 21:25:57 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d1ce7fd5aa61fe1b8e0a38bc3b79eeceab4f78903d1c01bcb236e5991cd5ee`  
		Last Modified: Fri, 17 Jan 2025 21:27:54 GMT  
		Size: 15.8 MB (15820920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfc79dfcd92abb707239dfa4340a7c0c3ad661ae93436e7dc36aa63a01941ff`  
		Last Modified: Fri, 17 Jan 2025 21:27:50 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef25254cfbf60567fb736f99c675a293904b4e3582558550245674529531c19c`  
		Last Modified: Fri, 17 Jan 2025 21:27:51 GMT  
		Size: 19.8 KB (19845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf5c50112abfe85c179e1d718c430eff615d3d8a49eaa7d7cb1997574139463`  
		Last Modified: Fri, 17 Jan 2025 21:27:51 GMT  
		Size: 9.2 KB (9194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc149c61380ff845797c7abdef5a23285483c8e7b7c58067afced50a6ef5391`  
		Last Modified: Wed, 12 Feb 2025 17:54:20 GMT  
		Size: 4.2 MB (4169643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c224f9669c8a763ab96bd25a7990a56080848bb435cc9a19b5e693df3fb8b45e`  
		Last Modified: Wed, 12 Feb 2025 17:54:20 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc200548dcf775118610efa28288e96caca1516d14dda5831e6e53f5ed857ed`  
		Last Modified: Wed, 12 Feb 2025 19:19:47 GMT  
		Size: 740.4 KB (740353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b29d1d2a473c25fdae3de7a0843ac479174528af5167474669ac818a827cdbc`  
		Last Modified: Wed, 12 Feb 2025 17:54:20 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5d3cd24ca242f3fe09df331f28f473adb16db2134d73e99781e19aed849e7f`  
		Last Modified: Wed, 12 Feb 2025 19:24:20 GMT  
		Size: 20.0 MB (20047559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:f7aa7ae03e858324d63e801a162a6dd14c4560412c438335df52615116439703
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.0 KB (388998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f176cad564aa4348b9c18340f745fc1437a275fcdd2fc2db799bc60eec011bc8`

```dockerfile
```

-	Layers:
	-	`sha256:5b55e1a5b22971d0f07a51bff40c9a55bd9f5ea54467d16387caa944399011cf`  
		Last Modified: Wed, 12 Feb 2025 19:24:18 GMT  
		Size: 357.5 KB (357507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4a08251dae8048d9c9578c72781db02e14d9ad64bd061aa4fd102728005fec5`  
		Last Modified: Wed, 12 Feb 2025 19:24:18 GMT  
		Size: 31.5 KB (31491 bytes)  
		MIME: application/vnd.in-toto+json
