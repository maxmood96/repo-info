## `joomla:6-php8.3-fpm-alpine`

```console
$ docker pull joomla@sha256:e9d61075cf07c1dbbadd86c8e5ebf248c3725ea5e487a5819cf5dbe9533728d6
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

### `joomla:6-php8.3-fpm-alpine` - linux; amd64

```console
$ docker pull joomla@sha256:ca2afbc1883308a6cb2957640bf49da41405c8563b55ba6b99ba6c552d3f6381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.8 MB (94837025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b16ca552b1c89e29e942dbdf6743b260ee19b314c9190ebb7675ec66855881d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 25 Sep 2025 23:53:24 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 25 Sep 2025 23:53:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Sep 2025 23:53:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_VERSION=8.3.26
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Sep 2025 23:53:24 GMT
WORKDIR /var/www/html
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Sep 2025 23:53:24 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 25 Sep 2025 23:53:24 GMT
CMD ["php-fpm"]
# Tue, 14 Oct 2025 17:16:27 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 		zstd 	; # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.24; 	pecl install memcached-3.3.0; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
VOLUME [/var/www/html]
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_VERSION=6.0.0
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_SHA512=ca19ea39f8cc1ef10b07abb84080d07f52e34d158522bf0b625948c4a077504cacdbe70e8eea80a3df381f21889a8f62367a9d8def861fa43d671f72b8daa73e
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/6.0.0/Joomla_6.0.0-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Oct 2025 17:16:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2f8e296f161a6df6f9e38f530b29164527358ae5a835ec9540902834c703b1`  
		Last Modified: Wed, 08 Oct 2025 22:43:17 GMT  
		Size: 3.5 MB (3463764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a14574d9b443903c59a6beaf7e1bcf42b816683f83bfa06b936dbedd14d72a`  
		Last Modified: Wed, 08 Oct 2025 22:43:17 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a5ec08747e2aa91406eff3773626f48070eaa9c93fed1ba8f3d7a612080daa`  
		Last Modified: Wed, 08 Oct 2025 22:43:17 GMT  
		Size: 214.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5014952dfec7269bd4bcc1ecd2d914b8ebce366dbd6671f3b785e004e38506af`  
		Last Modified: Wed, 08 Oct 2025 23:34:20 GMT  
		Size: 12.6 MB (12602021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10fcbbc3acfaa8ce094f6a16e827c849fb2ff561b8368b8fa6c20cd3c8d9ff38`  
		Last Modified: Wed, 08 Oct 2025 23:34:19 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fdcc22455b7b86b0da8d662df6b112a742153089b8f6c79f362a42da058012b`  
		Last Modified: Wed, 08 Oct 2025 23:34:20 GMT  
		Size: 13.3 MB (13268688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0059c8b22e0b11b909968e1478e106cea87bbe8ec16bda3d5f3604031943c9b`  
		Last Modified: Wed, 08 Oct 2025 23:34:17 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a805f6317d497be1dbfa5830b80465b47ce8f844972c20bd26b7e11cfaa9aa`  
		Last Modified: Wed, 08 Oct 2025 23:34:18 GMT  
		Size: 20.1 KB (20080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b3e1b68ffd778b41e5e1e0b9d9932bf64172edec92afd4b12f356bf61cf552`  
		Last Modified: Wed, 08 Oct 2025 23:34:17 GMT  
		Size: 20.1 KB (20074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fadf64aca9df3665d652dbdd29b5dc8ce9b4223a32bf52c862dae8ab9d5f0a`  
		Last Modified: Wed, 08 Oct 2025 23:34:17 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0069ec6ff5df67366ad39340212747a9a840152c69241d9ddd15c0e58cb92c8d`  
		Last Modified: Tue, 14 Oct 2025 17:57:51 GMT  
		Size: 28.4 MB (28419911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1945893df1d8eb52b248dadf4cd967d099b84ea8f157439d413862c2020559ad`  
		Last Modified: Tue, 14 Oct 2025 17:57:49 GMT  
		Size: 7.2 MB (7199952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06402e3ac6d6d484829d67a62beca2250150cf4354ac1c44154fa0f9370b46eb`  
		Last Modified: Tue, 14 Oct 2025 17:57:48 GMT  
		Size: 63.5 KB (63531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b3ecaadcb726484e98f5bc501ab97a89564ebbdb145584de03a8ee97b4d651`  
		Last Modified: Tue, 14 Oct 2025 17:57:49 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:012ca6e495cb5e5c1083f6246453d659b45c6441471a5df2ea9e7c96cc1a7a34`  
		Last Modified: Tue, 14 Oct 2025 17:57:52 GMT  
		Size: 26.0 MB (25958139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:415615ef25c716b70efd5240166bc7b4353509c586790ad135aba123bd909a6d`  
		Last Modified: Tue, 14 Oct 2025 17:57:48 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a260036fc7b50648b73f4fa52cfe12174fa2e49011f454d6fed1f15044f4d83`  
		Last Modified: Tue, 14 Oct 2025 17:57:48 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:6-php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:32424c38bc497dde6007241c267c3a31ed1eb84966ea4789495f5768de19162a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 KB (46078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bf91c16b87c1cfdd31a062d4ccaa8699ba521bd68c5122b751ca1c0ea374e08`

```dockerfile
```

-	Layers:
	-	`sha256:94e45c809c148282f5d72dcbdf2f8fc6547e67151fe9e994b4ca8f693c1f498c`  
		Last Modified: Tue, 14 Oct 2025 19:49:46 GMT  
		Size: 46.1 KB (46078 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:6-php8.3-fpm-alpine` - linux; arm variant v6

```console
$ docker pull joomla@sha256:803646c338bdc7a6f6cbf3dd2c9861f38db98990bf12a50e68b41f006a2326c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.9 MB (89911680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:039497c512510174c8ba01b4050319b63c505efc865fa0fa02a5e7b4282bcce8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 25 Sep 2025 23:53:24 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 25 Sep 2025 23:53:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Sep 2025 23:53:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_VERSION=8.3.26
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Sep 2025 23:53:24 GMT
WORKDIR /var/www/html
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Sep 2025 23:53:24 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 25 Sep 2025 23:53:24 GMT
CMD ["php-fpm"]
# Tue, 14 Oct 2025 17:16:27 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 		zstd 	; # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.24; 	pecl install memcached-3.3.0; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
VOLUME [/var/www/html]
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_VERSION=6.0.0
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_SHA512=ca19ea39f8cc1ef10b07abb84080d07f52e34d158522bf0b625948c4a077504cacdbe70e8eea80a3df381f21889a8f62367a9d8def861fa43d671f72b8daa73e
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/6.0.0/Joomla_6.0.0-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Oct 2025 17:16:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Wed, 08 Oct 2025 21:00:16 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3cdcb39afd821d13b22ca21c865ff19e58569c683f9e18b9a0ceb95c92b680`  
		Last Modified: Wed, 08 Oct 2025 21:46:05 GMT  
		Size: 3.4 MB (3428334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b8740db6975c9b8c5220191ade53612421b7da5301d9f3f7da94286205eb5ec`  
		Last Modified: Wed, 08 Oct 2025 21:46:04 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc4035a2fd0c27d5270cc96e2d8cfb3e6e50f6a5677241510df3134795ece31`  
		Last Modified: Wed, 08 Oct 2025 21:46:04 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9643c46440d442a3ea77f7680b646ca563c09924e3893a139f0fae39b0fe17b2`  
		Last Modified: Wed, 08 Oct 2025 21:52:36 GMT  
		Size: 12.6 MB (12602017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343fd232e2ed6ec2be8585a876afb24be002ab0ca52eaaffe0602b53ec99008a`  
		Last Modified: Wed, 08 Oct 2025 21:52:34 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7ebc2b7684c32e73e8386b551f89d6b67b81d3ea7bba27fdefd855628b0525`  
		Last Modified: Wed, 08 Oct 2025 21:52:35 GMT  
		Size: 12.0 MB (11983688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f744d5bcb115c5143f8a956a038bd848a40c6c1cba3a35da7cc19e2df4f1e9`  
		Last Modified: Wed, 08 Oct 2025 21:52:34 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b77520ca9455202004fbf3faf0048cd387a9893e8ec1d93699b3b2c83c6b93f`  
		Last Modified: Wed, 08 Oct 2025 21:52:34 GMT  
		Size: 19.9 KB (19866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf4961f2b4ef141575ff94a1fe99d95871bd0975125a7075a4e23109130d18e`  
		Last Modified: Wed, 08 Oct 2025 21:52:34 GMT  
		Size: 19.9 KB (19863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5c84b4f3a4d7577bc1b755f1ebdbecf63cf09fc3dc54d97d3e2803e4a736af`  
		Last Modified: Wed, 08 Oct 2025 21:52:34 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af87acc51b9ea129ee676d524503fe5c6d260742c22967412fedcc2f56504684`  
		Last Modified: Tue, 14 Oct 2025 17:58:53 GMT  
		Size: 25.4 MB (25423037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0356460db005aa9bf89078f4ead1e50b865120934a0c356c3a53d8c21bb3428e`  
		Last Modified: Tue, 14 Oct 2025 17:58:51 GMT  
		Size: 6.9 MB (6890746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2169d329aae93cac684dc6094bb220e2d07dcd01c66096c604666a0a570adc95`  
		Last Modified: Tue, 14 Oct 2025 17:58:49 GMT  
		Size: 63.5 KB (63510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a9c0a7d7c5bf261a4880d257e66b0445e5fd950c45f799d17ef05feab74e5a`  
		Last Modified: Tue, 14 Oct 2025 17:58:49 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad73973b9b799e0889fcb2f6818314e3bb44dc45a20641cb6e31cc7dd93d75f`  
		Last Modified: Tue, 14 Oct 2025 17:58:55 GMT  
		Size: 26.0 MB (25958121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddab1cdb513640604343238d35a4069eb0a9ded2caf6e4df970176e31c3deac`  
		Last Modified: Tue, 14 Oct 2025 17:58:50 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d4538ea3bb06089e48cfe5429cb48f5f5276ba4157672cadb92c54c2ea6719`  
		Last Modified: Tue, 14 Oct 2025 17:58:56 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:6-php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:19ea58d6a5d9a435f3bd596b3f37cbd8287b104315e6562284e580fb547cee5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 KB (46210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3b491005284d3f8f237e7110825e9763cf9ba9c9cc2d92bf9cf033cf5a08ff2`

```dockerfile
```

-	Layers:
	-	`sha256:3ef2a734f51e375e6882cd89c15dc2e5693315584aa735e6abff8da5c9584559`  
		Last Modified: Tue, 14 Oct 2025 19:49:50 GMT  
		Size: 46.2 KB (46210 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:6-php8.3-fpm-alpine` - linux; arm variant v7

```console
$ docker pull joomla@sha256:c6e3d0b3b6798c59a3019b10564a06a0df999f3bccece959d315f9c76a740d3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.4 MB (87448817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7791fff78e17b632f703f1a6caadd354c0347d6dae5a1626481578fc26ea3e62`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 25 Sep 2025 23:53:24 GMT
ADD alpine-minirootfs-3.22.2-armv7.tar.gz / # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 25 Sep 2025 23:53:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Sep 2025 23:53:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_VERSION=8.3.26
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Sep 2025 23:53:24 GMT
WORKDIR /var/www/html
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Sep 2025 23:53:24 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 25 Sep 2025 23:53:24 GMT
CMD ["php-fpm"]
# Tue, 14 Oct 2025 17:16:27 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 		zstd 	; # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.24; 	pecl install memcached-3.3.0; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
VOLUME [/var/www/html]
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_VERSION=6.0.0
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_SHA512=ca19ea39f8cc1ef10b07abb84080d07f52e34d158522bf0b625948c4a077504cacdbe70e8eea80a3df381f21889a8f62367a9d8def861fa43d671f72b8daa73e
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/6.0.0/Joomla_6.0.0-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Oct 2025 17:16:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2763c7fc79b66030222442365f4a0f69d9dbaa11f7fd47a918d29d732d52996c`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.2 MB (3221555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3cd31953efba831f10d0cb18b5b3ad75edf03f314e7bbe38c1aca633e797fb`  
		Last Modified: Wed, 08 Oct 2025 21:53:31 GMT  
		Size: 3.2 MB (3244402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076b71c74c2ecafb3a798b10fd0c6397ad7786a6849c4856db6dd514a2c975c4`  
		Last Modified: Wed, 08 Oct 2025 21:53:31 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c7f53a180a3a248d39673c498c7ab85a1a6d5183694c33d3038f736b071339`  
		Last Modified: Wed, 08 Oct 2025 21:53:31 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3ae452ce63af9658d481ffccc2ad1c744f0e444c5aba07d691b2bdbb9dce03`  
		Last Modified: Wed, 08 Oct 2025 21:53:32 GMT  
		Size: 12.6 MB (12602014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaafbcc1dbfaa222ffc2a08f1c645d03c40816a9ad7154fe580dc4f88638f2d3`  
		Last Modified: Wed, 08 Oct 2025 21:53:31 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469404dd41d3961db5905a469aba22f0ca5a2b50cc4ef6f27a787fd8969b7299`  
		Last Modified: Wed, 08 Oct 2025 21:53:31 GMT  
		Size: 11.3 MB (11290087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a611eba00f6c7e0ca133eac77c4d2469a32de3c937f62d6604ff7616b2fd03b8`  
		Last Modified: Wed, 08 Oct 2025 21:53:31 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4946eff1c882514c3fb48260ba445a5ea3166606dd48c64255490e71b4da599`  
		Last Modified: Wed, 08 Oct 2025 21:53:30 GMT  
		Size: 19.9 KB (19854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800d7396291b673444e3f1ca3abee6e42f50100bbafedb89359d1bbe624fe1ef`  
		Last Modified: Wed, 08 Oct 2025 21:53:31 GMT  
		Size: 19.8 KB (19847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9da2b8b4bf4b148499be92fb2365fb19dd97a47810a0c299a0d23f148cf37b`  
		Last Modified: Wed, 08 Oct 2025 21:53:31 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce38a8e6411033372d58e3e2cdb4c03da0f258ebb6e54876124e94e629473490`  
		Last Modified: Tue, 14 Oct 2025 17:57:17 GMT  
		Size: 24.1 MB (24133138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa4adbaa998bdcb7845ccea03fe8aed53fa6af3eddb8981e545e9631b671184`  
		Last Modified: Tue, 14 Oct 2025 17:57:13 GMT  
		Size: 6.9 MB (6877921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01712bd622e3d98cbfc17cc5aaf8c858e22173447823bd4d283c887e2647c66d`  
		Last Modified: Tue, 14 Oct 2025 17:57:13 GMT  
		Size: 63.5 KB (63462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9d52fce7ed7c3015c5c763d7631d090c9a95d799cdf96bb3c0cc48ceeab43e`  
		Last Modified: Tue, 14 Oct 2025 17:57:13 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26943f09f657cb8ba084ef7d22076ff5facece8d7e299b99d3df19e682879c02`  
		Last Modified: Tue, 14 Oct 2025 17:57:17 GMT  
		Size: 26.0 MB (25958122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255d712e4627daa622aac44f6c4f4ef517169f882179d4fbc2594118918dd1aa`  
		Last Modified: Tue, 14 Oct 2025 17:57:13 GMT  
		Size: 3.7 KB (3655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d529cade551389f195115109d4b70be9894c77b8284b1f2f1de5055f1cf74bd`  
		Last Modified: Tue, 14 Oct 2025 17:57:13 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:6-php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:c9f9e42aa1515e362b336a1d02f19d8e3c4cf130c4784e1f93902f19e2f8799a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 KB (46210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:452a4802c0a34737018af93676d192cdbb77a38a3d4e082f0a45f47366d2e52f`

```dockerfile
```

-	Layers:
	-	`sha256:ebe811989d24da35fe9c85f11d3cff968280163a36b6e4cf69c479c917cdb41e`  
		Last Modified: Tue, 14 Oct 2025 19:49:53 GMT  
		Size: 46.2 KB (46210 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:6-php8.3-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull joomla@sha256:19d8a15948aac0ab559feea4c8fd258c81e217cf2fd0e4b781f8dd8b726392e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.9 MB (94917203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed0b50f7f974b866110442386e5a1fb6b915b105c325e35a8e724a69b7b2ef61`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 25 Sep 2025 23:53:24 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 25 Sep 2025 23:53:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Sep 2025 23:53:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_VERSION=8.3.26
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Sep 2025 23:53:24 GMT
WORKDIR /var/www/html
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Sep 2025 23:53:24 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 25 Sep 2025 23:53:24 GMT
CMD ["php-fpm"]
# Tue, 14 Oct 2025 17:16:27 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 		zstd 	; # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.24; 	pecl install memcached-3.3.0; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
VOLUME [/var/www/html]
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_VERSION=6.0.0
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_SHA512=ca19ea39f8cc1ef10b07abb84080d07f52e34d158522bf0b625948c4a077504cacdbe70e8eea80a3df381f21889a8f62367a9d8def861fa43d671f72b8daa73e
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/6.0.0/Joomla_6.0.0-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Oct 2025 17:16:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa3e41c2bec91c6a90481f49cd9f7a03a7d1dbd5d60ce7c5743431e60b7d710`  
		Last Modified: Wed, 08 Oct 2025 21:38:06 GMT  
		Size: 3.5 MB (3466806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b621ccd53774b77e761ded3f6cfa38a6c70de2968d763a229a32620219f1de9`  
		Last Modified: Wed, 08 Oct 2025 21:38:05 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9695a5b19f8045abdfdfdba80a7cb2d67c597ce00657b1b8914af7122d3ff6f`  
		Last Modified: Wed, 08 Oct 2025 21:38:06 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebb674d348d7bbc3a447314380a4eb2158b7cd2e4f9bbed10e0b9ce37af4e83`  
		Last Modified: Wed, 08 Oct 2025 21:38:08 GMT  
		Size: 12.6 MB (12602011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:736ac14f3ae9d84197d99b5d9ded705973d83185f0d582651f07ae3bd6dbe5ff`  
		Last Modified: Wed, 08 Oct 2025 21:38:06 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf54de2111690e343d01da97a959c419582524f4f27a6284397fc4a5f59dcb59`  
		Last Modified: Wed, 08 Oct 2025 21:38:07 GMT  
		Size: 13.3 MB (13252360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a18f9f6d12709e6de4dd76cdb1d4becef27de271aa590b300b3bbff216238a`  
		Last Modified: Wed, 08 Oct 2025 21:38:06 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ed75515c438605782fbe38189fc3ae4dc33c1571cc0e21a0037a8d15eb5661`  
		Last Modified: Wed, 08 Oct 2025 21:38:06 GMT  
		Size: 19.9 KB (19864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dd0980473342d6525da82928bbf700163f81885d0f9f1cf04017cc39fffc376`  
		Last Modified: Wed, 08 Oct 2025 21:38:06 GMT  
		Size: 19.9 KB (19852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50cbe33dd0bd206a9b0e87239de20bf7735c0fe353b7765455c3a606f2323ed1`  
		Last Modified: Wed, 08 Oct 2025 21:38:06 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4470a36f859d9dfa25d9d31a017e703a74447c458caab6975f58cef15d58203`  
		Last Modified: Tue, 14 Oct 2025 18:00:20 GMT  
		Size: 28.2 MB (28235272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48434019efca82e81b8ac62e963511dbf976ac2cd3822b0c8889a9eb0ba5f896`  
		Last Modified: Tue, 14 Oct 2025 18:00:18 GMT  
		Size: 7.1 MB (7142944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b189913be641793ea9cf65239597cf300deea038f68f42f42ddb75c18f577ae5`  
		Last Modified: Tue, 14 Oct 2025 18:00:17 GMT  
		Size: 63.5 KB (63498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca7f81268ef443b7e56df93062e4676b6c6724f1632b6d227d3d9d3193ffe2f`  
		Last Modified: Tue, 14 Oct 2025 18:00:17 GMT  
		Size: 388.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8ad180a59036311f52c25dd08a2ed0bfb072feed6bdc0b67cc8f662c7b13a4`  
		Last Modified: Tue, 14 Oct 2025 18:00:21 GMT  
		Size: 26.0 MB (25958118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11329d0752900eb02bbcd5ca7137497e09c1edfe49fc06937a75ee4ece44dc8e`  
		Last Modified: Tue, 14 Oct 2025 18:00:17 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1738a0b27a73f2420f30cf2f2f07f479cbc32b7fb8b8de118fa496db688f696`  
		Last Modified: Tue, 14 Oct 2025 18:00:17 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:6-php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:a47dc89587c448935301ee383f82173a295ebe1779334232d759c453f01cdcab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 KB (46242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b467f1528f899b8f94e589d4d61c2d2377cf66f9965434aa16a1ca874fe46e`

```dockerfile
```

-	Layers:
	-	`sha256:e03ed59f91d88e2de8b601cfc6bedddbdbaff180e3144dcd4a2308f2ccf0bfdd`  
		Last Modified: Tue, 14 Oct 2025 19:49:56 GMT  
		Size: 46.2 KB (46242 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:6-php8.3-fpm-alpine` - linux; 386

```console
$ docker pull joomla@sha256:afd7e7fb1f2674214d9291b73aff09e469149b618284e7372e91f9f692b583af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.3 MB (95342982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa460651ce9828dcfa0e01e7720d0620fdf2c543ef730dd437ab4bac5748251`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 25 Sep 2025 23:53:24 GMT
ADD alpine-minirootfs-3.22.2-x86.tar.gz / # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 25 Sep 2025 23:53:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Sep 2025 23:53:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_VERSION=8.3.26
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Sep 2025 23:53:24 GMT
WORKDIR /var/www/html
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Sep 2025 23:53:24 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 25 Sep 2025 23:53:24 GMT
CMD ["php-fpm"]
# Tue, 14 Oct 2025 17:16:27 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 		zstd 	; # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.24; 	pecl install memcached-3.3.0; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
VOLUME [/var/www/html]
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_VERSION=6.0.0
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_SHA512=ca19ea39f8cc1ef10b07abb84080d07f52e34d158522bf0b625948c4a077504cacdbe70e8eea80a3df381f21889a8f62367a9d8def861fa43d671f72b8daa73e
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/6.0.0/Joomla_6.0.0-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Oct 2025 17:16:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:13c6e95c06ae06f126f5e940d6d88c2fec0da715c80878ad225c76ad48d0a31e`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.6 MB (3618931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc44e12fbc69b1f156d8436eec520233e385936119e6e0a134082ff123e16b8`  
		Last Modified: Wed, 08 Oct 2025 21:29:27 GMT  
		Size: 3.5 MB (3522953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07d58ed34924355103745542522524dcc6e0fbe84c3aeb4514d964f5f13593de`  
		Last Modified: Wed, 08 Oct 2025 21:29:28 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834a1d273fe98862d2876a4b50f8329c53bc213ac93598ead0a75cdeb2e0141f`  
		Last Modified: Wed, 08 Oct 2025 21:29:27 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a2c0e8a295ce017176da8f2dd0b22b2e9ad62dbade4a4899661a219fc0fb8f7`  
		Last Modified: Wed, 08 Oct 2025 22:18:01 GMT  
		Size: 12.6 MB (12601992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2ebff2d2e144484dbc07c92fda4ab6b679d071f3bb77c3d0efd1b8064c5bb24`  
		Last Modified: Wed, 08 Oct 2025 22:17:59 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d028b32894ac2aab87c098c7e23a0f05f3e95aec43114ccf54a21aa366535d8a`  
		Last Modified: Wed, 08 Oct 2025 22:18:01 GMT  
		Size: 13.6 MB (13577998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10aec0f569c9e4902cbf9d66e166dcbbbfe6b61419999b211d219048a93e2c4`  
		Last Modified: Wed, 08 Oct 2025 22:17:57 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5db0495d5a7730774dcb84ad77c626fb2287541938cc40337778b70420e1aef`  
		Last Modified: Wed, 08 Oct 2025 22:17:57 GMT  
		Size: 20.1 KB (20053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aedb159c872f256a2a413e338389f972e446f639c2f297b2ae2d6b0fa13c630`  
		Last Modified: Wed, 08 Oct 2025 22:17:58 GMT  
		Size: 20.0 KB (20047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e55aa185dcebdee08ebd308c270df822db903158cf3dfedb10187179fd12f7f`  
		Last Modified: Wed, 08 Oct 2025 22:17:57 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c2d03c82f173f17e8add1332a5f5a4a9f0589692d4d39158cb10419c155e1b8`  
		Last Modified: Tue, 14 Oct 2025 17:57:19 GMT  
		Size: 28.6 MB (28635069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720530d86afd8f52d2edb5b6db6732bc564818c5e5aedf5fff65dc1c637afb80`  
		Last Modified: Tue, 14 Oct 2025 17:57:13 GMT  
		Size: 7.3 MB (7305941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e51dc92cf1617f5789339c250ee282baa763bdad0962f03ff1469c3e4e302c`  
		Last Modified: Tue, 14 Oct 2025 17:57:12 GMT  
		Size: 63.5 KB (63467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cf15c5cfcf50f45cdf4dcaacc6a262ff72ebe5efa01c9fe10626ce4620cd64a`  
		Last Modified: Tue, 14 Oct 2025 17:57:11 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cfdd0a8b479b64dda24459b7839937735772e61ddbc493a98f9e00aba3ac476`  
		Last Modified: Tue, 14 Oct 2025 17:57:13 GMT  
		Size: 26.0 MB (25958124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3dd804d558bb109c216d94051d2ed753d7cbf69522914ef91577d9f1ed15d52`  
		Last Modified: Tue, 14 Oct 2025 17:57:12 GMT  
		Size: 3.7 KB (3654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c8819e855f0d756d3b9db351e5e500318829ac3458a4188d65bc38f67153d6`  
		Last Modified: Tue, 14 Oct 2025 17:57:12 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:6-php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:d6fb5f07e78f79c92a3a6bc2db51cd2d50b346e955b964aa3ea66e656ab66b99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 KB (46038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e65a616c953198f4aee7489ab9d4a8392263b607991c4b44cf42e7a895f5061`

```dockerfile
```

-	Layers:
	-	`sha256:ad6ea5299a9965e03bf1fdade118e75bb9b63cfc050e133eb345e23d30fada21`  
		Last Modified: Tue, 14 Oct 2025 19:49:59 GMT  
		Size: 46.0 KB (46038 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:6-php8.3-fpm-alpine` - linux; ppc64le

```console
$ docker pull joomla@sha256:591239a3e68ec8cb46baf140551fb597d26e7e17bea8450ad5c774c532ca6352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.1 MB (96129092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf1c9c8db10dacfcbed532f6e50e8a6f2aa3e02276fcd874a9b9014bb90229b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 25 Sep 2025 23:53:24 GMT
ADD alpine-minirootfs-3.22.2-ppc64le.tar.gz / # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 25 Sep 2025 23:53:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Sep 2025 23:53:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_VERSION=8.3.26
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Sep 2025 23:53:24 GMT
WORKDIR /var/www/html
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Sep 2025 23:53:24 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 25 Sep 2025 23:53:24 GMT
CMD ["php-fpm"]
# Tue, 14 Oct 2025 17:16:27 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 		zstd 	; # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.24; 	pecl install memcached-3.3.0; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
VOLUME [/var/www/html]
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_VERSION=6.0.0
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_SHA512=ca19ea39f8cc1ef10b07abb84080d07f52e34d158522bf0b625948c4a077504cacdbe70e8eea80a3df381f21889a8f62367a9d8def861fa43d671f72b8daa73e
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/6.0.0/Joomla_6.0.0-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Oct 2025 17:16:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:85a0f69f026b4a01420490809bed190217e05518f7b718c0bbc1ad4871e0dedf`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.7 MB (3732241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95a0b03903475651b081c7c705a4ab0f68ab5f5bba328735e8dae6e168526c7`  
		Last Modified: Thu, 09 Oct 2025 00:56:03 GMT  
		Size: 3.6 MB (3614664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436cae3ea479232d2bcf67ca55e6705ab3775fa412e53331855937a2a7340b65`  
		Last Modified: Thu, 09 Oct 2025 00:56:03 GMT  
		Size: 937.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1164e359044b0e56f99538c30031735fcef9128820673f06e10663118d04d0e3`  
		Last Modified: Thu, 09 Oct 2025 00:56:03 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0b42d58e391ad0f1f5d13bfd2403af675d228d3b129185fb0eb3df12bc8866`  
		Last Modified: Thu, 09 Oct 2025 01:39:30 GMT  
		Size: 12.6 MB (12602014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e665f371dd2830959b271d25aabbd16ef8d11adbb707c39a43673eb2057ddfd1`  
		Last Modified: Thu, 09 Oct 2025 01:39:28 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53022fcbac5d41db808326bcb87e5da06a60086224c11cf16f1f3ae311e1f20`  
		Last Modified: Thu, 09 Oct 2025 01:43:06 GMT  
		Size: 13.7 MB (13735090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271a15d264e42e304d6cc2c5e0e2ff96c58aacd02a2af6117e82b04227fe084f`  
		Last Modified: Thu, 09 Oct 2025 01:43:06 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240ad3e97e677aec19e1e0e54d17cb21e34cb506ac4dd8279b8830340fdbddb9`  
		Last Modified: Thu, 09 Oct 2025 01:43:06 GMT  
		Size: 19.9 KB (19876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84967c56e95e0d072a7a114705e830de8b6468b0bfea1f3bd8e0389441f5c34`  
		Last Modified: Thu, 09 Oct 2025 01:43:06 GMT  
		Size: 19.9 KB (19872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfcd5347e9bb3a574c8a9e66143009c0949d4ee66dfd42ccad3f4c834279113`  
		Last Modified: Thu, 09 Oct 2025 01:43:06 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5c837c4094b17f73f9c31d873b7e05a40ff931b00b9a7abad5e1db1fdb1d042`  
		Last Modified: Tue, 14 Oct 2025 18:05:14 GMT  
		Size: 29.1 MB (29069374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51f08887ceda2dcb85d605f418325ae95b36ab7c43309296d8298d098d0a418`  
		Last Modified: Tue, 14 Oct 2025 18:05:11 GMT  
		Size: 7.3 MB (7295895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77fdcb956db10a39d4c7ae9bc1eda7bdaced06dc5284c09d8507acc97f4e522b`  
		Last Modified: Tue, 14 Oct 2025 18:05:09 GMT  
		Size: 63.5 KB (63499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9ba7e5fc8364b90df10f875e65db314466479a98cbc183213cea6048559494`  
		Last Modified: Tue, 14 Oct 2025 18:05:09 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ee936db664e4f7553af56fae451b42df6a9165646c559aee3a7fa39f8ed0950`  
		Last Modified: Tue, 14 Oct 2025 18:05:17 GMT  
		Size: 26.0 MB (25958141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263da71fd585b812f26d0cf0fca03e1bed5ecea8eaff7e3b752e3855bb0d820c`  
		Last Modified: Tue, 14 Oct 2025 18:05:11 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a2f822dec99760ea146e2634d724650fc81ef309ad7615448d60d13a6c4c98`  
		Last Modified: Tue, 14 Oct 2025 18:05:11 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:6-php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:0c43f9fad49759aab1f04eb3dff9b05376166c1b07515ff5ba3abc6a7abc34bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 KB (46130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92c98d4a57390120958f3694a3a906e3d6212d5faef2a34cd253bae1bc0308ee`

```dockerfile
```

-	Layers:
	-	`sha256:7afe9dbd8c17278aad648435e7745011646cb08ad2657b680d957b77ac379fb5`  
		Last Modified: Tue, 14 Oct 2025 19:50:03 GMT  
		Size: 46.1 KB (46130 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:6-php8.3-fpm-alpine` - linux; riscv64

```console
$ docker pull joomla@sha256:44d5e6d20a36407f5444ff7c223e01915f614461fb9971ad16e1a708d64e2143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.8 MB (93786777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:507528e8903088acb79c0456c276098f9bdbd3784f17469690ce20488aa67881`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 25 Sep 2025 23:53:24 GMT
ADD alpine-minirootfs-3.22.2-riscv64.tar.gz / # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 25 Sep 2025 23:53:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Sep 2025 23:53:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_VERSION=8.3.26
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Sep 2025 23:53:24 GMT
WORKDIR /var/www/html
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Sep 2025 23:53:24 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 25 Sep 2025 23:53:24 GMT
CMD ["php-fpm"]
# Tue, 14 Oct 2025 17:16:27 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 		zstd 	; # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.24; 	pecl install memcached-3.3.0; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
VOLUME [/var/www/html]
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_VERSION=6.0.0
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_SHA512=ca19ea39f8cc1ef10b07abb84080d07f52e34d158522bf0b625948c4a077504cacdbe70e8eea80a3df381f21889a8f62367a9d8def861fa43d671f72b8daa73e
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/6.0.0/Joomla_6.0.0-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Oct 2025 17:16:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:139bee3c50b89b56dcbc72522ce83097d9beb59d9d3a5c19072ccd1ad54b11c8`  
		Last Modified: Wed, 08 Oct 2025 21:18:33 GMT  
		Size: 3.5 MB (3515240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58e9f10e445dbf7ba866462dd44d0f912a09342dc97a4685769a2d057bcc7a9`  
		Last Modified: Thu, 09 Oct 2025 06:22:36 GMT  
		Size: 3.6 MB (3600269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2579c35b4a5055268b9ccb82f8c3307c0a781af77168952679399ed4bde3b60a`  
		Last Modified: Thu, 09 Oct 2025 06:22:36 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98b6a920874b5f6759a41702af348a1eefb32a0674eeae4cd9d750418594caed`  
		Last Modified: Thu, 09 Oct 2025 06:22:36 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03263e1b6f1c73a37b178b02a21b7c17427888e4eb153b2755508c729213eb27`  
		Last Modified: Thu, 09 Oct 2025 16:49:21 GMT  
		Size: 12.6 MB (12602000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975ffc99c90d029fd3419e20d809a63121a30697cf84a60f5499b248f4cd5786`  
		Last Modified: Thu, 09 Oct 2025 16:49:20 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2184173e4def676da742c5127aaad9739256dab7c8163aa5edd9d476169f276a`  
		Last Modified: Thu, 09 Oct 2025 17:44:34 GMT  
		Size: 12.8 MB (12764032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c14d045c8c46fb244402385c3b185cf6f40f73bcbc7416c2dad660360f8bfc7e`  
		Last Modified: Thu, 09 Oct 2025 17:44:23 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc863be9c433ac61971602741b7cc76af0c6c03d515e882c74523021e83a2774`  
		Last Modified: Thu, 09 Oct 2025 17:44:23 GMT  
		Size: 19.9 KB (19864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a67571426b19f21fd32c7d88c4ed5e06d7b8036ca7863058a8251b59e0d2a4a`  
		Last Modified: Thu, 09 Oct 2025 17:44:23 GMT  
		Size: 19.9 KB (19861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac0611ae49a7eb6723fa289aa3f407f176f453cd84f5b0758ae9339937df923`  
		Last Modified: Thu, 09 Oct 2025 17:44:23 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26e3ecaaef95190d6633af6903744aeb54cbc98c884e8012d388bf107cd7761c`  
		Last Modified: Wed, 15 Oct 2025 08:46:12 GMT  
		Size: 28.2 MB (28223744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d63223941bbfb29bd79102e135a8bb330b5a0d12f6ae5a0f31b069a4471ae5`  
		Last Modified: Wed, 15 Oct 2025 08:46:11 GMT  
		Size: 7.0 MB (7001718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94395b2e791d3c12e456febf9ad49b8367530fd30a4c4f37d06a80667dba707c`  
		Last Modified: Wed, 15 Oct 2025 08:46:11 GMT  
		Size: 63.5 KB (63488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e777efb9bbfd29ec6b5443e9001f63b6c707ae614049dafeb14e8c41d0801a6`  
		Last Modified: Wed, 15 Oct 2025 08:46:11 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac575b3a9d38c271e1d249d98380f60b0b9d000dd87f445bf90ae77162c0ce66`  
		Last Modified: Wed, 15 Oct 2025 08:46:13 GMT  
		Size: 26.0 MB (25958125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57c93767d1210fd44457859fef9e9525d43ba84c03cb0ffa24b5fea17e25a34`  
		Last Modified: Wed, 15 Oct 2025 08:46:11 GMT  
		Size: 3.7 KB (3656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35a9c508e3724d868f2160462657bb4e5364f21b9c968c65779cbdd602ee56a`  
		Last Modified: Wed, 15 Oct 2025 08:46:11 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:6-php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:702ae2f9acd4211e356018fda57f43efdab50958dfc1962fe76d991bcdf035c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 KB (46130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fffe89a7689d3740e4cb4f2db98719965faa0dab5675d366278d4918cf5152fc`

```dockerfile
```

-	Layers:
	-	`sha256:e669c16714555543d70e9fe66d38b46143f76cf84e9e578d15e05b7e0263f6f2`  
		Last Modified: Wed, 15 Oct 2025 10:44:43 GMT  
		Size: 46.1 KB (46130 bytes)  
		MIME: application/vnd.in-toto+json

### `joomla:6-php8.3-fpm-alpine` - linux; s390x

```console
$ docker pull joomla@sha256:4e35ef027b5fc1c29067350a30f9b26639c143a05926b603ed85bae5c03a4345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.9 MB (95937666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce43de191b33563cef571869527f1800a813e3b6151af79605545409bd7a3aa1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 25 Sep 2025 23:53:24 GMT
ADD alpine-minirootfs-3.22.2-s390x.tar.gz / # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
CMD ["/bin/sh"]
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 25 Sep 2025 23:53:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 25 Sep 2025 23:53:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_VERSION=8.3.26
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.26.tar.xz.asc
# Thu, 25 Sep 2025 23:53:24 GMT
ENV PHP_SHA256=2f522eefa02c400c94610d07f25c4fd4c771f95e4a1f55102332ccb40663cbd2
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 25 Sep 2025 23:53:24 GMT
WORKDIR /var/www/html
# Thu, 25 Sep 2025 23:53:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 25 Sep 2025 23:53:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 25 Sep 2025 23:53:24 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 25 Sep 2025 23:53:24 GMT
CMD ["php-fpm"]
# Tue, 14 Oct 2025 17:16:27 GMT
LABEL maintainer=Llewellyn van der Merwe <llewellyn.van-der-merwe@community.joomla.org> (@Llewellynvdm), Harald Leithner <harald.leithner@community.joomla.org> (@HLeithner)
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	apk add --no-cache 		bash 		ghostscript 		imagemagick 		zstd 	; # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -ex; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		autoconf 		bzip2-dev 		gmp-dev 		icu-dev 		freetype-dev 		imagemagick-dev 		libjpeg-turbo-dev 		libmemcached-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		openldap-dev 		pcre-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg 		--with-webp 	; 	docker-php-ext-configure ldap; 	docker-php-ext-install -j "$(nproc)" 		bz2 		bcmath 		exif 		gd 		gmp 		intl 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 	pecl install imagick-3.8.0; 	docker-php-ext-enable imagick; 	rm -r /tmp/pear; 		out="$(php -r 'exit(0);')"; 	[ -z "$out" ]; 	err="$(php -r 'exit(0);' 3>&1 1>&2 2>&3)"; 	[ -z "$err" ]; 		extDir="$(php -r 'echo ini_get("extension_dir");')"; 	[ -d "$extDir" ]; 		pecl install APCu-5.1.24; 	pecl install memcached-3.3.0; 	pecl install redis-6.1.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive "$extDir" 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .joomla-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps; 		! { ldd "$extDir"/*.so | grep 'not found'; }; 	err="$(php --version 3>&1 1>&2 2>&3)"; 	[ -z "$err" ] # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -eux; 	docker-php-ext-enable opcache; 	{ 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
RUN { 		echo 'error_reporting = E_ERROR | E_WARNING | E_PARSE | E_CORE_ERROR | E_CORE_WARNING | E_COMPILE_ERROR | E_COMPILE_WARNING | E_RECOVERABLE_ERROR'; 		echo 'display_errors = Off'; 		echo 'display_startup_errors = Off'; 		echo 'log_errors = On'; 		echo 'error_log = /dev/stderr'; 		echo 'log_errors_max_len = 1024'; 		echo 'ignore_repeated_errors = On'; 		echo 'ignore_repeated_source = Off'; 		echo 'html_errors = Off'; 	} > /usr/local/etc/php/conf.d/error-logging.ini # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
VOLUME [/var/www/html]
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_VERSION=6.0.0
# Tue, 14 Oct 2025 17:16:27 GMT
ENV JOOMLA_SHA512=ca19ea39f8cc1ef10b07abb84080d07f52e34d158522bf0b625948c4a077504cacdbe70e8eea80a3df381f21889a8f62367a9d8def861fa43d671f72b8daa73e
# Tue, 14 Oct 2025 17:16:27 GMT
RUN set -ex; 	curl -o joomla.tar.zst -SL https://github.com/joomla/joomla-cms/releases/download/6.0.0/Joomla_6.0.0-Stable-Full_Package.tar.zst; 	echo "$JOOMLA_SHA512 *joomla.tar.zst" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar --zstd -xf joomla.tar.zst -C /usr/src/joomla; 	rm joomla.tar.zst; 	chown -R www-data:www-data /usr/src/joomla # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
COPY makedb.php /makedb.php # buildkit
# Tue, 14 Oct 2025 17:16:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 14 Oct 2025 17:16:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:e6b06613ca2e7cdf3e8ebbe71ca45137242628a4a3a4bfcb7a9f76d0d5b0e653`  
		Last Modified: Wed, 08 Oct 2025 12:04:35 GMT  
		Size: 3.6 MB (3649244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503d2dd4bd3263db65246a0eede02512575e505bf72959ea5d8d1c7f5b3dea5e`  
		Last Modified: Thu, 09 Oct 2025 00:54:03 GMT  
		Size: 3.7 MB (3692716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e39eb5e282665e4bd0e90c53a85f696e72ef63e8ef403c40cc9e67742ffe824`  
		Last Modified: Thu, 09 Oct 2025 00:54:03 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e0608d8b4902677a8ba1ccd4d718738714fa13e782091c89842c948b06a52f8`  
		Last Modified: Thu, 09 Oct 2025 00:54:03 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e5d7767e092986e311439804d82c94621cdc07020c2cfcb84da485ba569b2a`  
		Last Modified: Thu, 09 Oct 2025 01:18:08 GMT  
		Size: 12.6 MB (12602037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4d23c0c8379e4d961de41fc935cc0644f31f603e5735b2ab9bde5b1916e803`  
		Last Modified: Thu, 09 Oct 2025 01:18:06 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9150e22975e95705b6d41ac70482934d9fc69d5a840f61691cc8525c4844d650`  
		Last Modified: Thu, 09 Oct 2025 01:22:36 GMT  
		Size: 13.2 MB (13211624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f39b7641e3388630e2887c4d7b0b62a3b86482b341af5cb915137bcbf00f89`  
		Last Modified: Thu, 09 Oct 2025 01:22:34 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50e477dc5fb08d2ff82dd1cdbd24eb5d713a45aad2976e4e4f16aec64443df4a`  
		Last Modified: Thu, 09 Oct 2025 01:22:34 GMT  
		Size: 19.9 KB (19876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1d7a49df75b51f1418330aa54c5dfe17ab15c530c25a9eb04324f9d4900170`  
		Last Modified: Thu, 09 Oct 2025 01:22:34 GMT  
		Size: 19.9 KB (19870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ced3cdb237f75a8ac0451240bfbf51bfb808f1491aaf03fc88d3e2457601f3`  
		Last Modified: Thu, 09 Oct 2025 01:22:34 GMT  
		Size: 9.2 KB (9174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e0c703b26d8607412a66730820748b043598ea05a5df22af342f7a554813c1`  
		Last Modified: Tue, 14 Oct 2025 18:00:11 GMT  
		Size: 29.4 MB (29390992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ef39c1b459f04fb3d61a63131a77457e12d48aa30291e0afa8bd7fe52c6e53`  
		Last Modified: Tue, 14 Oct 2025 18:00:09 GMT  
		Size: 7.3 MB (7311301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bbca44b1adb698dd09db6b55a5f8a347afbb6af9a206aa174fa01ebef90181`  
		Last Modified: Tue, 14 Oct 2025 18:00:08 GMT  
		Size: 63.5 KB (63486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee58782857180b1231852a5ba3444e4ae8c0970d72aae139c625fc2c725b8b6`  
		Last Modified: Tue, 14 Oct 2025 18:00:08 GMT  
		Size: 389.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4662161ce90d6bd4ee77480d29f47ac5532389cb11181cda367be9547f873fc`  
		Last Modified: Tue, 14 Oct 2025 18:00:11 GMT  
		Size: 26.0 MB (25958118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0403e2ffd66a90d3fffddcb1e2967e6166c51d4ea95ca2601c59e99aec73eb6e`  
		Last Modified: Tue, 14 Oct 2025 18:00:09 GMT  
		Size: 3.7 KB (3652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca038f6158c39aa85a6854245339e12bea8057ab91697f2368b608c237136602`  
		Last Modified: Tue, 14 Oct 2025 18:00:09 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `joomla:6-php8.3-fpm-alpine` - unknown; unknown

```console
$ docker pull joomla@sha256:e11247844a381056f3bc06936831f044e524ad25d52fb928676df33ca0c3f8c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 KB (46078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57cdcb962ff63c014ec41f168d32d59c117bbee0e6e9c9e22c014b114305c063`

```dockerfile
```

-	Layers:
	-	`sha256:d3e744bedd8da2ec7b18e6c3bb0b978d529a61fda633c1ff13fc463c5983714b`  
		Last Modified: Tue, 14 Oct 2025 19:50:06 GMT  
		Size: 46.1 KB (46078 bytes)  
		MIME: application/vnd.in-toto+json
