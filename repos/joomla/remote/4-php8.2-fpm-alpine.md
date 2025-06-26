## `joomla:4-php8.2-fpm-alpine`

```console
$ docker pull joomla@sha256:f41b4589729ff917d4f22f1403fcd00d324c0b5ae530ec49cf18a07de7703986
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

### `joomla:4-php8.2-fpm-alpine` - linux; amd64

```console
$ docker pull joomla@sha256:0cd17e17ec35feb48ddda2ec208fb889b79f9f777988026b22c284a34218d6a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94024988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c56a763e1ad5d03479ecbc30188738785be6bf981319960e172361b2a41e8d0`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 09 Apr 2025 19:45:06 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_VERSION=8.2.28
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.28.tar.xz.asc
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_SHA256=af8c9153153a7f489153b7a74f2f29a5ee36f5cb2c6c6929c98411a577e89c91
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94add63fdddd4d35bdf004b110e02f517d30b3b54552e46b3a885a6cd79ee91d`  
		Last Modified: Wed, 25 Jun 2025 19:27:23 GMT  
		Size: 3.5 MB (3468347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf2097341024ea7aaabd873ee875580854d05f02ba077fb29731592b28ca8a2`  
		Last Modified: Wed, 25 Jun 2025 19:27:22 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fb8c48e387153476143ffd662efaad128051557598da0de65608fbd6d670c7b`  
		Last Modified: Wed, 25 Jun 2025 19:27:22 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab394df2c3ca2543a081b4eee0e45de38031cdbe4b43b1491433f5dc12e29c3`  
		Last Modified: Wed, 25 Jun 2025 19:27:24 GMT  
		Size: 12.2 MB (12169304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3464369e5e2273bf5c460ef3fec07503ce3d22159a841dbe0055c4f43926558f`  
		Last Modified: Wed, 25 Jun 2025 19:27:22 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edadbb104521becd07a7281f3e1e1f3852e01414ca6e5e17d97f187e4d22630a`  
		Last Modified: Wed, 25 Jun 2025 19:27:24 GMT  
		Size: 13.0 MB (13023511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daacba4af3a4b0df1148027bccece264e037fb8815d68707585c6277a8b46b62`  
		Last Modified: Wed, 25 Jun 2025 19:27:23 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d455e2081f32ca848a06b1a0066ee3c74c327ffa2e7110692bf3b3c38912d22`  
		Last Modified: Wed, 25 Jun 2025 19:27:23 GMT  
		Size: 20.2 KB (20204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99dd339f857ab3450b8e92c2e71641e4f8a993cf835bcdcb3e6553b84ea943ed`  
		Last Modified: Wed, 25 Jun 2025 19:27:23 GMT  
		Size: 20.2 KB (20200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d2abfd3b0d0e2e4f1317cecc612a4c246c2724e1eaa902a6d7e71d933aef271`  
		Last Modified: Wed, 25 Jun 2025 19:27:23 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7f2aec3259dd94461a5b506de2f5fa51f39b3b175c1fb46b6bff5e4b8e89c2`  
		Last Modified: Wed, 25 Jun 2025 22:45:50 GMT  
		Size: 28.3 MB (28272541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a56a2b4e47ff090bb6b389a7a8b83757f63a7c69e165001dc541b4642c6be1`  
		Last Modified: Wed, 25 Jun 2025 22:45:48 GMT  
		Size: 6.6 MB (6589777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e4192c0cd69768d3e677b0ad18683b691fee628e43797ab56d0bb55a28d534`  
		Last Modified: Wed, 25 Jun 2025 21:30:18 GMT  
		Size: 63.3 KB (63343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522760054ed09743831b13a7590cd0fc6260eedbfa1db68ff2341258692438d5`  
		Last Modified: Wed, 25 Jun 2025 21:30:22 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21880d3154bf1044b9ebe098ab26ab7907b1f4f345b6365efc584b538c002f8c`  
		Last Modified: Wed, 25 Jun 2025 22:45:49 GMT  
		Size: 26.6 MB (26582493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3c41acd77a0442d166c454e34091d389539547031e3dbef770aea188282412c`  
		Last Modified: Wed, 25 Jun 2025 21:23:44 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c834a250022432f9744392b9dc9bef79339a1dffad63bf8760ccab9edcf9c6a0`  
		Last Modified: Wed, 25 Jun 2025 21:23:44 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:4-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:723ae32aab2744597c82aa7ea370300a2b7eb654ad6bc19dc5b5da7c031a1b02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 KB (48014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b57c8da44fab78f4242cb3bba8f3d21dc270e431038ba1c2ac493341f4f8bdbe`

```dockerfile
```

-	Layers:
	-	`sha256:499f40789f0ef8cec33bf0e320fb96f85680c869b97c6fe718bc3ac52161d3ea`  
		Last Modified: Wed, 25 Jun 2025 22:45:13 GMT  
		Size: 48.0 KB (48014 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:4-php8.2-fpm-alpine` - linux; arm variant v6

```console
$ docker pull joomla@sha256:080d92649327464b50986c67db01e4b9f161151d07457642179a5f80b7e60365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.1 MB (89135435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af3417cd270bf8718b773b1949e8fe2ebd0da06b79c11fdfb8b5137c58012f5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 09 Apr 2025 19:45:06 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_VERSION=8.2.28
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.28.tar.xz.asc
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_SHA256=af8c9153153a7f489153b7a74f2f29a5ee36f5cb2c6c6929c98411a577e89c91
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b2fddcddb67f07dabc88b449999588f7b51998c1114a9e3f0ae4ad9519b41e`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 3.4 MB (3432459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f159e81bd801861164e94e01093125bcc7ed5b9fb65bed9a9f3ce4d3a707c8c`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:045dfb1ee98b64d4099b6b9d91bdb57fab7a640182f195075c814d3071429a5b`  
		Last Modified: Tue, 10 Jun 2025 23:54:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0dff249471cd62515b6a9e335a70906ab5c2c68c849a1426a442de9e68826a`  
		Last Modified: Wed, 11 Jun 2025 02:02:44 GMT  
		Size: 12.2 MB (12169272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6f1502c9f9334e07d8af9b78be78c7070f5f647aa3e00f7a400c7f3581a1a3`  
		Last Modified: Wed, 11 Jun 2025 00:27:03 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63ca5e70fb91bddd1e57ecfb99c9fb0ec075f97386e85208fb8132dc9700377`  
		Last Modified: Wed, 11 Jun 2025 01:12:30 GMT  
		Size: 11.8 MB (11761720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e30494faf521a7d381e63e18c78bdb5c2e11ff09222b51bb33552f81c86879`  
		Last Modified: Wed, 25 Jun 2025 20:02:22 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88003ab6922d5b4a69ce2145b84439fd81c7d0f5aa5a29219b9e2e29549bc852`  
		Last Modified: Wed, 25 Jun 2025 20:02:26 GMT  
		Size: 20.0 KB (19995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4940b361b14980057f8d901e5946833adb9846068045344b928c60065078041`  
		Last Modified: Wed, 25 Jun 2025 20:02:30 GMT  
		Size: 20.0 KB (19995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d591d73e67022352eaeb7938bc83424eb475a392b387ca4f650b0c0d5ba1fa71`  
		Last Modified: Wed, 25 Jun 2025 20:02:35 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac279db3738e2be95a22515c7d155ad036660259c4267c42e02670c2bed6d4f5`  
		Last Modified: Wed, 25 Jun 2025 20:41:21 GMT  
		Size: 24.4 MB (24359700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1852f495812bbcd70cde89e3fb4f8ddde2b1d08ce3da655e8ca628d5b6086236`  
		Last Modified: Wed, 25 Jun 2025 20:41:19 GMT  
		Size: 7.2 MB (7207094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84923858becb862fe5175c0fc19af2b8b7c11afe7422fb314ae2f7079a601f16`  
		Last Modified: Wed, 25 Jun 2025 20:41:18 GMT  
		Size: 63.3 KB (63330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dd514ad8654e2e76660c90dbbbf93524fe90ecda3758f7bca0add49ef7dc61a`  
		Last Modified: Wed, 25 Jun 2025 20:41:19 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c287bfde492f3c45a400d132db7d9e781b470fa2dead3bda1be3bd5a66fcd0`  
		Last Modified: Wed, 25 Jun 2025 20:41:21 GMT  
		Size: 26.6 MB (26582504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2eecbfcc30b74fb9974968782b25bb3d5ca5aa8c04d47473311dba4128f0630`  
		Last Modified: Wed, 25 Jun 2025 20:41:19 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4ee5ca6e47bd2117063fa652aa5e9d1743051066401aa2f802e4f0286fcb59`  
		Last Modified: Wed, 25 Jun 2025 20:41:19 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:4-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:fd72861f1c20397f5000ac7e487a750d513016784771d91358eca3456b000ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 KB (48133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98fe1e317602df062b93c716a37cbdcce330df5deba28963d31f54f1332da489`

```dockerfile
```

-	Layers:
	-	`sha256:f5aac45c7eab6219a8025713ce1606d0149c5b883c1d95f7093734900cb79a27`  
		Last Modified: Wed, 25 Jun 2025 22:45:16 GMT  
		Size: 48.1 KB (48133 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:4-php8.2-fpm-alpine` - linux; arm variant v7

```console
$ docker pull joomla@sha256:1afe1ca3ab4c50bee67a1cdb6020545a53cc156c2f7fbace3ec677502bd931ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.7 MB (86668865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8784ca9680be3e109947112aac79a69cce6c01f9c4c4d8d4cd9b8cc26201a6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 09 Apr 2025 19:45:06 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_VERSION=8.2.28
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.28.tar.xz.asc
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_SHA256=af8c9153153a7f489153b7a74f2f29a5ee36f5cb2c6c6929c98411a577e89c91
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
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
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec113fe1f048c8128d671c69cfadec1876ed37d14a445b7755326cbfa9acee36`  
		Last Modified: Wed, 11 Jun 2025 11:39:14 GMT  
		Size: 3.2 MB (3247470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3d974efcf5fd7ed95cd66bd2537770b4f31b8d7af064ae6e9119868bac3309`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b29a62342af1e9fd2e1392885a9e1a9439cdee5d849c8f557fb8693b5650363b`  
		Last Modified: Wed, 11 Jun 2025 11:39:13 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b82fe7311faa4207700833f5c8e393b83ad562aa8f8c66acef2f89df09ac068b`  
		Last Modified: Wed, 11 Jun 2025 12:11:21 GMT  
		Size: 12.2 MB (12169291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b41196cc2eeca02797027fd2dec6c3ab53211848594e5aeaca206fd7aa1ccc6a`  
		Last Modified: Wed, 11 Jun 2025 12:11:20 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af00d342fc44d65b0937961e484ba5589c348f600ff5096ddceca908fc7661bb`  
		Last Modified: Wed, 11 Jun 2025 12:16:25 GMT  
		Size: 11.1 MB (11073467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96ceaf266a230ecd372dbb9e2233c66908be5df5ce611c665b3188bc6c0e0f5`  
		Last Modified: Wed, 11 Jun 2025 12:16:24 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d9306897d2b8bbba158341448061d589f28a3616e6beb0306059e2eff7a213`  
		Last Modified: Wed, 11 Jun 2025 12:22:11 GMT  
		Size: 20.0 KB (19988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dabf3d132f03f866a51901e68e8c6a15ed51bdf7e39068955cff9b8b789385ce`  
		Last Modified: Wed, 11 Jun 2025 12:22:17 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b207b0165ce3b0ee02147c064f7f712fa54d02db1de9a1b9a8d84902bfa99b`  
		Last Modified: Wed, 11 Jun 2025 19:13:10 GMT  
		Size: 23.1 MB (23137830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ada809637ea27f625b07c95d73e94e62f432f7d2ff68cdc152197801cc7e6a60`  
		Last Modified: Wed, 11 Jun 2025 19:13:13 GMT  
		Size: 7.1 MB (7137388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:985ce1d8adf7efb1ad17a2123d6e76fe7d78c5a661e7d98415f1e41ae4ec65d4`  
		Last Modified: Wed, 11 Jun 2025 19:13:11 GMT  
		Size: 63.3 KB (63335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68fbd8bc4258ecab4b324d443005bc7694a46e04159e9c86de24d647a0507984`  
		Last Modified: Wed, 11 Jun 2025 19:13:11 GMT  
		Size: 387.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbef575555229667caa10cda764691de36f6eaf62d6968f12efcf55c4826106a`  
		Last Modified: Wed, 11 Jun 2025 19:13:15 GMT  
		Size: 26.6 MB (26582502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e4b58d9e0210a80a49452cd9959e1859c35694ea2bd1759e386d65799dfbff`  
		Last Modified: Wed, 11 Jun 2025 19:13:11 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a255cf341872ba6e44ed027995fcdc39c23a1fc8e41d62e137980d569294246d`  
		Last Modified: Wed, 11 Jun 2025 19:13:12 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:4-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:ab7b1a92f42bc9d7e33da424f361dfc1eafbec9788293f71e211f0f00e1bb040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 KB (46885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:799f37b2bbb2d8edaef8835ac0e6931d923fd1859aa9945a8de23bbdb2f113f5`

```dockerfile
```

-	Layers:
	-	`sha256:93ddf7c37b5f99b660d13b7e442a3a40a812ed84e73a2b444b00fe54b4db1c0e`  
		Last Modified: Wed, 11 Jun 2025 22:43:48 GMT  
		Size: 46.9 KB (46885 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:4-php8.2-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull joomla@sha256:2b408a16087439a69d30d4c471086f93c3201617155b223abf8cdeb32f86f307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.1 MB (94113011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e71787687f3d5665253b544408f7177ccc7063790902e7c9728c06e5493b26c`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 09 Apr 2025 19:45:06 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_VERSION=8.2.28
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.28.tar.xz.asc
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_SHA256=af8c9153153a7f489153b7a74f2f29a5ee36f5cb2c6c6929c98411a577e89c91
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
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
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:476e263556d24cfaaa81ec9153b95e1b25d54abdb35b46c3c74fa988a9f252f3`  
		Last Modified: Wed, 11 Jun 2025 09:16:54 GMT  
		Size: 3.5 MB (3470681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c1e5bea448bb73ac691df99daf5772e7cb7307f122b4e0544c289a55be9ee24`  
		Last Modified: Wed, 11 Jun 2025 09:17:12 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49a64acbbc8d220ea4c16baed763b26899f58299a8b85d3b8513f03b3023893`  
		Last Modified: Wed, 11 Jun 2025 09:17:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b90603f3edd6a58abbc910b5a9bac2e16f77bd6bc091320287d409f9a2e9be`  
		Last Modified: Wed, 11 Jun 2025 09:42:48 GMT  
		Size: 12.2 MB (12169283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbadee23b98c9e75cbc7946d396595d5fd3cffee2c3ff4b781c4de91570ecc1a`  
		Last Modified: Wed, 11 Jun 2025 09:42:46 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b0e11aea67c4227f9eea4c5248d7a892fa161abd087bc5bb14711c475aa7f29`  
		Last Modified: Wed, 11 Jun 2025 10:58:03 GMT  
		Size: 13.0 MB (13021651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01580fb33ca7e43818c66205ea56d998bedc6f072a04d5a544581994c59df3a1`  
		Last Modified: Wed, 11 Jun 2025 10:58:03 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa0aee2646aef54b3a71d83a2289487eb4cfce6533260a8a6a78ff953cfc4ff`  
		Last Modified: Wed, 11 Jun 2025 10:58:03 GMT  
		Size: 20.0 KB (19988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989d06dfc1d16cf1d4ce2d43c2e25f8f88a84f1dfb2f5c74308664178ca1e554`  
		Last Modified: Wed, 11 Jun 2025 10:58:05 GMT  
		Size: 9.2 KB (9173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1a0c5fea23010aa5f4786fe5531f75e9aad5c005470987bfc0706a2add0eb7f`  
		Last Modified: Wed, 11 Jun 2025 16:13:50 GMT  
		Size: 28.1 MB (28082080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3d9de5be333d0ce429920544d0ea31294f95016a0b4b454ac2dad5890a9d73`  
		Last Modified: Wed, 11 Jun 2025 16:13:45 GMT  
		Size: 6.5 MB (6549109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aa5514cdce87d507cd29bfb507dcd5550a46a66fc86c6e964be328f144c8771`  
		Last Modified: Wed, 11 Jun 2025 16:13:44 GMT  
		Size: 63.4 KB (63354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81078e70acbd535490611e0b366c31ff85712c207f58e332d1f9e63b2bcc1e88`  
		Last Modified: Wed, 11 Jun 2025 16:13:45 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b813aff8640761ede706300f6048d532847085c2b1baa2000f3ca99b3a4017e`  
		Last Modified: Wed, 11 Jun 2025 16:13:48 GMT  
		Size: 26.6 MB (26582513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bee8ca0b32bc9cc4c30a6eb2127d017fdcb9188b34f0d820bac77d34417dd86`  
		Last Modified: Wed, 11 Jun 2025 16:13:40 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4e3583b75c1ce91d5b63cd8d58f7a58d90b763dcffd8b01d307e393c57b08dd`  
		Last Modified: Wed, 11 Jun 2025 16:13:45 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:4-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:7c7b280bc665cc9fd9218ae78ee83c8a0d73ce594b7460b20e047e48fb52c9f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 KB (46918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59e29b31443839ebbca87fd9b44828021559e3e6973785928b6b2fb81cfa0630`

```dockerfile
```

-	Layers:
	-	`sha256:cfb4c429356bdb318bf77d497e5b91c5d792ab0a4ebfcbbf4d555605f512e9a7`  
		Last Modified: Wed, 11 Jun 2025 19:43:40 GMT  
		Size: 46.9 KB (46918 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:4-php8.2-fpm-alpine` - linux; 386

```console
$ docker pull joomla@sha256:de396e3fc7b5b18692cff51462d23e2b8b98936c0c73a6607b6bf26831503041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.6 MB (94579382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:458d0166ff166dbb6c0f630f4dd469add0124eafa5a616acd7754c7f7b19e469`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 09 Apr 2025 19:45:06 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_VERSION=8.2.28
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.28.tar.xz.asc
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_SHA256=af8c9153153a7f489153b7a74f2f29a5ee36f5cb2c6c6929c98411a577e89c91
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
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
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dae06500ff2e54f557185eedea4c98b5dece91ec7c4128be1c46796def93628`  
		Last Modified: Wed, 25 Jun 2025 19:28:36 GMT  
		Size: 3.5 MB (3527756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299bb410795ac1d4ae3258de89ea4670382f6e3f17fa93a72caae8321ae9a87e`  
		Last Modified: Wed, 25 Jun 2025 19:28:46 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c3523d1467bae44cadc1961a404a473dcdb8c92961bff6ff35c41acc8ec538`  
		Last Modified: Wed, 25 Jun 2025 19:28:47 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a2719cc0dfb9de60c9a640b97c0d32c9b8cd0741344dcf74aac70eb6194766`  
		Last Modified: Wed, 25 Jun 2025 19:28:48 GMT  
		Size: 12.2 MB (12169267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2783ba5591d0db40c3a6250b6ceec6256fc920727bd3e5f8c94d1cbdb9358e`  
		Last Modified: Wed, 25 Jun 2025 19:28:47 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab45d3b01375418b50f7aa640eae4006f536c17163952a94871a9581045f50f`  
		Last Modified: Wed, 25 Jun 2025 19:28:48 GMT  
		Size: 13.3 MB (13347262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011cf49e2689d42f1dcdd84248643f60a9af87774f8fc2b7766fe2c73ac7ae60`  
		Last Modified: Wed, 25 Jun 2025 19:28:47 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89782d591fb8f9c308f03ce195c6eaff9f7d8dde2c4ee5181ac7e6bcbb8d37e`  
		Last Modified: Wed, 25 Jun 2025 19:28:47 GMT  
		Size: 20.2 KB (20191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d58eb7a0a3c3f01bdc8cade318d408e7ea65a1b95f53ac7442e247f59136074`  
		Last Modified: Wed, 25 Jun 2025 19:28:47 GMT  
		Size: 20.2 KB (20183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44232f74ddddb8656332b9fb7b239ac3aed5c1448f2788358ecbd43ba4454a54`  
		Last Modified: Wed, 25 Jun 2025 19:28:47 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4710cea8551e939c7f60efd28d0c46845d812d22920285c6abf2951713fad9`  
		Last Modified: Wed, 25 Jun 2025 20:04:33 GMT  
		Size: 28.5 MB (28486802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8500df94c505494c3d5a36f4f9530406a7c4924ff78c1e55febb2fe5bebaad4d`  
		Last Modified: Wed, 25 Jun 2025 20:04:31 GMT  
		Size: 6.7 MB (6727697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b673fe10aa7584761442f224d6445cb590d039c085c082c60ba073acf1fea7`  
		Last Modified: Wed, 25 Jun 2025 20:04:30 GMT  
		Size: 63.3 KB (63281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa60f1131954f28bf79d181cdf4781dd91c828fd7a3c4b34e6ed8c5d08f75529`  
		Last Modified: Wed, 25 Jun 2025 22:45:49 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f842f2f72b3201220ee29022172687b6eec6588540019c8569724b4f678ee4`  
		Last Modified: Wed, 25 Jun 2025 22:45:50 GMT  
		Size: 26.6 MB (26582496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f05feb88680966236709500a389d812e53fc38a5b745c173abeda810a87bbda`  
		Last Modified: Wed, 25 Jun 2025 22:45:49 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d302511067901ecaa9f3be71c22348d11f8e9853ecc2f7f72e590cfd897c42e`  
		Last Modified: Wed, 25 Jun 2025 22:45:49 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:4-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:cf8f599267db8db1590d858b0d88fca25c8e435a317db15ca24111b178d656da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.0 KB (47979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40b2483e5edbb4019cdc293eb131ee8b8f0a71fd80f885b83f1358dcf289b2be`

```dockerfile
```

-	Layers:
	-	`sha256:9e269de28fbf85ecde123c13281e27e2aab200bed14eeec2cabedc0673a2f741`  
		Last Modified: Wed, 25 Jun 2025 22:45:27 GMT  
		Size: 48.0 KB (47979 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:4-php8.2-fpm-alpine` - linux; ppc64le

```console
$ docker pull joomla@sha256:39407542ceae07eaac34785aa73408929eb8a33a64a848a134986a03f199cc5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95319233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ccf1124278fc2d55631a6705eed6db4197da36d3c5284d808509adca08bf756`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 09 Apr 2025 19:45:06 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_VERSION=8.2.28
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.28.tar.xz.asc
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_SHA256=af8c9153153a7f489153b7a74f2f29a5ee36f5cb2c6c6929c98411a577e89c91
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
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
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a27d95a001e42dd9b82fe6b7e63b48f844b2bd3aa5239c663167b36d4f1fa42`  
		Last Modified: Wed, 11 Jun 2025 09:12:55 GMT  
		Size: 3.6 MB (3619144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0377d467323561e29ac5bd8915837530c91c4ef72b3a2f4ad73bbcd6d467c36d`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b63ba550992ed4fdaf12dd9e376ec5efd146f93f3e9f970030c609f95b4c30`  
		Last Modified: Wed, 11 Jun 2025 09:12:54 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33d6defed87550bbe8bae3b8e2c00cb275c3e29c2e9991b22b37a14047348b0`  
		Last Modified: Wed, 11 Jun 2025 11:53:52 GMT  
		Size: 12.2 MB (12169287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1331cd27e57b2da3f468abfd9571a170d1baca6d355735318e0b4799debec30`  
		Last Modified: Wed, 11 Jun 2025 09:44:15 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdc490df73a0a14f5f17d83c2eb421e4f1ecda0be6a6ac0d5581fcef66a4481e`  
		Last Modified: Wed, 11 Jun 2025 09:48:47 GMT  
		Size: 13.5 MB (13493557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1152fee193db712bdfce39fbfc79d165dec471de8a206eb2af96215545eb3593`  
		Last Modified: Wed, 11 Jun 2025 09:48:45 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555f65597f9807daff78872ac04ba2245905ff8aec0b2df2e4c2a90103d43fb7`  
		Last Modified: Wed, 11 Jun 2025 09:48:45 GMT  
		Size: 20.0 KB (19994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:378cf67e87a36018d9103482e2068b96fb5f0eae108500d8fc107029c19fcb5a`  
		Last Modified: Wed, 11 Jun 2025 09:48:46 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace57442386804cb25c32e36fb2600a6f31704f289b69acedebd1d87b36e73d1`  
		Last Modified: Wed, 11 Jun 2025 19:36:18 GMT  
		Size: 28.9 MB (28916047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:facb49ff9eb6e5051eea7a3cb34dcc8476d9602a2940b1ea2ff65ee93a24bc6e`  
		Last Modified: Wed, 11 Jun 2025 19:36:20 GMT  
		Size: 6.7 MB (6706725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:996837cc03e244f3eff481c664e18fdf87ba66babc8e4f718e4a1651864dd101`  
		Last Modified: Wed, 11 Jun 2025 19:36:16 GMT  
		Size: 63.4 KB (63360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d92b9f6107733cf661130de73fe70dc20a6938b8688f585185594719db9591c4`  
		Last Modified: Wed, 11 Jun 2025 19:36:16 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb137b672b195950b511437b10080e43e7806f5f27f8d5dba4704ca1492b033b`  
		Last Modified: Wed, 11 Jun 2025 19:36:24 GMT  
		Size: 26.6 MB (26582514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1220400ab5d6e6ac8008f7bbe969b9ab60f0f3a93944fc7f9d5d708887152f26`  
		Last Modified: Wed, 11 Jun 2025 19:36:19 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5df311f66f7829e918a7f88cfa70b46a3f2e63f8140730da68fdd7a912ee6ad`  
		Last Modified: Wed, 11 Jun 2025 19:36:20 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:4-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:56c09d85e951e4884b1ab4eb2dafb0dcc8eba35a133554d7107cd2a3c7fd7e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 KB (46812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23f29cc656a87994dff0c690db07c7c723695bdff288edb13c5b61213630b412`

```dockerfile
```

-	Layers:
	-	`sha256:e90cc247ea43df8f1eced7e91090468b2aa3d4ccd8d5048f7836e63fa66f3e00`  
		Last Modified: Wed, 11 Jun 2025 22:43:55 GMT  
		Size: 46.8 KB (46812 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:4-php8.2-fpm-alpine` - linux; riscv64

```console
$ docker pull joomla@sha256:4662fd65811f461abb70bdc5c6d1cc19cf32f446c5dcb42c07d57d89f0f9cd1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.8 MB (92770819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b84c7c5694e972b0f9a182ce1aa2ab9bed7b0970134b970b1587618b8645d7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 09 Apr 2025 19:45:06 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_VERSION=8.2.28
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.28.tar.xz.asc
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_SHA256=af8c9153153a7f489153b7a74f2f29a5ee36f5cb2c6c6929c98411a577e89c91
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
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
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fc9c1f5ef55f1b2ff3a6b36284b619ab1578de78bc84c439b1898065ffdd4f1`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 3.6 MB (3603347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:799ef8c3b461dc47d68354281bf2ae2d00422c181fa7d8f8084c1489e4f74b7c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6faf4f4cbdf1dd7a77faca53bd9b20a1a4be9c74973d2b4d795fed979f275c`  
		Last Modified: Wed, 11 Jun 2025 02:34:22 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f26c6f8306cb2e8a73b2662a9f1d5375d2cc5a6078ae298e8aa8414a6e212ece`  
		Last Modified: Wed, 11 Jun 2025 11:54:09 GMT  
		Size: 12.2 MB (12169293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b70c387a1864074bdc24a57fab728a76bc11f92673d2acef6eeda492be1e99`  
		Last Modified: Wed, 11 Jun 2025 08:18:37 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2d85f91dbc3e191579efa4ad31d21aa519b6b3a6b3e13429a8dc9b532be632`  
		Last Modified: Wed, 11 Jun 2025 20:41:15 GMT  
		Size: 12.3 MB (12304413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67538fae5cf4f223e736a34ef4b9578947ad239dd821d1f09289f51209875dee`  
		Last Modified: Wed, 11 Jun 2025 17:11:50 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc27a34a9f8e0c9e4a686b0f8ecd2ae06309b78b23320dbd848c7da20d182cc7`  
		Last Modified: Wed, 11 Jun 2025 17:11:52 GMT  
		Size: 20.0 KB (19992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eb2b653f1cd111db4fbc71c939d79ff560ad0257677bceecf25b8c595e00b70`  
		Last Modified: Wed, 11 Jun 2025 17:11:56 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa977e97319ef8dc78571a15a65eb92805bbdf504fda80afc033634f057048d`  
		Last Modified: Wed, 11 Jun 2025 22:44:14 GMT  
		Size: 28.1 MB (28067888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1389cd910de72f239562fb3a41ee927aa7694dd4fa8cfd630f5b0e71186a3c1e`  
		Last Modified: Wed, 11 Jun 2025 22:44:10 GMT  
		Size: 6.4 MB (6427752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e74e8e150ea1eb735d0f94bcd1d3d74cc5c634b7c50d28b072c50008ecc1a8`  
		Last Modified: Wed, 11 Jun 2025 21:28:34 GMT  
		Size: 63.4 KB (63377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3607bda03608c5b7bf42236a05bcefb3d04c9cbacf03b3de835dc7d4248a52fd`  
		Last Modified: Wed, 11 Jun 2025 21:28:39 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a58dd40506bd637677ca2e4443043b0e200a365054aa39536b6883a18442f0`  
		Last Modified: Wed, 11 Jun 2025 22:44:12 GMT  
		Size: 26.6 MB (26582514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0718b32f1e8c06262b73d89f67df6bf682e7ad1e50c39bab16f4a2d93e9330e3`  
		Last Modified: Wed, 11 Jun 2025 21:28:41 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89a6e634534c6637788a19cc9eb1f6e5a9281b67f2d552f6257c5d160cdc5af9`  
		Last Modified: Wed, 11 Jun 2025 21:28:48 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:4-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:7588f35962b0e0a1328b005cdf966d033d76d2fc29df7bb5a92ed1d185ddf99e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 KB (46812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dda6b68c7963f9b2f7e0fc0806ef138b8abaeea3642325a50b859a5e7271272c`

```dockerfile
```

-	Layers:
	-	`sha256:ba92db78480b750544d8cc7579f5f8be403030fcad7defccfe7ddc274730302b`  
		Last Modified: Wed, 11 Jun 2025 22:43:58 GMT  
		Size: 46.8 KB (46812 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:4-php8.2-fpm-alpine` - linux; s390x

```console
$ docker pull joomla@sha256:ab8f02e9c7d4a834655705fd4d5ca08b0c53e45e0adc5dcaad7bccdef770f160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.1 MB (95149801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ba5047655023905576526e8588f472dd74c290ea68c9452252c61b301e5782`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 09 Apr 2025 19:45:06 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
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
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_VERSION=8.2.28
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.28.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.28.tar.xz.asc
# Wed, 09 Apr 2025 19:45:06 GMT
ENV PHP_SHA256=af8c9153153a7f489153b7a74f2f29a5ee36f5cb2c6c6929c98411a577e89c91
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 09 Apr 2025 19:45:06 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
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
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78969cb3507a7e09a6a1541cd0fe9a6e6ba70522f240c985e34a594a5c5c2db`  
		Last Modified: Wed, 11 Jun 2025 06:32:49 GMT  
		Size: 3.7 MB (3698999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86831d5f3921b134159344ea1287339c8645e651a6ee0db4a544874087b848c3`  
		Last Modified: Wed, 11 Jun 2025 06:33:00 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bb672e9b170264102c0793a333d3f87a8a40a5f4ac69848957f71e5c752d123`  
		Last Modified: Wed, 11 Jun 2025 06:33:02 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e783b1d57cc1ad74a17a004d057e30ea7ab257956f95332223e8d9d242bf8e`  
		Last Modified: Wed, 11 Jun 2025 08:19:02 GMT  
		Size: 12.2 MB (12169291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bce6ce18a7483bdd6026b4bd3dfd5a8ee4c8af18c47e20b6ac49fd5f81fb47c`  
		Last Modified: Wed, 11 Jun 2025 06:37:55 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:febdb067cd9dffd70c60d97bc46facc5fc2a5e7961d7601cc0d5e7ae1c729d97`  
		Last Modified: Wed, 11 Jun 2025 08:19:22 GMT  
		Size: 13.0 MB (12978582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd8090f386cbe7b5b649c322780ef510558f5fd1b94efb0c069e0fe5400a03f2`  
		Last Modified: Wed, 11 Jun 2025 06:40:29 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf809347d98b90b43938854bc5b2eaaa3029ba3a45bda114323b710afc9520ed`  
		Last Modified: Wed, 11 Jun 2025 08:19:30 GMT  
		Size: 20.0 KB (19988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4310c4e587af3dbd8708125976b9035de1752e339009193ca49e10b858df403`  
		Last Modified: Wed, 11 Jun 2025 08:19:33 GMT  
		Size: 9.2 KB (9174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d63acacb507055af886516a15db4d158a2fcd9160f0f12f42f63fdaed4d0ec4`  
		Last Modified: Wed, 11 Jun 2025 11:53:20 GMT  
		Size: 29.3 MB (29250167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9bcba868752e8f0da96d2732984578fa6cdba811d121be718196e28d4ec98f`  
		Last Modified: Wed, 11 Jun 2025 11:53:18 GMT  
		Size: 6.7 MB (6720972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07ac269478839cbde39e585f2eb79e3a22b743aa069e3be39dc21b67bd6a7293`  
		Last Modified: Wed, 11 Jun 2025 11:53:17 GMT  
		Size: 63.4 KB (63362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7515d37e9ca32cc914b057f1cd889c2143bf55b2efe21519505681c5d303860a`  
		Last Modified: Wed, 11 Jun 2025 11:53:17 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451094747d4efc5debe8e6c8caeb2f410a205b95b4fe739d156abeacb6011cc0`  
		Last Modified: Wed, 11 Jun 2025 11:53:19 GMT  
		Size: 26.6 MB (26582497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25af6e8f066d68ad470fd0453c29ba560aa7355e8f8563cd631e09777bbecc50`  
		Last Modified: Wed, 11 Jun 2025 11:53:17 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72edc48f924fcdcb816715249192743d0d21d78c4ebd7003f8ca340834a1cb5a`  
		Last Modified: Wed, 11 Jun 2025 11:53:19 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:4-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:7c0cdcf39b99cee999cd9e60af908cf7ea258e576972baae183970ba367de03f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 KB (46766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883b2c8af1ca1e2b55a97575809d732f16bfa813cadaf3bdc3f2c14665bdb944`

```dockerfile
```

-	Layers:
	-	`sha256:cf6eaec8625613a73e6ea39e382d5364d5f0f082ff74fa9c24b80b4a80e2e690`  
		Last Modified: Wed, 11 Jun 2025 13:44:37 GMT  
		Size: 46.8 KB (46766 bytes)  
		MIME: application/vnd.in-toto+json
