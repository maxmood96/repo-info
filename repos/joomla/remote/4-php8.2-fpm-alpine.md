## `joomla:4-php8.2-fpm-alpine`

```console
$ docker pull joomla@sha256:06857aa3b9c2394632ef28855b7d17e71c479f5650e402d81eb56269a29d6f52
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
$ docker pull joomla@sha256:fb6a18d7dc261199f5c02472dda9fd64f138878ae2a8418a97a2342375f5fd4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92472400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad85dbfdf4a2d4546d9f970bc44a84ff1df38aea834b0d348842bbef1f920b55`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 16 Oct 2024 00:35:29 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 16 Oct 2024 00:35:29 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 16 Oct 2024 00:35:29 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_VERSION=8.2.26
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.26.tar.xz.asc
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_SHA256=54747400cb4874288ad41a785e6147e2ff546cceeeb55c23c00c771ac125c6ef
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 16 Oct 2024 00:35:29 GMT
WORKDIR /var/www/html
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Oct 2024 00:35:29 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 16 Oct 2024 00:35:29 GMT
CMD ["php-fpm"]
# Wed, 16 Oct 2024 00:35:29 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 16 Oct 2024 00:35:29 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
VOLUME [/var/www/html]
# Wed, 16 Oct 2024 00:35:29 GMT
ENV JOOMLA_VERSION=4.4.9
# Wed, 16 Oct 2024 00:35:29 GMT
ENV JOOMLA_SHA512=9ae442cff4f1cdb407d3beeda9258f2ab0e4a072eb8480f4804c7b83377cfc098a5b75e50ce7f34eadf41d85748f9b391cb0133a871a5c84be673a2dc0fef794
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.9/Joomla_4.4.9-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Oct 2024 00:35:29 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7231693c9fc92d8469b13bec5043b73f4ee1c29e2a4a72d15af93a61fd7323b5`  
		Last Modified: Wed, 11 Dec 2024 23:35:36 GMT  
		Size: 3.3 MB (3335078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adea0a37ec01acd4f78beb104975511fa18adcbd7e5e3ea0b22b6141501ee62`  
		Last Modified: Wed, 11 Dec 2024 23:35:36 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef563a2c247d9c4c35317d6d1f400451fa3de0f63ce71780b9b8f4e1ed7454c0`  
		Last Modified: Wed, 11 Dec 2024 23:35:36 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92908d18e994e247c5aeb529e13eca5478622d8a2e8e57f9888fb8a93869eba`  
		Last Modified: Wed, 11 Dec 2024 23:35:36 GMT  
		Size: 12.2 MB (12160425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915a493c5b754cda2fae535655ea856f6073f37dcee8c57f0c1eb72030fb5ef6`  
		Last Modified: Wed, 11 Dec 2024 23:35:37 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60fca2524d7e1755f43585e7ce1ffc1a50e1d181aaf0a86102ea205d335527d1`  
		Last Modified: Wed, 11 Dec 2024 23:35:39 GMT  
		Size: 13.0 MB (12967712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931b17db8a1a8add189b1c1773325874347f43ee9c0c7f5b8dbe12f372ed1acb`  
		Last Modified: Wed, 11 Dec 2024 23:35:37 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8c28138d0ace41897cb20f285b5ccb8beb48a0c8c39d3675725e2389676592`  
		Last Modified: Wed, 11 Dec 2024 23:35:37 GMT  
		Size: 20.1 KB (20064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f093a329bd9be92683bd9aa31cb54e732ee2135f75606a1041b998c77d08d45f`  
		Last Modified: Wed, 11 Dec 2024 23:35:38 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6c66710cd9e7cede3581f0411fcd59bc57fed15c2ca76f5ef3284b5d1017b9`  
		Last Modified: Thu, 12 Dec 2024 00:12:11 GMT  
		Size: 27.9 MB (27914210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919789b6a9fde45ab390d7e07a719793359eea4429f42abaf91850780a2abd62`  
		Last Modified: Thu, 12 Dec 2024 00:12:10 GMT  
		Size: 6.4 MB (6436141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c159a5fb3d3d4d1caffa1095f396f885604bf0be9d530d424332658232ec56e`  
		Last Modified: Thu, 12 Dec 2024 00:12:10 GMT  
		Size: 62.2 KB (62164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf09430869de8a5b25480fbd5f0ba1f15180495b4352e6a44109390b96d08dd0`  
		Last Modified: Thu, 12 Dec 2024 00:12:10 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e3a92713d857698053f0e3e71e85d5892351a7f7a9f99f3dbe2132d5ace85e4`  
		Last Modified: Thu, 12 Dec 2024 00:12:12 GMT  
		Size: 25.9 MB (25913742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1924a318d77c65e8c3c784cfb3b77a2d4c1a7481e60f915d79315c23f806f430`  
		Last Modified: Thu, 12 Dec 2024 00:12:11 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe02b2278f4220869bbc820fa61b154a12d5d980c6c22e8e27b47e90b6772e29`  
		Last Modified: Thu, 12 Dec 2024 00:12:11 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:4-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:26979026fb415eca35f6227d60685a8f6984199b6bf77ce7d431897e390da1ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 KB (46756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7905303fe4b8d4142a3986f938f98c23171564341f60227ef7aa00c1a3e36b1f`

```dockerfile
```

-	Layers:
	-	`sha256:8a209a2d26c98df5e867f715adfa2ebd49025d77def9fd32839cc7ae074ca6e5`  
		Last Modified: Thu, 12 Dec 2024 00:12:09 GMT  
		Size: 46.8 KB (46756 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:4-php8.2-fpm-alpine` - linux; arm variant v6

```console
$ docker pull joomla@sha256:8b53f1dda3b91b01e169e2c22d7df1614fa23bc5761d7d99f258e4ef40ef1fcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89515969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7300e48eb06c0af508418119d87a65d1eae1dfbab34f58a8db87096464600fa`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 16 Oct 2024 00:35:29 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 16 Oct 2024 00:35:29 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_VERSION=8.2.26
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.26.tar.xz.asc
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_SHA256=54747400cb4874288ad41a785e6147e2ff546cceeeb55c23c00c771ac125c6ef
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 16 Oct 2024 00:35:29 GMT
WORKDIR /var/www/html
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Oct 2024 00:35:29 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 16 Oct 2024 00:35:29 GMT
CMD ["php-fpm"]
# Wed, 16 Oct 2024 00:35:29 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 16 Oct 2024 00:35:29 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
VOLUME [/var/www/html]
# Wed, 16 Oct 2024 00:35:29 GMT
ENV JOOMLA_VERSION=4.4.9
# Wed, 16 Oct 2024 00:35:29 GMT
ENV JOOMLA_SHA512=9ae442cff4f1cdb407d3beeda9258f2ab0e4a072eb8480f4804c7b83377cfc098a5b75e50ce7f34eadf41d85748f9b391cb0133a871a5c84be673a2dc0fef794
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.9/Joomla_4.4.9-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Oct 2024 00:35:29 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cdae56950198dea1248e6f62d7e9ef311c976d55790449240dfa46ad43351f7`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 5.2 MB (5236002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773d98c98ade13dc692eaf9700be32a03220033d99905be410eda923ce054fb9`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ae964d3deb57dca49dadfc5c487d64a372e3df3db6ef51b58087c318beb33d`  
		Last Modified: Tue, 12 Nov 2024 02:51:00 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fed12445fce779f7609661a5ddfbd5013b730afe8c5437d7084bc7000661fe0e`  
		Last Modified: Thu, 21 Nov 2024 18:40:44 GMT  
		Size: 12.2 MB (12160106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:726a3601241799c2492d106e1c25d84d8a0a864d3b10aefc67e16497fe6fd8e2`  
		Last Modified: Thu, 21 Nov 2024 18:40:43 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc5f3b72e19e0850a1960cc8d78b2984bc09bbec324a83a416ae8d667e0f0879`  
		Last Modified: Thu, 21 Nov 2024 18:44:16 GMT  
		Size: 11.7 MB (11718721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe12d6c4a486847173423b020e0829f107902aafc0211fa4a53ced50de10cc4`  
		Last Modified: Thu, 21 Nov 2024 18:44:15 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d8bddd3723e8ab3c92d0d78c94bb962ec50246a058af21214364635a201074`  
		Last Modified: Thu, 21 Nov 2024 18:44:15 GMT  
		Size: 19.4 KB (19440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355f89cc0c29b0be1e863a2c1072e037e830d144edd3518f5e8fa9d11ffbff24`  
		Last Modified: Thu, 21 Nov 2024 18:44:15 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e50339df585e919c3de4fcfd40967681455bbffc6bee333da254c1ad40da3a2`  
		Last Modified: Thu, 21 Nov 2024 20:21:44 GMT  
		Size: 24.0 MB (23994289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a33dd2aa7081e1a2a30ef1d4e521d73d67899a65c66f857086e9b2e7a4bacc`  
		Last Modified: Thu, 21 Nov 2024 20:21:44 GMT  
		Size: 7.0 MB (7026983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fe881495f2418e7381dfa6e97edcf9dd9c044fc5ac62c548f55d4d3b049b69e`  
		Last Modified: Thu, 21 Nov 2024 20:21:43 GMT  
		Size: 61.6 KB (61650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3339bc62bcd4ed8c3bfa3f1b7af3f06e6ac31079dce3c7752297b2561399cf`  
		Last Modified: Thu, 21 Nov 2024 20:21:43 GMT  
		Size: 390.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b1783a13905676f394fd1fe23bda307178a03c7c37d35668b514943e8145ea`  
		Last Modified: Thu, 21 Nov 2024 20:21:45 GMT  
		Size: 25.9 MB (25913747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74cf202e8be467aaa38256da37f4fd8b4f0fbeb79ad27c79c168774bd8a80d5`  
		Last Modified: Thu, 21 Nov 2024 20:21:44 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d95bfb825a1b965004d07f218ff8a806cff4f5de50c38259f93cbd30c11519`  
		Last Modified: Thu, 21 Nov 2024 20:21:45 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:4-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:221009557ca593f4b05f7ecefde7bb0a169f29c23f04db397ebff810b276e14f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 KB (46877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f055743518004e76ead018b35fef322fdbd85eecdc666095067084f080b2b81`

```dockerfile
```

-	Layers:
	-	`sha256:f9d0e859e2487442c2fd50d5ad014dd827e03b5325ebfffc49f21553386ec303`  
		Last Modified: Thu, 21 Nov 2024 20:21:43 GMT  
		Size: 46.9 KB (46877 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:4-php8.2-fpm-alpine` - linux; arm variant v7

```console
$ docker pull joomla@sha256:f26c19f830b4f511c594524bb76d6bc9d37d32c4736b87b69c897a94330f5025
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.9 MB (86859804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e271561cda7c0a140d51c1ad521cc977ae775b3d2c9be4b95eff09aceedb4e2`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 16 Oct 2024 00:35:29 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 16 Oct 2024 00:35:29 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_VERSION=8.2.26
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.26.tar.xz.asc
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_SHA256=54747400cb4874288ad41a785e6147e2ff546cceeeb55c23c00c771ac125c6ef
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 16 Oct 2024 00:35:29 GMT
WORKDIR /var/www/html
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Oct 2024 00:35:29 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 16 Oct 2024 00:35:29 GMT
CMD ["php-fpm"]
# Wed, 16 Oct 2024 00:35:29 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 16 Oct 2024 00:35:29 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
VOLUME [/var/www/html]
# Wed, 16 Oct 2024 00:35:29 GMT
ENV JOOMLA_VERSION=4.4.9
# Wed, 16 Oct 2024 00:35:29 GMT
ENV JOOMLA_SHA512=9ae442cff4f1cdb407d3beeda9258f2ab0e4a072eb8480f4804c7b83377cfc098a5b75e50ce7f34eadf41d85748f9b391cb0133a871a5c84be673a2dc0fef794
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.9/Joomla_4.4.9-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Oct 2024 00:35:29 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2878563f55378e5cb0d2e6fc051acec0bad59706b4c55d991502e489d45f15b9`  
		Last Modified: Tue, 12 Nov 2024 03:55:38 GMT  
		Size: 4.9 MB (4894482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1da599409a1b1b855c6d69889b78470128711398dd127ceb61f803c590c9c39`  
		Last Modified: Tue, 12 Nov 2024 03:55:38 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fec221aedc472ddb77d24345957296ec946aab0b124953af99b1b103ca464d6`  
		Last Modified: Tue, 12 Nov 2024 03:55:37 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb21063f3233b9c4cbc161f73fb7191f6ec7e7b0657a1224361d57e24ff801a`  
		Last Modified: Thu, 21 Nov 2024 20:07:01 GMT  
		Size: 12.2 MB (12160109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ae63a63946e8af03ac9231adb4cb0a45fe0dc92ecaa44d33dcb9bf7d551de96`  
		Last Modified: Thu, 21 Nov 2024 20:07:00 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6cdfe7a1d4043fe144933e38dd2596b74fa2fa41e219acc2b52157ee7e8ab33`  
		Last Modified: Thu, 21 Nov 2024 20:11:28 GMT  
		Size: 11.0 MB (10982609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64427406f961284d2d676316b98dd88de69485e81b9075a2101560a975cc5ee`  
		Last Modified: Thu, 21 Nov 2024 20:11:27 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84fdcb08b6abe7b89bac68b1bf655025840f626e49a3a4aafcd82d95318bd256`  
		Last Modified: Thu, 21 Nov 2024 20:11:27 GMT  
		Size: 19.4 KB (19447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b6fbeea3265acf8a085fec659802943c35ebed6f911125775a52db88041290`  
		Last Modified: Thu, 21 Nov 2024 20:11:27 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a245c910af4916e2fbc75fc9cb48c7816b882f2dac37acc85a659d62b3a232fb`  
		Last Modified: Fri, 22 Nov 2024 00:03:34 GMT  
		Size: 22.8 MB (22782445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc03137af3df806a6a39d8dbde54f6b66f74910833127b0ba4dcd5acba6e1198`  
		Last Modified: Fri, 22 Nov 2024 00:03:33 GMT  
		Size: 6.9 MB (6931368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9378bb4ec420a8351cb27f9dbc7e289ce99bbbda7ce196e5b0d2410d8debb7eb`  
		Last Modified: Fri, 22 Nov 2024 00:03:33 GMT  
		Size: 61.7 KB (61672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d20fa98a0dd86d7ce9f52937504b52b966d52815a4c637ddea787b255cdf34`  
		Last Modified: Fri, 22 Nov 2024 00:03:33 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a81cf51ad4142797500c4596668b4294d417d5e6c15ad0301d8cb7d95663ad6`  
		Last Modified: Fri, 22 Nov 2024 00:03:35 GMT  
		Size: 25.9 MB (25913757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eab741f8ee9173f163dd439a19d8c8eae1553c536c7295f5ddf3fce61d191a0`  
		Last Modified: Fri, 22 Nov 2024 00:03:34 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420f6230421b8e20a00740b1c9a6cece0573a9f79c5a87e7ea42fff536304523`  
		Last Modified: Fri, 22 Nov 2024 00:03:34 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:4-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:ab4adc74b44340cb16c634da1e895ac7e38ac5e18b95bb8db70e4e70d035e37b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 KB (46876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f3af5b25449a25331cac3f1f252865fae2d9da432b4a13db2635aa89059e77d`

```dockerfile
```

-	Layers:
	-	`sha256:6e9591b908a8c4a37784629408724ae89ab58f7a5bb7cf81a88e61568200fa5a`  
		Last Modified: Fri, 22 Nov 2024 00:03:33 GMT  
		Size: 46.9 KB (46876 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:4-php8.2-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull joomla@sha256:81535580ac6d12a489ebc3de71c971891e752db0a6acad959907bfd30fb34abb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.6 MB (92593133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21739dde974773ab587fb55a180b874c7770f1d4551abd9b7b7661e40e8ac075`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 16 Oct 2024 00:35:29 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 16 Oct 2024 00:35:29 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 16 Oct 2024 00:35:29 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_VERSION=8.2.26
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.26.tar.xz.asc
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_SHA256=54747400cb4874288ad41a785e6147e2ff546cceeeb55c23c00c771ac125c6ef
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 16 Oct 2024 00:35:29 GMT
WORKDIR /var/www/html
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Oct 2024 00:35:29 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 16 Oct 2024 00:35:29 GMT
CMD ["php-fpm"]
# Wed, 16 Oct 2024 00:35:29 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 16 Oct 2024 00:35:29 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
VOLUME [/var/www/html]
# Wed, 16 Oct 2024 00:35:29 GMT
ENV JOOMLA_VERSION=4.4.9
# Wed, 16 Oct 2024 00:35:29 GMT
ENV JOOMLA_SHA512=9ae442cff4f1cdb407d3beeda9258f2ab0e4a072eb8480f4804c7b83377cfc098a5b75e50ce7f34eadf41d85748f9b391cb0133a871a5c84be673a2dc0fef794
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.9/Joomla_4.4.9-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Oct 2024 00:35:29 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02eb691f526c59a4feade4837dd3c26533d9fe4c9306da60dc23a30620af346`  
		Last Modified: Wed, 11 Dec 2024 23:34:10 GMT  
		Size: 3.3 MB (3331581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05f32f7c87db3a6447e39cf371cb0c2bb2c95f7a814793eff967d2a9a3b95122`  
		Last Modified: Wed, 11 Dec 2024 23:34:09 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7c12be75768edb813fc94e2e1d2c48d7cb1f4cea2c832026ca6ae796dff9ac`  
		Last Modified: Wed, 11 Dec 2024 23:34:09 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed5b44065f6e297c75173d3910ec2c38e2050d7fe649ab3f372733ccc21997d`  
		Last Modified: Thu, 12 Dec 2024 00:37:31 GMT  
		Size: 12.2 MB (12160432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd0d81a377f226e052c5d7d1bb25aa91521d1f7cc6963ee708006c167a218ee`  
		Last Modified: Thu, 12 Dec 2024 00:37:30 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f453b5647ed4e21482eeb723f70d24de0544e13f044b2fcf226eac14cca68d8`  
		Last Modified: Thu, 12 Dec 2024 00:42:01 GMT  
		Size: 13.0 MB (12968776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f31bc645a3590847510ee5e0f049773948c95e2e9fb6ef526ff103269da20cbc`  
		Last Modified: Thu, 12 Dec 2024 00:42:00 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad30d4134c2044a01cb39da86f7b4b24da4d9038abe55b8d12a24a03d1e8efe8`  
		Last Modified: Thu, 12 Dec 2024 00:42:01 GMT  
		Size: 19.9 KB (19892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc5ba0ee850f8f9cc92d325d49025a2365619fbe1622c9f2aa517b09be6308a`  
		Last Modified: Thu, 12 Dec 2024 00:42:01 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca657f8751e17adb1c055c4cc6a5d272ec6edbd8603d05a269485051b7bc683`  
		Last Modified: Thu, 12 Dec 2024 01:55:14 GMT  
		Size: 27.7 MB (27725139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef015bca4ae1e8a2ea03e3bd47b6c942df6d281f3ec27f18ca5463818139416`  
		Last Modified: Thu, 12 Dec 2024 01:55:14 GMT  
		Size: 6.4 MB (6399812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54401fbdfd6a66afea54da4b352b8f7e9db5b8062cec214b519110770a2a8a66`  
		Last Modified: Thu, 12 Dec 2024 01:55:13 GMT  
		Size: 62.1 KB (62141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3474914391b1ddb7e324b638e24fe723c33b267d819258edfc7734597ef738`  
		Last Modified: Thu, 12 Dec 2024 01:55:13 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fd2f2e03f7fc4a7cee4a667bb0235b73207343891af23001f65cc187419e87b`  
		Last Modified: Thu, 12 Dec 2024 01:55:15 GMT  
		Size: 25.9 MB (25913751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d995710ff69a94b09e0f73a56987e4f609555fce8b045a7ab3d7a1a77b9b788f`  
		Last Modified: Thu, 12 Dec 2024 01:55:14 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4293071a28ed5c218735d4bcf2ad2444112733cb4eb16545bbdbd05b9bb211ba`  
		Last Modified: Thu, 12 Dec 2024 01:55:15 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:4-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:22a12234544f65c2dcad2fbaa74e6738d1b7cda8b702c97b9d5eb0e4c7ca7668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 KB (46909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1b984acc7ce1064281d53c7e9d3742112066d0470129aca5ef4a9aabf366d09`

```dockerfile
```

-	Layers:
	-	`sha256:2feb158798067ea407c1dcfcb9f9e472c0021aa001c9f7e12e0634a3891343a6`  
		Last Modified: Thu, 12 Dec 2024 01:55:13 GMT  
		Size: 46.9 KB (46909 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:4-php8.2-fpm-alpine` - linux; 386

```console
$ docker pull joomla@sha256:79bb530056028f1e53664c30d5d6bdf74eabcc8ce96cfdc604cdc03f49cb94d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94882310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d91b519b81032130b369f166bcdc41fba55f55c4010d3a6be82d41ad197a5b6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 16 Oct 2024 00:35:29 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 16 Oct 2024 00:35:29 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_VERSION=8.2.26
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.26.tar.xz.asc
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_SHA256=54747400cb4874288ad41a785e6147e2ff546cceeeb55c23c00c771ac125c6ef
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 16 Oct 2024 00:35:29 GMT
WORKDIR /var/www/html
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Oct 2024 00:35:29 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 16 Oct 2024 00:35:29 GMT
CMD ["php-fpm"]
# Wed, 16 Oct 2024 00:35:29 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 16 Oct 2024 00:35:29 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
VOLUME [/var/www/html]
# Wed, 16 Oct 2024 00:35:29 GMT
ENV JOOMLA_VERSION=4.4.9
# Wed, 16 Oct 2024 00:35:29 GMT
ENV JOOMLA_SHA512=9ae442cff4f1cdb407d3beeda9258f2ab0e4a072eb8480f4804c7b83377cfc098a5b75e50ce7f34eadf41d85748f9b391cb0133a871a5c84be673a2dc0fef794
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.9/Joomla_4.4.9-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Oct 2024 00:35:29 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b02ed54ad69ac98c2f57cdd051e9114b4121c903f1b878113d2a3cee6753d2`  
		Last Modified: Thu, 21 Nov 2024 18:06:26 GMT  
		Size: 5.5 MB (5468316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017b303bf00f91130a3664570835b9be90b18be78dd08aadbf77aa4f565b8b7e`  
		Last Modified: Thu, 21 Nov 2024 18:06:26 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae6e2e934900463512281b001af0e2288d68068845ace0be5667683a4a7600d`  
		Last Modified: Thu, 21 Nov 2024 18:06:26 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:431d1e250b494339039af5a80033494e22e5abf5b2f8dc661ebe0e12f8f32ef9`  
		Last Modified: Thu, 21 Nov 2024 18:06:27 GMT  
		Size: 12.2 MB (12160104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5edd2c823cf24d31966d7ef8ce7bb0600e373ef0bb296202a0a4f1c9bcf44175`  
		Last Modified: Thu, 21 Nov 2024 18:06:26 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d37d78c5fbc589b28ee6c5d1e1b2c999382edce91a723f473770d670d032968`  
		Last Modified: Thu, 21 Nov 2024 18:06:27 GMT  
		Size: 13.2 MB (13223917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c3d9e3c434374c5c3f6572cc038f6a3ece1486f00dee913811fe46d46ef730`  
		Last Modified: Thu, 21 Nov 2024 18:06:27 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e2bd696385ddde6dac781089ec5fa58d5fd8b9fd97f73f953c0ef88cde5a08`  
		Last Modified: Thu, 21 Nov 2024 18:06:27 GMT  
		Size: 19.6 KB (19643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6089f7a0f97b8a50ae0ddd35e8a9e5d27a0ec33d08087152a6568bbc87336ac1`  
		Last Modified: Thu, 21 Nov 2024 18:06:28 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0fe0dfa6ed7a280ca914b9155ba71b6e8dcca89cfa05c60278d1ef3dcdb8ab3`  
		Last Modified: Thu, 21 Nov 2024 18:15:04 GMT  
		Size: 28.0 MB (28002383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e60521320a2582f1afee138afb243dec1d395ace0139b70ebd716dbd61fec2`  
		Last Modified: Thu, 21 Nov 2024 18:15:03 GMT  
		Size: 6.5 MB (6544925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d55c6198bd8e63b053b583f681a34514e7a1f5bc4d56fffe8967ff0626877f7`  
		Last Modified: Thu, 21 Nov 2024 18:15:03 GMT  
		Size: 61.6 KB (61639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42812f499afa66343a02494085d162c41409843279b0c903eb003cfd5f3c03b2`  
		Last Modified: Thu, 21 Nov 2024 18:15:03 GMT  
		Size: 386.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ef5b3c7b9a2509fd7daa8fa0b10d94448631d752c27d58bb01d6b1de918bff`  
		Last Modified: Thu, 21 Nov 2024 18:15:04 GMT  
		Size: 25.9 MB (25913748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e9ba9e612c467d4b0ef7e95b6a3c1e2511ef5c5974040751540f47e273869d`  
		Last Modified: Thu, 21 Nov 2024 18:15:04 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a791e4747d6799716594db690914693d2fc476f2cfc4646377ce9f516fbdd7`  
		Last Modified: Thu, 21 Nov 2024 18:15:04 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:4-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:0baf37e9ebef320c84f56fd3b4c214b8b76d3483cac3bbe91a30a8275f9e7987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 KB (46722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ff37eb64e40f34f4b79274124021106df790e008b128ab9df8d8e4024fdce49`

```dockerfile
```

-	Layers:
	-	`sha256:b67848b96bb42355f5fd26e59c9c2ac284eda5ec0aaeb384335934a9bd320582`  
		Last Modified: Thu, 21 Nov 2024 18:15:03 GMT  
		Size: 46.7 KB (46722 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:4-php8.2-fpm-alpine` - linux; ppc64le

```console
$ docker pull joomla@sha256:638e7d2f3d4ef76ef7f39098d89c5a3ab5c62c9c125bdd30f508761eda04b29f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.8 MB (93761333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcbba33e05929ed302f2c152b57f39696b9ad4add44c2a14971710bc9c4d1d50`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 16 Oct 2024 00:35:29 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 16 Oct 2024 00:35:29 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 16 Oct 2024 00:35:29 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_VERSION=8.2.26
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.26.tar.xz.asc
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_SHA256=54747400cb4874288ad41a785e6147e2ff546cceeeb55c23c00c771ac125c6ef
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 16 Oct 2024 00:35:29 GMT
WORKDIR /var/www/html
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Oct 2024 00:35:29 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 16 Oct 2024 00:35:29 GMT
CMD ["php-fpm"]
# Wed, 16 Oct 2024 00:35:29 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 16 Oct 2024 00:35:29 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
VOLUME [/var/www/html]
# Wed, 16 Oct 2024 00:35:29 GMT
ENV JOOMLA_VERSION=4.4.9
# Wed, 16 Oct 2024 00:35:29 GMT
ENV JOOMLA_SHA512=9ae442cff4f1cdb407d3beeda9258f2ab0e4a072eb8480f4804c7b83377cfc098a5b75e50ce7f34eadf41d85748f9b391cb0133a871a5c84be673a2dc0fef794
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.9/Joomla_4.4.9-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Oct 2024 00:35:29 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
		Last Modified: Thu, 05 Dec 2024 22:18:21 GMT  
		Size: 3.6 MB (3577108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62dab8c9093e7207bf34d7e27bcaf8a12d512bc9a6228a188ccd032ab556c048`  
		Last Modified: Wed, 11 Dec 2024 23:32:28 GMT  
		Size: 3.5 MB (3474267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6887eff0819f1e81cf0537030ec0eefbed710884b4bdcb74a53300dafe99af22`  
		Last Modified: Wed, 11 Dec 2024 23:32:28 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a40d10c33dd4ddf3d7039e24ae3ea2657811b8add42853a37557baa89339c584`  
		Last Modified: Wed, 11 Dec 2024 23:32:28 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5367085ac9608cfd996c39bb7adc28b2e7c20a16343b89e962fbbed2de5e574b`  
		Last Modified: Thu, 12 Dec 2024 00:21:34 GMT  
		Size: 12.2 MB (12160434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc676ea70f915f4899a80af1c9e4681d1f9a8ff6d54fda8b66eeac4f472df17`  
		Last Modified: Thu, 12 Dec 2024 00:21:34 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebf3211ea54b66cfb20d8ed96bf7cf6b99f9a1534d22592ff94591fefbf40db`  
		Last Modified: Thu, 12 Dec 2024 00:21:35 GMT  
		Size: 13.4 MB (13438423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d6a67fdb5a5c9671d4bff4aabe440754867264bfe12963d49d34d465445e6b`  
		Last Modified: Thu, 12 Dec 2024 00:21:34 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b4e2bfb92f5f44bd5860093fdea71e2259aed63213c5bb4ace2966a99e1b350`  
		Last Modified: Thu, 12 Dec 2024 00:21:35 GMT  
		Size: 19.9 KB (19876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:561c64ad5430307100f1e42e05efe8c5e51ebbd5d3786d7320837657fe0dfe14`  
		Last Modified: Thu, 12 Dec 2024 00:21:35 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d7d16febfde33a813dfb3de53a8f4864c91f1e77925083cfe61603b64d7f798`  
		Last Modified: Thu, 12 Dec 2024 01:59:35 GMT  
		Size: 28.5 MB (28547513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d270816f4baf3875bef11a758b2111db670771adb9d79f5a14e585a763759afa`  
		Last Modified: Thu, 12 Dec 2024 01:59:34 GMT  
		Size: 6.5 MB (6549412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc91da63eede6a6a51d5d413459a8e6ad8a03c99da460b34cad603876a01f10d`  
		Last Modified: Thu, 12 Dec 2024 01:59:34 GMT  
		Size: 62.1 KB (62122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ce781ce32b66a4d6b5820c488770f70a1b8bfcdd742ad028c32fb7970232e3`  
		Last Modified: Thu, 12 Dec 2024 01:59:34 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7300c985c2615a658e1d6c4a552f77c4c3795b1744772f35453c6c222ed9ee2e`  
		Last Modified: Thu, 12 Dec 2024 01:59:36 GMT  
		Size: 25.9 MB (25913751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1866541b569af1abcb8999224f8a69c509c136f6263f11547ba0652cbe28956`  
		Last Modified: Thu, 12 Dec 2024 01:59:35 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b6b5a6abdaba3cb1cc266ee1f66058f160ce0873036525f781a3154bd4d10f`  
		Last Modified: Thu, 12 Dec 2024 01:59:36 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:4-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:7de27bc58e9311121c51143b1144012bf491c4ec90eebfde0efd1408c52c1cfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 KB (46803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae970f880f5ccb8a5813d394cb8a7fb4e9da7e44bb238d945e30e8f5fe7990cb`

```dockerfile
```

-	Layers:
	-	`sha256:6c9372aaecad11c1d8a52a6f9cd234e5f244ef62a1a24f604e28608363a49327`  
		Last Modified: Thu, 12 Dec 2024 01:59:34 GMT  
		Size: 46.8 KB (46803 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:4-php8.2-fpm-alpine` - linux; riscv64

```console
$ docker pull joomla@sha256:c687721f9a1665da2bd4dfbe55800472be92894e01a69e1c07a1d5e5288f9df6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.7 MB (93744095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da288938574ae4cf9b88753f68f723817eaa1d7597604494fc75ea1682282ed3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 16 Oct 2024 00:35:29 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 16 Oct 2024 00:35:29 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_VERSION=8.2.26
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.26.tar.xz.asc
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_SHA256=54747400cb4874288ad41a785e6147e2ff546cceeeb55c23c00c771ac125c6ef
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 16 Oct 2024 00:35:29 GMT
WORKDIR /var/www/html
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Oct 2024 00:35:29 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 16 Oct 2024 00:35:29 GMT
CMD ["php-fpm"]
# Wed, 16 Oct 2024 00:35:29 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 16 Oct 2024 00:35:29 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
VOLUME [/var/www/html]
# Wed, 16 Oct 2024 00:35:29 GMT
ENV JOOMLA_VERSION=4.4.9
# Wed, 16 Oct 2024 00:35:29 GMT
ENV JOOMLA_SHA512=9ae442cff4f1cdb407d3beeda9258f2ab0e4a072eb8480f4804c7b83377cfc098a5b75e50ce7f34eadf41d85748f9b391cb0133a871a5c84be673a2dc0fef794
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.9/Joomla_4.4.9-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Oct 2024 00:35:29 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8ca85c9d20c6f76d0a8087ac3a4ddd6a1e40652d189dc8dad7ca6b0737c4b0`  
		Last Modified: Tue, 12 Nov 2024 06:14:49 GMT  
		Size: 5.4 MB (5382174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d2dfe107b4bddcc389bedcee9ca3fc81f02dc0799e313c21f307ddb454b4dc`  
		Last Modified: Tue, 12 Nov 2024 06:14:47 GMT  
		Size: 947.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df7310166e795cb48e721a885b92af688db981613ad6597943011293aca738c`  
		Last Modified: Tue, 12 Nov 2024 06:14:47 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00461ef25a8da9663dde52238b404adbe095c956efc7ac623b30400c2655143`  
		Last Modified: Thu, 21 Nov 2024 23:53:43 GMT  
		Size: 12.2 MB (12160118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ec3f05cf558307401a74ca7a4a86bf53af22a29fa8c331e3cd12951cb83715`  
		Last Modified: Thu, 21 Nov 2024 23:53:41 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a725ab8a7a468dd1d5a8a334a717f6d495bd106ed196403750cc24d84cd0a8`  
		Last Modified: Fri, 22 Nov 2024 00:37:37 GMT  
		Size: 12.7 MB (12719788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b25bb31da6bf0f478a0e4322f7653b278643d9ad51c0b36487b006ac50b5c8d`  
		Last Modified: Fri, 22 Nov 2024 00:37:35 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dff9d8f6c69067c90f019704e9d32c3737d19c4d8ce0dc2e36cc735c2ded007`  
		Last Modified: Fri, 22 Nov 2024 00:37:35 GMT  
		Size: 19.4 KB (19446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cc6d6d7ee9bb442383a47df3f3ccd11a7e4659c644b642219a26e054dea34c`  
		Last Modified: Fri, 22 Nov 2024 00:37:35 GMT  
		Size: 9.2 KB (9186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01526e5865b6143249973c19cd595a58a999eb69c6d4e327ca4d599bf92cfe5b`  
		Last Modified: Fri, 22 Nov 2024 08:25:46 GMT  
		Size: 27.8 MB (27824916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef955d97a7f9b875ee121e1f5452c5775f4a0c42848f387629c8ae06348ca34`  
		Last Modified: Fri, 22 Nov 2024 08:25:42 GMT  
		Size: 6.3 MB (6272311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e68c143748f9c3b6e6df85420a9a8f3d79b2891148b5e08849be31be1ad866`  
		Last Modified: Fri, 22 Nov 2024 08:25:41 GMT  
		Size: 61.6 KB (61645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572b6f25796948144dab15ea563649b03b95a223eb6d257cef77899092ce7914`  
		Last Modified: Fri, 22 Nov 2024 08:25:42 GMT  
		Size: 391.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d47098687254e72b1c4edbc3eb6303d7196ef4f865c0a13274e81ce551c6751`  
		Last Modified: Fri, 22 Nov 2024 08:25:47 GMT  
		Size: 25.9 MB (25913770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8696f6e5dea3e330f0e2c0042b5ab2f6c99314d768177c7e1fee4e8101b7248`  
		Last Modified: Fri, 22 Nov 2024 08:25:43 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f99aac3092c7e4af8a313fd2250dc9e9ecf52b1f6f501bc95c6de4dd1b5812a`  
		Last Modified: Fri, 22 Nov 2024 08:25:44 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:4-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:34066634fb49f23f75fd3cf9fe20f658d55e4992cd06342006e53ca16d5e5129
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 KB (46803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:533e9e8f2a58cc6c00f5a76bf07a6135d6886b54d91cfed35c536f2ed0dd8f1c`

```dockerfile
```

-	Layers:
	-	`sha256:b12060513f8c3f9cc17f00aba3b559f46f9fff6c92f780d44d179e102a2d94a7`  
		Last Modified: Fri, 22 Nov 2024 08:25:41 GMT  
		Size: 46.8 KB (46803 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:4-php8.2-fpm-alpine` - linux; s390x

```console
$ docker pull joomla@sha256:3f1b04cf1237b151b6e54708e347e2d365c66112b3852f35e81e966999cb35c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.6 MB (93572250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebbc29c3e50fc9d1afea10fbe938b218b50b8c7981221cd188ff1ca2f3188039`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 16 Oct 2024 00:35:29 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 16 Oct 2024 00:35:29 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 16 Oct 2024 00:35:29 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_VERSION=8.2.26
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.26.tar.xz.asc
# Wed, 16 Oct 2024 00:35:29 GMT
ENV PHP_SHA256=54747400cb4874288ad41a785e6147e2ff546cceeeb55c23c00c771ac125c6ef
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 16 Oct 2024 00:35:29 GMT
WORKDIR /var/www/html
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Oct 2024 00:35:29 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 16 Oct 2024 00:35:29 GMT
CMD ["php-fpm"]
# Wed, 16 Oct 2024 00:35:29 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Wed, 16 Oct 2024 00:35:29 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 	; # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	curl -fL -o imagick.tgz 'https://pecl.php.net/get/imagick-3.7.0.tgz'; 	echo '5a364354109029d224bcbb2e82e15b248be9b641227f45e63425c06531792d3e *imagick.tgz' | sha256sum -c -; 	tar --extract --directory /tmp --file imagick.tgz imagick-3.7.0; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php; 	test "$(grep -c '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php)" = '1'; 	sed -i -e 's!^//#endif$!#endif!' /tmp/imagick-3.7.0/Imagick.stub.php; 	grep '^//#endif$' /tmp/imagick-3.7.0/Imagick.stub.php && exit 1 || :; 	docker-php-ext-install /tmp/imagick-3.7.0; 	rm -rf imagick.tgz /tmp/imagick-3.7.0; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.23; 	pecl install memcached-3.2.0; 	pecl install redis-6.0.2; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
VOLUME [/var/www/html]
# Wed, 16 Oct 2024 00:35:29 GMT
ENV JOOMLA_VERSION=4.4.9
# Wed, 16 Oct 2024 00:35:29 GMT
ENV JOOMLA_SHA512=9ae442cff4f1cdb407d3beeda9258f2ab0e4a072eb8480f4804c7b83377cfc098a5b75e50ce7f34eadf41d85748f9b391cb0133a871a5c84be673a2dc0fef794
# Wed, 16 Oct 2024 00:35:29 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/4.4.9/Joomla_4.4.9-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
COPY makedb.php /makedb.php # buildkit
# Wed, 16 Oct 2024 00:35:29 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 16 Oct 2024 00:35:29 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ff43eb924acdd7a1002f16e7eb02fc41d4f0bae5329c5666d70c223b6e44f6a1`  
		Last Modified: Thu, 05 Dec 2024 22:19:55 GMT  
		Size: 3.5 MB (3469520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4b02d148e9caeb82d2cf6c286e6c9c576dbce389f6c2cb18910b789ebd4813`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 3.6 MB (3561751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d561dc5f913bf5ac5c30d9c4d42bdf7aa341b8fba0e0ded0354c6e1aca173438`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a465f443f2fadb2b0191af2eb2aae7a8ff4e66fef38973f7b9f36688fc1ff5cc`  
		Last Modified: Wed, 11 Dec 2024 23:32:40 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2674de720f25bb5b71d7f8774a771ac89e8ab99dea3639af9fadc4d1e14dddc7`  
		Last Modified: Thu, 12 Dec 2024 00:30:36 GMT  
		Size: 12.2 MB (12160438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9c043f8722fed85877c819d2496791d0286d909d938a3fdee44c1acd6275ba`  
		Last Modified: Thu, 12 Dec 2024 00:30:35 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c803f4ef265aef670fd6601d7134889b3fc80b59c865452fc4533f70a76d1aa0`  
		Last Modified: Thu, 12 Dec 2024 00:34:13 GMT  
		Size: 12.9 MB (12930313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc2fec91788a4e4d2f9c3375e62ace6119c1aae1080c9652499d938ea4596847`  
		Last Modified: Thu, 12 Dec 2024 00:34:13 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a9415870aed7f5ce4b985d52a9e0618013917620a911f6b424282c05aa8cca`  
		Last Modified: Thu, 12 Dec 2024 00:34:13 GMT  
		Size: 19.9 KB (19886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6314a372a9430338cde887b97392fd623cd6e42c89cc9779e87d225484f33b99`  
		Last Modified: Thu, 12 Dec 2024 00:34:13 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd96d279a340a044fbf88a214d2274aee600bda15befb12013fba4967d9d1963`  
		Last Modified: Thu, 12 Dec 2024 01:49:36 GMT  
		Size: 28.9 MB (28874044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c15c9b7639b4de85be7727d79fb091f6a66b2c3d4d30c304a968f342c6bcf21`  
		Last Modified: Thu, 12 Dec 2024 01:49:36 GMT  
		Size: 6.6 MB (6561957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4ce33ae956671952c25efe4fe5a594ce44e800486f2141d889535b65e17c63c`  
		Last Modified: Thu, 12 Dec 2024 01:49:35 GMT  
		Size: 62.2 KB (62166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00965d1fff6843643c6935d7ceb2b756cca944ef54d8a8f6086cb6df0554666e`  
		Last Modified: Thu, 12 Dec 2024 01:49:35 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f122d0d33e91b459fd01e0f8a0f31bea6d0d0277211332d89168048282c601a`  
		Last Modified: Thu, 12 Dec 2024 01:49:37 GMT  
		Size: 25.9 MB (25913749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0720deb5fbee7ec19152b87adfe4ee444c5e51b49658a14346deea18fb487cac`  
		Last Modified: Thu, 12 Dec 2024 01:49:36 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82662f2203058549152af1b82c910d9a238dc76ea264b63b99b3e77ce8d1375`  
		Last Modified: Thu, 12 Dec 2024 01:49:37 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:4-php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:cbb47af560097f5c486ad3f7ae725b4dec3dd36f317e4a3b5e9503b4175d50af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 KB (46756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be0e099930455b5341171bc8542ca609adbf6282a4f387cad13d7afbca7b8813`

```dockerfile
```

-	Layers:
	-	`sha256:ca0c28076da1bea804a5666da801f2fa46e0a605e93533d79e77f3ab34ad3a5e`  
		Last Modified: Thu, 12 Dec 2024 01:49:35 GMT  
		Size: 46.8 KB (46756 bytes)  
		MIME: application/vnd.in-toto+json
