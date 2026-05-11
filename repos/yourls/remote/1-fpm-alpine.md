## `yourls:1-fpm-alpine`

```console
$ docker pull yourls@sha256:e9c5bd5bdb2bf4a690d803ec8fc70ef4f21b92e9357f33b607ff523d2c16b381
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

### `yourls:1-fpm-alpine` - linux; amd64

```console
$ docker pull yourls@sha256:f083b045be26613b9fc6ae4af9814f6f19940760385bc4b7ae3d9ffa64dd644d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45398692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f089a726fa68b2a59026f42d07bce360b96609c600578b733a6575fa7c469f`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 16:42:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 08 May 2026 16:42:04 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 08 May 2026 16:42:04 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 08 May 2026 16:42:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 16:42:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 16:42:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:42:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:42:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 16:42:04 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 16:42:04 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 16:42:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 16:42:04 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:42:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 16:42:08 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:45:35 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:45:35 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:45:35 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:45:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:45:35 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 16:45:35 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 May 2026 16:45:35 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 16:45:35 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 May 2026 16:45:35 GMT
CMD ["php-fpm"]
# Fri, 08 May 2026 17:12:43 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Fri, 08 May 2026 17:12:44 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Fri, 08 May 2026 17:12:44 GMT
RUN apk add --no-cache bash # buildkit
# Fri, 08 May 2026 17:12:45 GMT
ARG YOURLS_VERSION=1.10.3
# Fri, 08 May 2026 17:12:45 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Fri, 08 May 2026 17:12:45 GMT
ENV YOURLS_VERSION=1.10.3
# Fri, 08 May 2026 17:12:45 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Fri, 08 May 2026 17:12:45 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 08 May 2026 17:12:46 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 08 May 2026 17:12:46 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 17:12:46 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 08 May 2026 17:12:46 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6da25cdcad8a32faafc4b542cf4b90e39c295ac89670b4314e8feb810a89962c`  
		Last Modified: Fri, 08 May 2026 16:45:43 GMT  
		Size: 3.6 MB (3587638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d50649ed47f559199419ec1b20502141e7af60570c77a3b33b4e73358da376`  
		Last Modified: Fri, 08 May 2026 16:45:43 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83f720402f5045c4b74351f1881835708726a004e12a3a3b810811030bdcfec4`  
		Last Modified: Fri, 08 May 2026 16:45:43 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb710cecb7b971f06bcce3547d6b9a04fbe9b912f63ea4e2799cd0474fce0e04`  
		Last Modified: Fri, 08 May 2026 16:45:43 GMT  
		Size: 14.4 MB (14417262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1dafdfac5a4dbc142737db9664dec2282d1adf21b1961413234b791649ad923`  
		Last Modified: Fri, 08 May 2026 16:45:44 GMT  
		Size: 484.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:335a8346ca24bbb539c4bba43eaf52c98eec28db20ccb1d957484e43db0dca92`  
		Last Modified: Fri, 08 May 2026 16:45:45 GMT  
		Size: 16.8 MB (16785308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ce476785360d55869d9d627ee6f7edf7b8c50f82129ec3f98a8210924c7f0f`  
		Last Modified: Fri, 08 May 2026 16:45:44 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427716e69c6b1d6bd4fce7a47244a8cb650f2b2559cc4eab69b968043f51500a`  
		Last Modified: Fri, 08 May 2026 16:45:45 GMT  
		Size: 23.4 KB (23390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75b137d6c608b1290bee5dc8f32fc673c7ae547575930dd3df1ec7546c9c2c3`  
		Last Modified: Fri, 08 May 2026 16:45:46 GMT  
		Size: 9.3 KB (9261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83c1d209aac1ca7803074d7e8502a494ea525fde667e61064f5bd609d6657b8`  
		Last Modified: Fri, 08 May 2026 17:12:50 GMT  
		Size: 133.2 KB (133155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805210e46a4d9c0a7b0bb5bdd76270b9cf097240d9af1ce45261dc002a4ad6ac`  
		Last Modified: Fri, 08 May 2026 17:12:50 GMT  
		Size: 323.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be9c1ad88911e7a9361137fdb87569d477e40dce483b5a9d8b02c3adc202d57`  
		Last Modified: Fri, 08 May 2026 17:12:50 GMT  
		Size: 521.4 KB (521360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba828bb37ed9a5c0489c100eaa453d66d298416f44c84e1856684f2d3a12d003`  
		Last Modified: Fri, 08 May 2026 17:12:50 GMT  
		Size: 6.0 MB (6048909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:386442fbbce91b193957a4e31eb42565be8b59d50002c9bf3747a01fcf34cef9`  
		Last Modified: Fri, 08 May 2026 17:12:51 GMT  
		Size: 2.1 KB (2094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae222e0e9b93fb8a1b41bc5420997e55c9f74ee647d8b213b5282ac544d87e10`  
		Last Modified: Fri, 08 May 2026 17:12:52 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:0101be13d8752b87c1a7cf01bddcba3baa2d9bacc9bca3c63f68cf9f817ae77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae5ec09c339149d010a3173df1749772407b232f00ccb61c44781622eb7661a3`

```dockerfile
```

-	Layers:
	-	`sha256:f19453ae6735841f62d1d5d21c477caea1ac455f72bb6616137a7a88f59ca971`  
		Last Modified: Fri, 08 May 2026 17:12:50 GMT  
		Size: 30.7 KB (30716 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; arm variant v6

```console
$ docker pull yourls@sha256:1319f3357e041b7fd79e0a223989c13f47cbd782db94a494c931755cfbd15b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (42953638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2667c659ef183193d24a53bef5972f38563e0e80b3cac77f9e322458ba45f49e`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 16:37:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 08 May 2026 16:37:16 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 08 May 2026 16:37:16 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 08 May 2026 16:37:16 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 16:37:16 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 16:37:16 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:37:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:37:16 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 16:37:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 16:37:16 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 16:37:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 16:37:16 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:37:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 16:37:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:40:45 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:40:45 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:40:46 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:40:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:40:46 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 16:40:46 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 May 2026 16:40:46 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 16:40:46 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 May 2026 16:40:46 GMT
CMD ["php-fpm"]
# Fri, 08 May 2026 17:16:42 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Fri, 08 May 2026 17:16:42 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Fri, 08 May 2026 17:16:43 GMT
RUN apk add --no-cache bash # buildkit
# Fri, 08 May 2026 17:16:44 GMT
ARG YOURLS_VERSION=1.10.3
# Fri, 08 May 2026 17:16:44 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Fri, 08 May 2026 17:16:44 GMT
ENV YOURLS_VERSION=1.10.3
# Fri, 08 May 2026 17:16:44 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Fri, 08 May 2026 17:16:44 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 08 May 2026 17:16:44 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 08 May 2026 17:16:44 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 17:16:44 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 08 May 2026 17:16:44 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d9605748e73e549791dde06cfd4e29cf21717dc98683f32e50c9eaac44970aa`  
		Last Modified: Fri, 08 May 2026 16:40:52 GMT  
		Size: 3.5 MB (3543647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20895ad54cafaa9671b8253f2087a35afe023bf472625c63b963aa5966ede482`  
		Last Modified: Fri, 08 May 2026 16:40:52 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6ed0c63f1240d980eafba8d68cc6b7470dce16d71212a97c3d916147fad9a6`  
		Last Modified: Fri, 08 May 2026 16:40:52 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb820e95f08461f05001ad429e7ae79c2fd9335d0e70b4e0ca9dc41c5a380ac`  
		Last Modified: Fri, 08 May 2026 16:40:52 GMT  
		Size: 14.4 MB (14417277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989a63405c5ef39622c107d4445036ce6a57d0f0b18f2432d4d9d1264ec36f4b`  
		Last Modified: Fri, 08 May 2026 16:40:53 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bf5bb3c54255f3a2825e6dae2ca3ccfe906c7a8572e62d034c934dde2956058`  
		Last Modified: Fri, 08 May 2026 16:40:53 GMT  
		Size: 14.7 MB (14686830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c6321415e15d7cca5b54126bba270bbf41e563f7c25ede9298b2a6716fa7fc`  
		Last Modified: Fri, 08 May 2026 16:40:53 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3636f519b999dc50d00c94f2023a1da4db1100915f72bceddefe0efe1a9bc1`  
		Last Modified: Fri, 08 May 2026 16:40:54 GMT  
		Size: 23.2 KB (23203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8096efc1ee3bf67e9ce12c77639c0f28e7e7cc5ab3256b55802c9d18d75ab91a`  
		Last Modified: Fri, 08 May 2026 16:40:54 GMT  
		Size: 9.3 KB (9258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66b1311b3b82421d2335fb6f19b7db6e1036a428d1d4a8317b9106f293f4e50`  
		Last Modified: Fri, 08 May 2026 17:16:49 GMT  
		Size: 120.9 KB (120919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00cd0d381a0f538d987fe35a05ef7c423664ef8712360ff1b22176706a9b6f0e`  
		Last Modified: Fri, 08 May 2026 17:16:49 GMT  
		Size: 318.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c75e4ae178019b2e1a77e48be491b9ae6149055ef82b0a5870b847bb21f1d25`  
		Last Modified: Fri, 08 May 2026 17:16:49 GMT  
		Size: 523.5 KB (523528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad0ba2d772a751b23e9b346f293be26f26a6eb6af2678aa022c2eca9107c04c`  
		Last Modified: Fri, 08 May 2026 17:16:49 GMT  
		Size: 6.0 MB (6048900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64b4ffe3caf87c0d6531f0124950f664cd131fb5995b2a4b7611dbda421992d5`  
		Last Modified: Fri, 08 May 2026 17:16:50 GMT  
		Size: 2.1 KB (2091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f786a689a5a659b47e0daf7536733bdc5f82f0ff48d06e9bdc05eaba8090bf`  
		Last Modified: Fri, 08 May 2026 17:16:50 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:6d4b2c7534087afbd2e2b7ef268087910ed7474336a478435829488cd6cd547b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a54f3f2c885e5221701b68612282ab466c80b29aedaf7eb1a5f51d11654318f6`

```dockerfile
```

-	Layers:
	-	`sha256:c8dcff8125454527923f83f3646a7972324be385eeff6b2ed69ad330b6081464`  
		Last Modified: Fri, 08 May 2026 17:16:49 GMT  
		Size: 30.8 KB (30835 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; arm variant v7

```console
$ docker pull yourls@sha256:0dcd08b793168c3d8e7ac46b63f7569bc91abce23890db9adfec40c46b78e1c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41603460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:195037b57114f6d4c0bd35dd76b3b648b9521e898fa001cb1c3a1f1e9021b22d`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 16:44:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 08 May 2026 16:44:40 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 08 May 2026 16:44:40 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 08 May 2026 16:44:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 16:44:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 16:44:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:44:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:44:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 16:44:40 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 16:44:40 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 16:44:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 16:44:40 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:44:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 16:44:44 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:47:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:47:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:47:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:47:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:47:56 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 16:47:56 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 May 2026 16:47:56 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 16:47:56 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 May 2026 16:47:56 GMT
CMD ["php-fpm"]
# Fri, 08 May 2026 17:18:00 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Fri, 08 May 2026 17:18:00 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Fri, 08 May 2026 17:18:00 GMT
RUN apk add --no-cache bash # buildkit
# Fri, 08 May 2026 17:18:01 GMT
ARG YOURLS_VERSION=1.10.3
# Fri, 08 May 2026 17:18:01 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Fri, 08 May 2026 17:18:01 GMT
ENV YOURLS_VERSION=1.10.3
# Fri, 08 May 2026 17:18:01 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Fri, 08 May 2026 17:18:01 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 08 May 2026 17:18:01 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 08 May 2026 17:18:01 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 17:18:01 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 08 May 2026 17:18:01 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ead381c639671ff5f17dadad5e7d67c029b5e50ab69c9b5a1735d9258b6c1a60`  
		Last Modified: Fri, 08 May 2026 16:48:03 GMT  
		Size: 3.3 MB (3343511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14c73596d0d2d68a4ca3fb905d3bae795fe6d840c1dacbc2b4bc6108b385d3ce`  
		Last Modified: Fri, 08 May 2026 16:48:03 GMT  
		Size: 932.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f4d8b4f7046d03ba011d87dd58ed805a2d58cc99dd7f09eb8546e077c53d769`  
		Last Modified: Fri, 08 May 2026 16:48:03 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a89e4834a3ad47ed2dc15877b5840b323cc2aefb24dcf7c3910c79f443c360`  
		Last Modified: Fri, 08 May 2026 16:48:03 GMT  
		Size: 14.4 MB (14417280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0cd5ea5d285a081e8f1cae645244dae42b483f33eebbf8a21642fec9ce95aa0`  
		Last Modified: Fri, 08 May 2026 16:48:04 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c7b267553dc73cca8bc9a53e8d51f0d384e0bc56dca5384b93a693d6fb4d582`  
		Last Modified: Fri, 08 May 2026 16:48:05 GMT  
		Size: 13.9 MB (13874980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c60b2d27c4b617e5e64b1ca5bf0f1be2d56e79374afb07a6ff2e010a998d12`  
		Last Modified: Fri, 08 May 2026 16:48:04 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d47b515bcbb7de00451bfc0cd45abf927413e649b877ab2a86fd021170e7c2e`  
		Last Modified: Fri, 08 May 2026 16:48:05 GMT  
		Size: 23.2 KB (23202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818d9d5a3eb7883ce0f6ecbe8988274b8bad12b134e63ff13d1f554609c63974`  
		Last Modified: Fri, 08 May 2026 16:48:06 GMT  
		Size: 9.3 KB (9259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e43c51c210a1705dbf9f321995a9778c20202d5b6c96598e80d7f33481fc03c7`  
		Last Modified: Fri, 08 May 2026 17:18:06 GMT  
		Size: 114.1 KB (114077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9219160949cdbc7931210f750d5774f53602e343509b51275c418fff14b0db`  
		Last Modified: Fri, 08 May 2026 17:18:06 GMT  
		Size: 323.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a015556ca1dceee4f822a130f534ad0c2212a0fc4b4b4074e5ee213f149c4606`  
		Last Modified: Fri, 08 May 2026 17:18:06 GMT  
		Size: 480.9 KB (480896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a851353c4045a3f5ec56112192b72d6e2c8dd6ea54891fadb48d7a414e462d3`  
		Last Modified: Fri, 08 May 2026 17:18:06 GMT  
		Size: 6.0 MB (6048910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62af7138c474d30168b7224bea2a9b8ec8463248202ca5509f9452a219135dac`  
		Last Modified: Fri, 08 May 2026 17:18:07 GMT  
		Size: 2.1 KB (2092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f754258ff37ea0700213d8829a010b6eeb2cd65634d7e79335e798cb975b1f5`  
		Last Modified: Fri, 08 May 2026 17:18:07 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:ad78058f9810c4d69ba8bbd72f6c8c4abeefbe2bec7b7d651e0626408ea77af8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:677d7662d14764d65fbe5241cd261e77936d4f101da0354726a52d3f2e78a296`

```dockerfile
```

-	Layers:
	-	`sha256:ae29ebeaff08900de074801ea80536ca1b1d1af79cd59e72bd8bc8a85b16edbb`  
		Last Modified: Fri, 08 May 2026 17:18:06 GMT  
		Size: 30.8 KB (30834 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:5858c9b8f4a486dc1ffa7eafcda726b8981fd1c98d5f92cbb3e2eb35d5d471b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45203320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3145cebafca58de3a25f582eeaa3c8874303c9825f4ca460fdb3ffffbc77fb8`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 16:42:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 08 May 2026 16:42:07 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 08 May 2026 16:42:07 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 08 May 2026 16:42:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 16:42:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 16:42:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:42:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:42:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 16:42:07 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 16:42:07 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 16:42:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 16:42:07 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:42:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 16:42:12 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:45:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:45:46 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:45:47 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:45:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:45:47 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 16:45:47 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 May 2026 16:45:47 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 16:45:47 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 May 2026 16:45:47 GMT
CMD ["php-fpm"]
# Fri, 08 May 2026 17:13:10 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Fri, 08 May 2026 17:13:10 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Fri, 08 May 2026 17:13:10 GMT
RUN apk add --no-cache bash # buildkit
# Fri, 08 May 2026 17:13:11 GMT
ARG YOURLS_VERSION=1.10.3
# Fri, 08 May 2026 17:13:11 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Fri, 08 May 2026 17:13:11 GMT
ENV YOURLS_VERSION=1.10.3
# Fri, 08 May 2026 17:13:11 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Fri, 08 May 2026 17:13:11 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 08 May 2026 17:13:11 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 08 May 2026 17:13:11 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 17:13:11 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 08 May 2026 17:13:11 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2b3e7f2886574cf11a41b493d528247150921482850c2a4f4ee2a901f97d8b`  
		Last Modified: Fri, 08 May 2026 16:45:55 GMT  
		Size: 3.6 MB (3596161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755b48bf212bbe38545947bc7db3c146ff9080c5ae77ebf48802ec75d699d84c`  
		Last Modified: Fri, 08 May 2026 16:45:55 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87eccd5d96a69196d8b5350353311d579c3bf4257eedf4262975eac4240156cc`  
		Last Modified: Fri, 08 May 2026 16:45:55 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0a644f04c14c335c296b69c6da91d05e35d02642444606e7bf63c79f6f6b52`  
		Last Modified: Fri, 08 May 2026 16:45:56 GMT  
		Size: 14.4 MB (14417266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19d7eff4a3f5495be9836fae1823a0dab7c7e81b9907498a44b36e46da00598`  
		Last Modified: Fri, 08 May 2026 16:45:56 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:300ff958f6a8fce57cdee2c3acc7dc67a438234dcf6b33ff9e7d691d2a24aa7b`  
		Last Modified: Fri, 08 May 2026 16:45:57 GMT  
		Size: 16.2 MB (16190561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e893c8ada273c1f6d2c33ad8bd4510d3f6f7b1b92bd40f7b11cd8027b49ea7`  
		Last Modified: Fri, 08 May 2026 16:45:57 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff26872446c3f21828995febd25b2668ba6b34d4b07e098d42fa5c1290958f2`  
		Last Modified: Fri, 08 May 2026 16:45:57 GMT  
		Size: 23.2 KB (23214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f10c6ed51255dd5657c579570f8bb4170954658eac26fefbe1b0a95d90af57d`  
		Last Modified: Fri, 08 May 2026 16:45:58 GMT  
		Size: 9.3 KB (9262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad350a92ae66276c711a7ce470f6243e0792cdda059705c5a602ee5742347649`  
		Last Modified: Fri, 08 May 2026 17:13:16 GMT  
		Size: 126.8 KB (126841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d773a7e5d41469de6b63c90a4442178d01f8b88a35c1d1ff4b94db63eee43c`  
		Last Modified: Fri, 08 May 2026 17:13:16 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4992e4636c760cea4674845773c56080f0f985727c24cbf22c78a5dcc9104136`  
		Last Modified: Fri, 08 May 2026 17:13:16 GMT  
		Size: 583.0 KB (583026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a05b206c755c42eae0b47b4018248892a2bd056fcfecd59e2d202cfdcc6f62e`  
		Last Modified: Fri, 08 May 2026 17:13:16 GMT  
		Size: 6.0 MB (6048900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ea7de1787194703ca74a1cbb8b8ffbfb03268bab0c98feaa7514d6ef413e85`  
		Last Modified: Fri, 08 May 2026 17:13:17 GMT  
		Size: 2.1 KB (2090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cdb2832da5ebf6ac53bcdb84164b864b8c5777f455a330a1e84864b631492c0`  
		Last Modified: Fri, 08 May 2026 17:13:17 GMT  
		Size: 1.7 KB (1688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:a44c16bb77e2ed77ed94259647dfecd5675b17c7e68cad124d4afa9513b06ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.9 KB (30864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6855027ae0847004be97f89cbefc03a9eceb5a9fce22bc6bb87d25763d77e74c`

```dockerfile
```

-	Layers:
	-	`sha256:87d6c48a6cf3f7aadea91b32e5440238346cd137e3a994ceab3abb3b485e5703`  
		Last Modified: Fri, 08 May 2026 17:13:16 GMT  
		Size: 30.9 KB (30864 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; 386

```console
$ docker pull yourls@sha256:a7426f329a87a87b283d3db506f128c0879ba934455d8bf03452f7ce921dd69b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45616742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16c0534a8234d7afb390ca407b872686b0c7f4af5580b16832491858744c878`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 16:45:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 08 May 2026 16:45:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 08 May 2026 16:45:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 08 May 2026 16:45:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 08 May 2026 16:45:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 08 May 2026 16:45:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:45:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 08 May 2026 16:45:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 08 May 2026 16:45:56 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Fri, 08 May 2026 16:45:56 GMT
ENV PHP_VERSION=8.5.6
# Fri, 08 May 2026 16:45:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Fri, 08 May 2026 16:45:56 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:46:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 16:46:03 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:49:33 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:49:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:49:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:49:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:49:34 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 16:49:34 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 May 2026 16:49:34 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 16:49:34 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 May 2026 16:49:34 GMT
CMD ["php-fpm"]
# Fri, 08 May 2026 17:12:56 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Fri, 08 May 2026 17:12:57 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Fri, 08 May 2026 17:12:57 GMT
RUN apk add --no-cache bash # buildkit
# Fri, 08 May 2026 17:12:59 GMT
ARG YOURLS_VERSION=1.10.3
# Fri, 08 May 2026 17:12:59 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Fri, 08 May 2026 17:12:59 GMT
ENV YOURLS_VERSION=1.10.3
# Fri, 08 May 2026 17:12:59 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Fri, 08 May 2026 17:12:59 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 08 May 2026 17:12:59 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 08 May 2026 17:12:59 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 17:12:59 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 08 May 2026 17:12:59 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b0ebfd84824b3c4f4b3c99040e715e8a62bd35776d952c0c5a6fc1167e13b72`  
		Last Modified: Fri, 08 May 2026 16:49:42 GMT  
		Size: 3.6 MB (3625743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54e55fa870194cea148562636a07a92b9eedd40517a047ccf88039b969b98f35`  
		Last Modified: Fri, 08 May 2026 16:49:41 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e22866eae8f9774eeac20cb226144dbf240bc572fd8adaba3ef79f81dcaa84`  
		Last Modified: Fri, 08 May 2026 16:49:41 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9813bba060d5f629ba6be311fce28a06414432144be476f8b94615a8b857b2c6`  
		Last Modified: Fri, 08 May 2026 16:49:42 GMT  
		Size: 14.4 MB (14417258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7436aad6bd1a229fdd98e0ba75ceb086c5a976119e0653700363d9b95da11dd9`  
		Last Modified: Fri, 08 May 2026 16:49:42 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641c063d430ba56ce8b65f92b163d8498d453bf4af500d7f2156a2af046c0967`  
		Last Modified: Fri, 08 May 2026 16:49:43 GMT  
		Size: 17.1 MB (17125541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95c15dc81b3a58276083c67de2f6233b5cda2f3af9c14d132b54fa91f63392c`  
		Last Modified: Fri, 08 May 2026 16:49:43 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1021b130e01ed8d667df6a68eeb1702f69f6821f19b910d4e72a552425adf0dd`  
		Last Modified: Fri, 08 May 2026 16:49:43 GMT  
		Size: 23.4 KB (23391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab215e280919d966d8eebcb733650518e2a29e6679a2f53df71d9baeb3b31bcb`  
		Last Modified: Fri, 08 May 2026 16:49:43 GMT  
		Size: 9.3 KB (9260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662dbbb7015c067b4db9897f28118bff5547806f9d7489a8c2667f87f38b4d40`  
		Last Modified: Fri, 08 May 2026 17:13:04 GMT  
		Size: 136.6 KB (136560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2a619d75d193da85aec3849d6a028e1e2ca6056f9e49929e0fbbb5248a43e06`  
		Last Modified: Fri, 08 May 2026 17:13:04 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a8d96a9ba51084658f1a44222242eb8ee3bb43d331830fe87e121b79144f90`  
		Last Modified: Fri, 08 May 2026 17:13:04 GMT  
		Size: 531.4 KB (531406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:263bd165222a7fb60d77ae7ddf159377467ddfbb0a87cdd24cfc9f5d43e7c754`  
		Last Modified: Fri, 08 May 2026 17:13:04 GMT  
		Size: 6.0 MB (6048909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58f637c6f40b5d6033040131fa1113439a80cf38838589e8b1cc5fd270f7a3f8`  
		Last Modified: Fri, 08 May 2026 17:13:05 GMT  
		Size: 2.1 KB (2094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60568467c72e18f55ece410e3f4b85145bcc7449fccd48e879a771c173e2093f`  
		Last Modified: Fri, 08 May 2026 17:13:05 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:2af8d1dfb2a11e6da5614e17f9d2f24f0095f7c64b4e2f41dfd7ffff0197cae4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf1efd58738521f170cb2d59cd1ac404cc17ddd748c0dfdab0731eb972db867`

```dockerfile
```

-	Layers:
	-	`sha256:af7beee44cfd6dbcaa9857c0918dd7f71b365d48a38ee605e4e585e3a7a01efc`  
		Last Modified: Fri, 08 May 2026 17:13:04 GMT  
		Size: 30.7 KB (30677 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; ppc64le

```console
$ docker pull yourls@sha256:20ec6d69f5bec3ffbf0d7d48ec69866f5a54de080ccb323e27fe76597b9135e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46017113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe8d3f2937eea7f31288458ddcb6b4f1bde8d0b7d17b05912b9e78cb191c0bb`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 15 Apr 2026 20:20:47 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 15 Apr 2026 20:20:47 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 15 Apr 2026 20:20:47 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 15 Apr 2026 20:20:47 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_VERSION=8.5.6
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Wed, 15 Apr 2026 20:20:47 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 19:47:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 19:47:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:53:50 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 19:53:50 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 19:53:51 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 19:53:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 19:53:51 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 19:53:52 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 May 2026 19:53:52 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 19:53:52 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 May 2026 19:53:52 GMT
CMD ["php-fpm"]
# Fri, 08 May 2026 22:30:12 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Fri, 08 May 2026 22:30:13 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Fri, 08 May 2026 22:30:15 GMT
RUN apk add --no-cache bash # buildkit
# Fri, 08 May 2026 22:30:17 GMT
ARG YOURLS_VERSION=1.10.3
# Fri, 08 May 2026 22:30:17 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Fri, 08 May 2026 22:30:17 GMT
ENV YOURLS_VERSION=1.10.3
# Fri, 08 May 2026 22:30:17 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Fri, 08 May 2026 22:30:17 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 08 May 2026 22:30:17 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 08 May 2026 22:30:17 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 22:30:17 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 08 May 2026 22:30:17 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a59216db1edcf64b90905df63416f821bfacdba590544dcdb3c340ea538567c`  
		Last Modified: Wed, 15 Apr 2026 20:26:31 GMT  
		Size: 3.8 MB (3767095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14dbb332183b4f53eb48b10e61f11a67b23c5647a6901cf35be6037e209a0f51`  
		Last Modified: Wed, 15 Apr 2026 20:26:31 GMT  
		Size: 931.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fd758015c67cd7fae70202df89f7e42a01ff424cadf0cd92070805333b28821`  
		Last Modified: Wed, 15 Apr 2026 20:26:31 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5702960144fbb228318e4c40ca2e9c98158a8c7b9f71390320236bda898ca95`  
		Last Modified: Fri, 08 May 2026 19:53:03 GMT  
		Size: 14.4 MB (14417280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5358ab27e77a70ddec9b84d07b8f7d4afdddd40d4273150e0f53f745558ec45e`  
		Last Modified: Fri, 08 May 2026 19:53:03 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f5e20a7b6b5765895c8296f8204024e82281e559e87ad15a420fc31bb4efc0`  
		Last Modified: Fri, 08 May 2026 19:54:06 GMT  
		Size: 17.2 MB (17171248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990f178932a601a6990813088b704d9b9034cb725c8f0ee3f3d1c7f301c339b7`  
		Last Modified: Fri, 08 May 2026 19:54:05 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a64edc37ba8cf372793f109c6d759c0a97efc748d958084e0da5c19c002c2ff1`  
		Last Modified: Fri, 08 May 2026 19:54:05 GMT  
		Size: 23.3 KB (23274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f31168ba8e675d248ca654c4bbb3880eb917b7d20963c0310bf801bec77102be`  
		Last Modified: Fri, 08 May 2026 19:54:05 GMT  
		Size: 9.3 KB (9264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6800c529e02702102cad59f08afae52b06b1b159dc924e2176c180f79544c48d`  
		Last Modified: Fri, 08 May 2026 22:30:24 GMT  
		Size: 142.2 KB (142225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa29a788ce9e47ad7674a501f412d56c96bb97fcec88a65bad7739bf8be27f3`  
		Last Modified: Fri, 08 May 2026 22:30:24 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff4ac5a74ac2db7eba32bdaf22e34716c0dbf15ebaa9fa4056feabf215a4fc1`  
		Last Modified: Fri, 08 May 2026 22:30:24 GMT  
		Size: 598.7 KB (598670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:318bd5aac3f77b7f15b9513fdfd31146947df7403ebcbf02c4b2c209069f5a38`  
		Last Modified: Fri, 08 May 2026 22:30:25 GMT  
		Size: 6.0 MB (6048900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d441e98e39053d77b4fc12b615dfe05a425c3b390e276a417fa07d959fcac1a`  
		Last Modified: Fri, 08 May 2026 22:30:26 GMT  
		Size: 2.1 KB (2090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dc57cefb709a7592d148533cdabdd921d9f2d41b62f6920df2f0a7a27c32bda`  
		Last Modified: Fri, 08 May 2026 22:30:25 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:914136426ed85a1b83c8babe213902b1ea7aede8b106243255d4e994b85c3178
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bad5bd341fcdd405b70a2a37be11f0efeaa6ca24f53d15f1a5d217f68260f0b8`

```dockerfile
```

-	Layers:
	-	`sha256:93966178869f2bbd0d4cac2c442e8cd18386bea82611e9d8a1c136df33136ef0`  
		Last Modified: Fri, 08 May 2026 22:30:24 GMT  
		Size: 30.8 KB (30766 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; riscv64

```console
$ docker pull yourls@sha256:9d55759c65bdf62c94c94c108b9937b9ea3b87f80e236c91e9cf78e16adc3ecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 MB (44268332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e3aa29db16aba054b25760948fa93816cabf14acc83f9ec37f869e235a8f1d2`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 16 Apr 2026 00:30:18 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Thu, 16 Apr 2026 00:30:18 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Apr 2026 00:30:18 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 16 Apr 2026 00:30:18 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_VERSION=8.5.6
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Thu, 16 Apr 2026 00:30:18 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 21:51:41 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 21:51:41 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 23:54:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 23:54:51 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 23:54:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 23:54:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 23:54:56 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 23:54:57 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 May 2026 23:54:57 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 23:54:57 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 May 2026 23:54:57 GMT
CMD ["php-fpm"]
# Mon, 11 May 2026 00:45:57 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Mon, 11 May 2026 00:45:58 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Mon, 11 May 2026 00:46:02 GMT
RUN apk add --no-cache bash # buildkit
# Mon, 11 May 2026 00:46:05 GMT
ARG YOURLS_VERSION=1.10.3
# Mon, 11 May 2026 00:46:05 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Mon, 11 May 2026 00:46:05 GMT
ENV YOURLS_VERSION=1.10.3
# Mon, 11 May 2026 00:46:05 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Mon, 11 May 2026 00:46:05 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Mon, 11 May 2026 00:46:06 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Mon, 11 May 2026 00:46:06 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 11 May 2026 00:46:06 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Mon, 11 May 2026 00:46:06 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78828518b8b5af0bc74ba3bd169a5c835b32f2a1452a7cd03ad8117a0128165b`  
		Last Modified: Thu, 16 Apr 2026 01:32:16 GMT  
		Size: 3.7 MB (3734242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e1c9b4ddefe159b602dd6cdf3bcfff1bf48c922a0f1047bb5402dc2c6c988b`  
		Last Modified: Thu, 16 Apr 2026 01:32:15 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2a62067bd9660d4987f0df8c18a9ac2818a33d0443ac9c5c806eb7925b9957`  
		Last Modified: Thu, 16 Apr 2026 01:32:15 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b300791544e0c87f44b461c514787bf7d38ce6f5ad1d34bad34bc1c4782d3f`  
		Last Modified: Fri, 08 May 2026 22:53:24 GMT  
		Size: 14.4 MB (14417294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a331978dcb7855b965e50fa41230cb7f963d49113c956b0e49057d02df423466`  
		Last Modified: Fri, 08 May 2026 22:53:20 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccde3225267fcd1ea4c4cd6b016a28d28c79e3b33e184ddbd9efa14137d9293f`  
		Last Modified: Fri, 08 May 2026 23:55:55 GMT  
		Size: 15.8 MB (15773501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6412f614d391b5cfbd9bcdffcbcb7461d19e938a200e287a528349527f38faf6`  
		Last Modified: Fri, 08 May 2026 23:55:53 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79ab010ae91ba701e6b95d825f6af52b90118e4200301857fe7a0ec82730b3d9`  
		Last Modified: Fri, 08 May 2026 23:55:53 GMT  
		Size: 23.3 KB (23282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:545a5e1932e8e5c649882a1484e9a96c32b30561db4a9b6dbe0e0435dcdc94ac`  
		Last Modified: Fri, 08 May 2026 23:55:52 GMT  
		Size: 9.3 KB (9265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e46b32cd75b9f04fb3bca2e69634b7c8bd8cb1618dd229b5684efee04b2ab6b`  
		Last Modified: Mon, 11 May 2026 00:46:27 GMT  
		Size: 128.5 KB (128482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20cbee6d8993e6bc0f43a8cce47d034d5a8470836e0818b1f3a5b310f1c81e40`  
		Last Modified: Mon, 11 May 2026 00:46:27 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0348b5ddb6c6a0b74fe43fa404989b6c9fd7045a96d034dd70cb112f813d6bd8`  
		Last Modified: Mon, 11 May 2026 00:46:27 GMT  
		Size: 537.4 KB (537434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9078ee014b8f07fc14fc444a342b89964729d6c95243689750e74cacecc9910`  
		Last Modified: Mon, 11 May 2026 00:46:28 GMT  
		Size: 6.0 MB (6048913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334def093749683d5439fe3aebb5c734f10b15d27d49d6438c314b037f72c060`  
		Last Modified: Mon, 11 May 2026 00:46:28 GMT  
		Size: 2.1 KB (2096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672cad8cb964d9d145b25095b305737b5a1247ea14619fa6d75f68ad0988eaec`  
		Last Modified: Mon, 11 May 2026 00:46:28 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:611ac4d60e0822460e5afada02a1c2241fa1f6259db71e74141137d1b76efe23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.8 KB (30766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b393bbfbd1519d9a782d1aad007b5eaf2dcc1cbd1c9704b82a1c0d78805664`

```dockerfile
```

-	Layers:
	-	`sha256:5b5ddfa72dc86e63a272b2384130aa7e460420bb516a5284e02a2e1f7a8acbb1`  
		Last Modified: Mon, 11 May 2026 00:46:27 GMT  
		Size: 30.8 KB (30766 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm-alpine` - linux; s390x

```console
$ docker pull yourls@sha256:dad137b9c3b58d08fbf18601970051f1645b919a34aa3b74a435571d8b8ef9df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44763243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1f57adf17c64f8da739e00be23882015232dc44b379b868259db7eb1c818fe7`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Tue, 05 May 2026 23:41:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 05 May 2026 23:41:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 05 May 2026 23:41:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 05 May 2026 23:41:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 05 May 2026 23:41:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 05 May 2026 23:41:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 May 2026 23:41:30 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 05 May 2026 23:41:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 05 May 2026 23:41:30 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Tue, 05 May 2026 23:41:30 GMT
ENV PHP_VERSION=8.5.6
# Tue, 05 May 2026 23:41:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.6.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.6.tar.xz.asc
# Tue, 05 May 2026 23:41:30 GMT
ENV PHP_SHA256=826c600b7c6f956bd335558ca3bdbcab23b22126c1cc8d9348be2280a2204bb7
# Fri, 08 May 2026 16:51:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 08 May 2026 16:51:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:57:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 08 May 2026 16:57:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 08 May 2026 16:57:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 08 May 2026 16:57:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 08 May 2026 16:57:34 GMT
WORKDIR /var/www/html
# Fri, 08 May 2026 16:57:35 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 08 May 2026 16:57:35 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 16:57:35 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 08 May 2026 16:57:35 GMT
CMD ["php-fpm"]
# Fri, 08 May 2026 17:14:01 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Fri, 08 May 2026 17:14:01 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Fri, 08 May 2026 17:14:02 GMT
RUN apk add --no-cache bash # buildkit
# Fri, 08 May 2026 17:14:04 GMT
ARG YOURLS_VERSION=1.10.3
# Fri, 08 May 2026 17:14:04 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Fri, 08 May 2026 17:14:04 GMT
ENV YOURLS_VERSION=1.10.3
# Fri, 08 May 2026 17:14:04 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Fri, 08 May 2026 17:14:04 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 08 May 2026 17:14:04 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 08 May 2026 17:14:04 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 08 May 2026 17:14:04 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 08 May 2026 17:14:04 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677f4e03a78a2789370c79cc98bf70277df54605d03b98f1ddd8c95295d1f52f`  
		Last Modified: Tue, 05 May 2026 23:48:52 GMT  
		Size: 3.8 MB (3787519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42209df548fd1cd70d82f40e163f4aa9f58445e4a5853781b9c21d3fcfd67c68`  
		Last Modified: Tue, 05 May 2026 23:48:52 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7564dcf40411cee3aeb67bfbec40b4f100e81196fd1c15db9a1bd419fe441d`  
		Last Modified: Tue, 05 May 2026 23:48:52 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c592f1265316127c2e15182e8676298d3e21d127a82fc58cd67b72a4f3ca8a19`  
		Last Modified: Fri, 08 May 2026 16:57:53 GMT  
		Size: 14.4 MB (14417278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19d8fdf19b789c45cdb71800ee57fe461b7c146f9f093c3b1dcd44c74954e52`  
		Last Modified: Fri, 08 May 2026 16:57:53 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f51bbbbebc099f775041d876e0afd0ae8a7ced6d3c75d5a06c8684569e3ff455`  
		Last Modified: Fri, 08 May 2026 16:57:54 GMT  
		Size: 16.0 MB (16048993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ca990ff5a114bf1d85d1f58b0b00df32f7bb51418c187260b0a2c5495925e5`  
		Last Modified: Fri, 08 May 2026 16:57:53 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204d885175952be1ff2ead40fe06ab424cdc469be23e35c1190e6c05992a3b74`  
		Last Modified: Fri, 08 May 2026 16:57:54 GMT  
		Size: 23.2 KB (23227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80a05b00b2804eadea7374ce19ccb95c57cb99197e267968e47758d30fb2530e`  
		Last Modified: Fri, 08 May 2026 16:57:54 GMT  
		Size: 9.3 KB (9262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf34b4c013b423361edc074a2a8ccc055ff87791e86fd1f4870b2e0d0d907e7c`  
		Last Modified: Fri, 08 May 2026 17:14:12 GMT  
		Size: 135.3 KB (135265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef7528b0834a93c78b232c4c0575b4ffb7a81fdbc0181b4b719619ae0847dea`  
		Last Modified: Fri, 08 May 2026 17:14:12 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88783a45e83a54f1d7b74a4e8b7e590529a9b3c2c344f4aef16f3316bde805d5`  
		Last Modified: Fri, 08 May 2026 17:14:12 GMT  
		Size: 558.0 KB (558024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eeb581c65f80d76ce3eb6c979760791686692523b790d0b16884ec7721b3604`  
		Last Modified: Fri, 08 May 2026 17:14:12 GMT  
		Size: 6.0 MB (6048909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c863a8db94f6bf693c44c7745e2588c01e16a34ddce20995816d22e931aef10a`  
		Last Modified: Fri, 08 May 2026 17:14:13 GMT  
		Size: 2.1 KB (2092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2c7acee3b5a30808bec4c437408599d10a40c0df8e0645de3cf6c6849a15d0`  
		Last Modified: Fri, 08 May 2026 17:14:13 GMT  
		Size: 1.7 KB (1687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm-alpine` - unknown; unknown

```console
$ docker pull yourls@sha256:2261a2df824e19660c03c8b904519517b3d8b7ea9a683a46654e9c699b81be97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64b2c09009131bd86170b9351d3c3d350cf41b3bb3a94adb6c0dae241bc6cdca`

```dockerfile
```

-	Layers:
	-	`sha256:e7587fd4167a3d3569cb5ac32da296d75bb7380f291df746524614fab6338ffc`  
		Last Modified: Fri, 08 May 2026 17:14:12 GMT  
		Size: 30.7 KB (30716 bytes)  
		MIME: application/vnd.in-toto+json
