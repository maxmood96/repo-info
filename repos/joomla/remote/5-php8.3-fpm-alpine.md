## `joomla:5-php8.3-fpm-alpine`

```console
$ docker pull joomla@sha256:4ffed73611a6e7a17b9ddeae4358b6712aa75b00e737a46dc5705ae388e53546
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

### `joomla:5-php8.3-fpm-alpine` - linux; amd64

```console
$ docker pull joomla@sha256:3765144585a44e5c72b1f362f6cc41dfc796f0e25fb2507b5fd60d6258cf1738
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.2 MB (91234398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af836d94f1dfd9833a4d617cced98edeb4df39deabaeb37eb52981e5c5b6ed23`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Jan 2025 08:12:24 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["/bin/sh"]
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 08 Jan 2025 08:12:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 08 Jan 2025 08:12:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_VERSION=8.3.16
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 08 Jan 2025 08:12:24 GMT
WORKDIR /var/www/html
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 08 Jan 2025 08:12:24 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["php-fpm"]
# Wed, 08 Jan 2025 08:12:24 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 		zstd 	; # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
VOLUME [/var/www/html]
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_VERSION=5.2.3
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_SHA512=23c74065759fcf812c9c27b14bdefc1d255e074227585e154b39ef5fb9279668a63a51c12b1fec3d4e611dd7147c8ab2eec972bc5e31bacb12cb08989b37c3e9
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.2.3/Joomla_5.2.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae49de6b59a3ada68038915c6ced5c3fe9a4d9734c795f5a290799df9bd4beaf`  
		Last Modified: Fri, 17 Jan 2025 01:33:31 GMT  
		Size: 3.3 MB (3333625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71cba018865568c1d0e52317c42c2372693e63212bbfa9fdef74f0c36c092346`  
		Last Modified: Fri, 17 Jan 2025 01:33:31 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8c926c51f944e1f73fd121e3ad6f36a2e3123fc91798822958f3a06b35df2d`  
		Last Modified: Fri, 17 Jan 2025 01:33:31 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a294ad2fc4eb0744141cbe376c87751574ed0855e5b42d9e2387d5eac2b3bfd8`  
		Last Modified: Fri, 17 Jan 2025 01:33:32 GMT  
		Size: 12.6 MB (12565913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40cc7f0f5d0d50ab5cd390cd67c5019f95bc45bbd11f47693935c52fffcc25b4`  
		Last Modified: Fri, 17 Jan 2025 01:33:31 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf65272aeb380d63ca16f6621ea3bc1d8d9030fef6e0ff42c422894fc45c1ab5`  
		Last Modified: Fri, 17 Jan 2025 01:33:32 GMT  
		Size: 13.2 MB (13203109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571b396ed0cd01828f98f7e5a13d4df7250f2e4797a89f0f390ce47365a55a9c`  
		Last Modified: Fri, 17 Jan 2025 01:33:32 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef85654c4194b6058eda05850776a84949d19908ae00916f1633a7d6d173ebc`  
		Last Modified: Fri, 17 Jan 2025 01:33:32 GMT  
		Size: 20.0 KB (20028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e071def809824dc2b374a01f9cb3df2da7b62130b74b519243dba0d7d7b6539`  
		Last Modified: Fri, 17 Jan 2025 01:33:33 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07dfe1ba7fbdfd076e5652384408f3e7129d36d51b3e0b0512dc91071b5eab7a`  
		Last Modified: Fri, 17 Jan 2025 02:12:32 GMT  
		Size: 28.0 MB (28045779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ac44ab1ecbf057280f7e7fac7991ab072030069b4c0f6e71595f31aad2c226`  
		Last Modified: Fri, 17 Jan 2025 02:12:31 GMT  
		Size: 6.4 MB (6449106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0140aed982e5e6b94654ab8e6328ec37412aa6614eabf0f51d8ac25894d9381`  
		Last Modified: Fri, 17 Jan 2025 02:12:31 GMT  
		Size: 62.4 KB (62402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4e455b3332568cc9bdd09eaff6190cc78c13d500ff45b4b351938fe42ed47c8`  
		Last Modified: Fri, 17 Jan 2025 02:12:31 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2246cc12fd988d0bcdaad5d5f27a1291944616c293fbcb992ec3f2e4443371f9`  
		Last Modified: Fri, 17 Jan 2025 02:12:32 GMT  
		Size: 23.9 MB (23894310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f87b90fd717cb093e1bd130707f6778245ecb7c5021859f7f6d65ce4ea7bfd4`  
		Last Modified: Fri, 17 Jan 2025 02:12:32 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942a1d92f479e48c4bb6ff91094ec9ff4f233a442d29d6f24696c158e7cdc7bd`  
		Last Modified: Fri, 17 Jan 2025 02:12:33 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:92b9ad5364762e378f271ec30df04c7752e209722626365347d305921afe8e43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 KB (47245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecfd29ababb01323bb7179656af77e509687f63f78d1cf589107f48bdb32d364`

```dockerfile
```

-	Layers:
	-	`sha256:557a7f4e31125af6c519e9dcee512c001e2b0bc162b744580683c5cb06c5989e`  
		Last Modified: Fri, 17 Jan 2025 02:12:31 GMT  
		Size: 47.2 KB (47245 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:5-php8.3-fpm-alpine` - linux; arm variant v6

```console
$ docker pull joomla@sha256:45d96649ab140051ecb29ee492eb66777144f031a82ebaa1c9758c91f00dd5da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86435271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7978616270f7d9a2889b68c992173cedb9025227f6e92a21f7e302d6e1584b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Jan 2025 08:12:24 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["/bin/sh"]
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 08 Jan 2025 08:12:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 08 Jan 2025 08:12:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_VERSION=8.3.16
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 08 Jan 2025 08:12:24 GMT
WORKDIR /var/www/html
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 08 Jan 2025 08:12:24 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["php-fpm"]
# Wed, 08 Jan 2025 08:12:24 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 		zstd 	; # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
VOLUME [/var/www/html]
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_VERSION=5.2.3
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_SHA512=23c74065759fcf812c9c27b14bdefc1d255e074227585e154b39ef5fb9279668a63a51c12b1fec3d4e611dd7147c8ab2eec972bc5e31bacb12cb08989b37c3e9
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.2.3/Joomla_5.2.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d3e229a4bb72770bd404e0f6590519a8e566146523e984834c6a3d82836f0069`  
		Last Modified: Wed, 08 Jan 2025 17:23:44 GMT  
		Size: 3.4 MB (3363879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a27df19b1748e0c5336a2934dab90837cecaea9ecf548f60ec89ced0bb3caa23`  
		Last Modified: Wed, 08 Jan 2025 18:49:59 GMT  
		Size: 3.3 MB (3300488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3d8c9d60966ee150dd112939c109e4bdb3925301588315d098c22b807f8a62c`  
		Last Modified: Wed, 08 Jan 2025 18:49:58 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5af0368056bd9d6658ab6d584d82811582bf7d94d14851784fefbce2ac6bd01`  
		Last Modified: Wed, 08 Jan 2025 18:49:58 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:068b09f0e8dc78e913aaad70d25f734a600d78100c16366fca66a9bebbfe531e`  
		Last Modified: Fri, 17 Jan 2025 01:33:46 GMT  
		Size: 12.6 MB (12565930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2094e59041bb8925e36b0bf995cb79b19941687dede68b21c05e92360173b59`  
		Last Modified: Fri, 17 Jan 2025 01:33:46 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d010aa65b2cf9285c0a86d1caa6a16d913c49c1813858d78b0bd8ccae8437ab7`  
		Last Modified: Fri, 17 Jan 2025 01:39:18 GMT  
		Size: 11.9 MB (11937661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52e637602c4e03b081c973998cfe353a12e8c8619843b987558eb9306ebbb1a3`  
		Last Modified: Fri, 17 Jan 2025 01:39:17 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f971bdca2e24bdbc12572ed7d0d9903e3dee6ffbc43eb5fcde682e21aa8a5e3`  
		Last Modified: Fri, 17 Jan 2025 01:39:17 GMT  
		Size: 19.8 KB (19845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8419b0ac28228fb2d23f9f6c41f2e86f0f12dc80da105999b81667e954196c7a`  
		Last Modified: Fri, 17 Jan 2025 01:39:17 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532227a7e31e96cf5f81e36c8774ecb5ee25fee18ea435cff27e1687788d905d`  
		Last Modified: Fri, 17 Jan 2025 02:26:28 GMT  
		Size: 25.1 MB (25102842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:038cf34886cd060520f3e345bad4282f13ed3bfd3d15764e1ab088139c9e567b`  
		Last Modified: Fri, 17 Jan 2025 02:26:26 GMT  
		Size: 6.2 MB (6169447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240a9aefced22f12adc36a482f33573af60b300e5f34a82f48636280f940956d`  
		Last Modified: Fri, 17 Jan 2025 02:26:26 GMT  
		Size: 62.4 KB (62399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877c1dce281855aa1ae7bae1cfa153bc7ba0d3b8e9aea23dff97e494c502d86b`  
		Last Modified: Fri, 17 Jan 2025 02:26:26 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2eb6a6f78482e311e7f284cd05e844a97e17b974d1bc2305cda252f6c25dab3`  
		Last Modified: Fri, 17 Jan 2025 02:26:28 GMT  
		Size: 23.9 MB (23894362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83453766912e60e44054a31fbcb34eb9f344734edb6074aecef83ebba6a051d5`  
		Last Modified: Thu, 09 Jan 2025 09:34:52 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75c51612eaf149aae2455194276a16d3c98fcc2c2d780fb35edf7234dc88a10b`  
		Last Modified: Thu, 09 Jan 2025 09:34:53 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:d97b7dd7f40ed9f1844bb539de753e7f63c6fb489f82ee23dbd6a93a62c22a0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 KB (47373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fff59a678f0531c71108b444fd353f79dbb6338a9c8b9b4ca28f96119d070360`

```dockerfile
```

-	Layers:
	-	`sha256:e1194ba1bb321ec56e2664e6851b2c63cdfbd87cb84837b8cfd369f5d284bf5c`  
		Last Modified: Fri, 17 Jan 2025 02:26:25 GMT  
		Size: 47.4 KB (47373 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:5-php8.3-fpm-alpine` - linux; arm variant v7

```console
$ docker pull joomla@sha256:9f6d059b91abbc7def81ec5e650ca45a23d49e8f5e3ed378d879f9516f1b0b47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.0 MB (84008463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0423314cf9ee3a64fff1109ffaaae844b5a4efaacac77cc2ad9216a067c60e73`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Jan 2025 08:12:24 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["/bin/sh"]
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 08 Jan 2025 08:12:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 08 Jan 2025 08:12:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_VERSION=8.3.16
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 08 Jan 2025 08:12:24 GMT
WORKDIR /var/www/html
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 08 Jan 2025 08:12:24 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["php-fpm"]
# Wed, 08 Jan 2025 08:12:24 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 		zstd 	; # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
VOLUME [/var/www/html]
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_VERSION=5.2.3
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_SHA512=23c74065759fcf812c9c27b14bdefc1d255e074227585e154b39ef5fb9279668a63a51c12b1fec3d4e611dd7147c8ab2eec972bc5e31bacb12cb08989b37c3e9
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.2.3/Joomla_5.2.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Wed, 08 Jan 2025 17:34:01 GMT  
		Size: 3.1 MB (3097112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5ceb78f083649061e4b802531e1ff0a876077474242c75cfdca63feceddf42`  
		Last Modified: Wed, 08 Jan 2025 18:51:56 GMT  
		Size: 3.1 MB (3115360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3874d1ba95c5456f76e6eaf3fcad122706769776c7031c7f79e4104de9979281`  
		Last Modified: Wed, 08 Jan 2025 18:51:56 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237b35dc6dca52f50940237e3dd268e0dbbd22216c7d386d5989137c1f820852`  
		Last Modified: Wed, 08 Jan 2025 18:51:56 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0204e80c0296cdae0cbaa8fe8c132f49b9c6f8c1700e5c9d1b71849266b1c96`  
		Last Modified: Fri, 17 Jan 2025 02:07:11 GMT  
		Size: 12.6 MB (12565935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7b976bccfd388504dcb1ae8991cef4eb2890a7d4f843ed9d26528f97837f9da`  
		Last Modified: Fri, 17 Jan 2025 02:07:10 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06915eca9877d9be2e06530e8c442b3a0bea045c98d533126fc6ff2bceee37d4`  
		Last Modified: Fri, 17 Jan 2025 02:10:19 GMT  
		Size: 11.2 MB (11249099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30c86c92b496bccd4526be3879519d53e5daa8819acd1e44b18e710d8ac090ca`  
		Last Modified: Fri, 17 Jan 2025 02:10:18 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb1ced4a77966f8850c5fb7d6bfc943c4888012a4921f49b3a3dacc4bc627f7`  
		Last Modified: Fri, 17 Jan 2025 02:10:18 GMT  
		Size: 19.8 KB (19846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf3ec4d14ce3d25d025ee7927a6c0d15093dfff4d08c3c458131c6cd56b57bfb`  
		Last Modified: Fri, 17 Jan 2025 02:10:19 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b997d015ea6ddc7c6c345b919ceec65e687868b04fbd7ccf66ccfd0adb642fd`  
		Last Modified: Fri, 17 Jan 2025 03:24:03 GMT  
		Size: 23.8 MB (23844418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f98a09f1c8e6770e7bcd58f79dbfeadcc74d712594d07f6eeec5f9020363c292`  
		Last Modified: Fri, 17 Jan 2025 03:24:02 GMT  
		Size: 6.1 MB (6141572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f5d206c3d8855b7d417d7610198c39709b2bd1cc408bb0ef856307da983e3c6`  
		Last Modified: Fri, 17 Jan 2025 03:24:02 GMT  
		Size: 62.4 KB (62367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a686de6595a4bd697a17fa59e11c98970ce6343ac1c63bbeb8c1e17be30f775`  
		Last Modified: Fri, 17 Jan 2025 03:24:02 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326eadf075abb2cf61e4a49f27f00a97a465c833fa216304eb3d4d1354d27670`  
		Last Modified: Fri, 17 Jan 2025 03:24:04 GMT  
		Size: 23.9 MB (23894327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04723775fe372a6634790f8ec870e4b894135a3346f4d35656e87a855cce155d`  
		Last Modified: Fri, 17 Jan 2025 03:24:03 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4253ab8ba33363397a136250441d7486c3b1466a21c5e43fdb683cb663b05fb8`  
		Last Modified: Fri, 17 Jan 2025 03:24:03 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:d052cdf1c816712fc31f413644cd00f69872352a1fead3f227e2bcc98541a3eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 KB (47373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28083c3eff9d09c1f3e2ff28fe0cfef4ac06c92a4ebbda1f29eab4f505f14900`

```dockerfile
```

-	Layers:
	-	`sha256:21c68a1e709b327f2bc11f8a8468de49a7e68d7541d958129cad91ba999ef223`  
		Last Modified: Fri, 17 Jan 2025 03:24:01 GMT  
		Size: 47.4 KB (47373 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:5-php8.3-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull joomla@sha256:b881210f724bb3c03c18ebac4e9d205c00ed2a24cd6bf6e118fda214c0fab3aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.3 MB (91340897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57760b21c76dde88a5a540cb6d4ba71a895c84a606b60243d7a4164c00b9d15`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Jan 2025 08:12:24 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["/bin/sh"]
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 08 Jan 2025 08:12:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 08 Jan 2025 08:12:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_VERSION=8.3.16
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 08 Jan 2025 08:12:24 GMT
WORKDIR /var/www/html
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 08 Jan 2025 08:12:24 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["php-fpm"]
# Wed, 08 Jan 2025 08:12:24 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 		zstd 	; # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
VOLUME [/var/www/html]
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_VERSION=5.2.3
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_SHA512=23c74065759fcf812c9c27b14bdefc1d255e074227585e154b39ef5fb9279668a63a51c12b1fec3d4e611dd7147c8ab2eec972bc5e31bacb12cb08989b37c3e9
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.2.3/Joomla_5.2.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:52f827f723504aa3325bb5a54247f0dc4b92bb72569525bc951532c4ef679bd4`  
		Last Modified: Wed, 08 Jan 2025 17:23:52 GMT  
		Size: 4.0 MB (3992359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a259b492a8c3558416dd48f8aad1dda78fda9cef38298295c5e43623b56a18c`  
		Last Modified: Wed, 08 Jan 2025 18:47:48 GMT  
		Size: 3.3 MB (3327674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549c6a796a4d698d720516d98efaded2b858014b8a81418484745626b542df1b`  
		Last Modified: Wed, 08 Jan 2025 18:47:47 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e06c334c2725cc400bba17c21a0380b9f9c970473c4959000a3921b22cdf4a8`  
		Last Modified: Wed, 08 Jan 2025 18:47:47 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce86ef064edc436017f8d7adf39a34791690aa9358ada4968c2846dc852ca8a5`  
		Last Modified: Fri, 17 Jan 2025 01:59:01 GMT  
		Size: 12.6 MB (12565957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82573dd219577096ad073ab5cc5aec03711465792e841e32a69de3f869ad15db`  
		Last Modified: Fri, 17 Jan 2025 01:59:00 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bbbae26bb0f5db0f77bfe9fcba38e8bcc044c378146650d12820205ac9a1e6f`  
		Last Modified: Fri, 17 Jan 2025 02:04:09 GMT  
		Size: 13.2 MB (13193421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c60f0abd9ea38dd6ecb2f0cb65f214d431a2b1baf0daa5356300de042fbf19e`  
		Last Modified: Fri, 17 Jan 2025 02:04:08 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ab9b6841504d1eebe9d868b28fbea6b9f043a83188fb388330853ee17ac2a32`  
		Last Modified: Fri, 17 Jan 2025 02:04:09 GMT  
		Size: 19.8 KB (19848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4b77cf854b474df3e3d58c03e8b3ccc81841d1ab6e9539f4d028a1eb69438a`  
		Last Modified: Fri, 17 Jan 2025 02:04:09 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7804a3d51ae3db0f2a0fad96475764a392fcc4b851cd5d4e4902e7697f1a362`  
		Last Modified: Fri, 17 Jan 2025 03:04:16 GMT  
		Size: 27.9 MB (27855463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76cbde6eefd7c7ce38a0627ca9127faa075dbfd35e83e50e3bc124552adef6b`  
		Last Modified: Fri, 17 Jan 2025 03:04:15 GMT  
		Size: 6.4 MB (6411011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:864a0f3615567d4b6f8486fdab4201c330a0186b35a7e2fec6dfe3f5062d77d4`  
		Last Modified: Fri, 17 Jan 2025 03:04:15 GMT  
		Size: 62.4 KB (62379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7cc4b76efe6cc1033321250c2c0c29532feb5901a24504a2b11fbbaee660725`  
		Last Modified: Fri, 17 Jan 2025 03:04:15 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e0c27b1e80323b33d9999f1215a33d899abc03245c74547bb50f02983ee423`  
		Last Modified: Fri, 17 Jan 2025 03:04:17 GMT  
		Size: 23.9 MB (23894361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098c2d1e5c041248394113089daa3541455006fe2480e87d3aea979ada5e841d`  
		Last Modified: Fri, 17 Jan 2025 03:04:16 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dcff393f7955fc8c7f69fe7703b99b496c0b1e536f9db504375d05656b4782c`  
		Last Modified: Fri, 17 Jan 2025 03:04:16 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:93acf413e3a49c798856654fec1801ca9ad83cc328648b31f1f2f1c696591f6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 KB (47408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d97b66368eb8d0729ba064c949c048a3e66c7a4c2e32f50a458ab6ec13b0ce1d`

```dockerfile
```

-	Layers:
	-	`sha256:e522daeb12f51f2f4b4be93f7466448f05d0b6aab409ec44f4b10549f48aa1ba`  
		Last Modified: Fri, 17 Jan 2025 03:04:14 GMT  
		Size: 47.4 KB (47408 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:5-php8.3-fpm-alpine` - linux; 386

```console
$ docker pull joomla@sha256:e662f88b949f6330dc8632e4fa66df8bb4f43c16bba100707c6acbf74298c37f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.8 MB (91763611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8941ef65c60d2a1ba23013419afc229b6c9fe70786d99114f3829b11015f8d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Jan 2025 08:12:24 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["/bin/sh"]
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 08 Jan 2025 08:12:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 08 Jan 2025 08:12:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_VERSION=8.3.16
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 08 Jan 2025 08:12:24 GMT
WORKDIR /var/www/html
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 08 Jan 2025 08:12:24 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["php-fpm"]
# Wed, 08 Jan 2025 08:12:24 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 		zstd 	; # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
VOLUME [/var/www/html]
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_VERSION=5.2.3
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_SHA512=23c74065759fcf812c9c27b14bdefc1d255e074227585e154b39ef5fb9279668a63a51c12b1fec3d4e611dd7147c8ab2eec972bc5e31bacb12cb08989b37c3e9
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.2.3/Joomla_5.2.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7386cf222b0d875e8873ae391fb2d15011557c0a8620c08a86ab8eb339acf635`  
		Last Modified: Fri, 17 Jan 2025 01:33:35 GMT  
		Size: 3.4 MB (3373803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8525db88a29b4c886a172b95463f3cbeb75981b131056a27ec1d34b472f723`  
		Last Modified: Fri, 17 Jan 2025 01:33:35 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe8c926c51f944e1f73fd121e3ad6f36a2e3123fc91798822958f3a06b35df2d`  
		Last Modified: Fri, 17 Jan 2025 01:33:31 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9bb97ef72591d7a252d2c567d034f1d42c39c517e4bf7b40d76af00388a69a2`  
		Last Modified: Fri, 17 Jan 2025 01:33:36 GMT  
		Size: 12.6 MB (12565914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078c0c085a68b162b4a08ce3f62ee131733144fa995805dcbb1ec1c0bed32d93`  
		Last Modified: Fri, 17 Jan 2025 01:33:36 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a989d28458c66567b0462fb250a097a5e8e43fa6c99db424e0790d2752ee9b`  
		Last Modified: Fri, 17 Jan 2025 01:33:36 GMT  
		Size: 13.5 MB (13508578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ccb8157a8df0c5fb29facf095e22d3a5e06bcda653decc4fd9a4c52b6cba26e`  
		Last Modified: Fri, 17 Jan 2025 01:33:36 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02c5080299e22b134ac88f26f4b139c8287e924c496e1df4d2641bcdef65b39`  
		Last Modified: Fri, 17 Jan 2025 01:33:36 GMT  
		Size: 20.0 KB (20027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e332158c0c707083d07db3f2918aa5541ff27a86a7fa5810ed217c892482dee9`  
		Last Modified: Fri, 17 Jan 2025 01:33:37 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f514e4e8283260b2658e51282aa01ef6204a5ea9e300e7f172dab9d6673af7`  
		Last Modified: Fri, 17 Jan 2025 02:14:11 GMT  
		Size: 28.3 MB (28276224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8da724eadb10d2e677dcbca9be883590016d93fafc2d81afa32ab464c658b1e`  
		Last Modified: Fri, 17 Jan 2025 02:14:10 GMT  
		Size: 6.6 MB (6580836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc35596b5c61d292a2ef0f6112d7b95a8bcdeecec1fc44ab27c01f85b9914a7a`  
		Last Modified: Fri, 17 Jan 2025 02:14:10 GMT  
		Size: 62.3 KB (62335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:013d03897da7e9ddccc6c874cc578fc1726b428cf60ac107025526516615a63b`  
		Last Modified: Fri, 17 Jan 2025 02:14:10 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7032b972473da08288a76930bacaea03e8cb450ae47831da1e3a53746420fe5`  
		Last Modified: Fri, 17 Jan 2025 02:14:11 GMT  
		Size: 23.9 MB (23894354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8b5ccc3d133ce452511623de5d4cab9c0b9189b84ec01e663933bb55f38617`  
		Last Modified: Fri, 17 Jan 2025 02:14:10 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc2f7c2a52659792cb71468637173cfd8b2167636e7408b35a12c6af0dfc6f6`  
		Last Modified: Fri, 17 Jan 2025 02:14:11 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:5f663835e348fe201b0703160c1ea7d608791a167fb53d41fbb531180753d491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 KB (47205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5153e97436e7d6795bd74033109750a79fed09d9e13e836673452a2fe55595f9`

```dockerfile
```

-	Layers:
	-	`sha256:05b624129db87e350121db55edaa50ca29f123dc8dbe693ac6e62d1ac22e16db`  
		Last Modified: Fri, 17 Jan 2025 02:14:09 GMT  
		Size: 47.2 KB (47205 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:5-php8.3-fpm-alpine` - linux; ppc64le

```console
$ docker pull joomla@sha256:06125eaa3fb2d8d8f6892b3baabe5c4790f5087b8d1f074d46d27419f40033d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92533399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77a8c4c7b29f41c2e383417493daefd7533dd7dd77fd600f96767c0b1613893`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Jan 2025 08:12:24 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["/bin/sh"]
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 08 Jan 2025 08:12:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 08 Jan 2025 08:12:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_VERSION=8.3.16
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 08 Jan 2025 08:12:24 GMT
WORKDIR /var/www/html
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 08 Jan 2025 08:12:24 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["php-fpm"]
# Wed, 08 Jan 2025 08:12:24 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 		zstd 	; # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
VOLUME [/var/www/html]
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_VERSION=5.2.3
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_SHA512=23c74065759fcf812c9c27b14bdefc1d255e074227585e154b39ef5fb9279668a63a51c12b1fec3d4e611dd7147c8ab2eec972bc5e31bacb12cb08989b37c3e9
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.2.3/Joomla_5.2.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e88c0bde0da532d37286f677138c7e480dcb6f566920007e98f5e5eb88d6d4`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 3.5 MB (3476342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e3cc68900042575ac984146d93aef63e5c37b3e8c420156abe75bd0eab7f3e2`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bec6f6109cf776dd85e5729606c85d0024f7d6d1ec08e54ddb40c264cc4f45`  
		Last Modified: Wed, 08 Jan 2025 18:35:23 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e937f22521a2c5c57bad977a229d6e9072d584f968720e77c7468f3c07adc51`  
		Last Modified: Fri, 17 Jan 2025 01:40:50 GMT  
		Size: 12.6 MB (12565963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ee2fef4b8ba52f45ba1a66f55a24b49b2c1ff5223ab683fe5fafc0545d1749b`  
		Last Modified: Fri, 17 Jan 2025 01:40:49 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cad7e358e9c338d3f835700b6f489786f3dcc391427afaa4ab0b9ba7f75dc5f1`  
		Last Modified: Fri, 17 Jan 2025 01:44:02 GMT  
		Size: 13.7 MB (13676174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ac65a743e7d76f558c2bf53b7d11a2802a7e6ce2e55ea2c59bb892dda843fb`  
		Last Modified: Fri, 17 Jan 2025 01:44:01 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f57ceab25bd72011ba80ae068a79d6a6b3a33aead15a7ab9b8dd8ca6feac47`  
		Last Modified: Fri, 17 Jan 2025 01:44:01 GMT  
		Size: 19.8 KB (19848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403622d54d10d493a25581d099ee8432c3185b8b7424313137ed99d2669bb837`  
		Last Modified: Fri, 17 Jan 2025 01:44:02 GMT  
		Size: 9.2 KB (9175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b05237afc2c4d07eeb0fd0cea5829c7080702496094b1a4e01eb9249345157`  
		Last Modified: Fri, 17 Jan 2025 02:52:21 GMT  
		Size: 28.7 MB (28683525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9f2582afded0036e30aef0e1d273f4265fb77df7a146bcfb70ff69763a09e4`  
		Last Modified: Fri, 17 Jan 2025 02:52:20 GMT  
		Size: 6.6 MB (6562817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e522f3bf0e9361f0e3113a013633d52bbee01817fa9cf7dd010087dbc4abc2e0`  
		Last Modified: Fri, 17 Jan 2025 02:52:19 GMT  
		Size: 62.4 KB (62363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5a9410923d2599e4bc956d7a0722e4c53a14cb80dfd9991f952da8210a4e9a`  
		Last Modified: Fri, 17 Jan 2025 02:52:19 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461ece6e7a1aacac5612c6fceec2b6c8695223ee3e808429671f9098222c0b5b`  
		Last Modified: Fri, 17 Jan 2025 02:52:22 GMT  
		Size: 23.9 MB (23894340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de091b4813e3d90c93b31005ca57d4c1fc4bcdcae62469c0a78f6d59f47fc0f6`  
		Last Modified: Fri, 17 Jan 2025 02:52:20 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2ce0634d6a41742198c841d820b52e88852769d05c88ed82907821c7f88c719`  
		Last Modified: Fri, 17 Jan 2025 02:52:21 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:d08ec270b1200d87861677ec84e08ac6934358467cda181971640b973a57a15e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 KB (47297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8089624b5164d3b64eabd2b537658ef6efecec3682a96c284e9838a2712d87`

```dockerfile
```

-	Layers:
	-	`sha256:22492aa8bbd69113b9e2be4bfaac9403a99a56f944795e0db4bec261a5c77ae0`  
		Last Modified: Fri, 17 Jan 2025 02:52:18 GMT  
		Size: 47.3 KB (47297 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:5-php8.3-fpm-alpine` - linux; riscv64

```console
$ docker pull joomla@sha256:f1d28fdd9ac568c47cf2c8438179bd80f23fe0ee222f4d24daab228b48766a0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.2 MB (90206948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced0e277275359824eaca987d0ddbce1755ba85e7ee424fde378e00898f4bda4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Jan 2025 08:12:24 GMT
ADD alpine-minirootfs-3.21.2-riscv64.tar.gz / # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["/bin/sh"]
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 08 Jan 2025 08:12:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 08 Jan 2025 08:12:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_VERSION=8.3.16
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 08 Jan 2025 08:12:24 GMT
WORKDIR /var/www/html
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 08 Jan 2025 08:12:24 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["php-fpm"]
# Wed, 08 Jan 2025 08:12:24 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 		zstd 	; # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
VOLUME [/var/www/html]
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_VERSION=5.2.3
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_SHA512=23c74065759fcf812c9c27b14bdefc1d255e074227585e154b39ef5fb9279668a63a51c12b1fec3d4e611dd7147c8ab2eec972bc5e31bacb12cb08989b37c3e9
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.2.3/Joomla_5.2.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:21a89fc8a7107842fa0935d999d700ca9a9df964110a7076d946b16f07a54de5`  
		Last Modified: Wed, 08 Jan 2025 17:48:43 GMT  
		Size: 3.4 MB (3350256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743579fbfa9d6a462255cb84fc5b099d3cf542442a9305bc0f96bce81c76e4f3`  
		Last Modified: Wed, 08 Jan 2025 23:26:57 GMT  
		Size: 3.5 MB (3457918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550ac1c09c8b9181323bf079ede440cee01f0fec62e09b75afcae7c35627d0e6`  
		Last Modified: Wed, 08 Jan 2025 23:26:55 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0810a5f710bc8b0a06b441c232e302e968233890edb8bd1ae54afee19878e9f1`  
		Last Modified: Wed, 08 Jan 2025 23:26:55 GMT  
		Size: 219.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:044c854e2cba647439f26a7d0b24155b340a9a97a8bea54cae4edb04ce316e3b`  
		Last Modified: Fri, 17 Jan 2025 02:24:28 GMT  
		Size: 12.6 MB (12565947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5208dea30f4cbfdbd69272b2539a5aceed97314ced7683c24f4e75682aea69b`  
		Last Modified: Fri, 17 Jan 2025 02:24:25 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec2e737da444f8cf56464c21df42f053a1a20f43f35dd6bc090a31fcf8a950c`  
		Last Modified: Fri, 17 Jan 2025 03:20:33 GMT  
		Size: 12.7 MB (12707916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657257c14b8e54699917dd349034c8d18b16bdc62c1e7f1eb1d680964213e21d`  
		Last Modified: Fri, 17 Jan 2025 03:20:31 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ebd4c148eccfa2f452d65d0bb8ba957238e07396d52644294130912e21e92f`  
		Last Modified: Fri, 17 Jan 2025 03:20:32 GMT  
		Size: 19.8 KB (19839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65527607b8b35978e44a3d2cf267580ac3f2f6286b5e52995027711f9d36f18f`  
		Last Modified: Fri, 17 Jan 2025 03:20:32 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3918b14b521881dc39efe558d7778f4833ff40d4e790e957d69d7c8393904e1`  
		Last Modified: Fri, 17 Jan 2025 08:41:54 GMT  
		Size: 27.8 MB (27848057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b6c86470f0c0c0ce227716774990736d93af8206249df480b6428c15b615f09`  
		Last Modified: Fri, 17 Jan 2025 08:41:50 GMT  
		Size: 6.3 MB (6281867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ec25b929214540b4445f9958d25a7ac97c771e55bcb9360c8274d55f549188`  
		Last Modified: Fri, 17 Jan 2025 08:41:50 GMT  
		Size: 62.4 KB (62373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e14a3e0d7f05ddea162631731f73c31cf8fa9e68aeb03a976b1b62304832693`  
		Last Modified: Fri, 17 Jan 2025 08:41:49 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e458e37af29bfdf99de6c01cdc447969583fbc64f14089585149d702035c3412`  
		Last Modified: Fri, 17 Jan 2025 08:41:54 GMT  
		Size: 23.9 MB (23894339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a43e28166fa69e541c2200e021dbc701c5c4d6048045c8276c0e269d4d4eb8a`  
		Last Modified: Fri, 17 Jan 2025 08:41:51 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89442a5a1e561a2c500e02be66677bf736655f45d2c7bcb2f5c07067fff831a8`  
		Last Modified: Fri, 17 Jan 2025 08:41:51 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:0b1029edde0e806469cdee54456df4148e7886b6e87f3b0827507aea9b61a932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 KB (47296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:540960c02d570a588fc4fb4206642a742c63e27d3f209d60cae3b4e57c27db97`

```dockerfile
```

-	Layers:
	-	`sha256:caf96ff13abc5bcdada370559866cd9915bc4d602151b1caff7496ee89d0fe91`  
		Last Modified: Fri, 17 Jan 2025 08:41:48 GMT  
		Size: 47.3 KB (47296 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:5-php8.3-fpm-alpine` - linux; s390x

```console
$ docker pull joomla@sha256:49f83c2754ab7ed7b20f34a620e2733edd2d041c471338cf0f5ee0acc01e5be6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.3 MB (92321815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08635cf5b58d04dfb3fc1907acdee7b19176e5fc09022f6fd0f7408d49ba6a69`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 08 Jan 2025 08:12:24 GMT
ADD alpine-minirootfs-3.21.2-s390x.tar.gz / # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["/bin/sh"]
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 08 Jan 2025 08:12:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 08 Jan 2025 08:12:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_VERSION=8.3.16
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.16.tar.xz.asc
# Wed, 08 Jan 2025 08:12:24 GMT
ENV PHP_SHA256=40d3b4e6cac33d3bcefe096d75a28d4fb4e3a9615eb20a4de55ba139fbfacdd5
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 08 Jan 2025 08:12:24 GMT
WORKDIR /var/www/html
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 08 Jan 2025 08:12:24 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["php-fpm"]
# Wed, 08 Jan 2025 08:12:24 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 		zstd 	; # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
VOLUME [/var/www/html]
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_VERSION=5.2.3
# Wed, 08 Jan 2025 08:12:24 GMT
ENV JOOMLA_SHA512=23c74065759fcf812c9c27b14bdefc1d255e074227585e154b39ef5fb9279668a63a51c12b1fec3d4e611dd7147c8ab2eec972bc5e31bacb12cb08989b37c3e9
# Wed, 08 Jan 2025 08:12:24 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/5.2.3/Joomla_5.2.3-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 08 Jan 2025 08:12:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 08 Jan 2025 08:12:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b2af93686f9384c40cfe861d7173877bb2ee1675c3ee70181799693c34c8722f`  
		Last Modified: Wed, 08 Jan 2025 17:25:12 GMT  
		Size: 3.5 MB (3466867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26282a4a0a714cd1f4efa558a9c16c549bcb3d98039f808a2da09f37551fac63`  
		Last Modified: Wed, 08 Jan 2025 18:38:12 GMT  
		Size: 3.6 MB (3561274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82035fdc219157bbb0deab69c2a1382fccf8a51ac5b20be190e26173e8a8be95`  
		Last Modified: Wed, 08 Jan 2025 18:38:11 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c31af6d9d81023b2dbb6d6e14114bb3c0a961f429216de8f8cdfd98fb13c317`  
		Last Modified: Wed, 08 Jan 2025 18:38:11 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e2199922fd8d7b8d2453ad72d0f34a391222745fd39879844966ec900938f5`  
		Last Modified: Fri, 17 Jan 2025 01:47:22 GMT  
		Size: 12.6 MB (12565955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adde8da54c2f0f411f50cf6a809c4a1af1aee5affd7cb940e862bfdca93c3518`  
		Last Modified: Fri, 17 Jan 2025 01:47:22 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f7fb1fc245741323ebc4eb147da95dfcd8a2c6e0bb633d0061f597f51444c1`  
		Last Modified: Fri, 17 Jan 2025 01:51:30 GMT  
		Size: 13.2 MB (13152506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34851439a144f35dca37236ffcb0218a7ba02b3fc0d1b49db93660c3043c71b1`  
		Last Modified: Fri, 17 Jan 2025 01:51:28 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cddda9c549e9df5904213a2c37a90c34f6e4295fb9272bc5fcae0ab585797b5`  
		Last Modified: Fri, 17 Jan 2025 01:51:28 GMT  
		Size: 19.8 KB (19846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acbf5ae9a1ef4a2a5234e34dc0987fcc6e4c2424e71f5b50c5cb7d4b4725de4b`  
		Last Modified: Fri, 17 Jan 2025 01:51:28 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08d233abed1220244cde7cefe9e3cb830363c536fd5e419507501e936978dce3`  
		Last Modified: Fri, 17 Jan 2025 02:53:30 GMT  
		Size: 29.0 MB (29002029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c685615e26ebacad289d6384e622819a1d4965bffde41bbafd7d41999cf547`  
		Last Modified: Fri, 17 Jan 2025 02:53:29 GMT  
		Size: 6.6 MB (6578147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabc9265aacbf3701b1b1987d142aeadeaaca62f96289ae637386c51e931475c`  
		Last Modified: Fri, 17 Jan 2025 02:53:29 GMT  
		Size: 62.4 KB (62403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccffa4415d27fa3c9ab9555cbe428ee3a0132968193ea84e8e7ea3855eaccc67`  
		Last Modified: Fri, 17 Jan 2025 02:53:29 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16f5545c5f79d56361b810e5eeba26e6332fa2d0cb37e3589dde32d809d38190`  
		Last Modified: Fri, 17 Jan 2025 02:53:32 GMT  
		Size: 23.9 MB (23894362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef570e4e2c19310fd1af143038de3e1bf25f636dd9bb40bfa8b0009b42a25ed2`  
		Last Modified: Fri, 17 Jan 2025 02:53:30 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c80e2fc5e54ba136e73db8e722a91395fda735ff60cead91a38ced85450378f`  
		Last Modified: Fri, 17 Jan 2025 02:53:30 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:5-php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:dacc417bb31649a48ac0d3616bee71e944df709a9dee3ffbfb5bf40ab50e942e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 KB (47245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f7672b7cdae050944a1e43557be707ed64a004c33c261bfeeca9709d8049a7`

```dockerfile
```

-	Layers:
	-	`sha256:d7f193e207c8e93907b736faa82bd6b98ea025a7fb3df496e41040713217c7b9`  
		Last Modified: Fri, 17 Jan 2025 02:53:28 GMT  
		Size: 47.2 KB (47245 bytes)  
		MIME: application/vnd.in-toto+json
