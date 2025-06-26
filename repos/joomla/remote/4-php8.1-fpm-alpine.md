## `joomla:4-php8.1-fpm-alpine`

```console
$ docker pull joomla@sha256:2651c17cc510db393a213c405d6bba2610762f26ceca3625686ab5c52491bbfa
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

### `joomla:4-php8.1-fpm-alpine` - linux; amd64

```console
$ docker pull joomla@sha256:4de18751210eee3039593be60ad8bad07d8d9d7d5e3874923ddc92a0e92f3ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.0 MB (92966540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b93d44d6f03f52bb576b83227ce3110fcfcecb33208e5dadc731758b7e53b93`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 09 Apr 2025 19:45:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 09 Apr 2025 19:45:06 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_VERSION=8.1.32
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.32.tar.xz.asc
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_SHA256=c582ac682a280bbc69bc2186c21eb7e3313cc73099be61a6bc1d2cd337cbf383
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 09 Apr 2025 19:45:06 GMT
WORKDIR /var/www/html
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
STOPSIGNAL SIGQUIT
# Wed, 09 Apr 2025 19:45:06 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 09 Apr 2025 19:45:06 GMT
CMD ["php-fpm"]
# Wed, 09 Apr 2025 19:45:06 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 09 Apr 2025 19:45:06 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
VOLUME [/var/www/html]
# Wed, 09 Apr 2025 19:45:06 GMT
ENV JOOMLA_VERSION=4.4.13
# Wed, 09 Apr 2025 19:45:06 GMT
ENV JOOMLA_SHA512=c88f1779592fc74ff1fb3a26c81d113868d675f15afd45d0547c34216d49071a0d43b1f603e9f1daa5093499231dc95a77d165caff472d3d72ecb56af87a331e
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.13/Joomla_4.4.13-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 09 Apr 2025 19:45:06 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36e1f917266ae22bc1980cdbc217f4eb12d006ab929dc0b50bcef12f3cc6df1b`  
		Last Modified: Wed, 25 Jun 2025 19:29:49 GMT  
		Size: 3.3 MB (3339422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24fefb23ff1a5ecdf9b0780b7e1b9dd506b906e4e8dd6ab32df9974acc3fd9b`  
		Last Modified: Wed, 25 Jun 2025 19:29:49 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a44a3579243452efd6d721fbbefb2f9b5ab469ea324e3eff11a75b1f4fdf60a`  
		Last Modified: Wed, 25 Jun 2025 19:29:49 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:866d5a340ba5b87d4ef1dc941b710fbc2949db6dd54858ed99b73ef8f58c07d8`  
		Last Modified: Wed, 25 Jun 2025 19:29:50 GMT  
		Size: 11.9 MB (11914913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666887c25164ca7e6afd11c2922fc8618b021b3e1910450051550812c4fd0731`  
		Last Modified: Wed, 25 Jun 2025 19:29:49 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b243a6b0197a876662dc8a42fc7f1d431732dd5218d9e01bc3ce6b53cb563d`  
		Last Modified: Wed, 25 Jun 2025 19:29:51 GMT  
		Size: 12.7 MB (12742937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80430f2ac487b68f1718135460a9e750a8856510afc9a2cdccafef9f52a4f5c1`  
		Last Modified: Wed, 25 Jun 2025 19:29:49 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf20ba6fb0f7e2d9c07210a408125c1a6523f0070dc353a0a04e081d2dedc7b7`  
		Last Modified: Wed, 25 Jun 2025 19:29:49 GMT  
		Size: 20.1 KB (20053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:898958703a76af5ff02c16d75b163ca928e3c7808fb86ef898076b989d2422f3`  
		Last Modified: Wed, 25 Jun 2025 19:29:49 GMT  
		Size: 20.0 KB (20047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:267a8a449f760665e1ac8508a4bdb95cdd074248052e0a3fea27e6372bf8f60a`  
		Last Modified: Wed, 25 Jun 2025 19:29:50 GMT  
		Size: 8.9 KB (8877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:092d5996c90a729af7da56017eae6e4bafc2c303bb5855550cedb24861594a83`  
		Last Modified: Wed, 25 Jun 2025 22:45:11 GMT  
		Size: 28.2 MB (28238558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cccc0e0469510bf5ea866f7b27d66527291627f314b3e01dabd69cf7febb0f2`  
		Last Modified: Wed, 25 Jun 2025 22:45:10 GMT  
		Size: 6.4 MB (6384899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d605addcbbdd82e808f3ed2a7be57275debc23935a5b33fb7eec1dbff5360e1`  
		Last Modified: Wed, 25 Jun 2025 20:08:48 GMT  
		Size: 62.9 KB (62858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7eec9e8e66cf256d8c8a47e45e581cf4facf54422f92e419feb70ddfc217cd8c`  
		Last Modified: Wed, 25 Jun 2025 20:08:52 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d23386ff218b5f0a3979efa3ba27b95d7b0eeb9c11f1724a21a3ae7cacbd15`  
		Last Modified: Wed, 25 Jun 2025 22:45:10 GMT  
		Size: 26.6 MB (26582500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6ba1e3b802217132fdabee04839467f1edd0ef5e52cc868637524d83c4aac7`  
		Last Modified: Wed, 25 Jun 2025 20:08:56 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4f714c91a25fe321ff2507b351c88d8d8a3c20f16f4bc103bb27996a0aa707`  
		Last Modified: Wed, 25 Jun 2025 20:09:01 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:4-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:369cf302b0d973bf45d295d7a6062f1fab955ceab9e87cf6bd6a244804e78d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 KB (48014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbd3151b005d659361ff81d4a72e394d0f041108f05068949e50965f74866a37`

```dockerfile
```

-	Layers:
	-	`sha256:f2f0a9be765afbff30ecbd663b0e381d8a0df5ea250bb3e42f17b869bc0e8927`  
		Last Modified: Wed, 25 Jun 2025 22:44:33 GMT  
		Size: 48.0 KB (48014 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:4-php8.1-fpm-alpine` - linux; arm variant v6

```console
$ docker pull joomla@sha256:d53c90b3ccd4187632881e54fd308c446e42ee09953c98bc958143ce97fd29b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.1 MB (89055170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1532ff6e5df24139fdddc2f9f0db752a4d7cfbb18354d5738a2eaa4d5a80bf0d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 09 Apr 2025 19:45:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 09 Apr 2025 19:45:06 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_VERSION=8.1.32
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.32.tar.xz.asc
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_SHA256=c582ac682a280bbc69bc2186c21eb7e3313cc73099be61a6bc1d2cd337cbf383
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 09 Apr 2025 19:45:06 GMT
WORKDIR /var/www/html
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
STOPSIGNAL SIGQUIT
# Wed, 09 Apr 2025 19:45:06 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 09 Apr 2025 19:45:06 GMT
CMD ["php-fpm"]
# Wed, 09 Apr 2025 19:45:06 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 09 Apr 2025 19:45:06 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
VOLUME [/var/www/html]
# Wed, 09 Apr 2025 19:45:06 GMT
ENV JOOMLA_VERSION=4.4.13
# Wed, 09 Apr 2025 19:45:06 GMT
ENV JOOMLA_SHA512=c88f1779592fc74ff1fb3a26c81d113868d675f15afd45d0547c34216d49071a0d43b1f603e9f1daa5093499231dc95a77d165caff472d3d72ecb56af87a331e
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.13/Joomla_4.4.13-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 09 Apr 2025 19:45:06 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee7560caccbd432ecca159038f0b286f2c0b02efec5546bf18a775ad0e99486`  
		Last Modified: Fri, 14 Feb 2025 20:54:54 GMT  
		Size: 3.3 MB (3309064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9633ce950391c85eec86506afa8a80635896647c5785246258ef925ff53571b2`  
		Last Modified: Fri, 14 Feb 2025 20:54:54 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25cec00a4490a77b96f81fdbda726d926b9b6c604919f947a6b1af7adfd131e9`  
		Last Modified: Fri, 14 Feb 2025 20:54:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc697e640fdf7c95632b75f83db5776be2d4fac47736631609c8f5d1015fc618`  
		Last Modified: Fri, 09 May 2025 01:55:41 GMT  
		Size: 11.9 MB (11914898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a73ad87ee15139514c99ef994368414968ccdcfc78bfdb113a23d9ca948c80`  
		Last Modified: Fri, 09 May 2025 01:53:41 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2e8e3644380e63c590ad28d7a2c76c15453af42da651f239ca2a9e2e98233c`  
		Last Modified: Fri, 16 May 2025 13:08:25 GMT  
		Size: 11.5 MB (11470551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95994391951b650b836de4c7da4d91b4011b4bf9916f22006bfdcbbbc69f809b`  
		Last Modified: Wed, 25 Jun 2025 19:21:48 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:678e5562f5dd2d4c32c1a112e2d000bd4c5675115dfb9638cb3c7d9a62865b28`  
		Last Modified: Wed, 25 Jun 2025 19:21:48 GMT  
		Size: 19.8 KB (19847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc55695c01990e7dd39a8395823869cc881dd51ecab97272324f895689ce7ed`  
		Last Modified: Wed, 25 Jun 2025 19:21:49 GMT  
		Size: 19.8 KB (19843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1af83e5f885e3b0dbdafb7fa5b1c70d6d9cd17a5f4bd03cef0f66e5e90f9ef`  
		Last Modified: Wed, 25 Jun 2025 19:21:49 GMT  
		Size: 8.9 KB (8888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84eda08ca88d6730348e9f21b45461f839f62b29db3c420c429ff4badd69284`  
		Last Modified: Wed, 25 Jun 2025 20:37:40 GMT  
		Size: 24.3 MB (24330928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5afa3fd110abafc6812d3485fef93ef84828bfbaa73e0e52b741351299adaa99`  
		Last Modified: Wed, 25 Jun 2025 20:37:39 GMT  
		Size: 8.0 MB (7961804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52fed4c23821411fbbb4a6ac3986e03b0d238eb087fd3de85b14d3872315454d`  
		Last Modified: Wed, 25 Jun 2025 20:37:39 GMT  
		Size: 62.9 KB (62855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f89d1bfdf60eecbf8a378e2243db652cbed0daa4513773f4760f4822a3573f0`  
		Last Modified: Wed, 25 Jun 2025 20:37:39 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55119d09863f4bc91b7c01b7898d470893dbf869f4d0c8c5933ed6507e328f45`  
		Last Modified: Wed, 25 Jun 2025 20:37:41 GMT  
		Size: 26.6 MB (26582506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eef5ae3b6d0f1d7b34c55e08aecd7827b8b814dee9e014e3230a17b755eedb58`  
		Last Modified: Wed, 25 Jun 2025 20:45:10 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fd75447b926b20f4f0c81d3a84cfd3d7b559f2a8ed8661fab2671a75ce078f`  
		Last Modified: Wed, 25 Jun 2025 20:45:21 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:4-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:e7676ea4a7988d4075466fee7673280996b58bd0aceee6f023499b4b2fbf16b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 KB (48133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21103457fe2d95ce397aa18e0b2c00d330a31ae66a465f6776406959a6c9be84`

```dockerfile
```

-	Layers:
	-	`sha256:8a4057da865d646b7668f725be3e7107d68f9c6ce811f38c600ff5b92d6e6ea4`  
		Last Modified: Wed, 25 Jun 2025 22:44:36 GMT  
		Size: 48.1 KB (48133 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:4-php8.1-fpm-alpine` - linux; arm variant v7

```console
$ docker pull joomla@sha256:af6823a627adcae460e8f69e351d3cadb35938fcf2ede6c0562941e26fc0fb1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.4 MB (86351554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:083ff9cc9ec622760a7ac0faf9ad5685f61c52fc14c57e7d4b86322e31c554b2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 09 Apr 2025 19:45:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 09 Apr 2025 19:45:06 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_VERSION=8.1.32
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.32.tar.xz.asc
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_SHA256=c582ac682a280bbc69bc2186c21eb7e3313cc73099be61a6bc1d2cd337cbf383
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 09 Apr 2025 19:45:06 GMT
WORKDIR /var/www/html
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
STOPSIGNAL SIGQUIT
# Wed, 09 Apr 2025 19:45:06 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 09 Apr 2025 19:45:06 GMT
CMD ["php-fpm"]
# Wed, 09 Apr 2025 19:45:06 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 09 Apr 2025 19:45:06 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
VOLUME [/var/www/html]
# Wed, 09 Apr 2025 19:45:06 GMT
ENV JOOMLA_VERSION=4.4.13
# Wed, 09 Apr 2025 19:45:06 GMT
ENV JOOMLA_SHA512=c88f1779592fc74ff1fb3a26c81d113868d675f15afd45d0547c34216d49071a0d43b1f603e9f1daa5093499231dc95a77d165caff472d3d72ecb56af87a331e
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.13/Joomla_4.4.13-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 09 Apr 2025 19:45:06 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f58037841180f7071b0cb17f16a917752d43e658ee1f1d1590b910d941697a3`  
		Last Modified: Fri, 14 Feb 2025 21:49:05 GMT  
		Size: 3.1 MB (3120400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03b42d7db9fed02f8be351555a7c1cb492e5de9aeba350f89727c645ea19994`  
		Last Modified: Fri, 14 Feb 2025 21:49:04 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9997ea5283ca84c2230478f14c34317ce0e2df8d2463a0535910174e4ed66809`  
		Last Modified: Fri, 14 Feb 2025 21:48:39 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258512862c319b85db1b7f608a84a2f59513ee23ab1fd5757eece2466773b1c2`  
		Last Modified: Wed, 25 Jun 2025 21:04:12 GMT  
		Size: 11.9 MB (11914929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ccbdc8a2df6142d15fcf8952615949e4c7663bc2dac87170cabd0658c8d56d2`  
		Last Modified: Wed, 25 Jun 2025 21:04:10 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53637b251ed71802b4a53ef15228753b44640ef3be8af5d988d6cefffec4297`  
		Last Modified: Wed, 25 Jun 2025 21:07:50 GMT  
		Size: 11.5 MB (11490653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b82bf0c555a3985da4dca98cac103917f4ebe7444a43aef9ef44f9328ddbba`  
		Last Modified: Wed, 25 Jun 2025 21:07:49 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9075858598cecb5422dbe997fa836570822357246359c81ccacf24b8dc6e3d5`  
		Last Modified: Wed, 25 Jun 2025 21:07:49 GMT  
		Size: 19.9 KB (19877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4267bceda2a52b196d3dea8b3c53847decbd712c6a8a9121cb4fadd5d6b93282`  
		Last Modified: Wed, 25 Jun 2025 21:07:49 GMT  
		Size: 19.9 KB (19872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fc23db26e5b716f78a714db3f66e3ef0066630f0430c76af835477804552f25`  
		Last Modified: Wed, 25 Jun 2025 21:07:49 GMT  
		Size: 8.9 KB (8878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50f48b9373457f4483881ef99bd6151a435330b3ae9013aa376361802e8e3546`  
		Last Modified: Thu, 26 Jun 2025 01:44:24 GMT  
		Size: 23.1 MB (23115578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b2c9f848ea0696258819c1603de4dc8fb57fabdee08ab9e651d8a2a04f19f0`  
		Last Modified: Thu, 26 Jun 2025 01:44:23 GMT  
		Size: 6.9 MB (6908675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724f0e5c31c4031d7539a4e1a3606a9ec20c0cfaebdb61af0b2fa584cb7bff02`  
		Last Modified: Thu, 26 Jun 2025 01:16:42 GMT  
		Size: 62.8 KB (62826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d765f0c9fb30bac193bd82e30e2fe3696203930bb114d92d199ba64a7061c32f`  
		Last Modified: Thu, 26 Jun 2025 01:16:46 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:191a643bda2ac61eee161ffa6924233a81d67cc0ee7b71aaa54456f173a03aa0`  
		Last Modified: Thu, 26 Jun 2025 01:44:25 GMT  
		Size: 26.6 MB (26582497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059797bfea2fc124d78dfd09c54a38dbfde0743c4811a3593703b4d3d751f4f7`  
		Last Modified: Thu, 26 Jun 2025 01:16:49 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b42e964d4ae4dc9c914e2b88fa8236c96a93bf994e49095b8bd5162029b1c2`  
		Last Modified: Thu, 26 Jun 2025 01:16:52 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:4-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:9bea7c633d4ff6c09a4b8c21780ab77de6a39ce3f4141d670a2d1d80870ac565
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 KB (48134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47d03cc634c2c8a8d554587371a3d4a3dc3cd171618bb2fafe13385e18f14668`

```dockerfile
```

-	Layers:
	-	`sha256:9d932f275df22f21079d3f5de33e459725df7c10bb3e7ae8477115717cc81216`  
		Last Modified: Thu, 26 Jun 2025 01:44:05 GMT  
		Size: 48.1 KB (48134 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:4-php8.1-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull joomla@sha256:9ac47bbd68a85357f26287e99e3ef2591fff52fb70679123eab38cc5ad5a97ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.1 MB (93068051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ec4a3d73951c105b40e4f771343f3e0d2a115d0e4e7e18b2917f4050c4b7ba4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 09 Apr 2025 19:45:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 09 Apr 2025 19:45:06 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_VERSION=8.1.32
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.32.tar.xz.asc
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_SHA256=c582ac682a280bbc69bc2186c21eb7e3313cc73099be61a6bc1d2cd337cbf383
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 09 Apr 2025 19:45:06 GMT
WORKDIR /var/www/html
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
STOPSIGNAL SIGQUIT
# Wed, 09 Apr 2025 19:45:06 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 09 Apr 2025 19:45:06 GMT
CMD ["php-fpm"]
# Wed, 09 Apr 2025 19:45:06 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 09 Apr 2025 19:45:06 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
VOLUME [/var/www/html]
# Wed, 09 Apr 2025 19:45:06 GMT
ENV JOOMLA_VERSION=4.4.13
# Wed, 09 Apr 2025 19:45:06 GMT
ENV JOOMLA_SHA512=c88f1779592fc74ff1fb3a26c81d113868d675f15afd45d0547c34216d49071a0d43b1f603e9f1daa5093499231dc95a77d165caff472d3d72ecb56af87a331e
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.13/Joomla_4.4.13-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 09 Apr 2025 19:45:06 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e83372af8a678b04e4062678a6e4749712b1fe89b6611f08010a941229230e7f`  
		Last Modified: Fri, 06 Jun 2025 18:10:42 GMT  
		Size: 3.3 MB (3332268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023a04181e8579deb4c7737e06d7975655168e25be9a5a71b334a4c7cfdbefde`  
		Last Modified: Fri, 06 Jun 2025 18:10:42 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fcb24e42119e8047a1da41cf57b92f5aa3f71a0111ccbbd3fea2d1bfea9ee75`  
		Last Modified: Fri, 06 Jun 2025 18:10:39 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b87f30bc5023f39d357fb4cf5c99b40cff582716da5231b03c6a6edd4caf0d5`  
		Last Modified: Wed, 25 Jun 2025 22:48:10 GMT  
		Size: 11.9 MB (11914936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9d628cb671feff539d23111215b908364be31f536ec2258cdcbc91b34e482c`  
		Last Modified: Wed, 25 Jun 2025 22:48:08 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c5c2c1e28d85bd7020ccd6b86c28089fab567e689d05b3b995ee7d07b8c5313`  
		Last Modified: Wed, 25 Jun 2025 22:52:53 GMT  
		Size: 12.7 MB (12729574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fae7e588f1f6dfbb5b83c413083b9ea52931f442f49456ec14a1747e734a0544`  
		Last Modified: Wed, 25 Jun 2025 22:52:51 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73c2a7d84b54ab8aeb08754ea093e5460daf932ee61de2393b9831e95c129414`  
		Last Modified: Wed, 25 Jun 2025 22:52:52 GMT  
		Size: 19.9 KB (19863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b95221f0ce79511286edbfede3fe2ba12c2d0690ac3ce482479adfd5416eabf`  
		Last Modified: Wed, 25 Jun 2025 22:52:52 GMT  
		Size: 19.9 KB (19858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38edca7e0bec875be11b24c3e5ce6e6b39dc493194b51c1364c0916bc975fcd9`  
		Last Modified: Wed, 25 Jun 2025 22:52:52 GMT  
		Size: 8.9 KB (8877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cfcbbc0e9e22dcd40ded4bc93a69b0125e7b06536c5caf5c8192c98b711bf0f`  
		Last Modified: Thu, 26 Jun 2025 04:44:28 GMT  
		Size: 28.1 MB (28057007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43c9383ddf972ad763be25e71e6fd682666b499c64ad4d4fc4ad76875554f65`  
		Last Modified: Thu, 26 Jun 2025 04:44:28 GMT  
		Size: 6.3 MB (6338072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc51c11b70555d7935891740f588b0e45d702eb06943d6675bfed5ca973758da`  
		Last Modified: Thu, 26 Jun 2025 04:44:26 GMT  
		Size: 62.8 KB (62819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f336f76e6197643516d540ea8671508a8282dc841a24a78a5758694ef23d3b`  
		Last Modified: Thu, 26 Jun 2025 04:44:27 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af79fef941671eb58a905e45fc83058a5952e019ff22d6274f97d279890b1563`  
		Last Modified: Thu, 26 Jun 2025 04:44:28 GMT  
		Size: 26.6 MB (26582512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a07e30aceb20d987117552f9168b505618d30407065a440e2d3894823db4c9`  
		Last Modified: Thu, 26 Jun 2025 04:44:27 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e9e06530284737c3ad2df983142a8530584c7d7d97f7d2cde9866c6b74d9303`  
		Last Modified: Thu, 26 Jun 2025 04:44:27 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:4-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:f5b38b587ad9bc62ca822df9cfd078dc367b815a78699634686b24a4277333e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 KB (48166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17b049f007e08ca55a3a3b963618ac7d4bd7918b4a202adc267e91b4e18d8571`

```dockerfile
```

-	Layers:
	-	`sha256:bbccc1185d39e9a5b72769705dcd2540bef2cf6a1c31be6a819c5a55b4219e89`  
		Last Modified: Thu, 26 Jun 2025 04:44:03 GMT  
		Size: 48.2 KB (48166 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:4-php8.1-fpm-alpine` - linux; 386

```console
$ docker pull joomla@sha256:c8bf224ec8ec2d535435125bbcac416c25ed9af30996b619e16bcee59d2f372e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.5 MB (93484096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d8239085ba74895faf0ecc352914118f8e39407d7b8e3750e94bc23e24963c7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 09 Apr 2025 19:45:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 09 Apr 2025 19:45:06 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_VERSION=8.1.32
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.32.tar.xz.asc
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_SHA256=c582ac682a280bbc69bc2186c21eb7e3313cc73099be61a6bc1d2cd337cbf383
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 09 Apr 2025 19:45:06 GMT
WORKDIR /var/www/html
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
STOPSIGNAL SIGQUIT
# Wed, 09 Apr 2025 19:45:06 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 09 Apr 2025 19:45:06 GMT
CMD ["php-fpm"]
# Wed, 09 Apr 2025 19:45:06 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 09 Apr 2025 19:45:06 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
VOLUME [/var/www/html]
# Wed, 09 Apr 2025 19:45:06 GMT
ENV JOOMLA_VERSION=4.4.13
# Wed, 09 Apr 2025 19:45:06 GMT
ENV JOOMLA_SHA512=c88f1779592fc74ff1fb3a26c81d113868d675f15afd45d0547c34216d49071a0d43b1f603e9f1daa5093499231dc95a77d165caff472d3d72ecb56af87a331e
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.13/Joomla_4.4.13-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 09 Apr 2025 19:45:06 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b29434b52cfb4493b23e5a7af91f06b1c95402d05a489c0b5d2e04f3fa4eed3`  
		Last Modified: Wed, 25 Jun 2025 19:30:36 GMT  
		Size: 3.4 MB (3379892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e83840668e25e1cef7d8ef078ff2804929f9be9c5a10c7ed9d2f205c5bc458`  
		Last Modified: Wed, 25 Jun 2025 19:30:35 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50fcdac9f85ccc7d2e1619555d7724092fd0fd7a820a7038f3a2ddf68ba7d050`  
		Last Modified: Wed, 25 Jun 2025 19:30:35 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb7a90fcfbb2fbf5e5627b095be7401329893d895273b027cb0557fb9a4d7fa`  
		Last Modified: Wed, 25 Jun 2025 19:30:37 GMT  
		Size: 11.9 MB (11914909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:443a9d25d5c673c0915425227c74e237b6e062b1dbfccf211b97c0fff1b3d11e`  
		Last Modified: Wed, 25 Jun 2025 19:30:35 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e40a8ef4f6de922d3a05ec44d22433642c5d29ff79674068e18e3ea4084afc`  
		Last Modified: Wed, 25 Jun 2025 19:30:38 GMT  
		Size: 13.1 MB (13053939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70e6a1d20c2287fd3f3c17af456272e94b8c8f940cb2caa36e2f2d6a2b6c36c`  
		Last Modified: Wed, 25 Jun 2025 19:30:36 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15492dc032d484fcfc0dfee562e60994e7794d8768e53d90c9367881b84ef4c3`  
		Last Modified: Wed, 25 Jun 2025 19:30:36 GMT  
		Size: 20.1 KB (20057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a9f001b35f668f74083eb516d85a2d35759029b342ba0e05091f35e5558d66`  
		Last Modified: Wed, 25 Jun 2025 19:30:36 GMT  
		Size: 20.1 KB (20050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ec598ed77f5542e6c91c3c9b5297d346fc9b4a53274a113028a4b5520c49f59`  
		Last Modified: Wed, 25 Jun 2025 19:30:37 GMT  
		Size: 8.9 KB (8878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ef28207210df48e7be8fcdfcdb9357288444f1f4002c9031283bbd3391dccf`  
		Last Modified: Wed, 25 Jun 2025 20:04:13 GMT  
		Size: 28.5 MB (28456718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d4ba380074005ca17db54050ec81ddf752bb3fba9e3823db2b69e4b02e0633`  
		Last Modified: Wed, 25 Jun 2025 20:04:07 GMT  
		Size: 6.5 MB (6511488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd2b8ca8fd33d2fb3f5a74bea7564a9297a9e8bf417a903913840c7b0a948a4`  
		Last Modified: Wed, 25 Jun 2025 20:04:06 GMT  
		Size: 62.8 KB (62797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0eae0d4f60217889ee0efb07767c6aa794ec76fcee38cb73eb1455c49f44047`  
		Last Modified: Wed, 25 Jun 2025 20:04:07 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4990f7932c9ae3fb2c58f65db6245f445d6671c9f293cbe021ed43b47737cd`  
		Last Modified: Wed, 25 Jun 2025 20:04:10 GMT  
		Size: 26.6 MB (26582513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29cd04354436e337cd7f3382498f1f7322f33570a57164481db8f4c58babc907`  
		Last Modified: Wed, 25 Jun 2025 20:04:09 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543bada828de21ac2a6bce3c21eace86145cbd7ee5ff346390b5ea986c984405`  
		Last Modified: Wed, 25 Jun 2025 22:45:11 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:4-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:6fed7cced09a9dffdaa8b06dae2a6ffd603c43c110ec431c5bab13ed75723abd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 KB (47979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdea3d1d34f9d570704b92a01290b255f4724f9fc4d2fd870909f758a527f616`

```dockerfile
```

-	Layers:
	-	`sha256:9f75047f5b1e0e892b9162fa83a02be3ee75eb832beee60272667186e2eaf532`  
		Last Modified: Wed, 25 Jun 2025 22:44:47 GMT  
		Size: 48.0 KB (47979 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:4-php8.1-fpm-alpine` - linux; ppc64le

```console
$ docker pull joomla@sha256:412ef06dacd7d120a6d6847d886c044b4131f43e813304463304afeec2c5849f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95032300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d55c7b1ab48861ebcb5b8d947baab6615b82b910aed7e0a40badcfa79eac6f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 09 Apr 2025 19:45:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 09 Apr 2025 19:45:06 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_VERSION=8.1.32
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.32.tar.xz.asc
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_SHA256=c582ac682a280bbc69bc2186c21eb7e3313cc73099be61a6bc1d2cd337cbf383
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 09 Apr 2025 19:45:06 GMT
WORKDIR /var/www/html
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
STOPSIGNAL SIGQUIT
# Wed, 09 Apr 2025 19:45:06 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 09 Apr 2025 19:45:06 GMT
CMD ["php-fpm"]
# Wed, 09 Apr 2025 19:45:06 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 09 Apr 2025 19:45:06 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
VOLUME [/var/www/html]
# Wed, 09 Apr 2025 19:45:06 GMT
ENV JOOMLA_VERSION=4.4.13
# Wed, 09 Apr 2025 19:45:06 GMT
ENV JOOMLA_SHA512=c88f1779592fc74ff1fb3a26c81d113868d675f15afd45d0547c34216d49071a0d43b1f603e9f1daa5093499231dc95a77d165caff472d3d72ecb56af87a331e
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.13/Joomla_4.4.13-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 09 Apr 2025 19:45:06 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b0c526beb901f3bef02cf410e0d947ea692436a5dbc5258b999b61fcd3f138`  
		Last Modified: Fri, 14 Feb 2025 21:49:13 GMT  
		Size: 3.5 MB (3481114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa0f40451f4984088d9122ed91962de6fe91c34c09944da85f4c5c0b7bebf552`  
		Last Modified: Fri, 14 Feb 2025 21:49:12 GMT  
		Size: 930.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08e0c24d8ed4f70ce3641f51d7fb3e73e1e18d70e33576240bae71133a633b9`  
		Last Modified: Fri, 14 Feb 2025 21:49:12 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df01d2c0b6640532bc58b6c82658b409e843166f637a5bc08b0849fe9e8a5283`  
		Last Modified: Wed, 25 Jun 2025 21:18:34 GMT  
		Size: 11.9 MB (11914923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819387e4acca2a00cdc79295ac8e2c42bd804e2cd32162664d5f9252f8c15881`  
		Last Modified: Wed, 25 Jun 2025 21:18:32 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9b8dbc4aa23582b8c739c8f7ef1602346fa33153d7a386b649721fece7b9e0`  
		Last Modified: Wed, 25 Jun 2025 21:22:26 GMT  
		Size: 14.0 MB (13977885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4113498777d5f6bc859f28da143751449d2b8d2ec5b5065d705466f4de4a111`  
		Last Modified: Wed, 25 Jun 2025 21:22:24 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24170f2e198185df849286af1506304c792f9e5177224670dfeef032d388645`  
		Last Modified: Wed, 25 Jun 2025 21:22:24 GMT  
		Size: 19.9 KB (19855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ddbecf2a3d669c27dd194ea250c3f94f68eeac62911a70a2ccc08bd868f78b`  
		Last Modified: Wed, 25 Jun 2025 21:22:25 GMT  
		Size: 19.9 KB (19852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5210913bf296d2117b0b4667a25f12400247e8851216e984bb108efad9dcb45`  
		Last Modified: Wed, 25 Jun 2025 21:37:41 GMT  
		Size: 8.9 KB (8876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b82c9af741431b32a00c9cf5c3df32550453a5cd4c13c9906f21b37917c9a8`  
		Last Modified: Thu, 26 Jun 2025 03:13:38 GMT  
		Size: 28.9 MB (28883459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c66670627d6841e1e4b9b4c59eac0013271d225478a56d8f8712f1becd405b2`  
		Last Modified: Thu, 26 Jun 2025 03:13:15 GMT  
		Size: 6.5 MB (6497440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f1dad37d6700fa0f51986d44dab413cb8b9233153123ae83f0df4f72d6e7b4`  
		Last Modified: Thu, 26 Jun 2025 03:13:16 GMT  
		Size: 62.8 KB (62799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6d13d1de2b1a36f434d276da32fb166e56c5aaf80e825a398d1f64f392c0ea`  
		Last Modified: Thu, 26 Jun 2025 03:13:19 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f9b88059faed025cb34a7738359d883471a8b0e1c593a4feab9cab596cced1`  
		Last Modified: Thu, 26 Jun 2025 03:13:49 GMT  
		Size: 26.6 MB (26582505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b40fe72d80558e3b2caea49d0d75b65b05ff4f2285807b27b7e29db1e522ca5`  
		Last Modified: Thu, 26 Jun 2025 03:13:23 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec26e439c5bab8459b7d548b60fd86c4d8eea2a086875834eb227414afab7447`  
		Last Modified: Thu, 26 Jun 2025 03:13:27 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:4-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:a9576849219f775716987565ec2ef40c3abf7ff63c4d6d3428e53970959cecda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 KB (48060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f37d3e036d10b8a525edf935e96768bc2adbc345013851f020cabc6d19a126`

```dockerfile
```

-	Layers:
	-	`sha256:e9dc86029614a3c2bf2c8d4d5455f958a3935b906f8e71053a21dfcc2dab1a0c`  
		Last Modified: Thu, 26 Jun 2025 04:44:08 GMT  
		Size: 48.1 KB (48060 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:4-php8.1-fpm-alpine` - linux; riscv64

```console
$ docker pull joomla@sha256:6b879a5da7db7e30afb1800d084ad8eb91f3327777da26f81655f32462c8a06b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92471286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e96a9386eeaa166a5de38a87ac340f0499b08a2e553113b5d9c2c290ca71682c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 09 Apr 2025 19:45:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 09 Apr 2025 19:45:06 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_VERSION=8.1.32
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.32.tar.xz.asc
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_SHA256=c582ac682a280bbc69bc2186c21eb7e3313cc73099be61a6bc1d2cd337cbf383
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 09 Apr 2025 19:45:06 GMT
WORKDIR /var/www/html
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
STOPSIGNAL SIGQUIT
# Wed, 09 Apr 2025 19:45:06 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 09 Apr 2025 19:45:06 GMT
CMD ["php-fpm"]
# Wed, 09 Apr 2025 19:45:06 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 09 Apr 2025 19:45:06 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
VOLUME [/var/www/html]
# Wed, 09 Apr 2025 19:45:06 GMT
ENV JOOMLA_VERSION=4.4.13
# Wed, 09 Apr 2025 19:45:06 GMT
ENV JOOMLA_SHA512=c88f1779592fc74ff1fb3a26c81d113868d675f15afd45d0547c34216d49071a0d43b1f603e9f1daa5093499231dc95a77d165caff472d3d72ecb56af87a331e
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.13/Joomla_4.4.13-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 09 Apr 2025 19:45:06 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b75a14eca9423f582254c3b4d8d658ea4f006113a3355a1688bdbc6bac3eb770`  
		Last Modified: Sat, 15 Feb 2025 04:03:11 GMT  
		Size: 3.5 MB (3462944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be8a148fbb1301ad573d1000e2ec04300c75cbfc42b27312197cb623017dae4d`  
		Last Modified: Sat, 15 Feb 2025 04:02:57 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce5298f8d578c92ab374fdbb481a72f1557c4e7a726be21e513d65f51dd957cf`  
		Last Modified: Sat, 15 Feb 2025 04:02:55 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:481fc66a2a2a662284e9b5ae26a69f504b0aad51078164ae58c8343d6e822d5d`  
		Last Modified: Thu, 26 Jun 2025 03:27:36 GMT  
		Size: 11.9 MB (11914922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44d8689b214fe4b3e71671782b36fe3a9134d11f33aa7e402da96218be2ea39`  
		Last Modified: Thu, 26 Jun 2025 03:27:35 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb248e6543aec77413b221794761a5e4298f0463db0f630674700b32cbbed198`  
		Last Modified: Thu, 26 Jun 2025 07:07:27 GMT  
		Size: 12.8 MB (12774960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a3d7a6f8e0605666c355fe8643fd1ba475a1ef56b9ca4f34e83fe199c37cfe5`  
		Last Modified: Thu, 26 Jun 2025 07:07:36 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a931ea2cc88eaf3853a177a178cce598b1d6fb15443adb9d74981d33142d207`  
		Last Modified: Thu, 26 Jun 2025 07:07:37 GMT  
		Size: 19.8 KB (19847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf0b6ab657dac9f2355191a07bb236dc380b829c34484b9c9a1827648d5dff2`  
		Last Modified: Thu, 26 Jun 2025 07:07:38 GMT  
		Size: 19.8 KB (19846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b56756206406ccc642fce165b6255c70b8d0874f1019ddd31927fb44e37954d4`  
		Last Modified: Thu, 26 Jun 2025 07:07:38 GMT  
		Size: 8.9 KB (8882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18316da5d077c526d12c5e240deafbaa0f5b8ba5c67fb8eff8dc9c97494e7835`  
		Last Modified: Thu, 26 Jun 2025 11:07:29 GMT  
		Size: 28.0 MB (28048706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a10b5d640691fe082ed2219895371169f56bf36d9c7b21e587d8d11bc77d125`  
		Last Modified: Thu, 26 Jun 2025 11:07:19 GMT  
		Size: 6.2 MB (6215109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9bed8c983f5df3a6656a4b0aab4599f839773030a59ced4d7692b1c42bac731`  
		Last Modified: Thu, 26 Jun 2025 11:07:21 GMT  
		Size: 62.8 KB (62832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06e7a29a85dfdf78503378fabd8af6862d095acbc5101305c594e618e2ef301c`  
		Last Modified: Thu, 26 Jun 2025 11:07:21 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56396721c1e4e6a626deb76e6139dcacfaa1163673b90c98ba229d4ce14168e2`  
		Last Modified: Thu, 26 Jun 2025 11:07:33 GMT  
		Size: 26.6 MB (26582541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f42349074daca15b1053c6bb084096ac9cc697816dfd6059b85e9f7360463c54`  
		Last Modified: Thu, 26 Jun 2025 11:07:24 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8176b2c712beee727b86f44e61eae5b65ad91f72d9fd0743ae6bdad99da6c1b`  
		Last Modified: Thu, 26 Jun 2025 11:07:24 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:4-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:5855480628ed79a49bb040488f3cbe4d760e6cdf0213c75526ddf5a8db5a39bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 KB (48060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d1634d9da028e22e3b3dc8077a82d75dda37e15febfc2744ea4540e2346d197`

```dockerfile
```

-	Layers:
	-	`sha256:e98a1df053be0e165a17b439b77a9096700e4dec7b7bd94753d54e1337a6d678`  
		Last Modified: Thu, 26 Jun 2025 13:43:49 GMT  
		Size: 48.1 KB (48060 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:4-php8.1-fpm-alpine` - linux; s390x

```console
$ docker pull joomla@sha256:a306d3b2a1731940db2bfd4276854d71edee5ebde061115f8089bc5b0d716f0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94043258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abc068f7f114d19023249a317b6907ddbee66378e99be5e627a8ccba59066839`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 09 Apr 2025 19:45:06 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 09 Apr 2025 19:45:06 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_VERSION=8.1.32
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.32.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.32.tar.xz.asc
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_SHA256=c582ac682a280bbc69bc2186c21eb7e3313cc73099be61a6bc1d2cd337cbf383
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 09 Apr 2025 19:45:06 GMT
WORKDIR /var/www/html
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
STOPSIGNAL SIGQUIT
# Wed, 09 Apr 2025 19:45:06 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 09 Apr 2025 19:45:06 GMT
CMD ["php-fpm"]
# Wed, 09 Apr 2025 19:45:06 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 09 Apr 2025 19:45:06 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.23; 	pecl install memcached-3.3.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
VOLUME [/var/www/html]
# Wed, 09 Apr 2025 19:45:06 GMT
ENV JOOMLA_VERSION=4.4.13
# Wed, 09 Apr 2025 19:45:06 GMT
ENV JOOMLA_SHA512=c88f1779592fc74ff1fb3a26c81d113868d675f15afd45d0547c34216d49071a0d43b1f603e9f1daa5093499231dc95a77d165caff472d3d72ecb56af87a331e
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.13/Joomla_4.4.13-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 09 Apr 2025 19:45:06 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa7d28698cb4cc98a3c525b5346c0c8522a2a4846e43b94c50556f15452592b`  
		Last Modified: Fri, 20 Jun 2025 19:32:42 GMT  
		Size: 3.6 MB (3567602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819d06c495f1b450032fb9cb4086a80e92288114c0acb8f12f64f6a278248a35`  
		Last Modified: Fri, 20 Jun 2025 19:32:42 GMT  
		Size: 937.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9920563bfcae5d1b60910142a8784ed9ddb74a196d0461fe9b2e1c45957d46fd`  
		Last Modified: Fri, 20 Jun 2025 19:32:42 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0623fc8a9e42dd6278c6ad352014b5a00bfd7f225cb3dd7c3a9c60b1f143a97`  
		Last Modified: Thu, 26 Jun 2025 04:13:48 GMT  
		Size: 11.9 MB (11914939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfb5f51a2a4a22d7aa76895f4488866a1eb8cc393cf1961cedc02174b68b8767`  
		Last Modified: Thu, 26 Jun 2025 02:04:43 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7227503509a4b048970fc5c8d031768cac4050624d687783da6d622ec9eb9147`  
		Last Modified: Thu, 26 Jun 2025 01:59:37 GMT  
		Size: 12.7 MB (12666787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9601de501c4c6746dd23717b901acae4bf010647d6af15f513a760ad6ab51965`  
		Last Modified: Thu, 26 Jun 2025 01:59:36 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b93563f8e8bd31b8312663758d6624f62f22fa8c5df828a446468f52508a31`  
		Last Modified: Thu, 26 Jun 2025 01:59:36 GMT  
		Size: 19.9 KB (19870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a561f8bbcdfda8348ab2d4626b6a824bbf6996a0b8f73615ea5c7f1aebab9228`  
		Last Modified: Thu, 26 Jun 2025 01:59:37 GMT  
		Size: 19.9 KB (19865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628f3f21446d1be5d0f2efc03a8d53d913cdeedb9e4ca4dc9ba567a45a20f35d`  
		Last Modified: Thu, 26 Jun 2025 01:59:37 GMT  
		Size: 8.9 KB (8881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1565524b98b0a00aeada20894618c1ddaf149a7a1500d367e0d2b51ba6ee88`  
		Last Modified: Thu, 26 Jun 2025 04:13:02 GMT  
		Size: 29.2 MB (29220109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ac2799c585f1629892eec87d4cb6514965bb77f8df1ee12bff0e21fd3c26ed`  
		Last Modified: Thu, 26 Jun 2025 04:12:57 GMT  
		Size: 6.5 MB (6503037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4274675195c2c0b4a989ee2cd8095c547f658a2284e8d1e79075da796099b777`  
		Last Modified: Thu, 26 Jun 2025 04:12:57 GMT  
		Size: 62.9 KB (62857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1942c38a6bb368fb4110be02f36276000a633e107ab43209fab680231ba390`  
		Last Modified: Thu, 26 Jun 2025 04:12:57 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faa08548dba20b688d0a9ff51ad0cf26eaf148386ae67fd170b0829be88d2080`  
		Last Modified: Thu, 26 Jun 2025 04:13:00 GMT  
		Size: 26.6 MB (26582496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e4454bb897e08d5ebb948d831be68845d07de0c7b74ec0e96fb860b9672fd07`  
		Last Modified: Thu, 26 Jun 2025 04:12:57 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce99d1934012c4cae3c2045048c00e10b3103fbdd14f968ae4ba088569b2f71`  
		Last Modified: Thu, 26 Jun 2025 04:12:57 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:4-php8.1-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:55fc028c578694d2198759b9cacd4d02e10715577e3fc22bd1904051d004f06a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 KB (48013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:591174be6fda5e6973500c40675bf6956ff0b5d5d9cc7262f4b88f5005858d76`

```dockerfile
```

-	Layers:
	-	`sha256:5eebc2eb068425a85e48e2e0deb64b90f48ab91beaa7d8f48c02b9ff845b012c`  
		Last Modified: Thu, 26 Jun 2025 07:44:07 GMT  
		Size: 48.0 KB (48013 bytes)  
		MIME: application/vnd.in-toto+json
