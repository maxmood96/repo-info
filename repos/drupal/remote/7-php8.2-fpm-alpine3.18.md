## `drupal:7-php8.2-fpm-alpine3.18`

```console
$ docker pull drupal@sha256:2526a486cae1776e05725e6fcd0d8ae45a6ae2b7eec5397db299f8e069ec5284
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

### `drupal:7-php8.2-fpm-alpine3.18` - linux; amd64

```console
$ docker pull drupal@sha256:33b1421b43741418d15b37461dfb56e7e7deea54ad21adc0f3fc0f0845ef2f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39290913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afbd3b51c2a9248ebbe471132f8a5e7968ba3dea9acea6e8c088e48a0d12fad4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 06 Mar 2024 16:28:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Mar 2024 16:28:12 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_VERSION=8.2.19
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.19.tar.xz.asc
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_SHA256=aecd63f3ebea6768997f5c4fccd98acbf897762ed5fc25300e846197a9485c13
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 06 Mar 2024 16:28:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 06 Mar 2024 16:28:12 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 06 Mar 2024 16:28:12 GMT
RUN docker-php-ext-enable sodium
# Wed, 06 Mar 2024 16:28:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Mar 2024 16:28:12 GMT
WORKDIR /var/www/html
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 06 Mar 2024 16:28:12 GMT
STOPSIGNAL SIGQUIT
# Wed, 06 Mar 2024 16:28:12 GMT
EXPOSE 9000
# Wed, 06 Mar 2024 16:28:12 GMT
CMD ["php-fpm"]
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 06 Mar 2024 16:28:12 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_VERSION=7.100
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.100.tar.gz
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_MD5=e1e0963944555bee14bf54af5467192a
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13897fa07479841b7362218b636f8c05c19a0cf40407ac05f337e5ef28f00394`  
		Last Modified: Sat, 16 Mar 2024 02:37:37 GMT  
		Size: 2.7 MB (2682503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ef497c75c3ec43061ab5cb29b2fafede17c4a16c0fe6374edb450b8ed8a8aa`  
		Last Modified: Sat, 16 Mar 2024 02:37:36 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11470412841e18160622c7c4debf9802a12a4b3cf6c882a63d8689cdda4a0561`  
		Last Modified: Sat, 16 Mar 2024 02:37:36 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d798c687c994aa72f43f34079f381bdbb76dbdf706e02e6eea3038a5f2e1669`  
		Last Modified: Fri, 10 May 2024 23:22:27 GMT  
		Size: 12.1 MB (12114798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bddae8afe55766ca6916131cc4496c5ccee8b92543c32600b5cd4a6f14b41f9`  
		Last Modified: Fri, 10 May 2024 23:22:27 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab5242c4bbff74880f46f054643f27472098ba3e979f66621697078c1a66b5f8`  
		Last Modified: Fri, 10 May 2024 23:22:45 GMT  
		Size: 15.2 MB (15192558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abb97d8dc59dcbad050b76a5eda3f23b264f32d510efbd01607fe8ce944dd990`  
		Last Modified: Fri, 10 May 2024 23:22:42 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76aeccebd0a21dd9543859a4e17b6e118174d26eac1a520ec7aeb08f3ae5b3bd`  
		Last Modified: Fri, 10 May 2024 23:22:42 GMT  
		Size: 19.0 KB (18966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca21c68e73c612cdeb85b1ddb53af78ecfd9be4015395f9cdc93ccbf72165c0`  
		Last Modified: Fri, 10 May 2024 23:22:42 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34b7066f841b41aebda03ca569fc837f9c639f5b4f1450ff5a49f44c897fba2`  
		Last Modified: Fri, 10 May 2024 23:50:54 GMT  
		Size: 2.4 MB (2439588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d838b6511aedbb6a54be81282dac2095209494b72cb8d8ab24d049ee458b350`  
		Last Modified: Fri, 10 May 2024 23:50:54 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8650a6f0a858ff3210c91385749d070ba9107985a7cfff5bfce59f4591fc58`  
		Last Modified: Fri, 10 May 2024 23:50:55 GMT  
		Size: 3.4 MB (3425994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-fpm-alpine3.18` - unknown; unknown

```console
$ docker pull drupal@sha256:95ed586792f0f12094df3962b66d0fee6f05644e565fd711d9c46e1a273479be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 KB (289843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f711240341fba7838dc4766da6e7e77cc76c502b6d2b6a9d0e39d98293595128`

```dockerfile
```

-	Layers:
	-	`sha256:355fc3d1c5d1d51f18fdf60abca71f06d623334a758d74d000f48b3769e2005b`  
		Last Modified: Fri, 10 May 2024 23:50:54 GMT  
		Size: 266.9 KB (266927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e2ce2532804cde876c30d40b4b064ef9a6b320f7549eb3e6175904ffcc43816`  
		Last Modified: Fri, 10 May 2024 23:50:54 GMT  
		Size: 22.9 KB (22916 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-fpm-alpine3.18` - linux; arm variant v6

```console
$ docker pull drupal@sha256:b584a99d31c7457de60e182008664422bc2ba33b56423dbae100f131f30f6ae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.0 MB (37017975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd7ef0320f57f11536aea437d4419fd606d232066196c48cdbcbed9379bb0093`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 06 Mar 2024 16:28:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Mar 2024 16:28:12 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_VERSION=8.2.19
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.19.tar.xz.asc
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_SHA256=aecd63f3ebea6768997f5c4fccd98acbf897762ed5fc25300e846197a9485c13
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 06 Mar 2024 16:28:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 06 Mar 2024 16:28:12 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 06 Mar 2024 16:28:12 GMT
RUN docker-php-ext-enable sodium
# Wed, 06 Mar 2024 16:28:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Mar 2024 16:28:12 GMT
WORKDIR /var/www/html
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 06 Mar 2024 16:28:12 GMT
STOPSIGNAL SIGQUIT
# Wed, 06 Mar 2024 16:28:12 GMT
EXPOSE 9000
# Wed, 06 Mar 2024 16:28:12 GMT
CMD ["php-fpm"]
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 06 Mar 2024 16:28:12 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_VERSION=7.100
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.100.tar.gz
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_MD5=e1e0963944555bee14bf54af5467192a
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a5334375d5d53ab2cbe7e8154282924c3ca1c797b751fcdd7879af12c63b90`  
		Last Modified: Sat, 16 Mar 2024 01:02:58 GMT  
		Size: 2.7 MB (2688469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2085b07fdb89abbb9be7808c25c7ec1a393842c3f295e51dad0c4913e651a5a5`  
		Last Modified: Sat, 16 Mar 2024 01:02:56 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23b0507453de6ba0f1321106e52d805d11981b5f62544697a6a01ed7d83ac75e`  
		Last Modified: Sat, 16 Mar 2024 01:02:56 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18863cd27885cb7cac873741db702f41a37cc356a1f094a7506e55a9c441c880`  
		Last Modified: Fri, 10 May 2024 21:44:22 GMT  
		Size: 12.1 MB (12114779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5dd6e04bcf90c5f397d52c8875eb06f546734d858933c4ec52df8c94810a2f7`  
		Last Modified: Fri, 10 May 2024 21:44:20 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1236c42560b823b43d467b30b578c7b59dd34e2b9f1765d9919bb74ab3a5a74`  
		Last Modified: Fri, 10 May 2024 21:44:41 GMT  
		Size: 13.8 MB (13753307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e06120eff340607d5dd253ceb27042f9a1b2f6b9c4852dd425189f83db3af1b4`  
		Last Modified: Fri, 10 May 2024 21:44:37 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89573f591e209f61ed92d0d0e7bee9b6d192f37a2ab496d3c1c625dadd65d561`  
		Last Modified: Fri, 10 May 2024 21:44:37 GMT  
		Size: 18.8 KB (18792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cac6836b707003d3235fa15e76118cec420797bdac9e88096c46c477afbf5c1d`  
		Last Modified: Fri, 10 May 2024 21:44:38 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750651f7b37c5db8313ccebb670a3fa0ec836f5c43baf2fe8f0307d695c6a445`  
		Last Modified: Fri, 10 May 2024 22:56:45 GMT  
		Size: 1.9 MB (1855608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c187d06c31dce42e9c425e0c69728283f57cc4cfe85d4198454eaabfc9e8cbad`  
		Last Modified: Fri, 10 May 2024 22:56:44 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c5625bf447b0edd4ef39acbb8193e5d07d300a08aeb16132586994c4529c427`  
		Last Modified: Fri, 10 May 2024 23:00:47 GMT  
		Size: 3.4 MB (3425994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-fpm-alpine3.18` - unknown; unknown

```console
$ docker pull drupal@sha256:4dbaf5bae2abe740db67fa1315d833cab2d9feed78593806941c7df2fa272892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 KB (21152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5300d47ee51cdf4eef952283084f6ebb309a7a4da4772e7165cc2134b537cf0c`

```dockerfile
```

-	Layers:
	-	`sha256:9ff4ecea22000aa6832f60bfdec4eb109931d76b0b64bf85ce7a7ff2e8237dbc`  
		Last Modified: Fri, 10 May 2024 23:00:46 GMT  
		Size: 21.2 KB (21152 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-fpm-alpine3.18` - linux; arm variant v7

```console
$ docker pull drupal@sha256:e3ea8375e0d4d880bfa4c0c2d9cc38fb87ccc19aa8c42bb6498af0632fa2c9c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.6 MB (35609105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f9388a036dc606d0e84903597881d3acf26d4eac4df81f35182da707d54cb3`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 06 Mar 2024 16:28:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Mar 2024 16:28:12 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_VERSION=8.2.19
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.19.tar.xz.asc
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_SHA256=aecd63f3ebea6768997f5c4fccd98acbf897762ed5fc25300e846197a9485c13
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 06 Mar 2024 16:28:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 06 Mar 2024 16:28:12 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 06 Mar 2024 16:28:12 GMT
RUN docker-php-ext-enable sodium
# Wed, 06 Mar 2024 16:28:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Mar 2024 16:28:12 GMT
WORKDIR /var/www/html
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 06 Mar 2024 16:28:12 GMT
STOPSIGNAL SIGQUIT
# Wed, 06 Mar 2024 16:28:12 GMT
EXPOSE 9000
# Wed, 06 Mar 2024 16:28:12 GMT
CMD ["php-fpm"]
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 06 Mar 2024 16:28:12 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_VERSION=7.100
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.100.tar.gz
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_MD5=e1e0963944555bee14bf54af5467192a
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877c30b1f72f1526cddc021d2b859d86b5a8d0e2aabe709882a5d7cc8dd57bb8`  
		Last Modified: Sat, 16 Mar 2024 11:02:08 GMT  
		Size: 2.5 MB (2528499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:844fe925ffab3b3d464c27f2e2642ae7ef7ac6628fea88ca307550162a6d5f72`  
		Last Modified: Sat, 16 Mar 2024 11:02:07 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e49f0a3ae26a8cfcb5fbc56873fa0387b44be5fbfb7bd5a8256889166393c75d`  
		Last Modified: Sat, 16 Mar 2024 11:02:07 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c613e80efaa4a0bdd0595c899e65545955aeac9919b5ec944f027764f61cf179`  
		Last Modified: Fri, 10 May 2024 22:49:00 GMT  
		Size: 12.1 MB (12114800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7397110a2899eb23146eb4439a9fe083f40268888ee4f6f0a27bd3834579272`  
		Last Modified: Fri, 10 May 2024 22:48:58 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327a6ea1569d2842c74d277e43117d2cf61b53a25431eec6ec144190ade2841d`  
		Last Modified: Fri, 10 May 2024 22:49:16 GMT  
		Size: 12.9 MB (12884006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb9fd9e4c59811e6d5fd61e9554eadaac73be88928802357b567a948f5119db6`  
		Last Modified: Fri, 10 May 2024 22:49:14 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c634dd89b613a7240c18c34562193fb5adb31bb97bcfe9e2deb598d08e95716e`  
		Last Modified: Fri, 10 May 2024 22:49:14 GMT  
		Size: 18.8 KB (18783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904d9e4b2a746aa60e905c65414abcc7c36a51d5bf68db454c1eb3ee1c153946`  
		Last Modified: Fri, 10 May 2024 22:49:15 GMT  
		Size: 9.2 KB (9174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc27045957ad2d916b387ad6b71d8fee765c7bdf46344c4385a13d68120f719b`  
		Last Modified: Sat, 11 May 2024 01:25:57 GMT  
		Size: 1.7 MB (1721675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc2796d035752e738ae7fe228133fcb62f15ef31f0f59964449f72467f0b999`  
		Last Modified: Sat, 11 May 2024 01:25:57 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3457596c323c7b801fe21a01cb6214f0f6e5556e354f776e514a74c9a8db398`  
		Last Modified: Sat, 11 May 2024 01:33:41 GMT  
		Size: 3.4 MB (3425990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-fpm-alpine3.18` - unknown; unknown

```console
$ docker pull drupal@sha256:30d00d5b06872cf050728778fed3e0ec6929770d88c3b10c5d01e94a36a5981e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.7 KB (285736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc2c4bf1dcb080c45525e6372ff69cd2fddf2b143965cec6eae991e0a97f09d`

```dockerfile
```

-	Layers:
	-	`sha256:00e698a8bd41b878e6841737b7a6c51b0f8c733027a18e7fece0a6d09b490f16`  
		Last Modified: Sat, 11 May 2024 01:33:41 GMT  
		Size: 264.4 KB (264365 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8a4563a5da83b7ec55bdbf477f68b92696b98d294c9f57cd7f72858fdca1944`  
		Last Modified: Sat, 11 May 2024 01:33:41 GMT  
		Size: 21.4 KB (21371 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-fpm-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:32969e84c35607988c5ce794aa30cfabf0b9958ba13534a7090f5b92f66c9438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39469352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4bad19c427c61dcec5e91222a841ea6ccc012b8c185a5dc21302b3768119bb`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 06 Mar 2024 16:28:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Mar 2024 16:28:12 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_VERSION=8.2.18
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.18.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.18.tar.xz.asc
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_SHA256=44b306fc021e56441f691da6c3108788bd9e450f293b3bc70fcd64b08dd41a50
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 06 Mar 2024 16:28:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 06 Mar 2024 16:28:12 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 06 Mar 2024 16:28:12 GMT
RUN docker-php-ext-enable sodium
# Wed, 06 Mar 2024 16:28:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Mar 2024 16:28:12 GMT
WORKDIR /var/www/html
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 06 Mar 2024 16:28:12 GMT
STOPSIGNAL SIGQUIT
# Wed, 06 Mar 2024 16:28:12 GMT
EXPOSE 9000
# Wed, 06 Mar 2024 16:28:12 GMT
CMD ["php-fpm"]
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 06 Mar 2024 16:28:12 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_VERSION=7.100
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.100.tar.gz
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_MD5=e1e0963944555bee14bf54af5467192a
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e601a28173344b71be71b0d7a2633c23c69f25ec74040afe605a768aacd30a89`  
		Last Modified: Sat, 16 Mar 2024 02:18:54 GMT  
		Size: 2.7 MB (2721124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f164a523c27bde7c2353e22af7d9bdd2228101eb5ace7722e7a8716db495422`  
		Last Modified: Sat, 16 Mar 2024 02:18:53 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de840efe1c7b496ed20ba13864f968f886917e80308d87b4132fc087ac38a2c6`  
		Last Modified: Sat, 16 Mar 2024 02:18:53 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d59bffb9f02bfef89da4a3e88f30dab2ea0af2d0497f7986b78bcd4d9b5bec3`  
		Last Modified: Thu, 11 Apr 2024 20:22:17 GMT  
		Size: 12.1 MB (12110390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e108022b8a124398612388650d8c8908e34ba0acede5344064a9f4f2783141c1`  
		Last Modified: Thu, 11 Apr 2024 20:22:16 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ab742d3ed4c468da9e43f32e1a25540b629f4ebd0c1beafb68311fe8c68d8a`  
		Last Modified: Thu, 11 Apr 2024 20:22:34 GMT  
		Size: 15.1 MB (15139979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2700972eafe59941b4880016fbd953879fcff258e49b0b8c1706b2763d848df3`  
		Last Modified: Thu, 11 Apr 2024 20:22:31 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69fcbaa5cf40514424aab1763b685dad1aa46239b76be8e5c374b4399de77614`  
		Last Modified: Thu, 11 Apr 2024 20:22:31 GMT  
		Size: 18.7 KB (18748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0a82c35ddc3445f13eba5327e193ef9964538a791b774f2091c4d850717dd9`  
		Last Modified: Thu, 11 Apr 2024 20:22:31 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87383ed9f0b84a4ee64f3ce3f50c37b6373d367898013a2d33cc5c936abf09d9`  
		Last Modified: Fri, 12 Apr 2024 03:01:53 GMT  
		Size: 2.7 MB (2705793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80c01e6d8c556621bc7aef5ff7bb1c3d160ef2b6311a1766e27806e5a9d7283e`  
		Last Modified: Fri, 12 Apr 2024 03:01:53 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b74cb2891f4895aa9b6712828bcf8f8779b38263bcc0701f8fcafde6d38331`  
		Last Modified: Fri, 12 Apr 2024 03:01:54 GMT  
		Size: 3.4 MB (3425993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-fpm-alpine3.18` - unknown; unknown

```console
$ docker pull drupal@sha256:cb5b0e7fcfbbb5c0c1d7622a3a1a3ac7c49e3e5061f0804d3a958c21192ba253
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.3 KB (287270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b7c427669ab72c279d74db67c1e301c4981c9f5936f10d3154e867560e942f7`

```dockerfile
```

-	Layers:
	-	`sha256:ba9de4420a4cfb671b41d0a9f105d223e51c76f7c3d9c5421659f497154fa2a0`  
		Last Modified: Fri, 12 Apr 2024 03:01:51 GMT  
		Size: 264.4 KB (264352 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1432a1c8dc99dc57ebad35ad1d9f28b5eb0c02b9c3f0ea820b1b41d6e7440799`  
		Last Modified: Fri, 12 Apr 2024 03:01:51 GMT  
		Size: 22.9 KB (22918 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-fpm-alpine3.18` - linux; 386

```console
$ docker pull drupal@sha256:8fdce8e9a5766292fe0995cffaaaf51bc50827e6a511c9a5166674cd7ec82e6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39177138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1fab5b0c648c045094d369ff62e0850a5c07d25fcbfb406e104048bd5dfcd40`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 06 Mar 2024 16:28:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Mar 2024 16:28:12 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_VERSION=8.2.19
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.19.tar.xz.asc
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_SHA256=aecd63f3ebea6768997f5c4fccd98acbf897762ed5fc25300e846197a9485c13
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 06 Mar 2024 16:28:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 06 Mar 2024 16:28:12 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 06 Mar 2024 16:28:12 GMT
RUN docker-php-ext-enable sodium
# Wed, 06 Mar 2024 16:28:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Mar 2024 16:28:12 GMT
WORKDIR /var/www/html
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 06 Mar 2024 16:28:12 GMT
STOPSIGNAL SIGQUIT
# Wed, 06 Mar 2024 16:28:12 GMT
EXPOSE 9000
# Wed, 06 Mar 2024 16:28:12 GMT
CMD ["php-fpm"]
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 06 Mar 2024 16:28:12 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_VERSION=7.100
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.100.tar.gz
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_MD5=e1e0963944555bee14bf54af5467192a
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af34684a7b3881a9a977f355fa735564b2d2e35a3af88d57a1c3241f81e703d8`  
		Last Modified: Sat, 16 Mar 2024 05:00:34 GMT  
		Size: 2.7 MB (2727209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19299d6b146365bdee94bccc9339519a9b8461e518c86a56894baae815451c66`  
		Last Modified: Sat, 16 Mar 2024 05:00:33 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e310507a1fd78ab348b9f374ef37b46b74e45d08fa7559fe1f07dcd280936d21`  
		Last Modified: Sat, 16 Mar 2024 05:00:33 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a018abcd3e4490872309e1927d20b4c98af3453f4752dfdfbf850e754e646d`  
		Last Modified: Sat, 11 May 2024 00:59:37 GMT  
		Size: 12.1 MB (12114790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22eb47b43272e9fe534c00a1e1e3e7fd3736555addb16b94f3121ae01ab7d09e`  
		Last Modified: Sat, 11 May 2024 00:59:35 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520a42321135e99260ab2ca8be7b50815e64c8b02d77cc80664a91249c08f656`  
		Last Modified: Sat, 11 May 2024 00:59:57 GMT  
		Size: 15.2 MB (15206063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fa4e775e329ed3c8ce7de86a46f0b6bf4d406f80d0c782e6a011396b07aa00`  
		Last Modified: Sat, 11 May 2024 00:59:53 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:939ca26ce576cb2a366f0fa0f1bf16ad2789789db04d992bb4c224e3b403d44d`  
		Last Modified: Sat, 11 May 2024 00:59:53 GMT  
		Size: 18.9 KB (18941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ac9389af40dbbddb0a323dcdebf5e15a0ee701484457089d7ca55cbac1fddb`  
		Last Modified: Sat, 11 May 2024 00:59:53 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e56e2ed74a78044957b2120fffb199b120b8bf45b6f994cea2b35b8603b7143`  
		Last Modified: Sat, 11 May 2024 01:53:31 GMT  
		Size: 2.4 MB (2431111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0ebfce989aa54a24c65ea6957655c034eb4a8963d309da57d424c082c1f736`  
		Last Modified: Sat, 11 May 2024 01:53:32 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0054295ed93abb0fe52c4401477cedce2471ac86707462c99f7ecadc23a6728`  
		Last Modified: Sat, 11 May 2024 01:53:32 GMT  
		Size: 3.4 MB (3425989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-fpm-alpine3.18` - unknown; unknown

```console
$ docker pull drupal@sha256:2ffcb9687cc30b8eeb5ff336731981b86e6125723ea70e3e977e46545d9b39f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.8 KB (289805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5419ff266960155e17bbc261b8d1da92c61817c74d1f36a0581985b4b3bd08e1`

```dockerfile
```

-	Layers:
	-	`sha256:147d9b77d78f616a89d5543fdf7c27d8dc45c7c6a705cbf80a8ce528a9d4b4c8`  
		Last Modified: Sat, 11 May 2024 01:53:30 GMT  
		Size: 266.9 KB (266912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c2d9b5d4ecd0775fc289d71456206a278445bba09b7a13999e1e0c279dc313b`  
		Last Modified: Sat, 11 May 2024 01:53:30 GMT  
		Size: 22.9 KB (22893 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-fpm-alpine3.18` - linux; ppc64le

```console
$ docker pull drupal@sha256:5e6ddaadd6a2cbc4285c6b90a20d1cce1387e83efa75c0dcd869af338ffc5757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.4 MB (39427230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d2c3cba314671afcf2d1e01186394db676229ffed65040c8c53a4c0db913300`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 06 Mar 2024 16:28:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Mar 2024 16:28:12 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_VERSION=8.2.19
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.19.tar.xz.asc
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_SHA256=aecd63f3ebea6768997f5c4fccd98acbf897762ed5fc25300e846197a9485c13
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 06 Mar 2024 16:28:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 06 Mar 2024 16:28:12 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 06 Mar 2024 16:28:12 GMT
RUN docker-php-ext-enable sodium
# Wed, 06 Mar 2024 16:28:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Mar 2024 16:28:12 GMT
WORKDIR /var/www/html
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 06 Mar 2024 16:28:12 GMT
STOPSIGNAL SIGQUIT
# Wed, 06 Mar 2024 16:28:12 GMT
EXPOSE 9000
# Wed, 06 Mar 2024 16:28:12 GMT
CMD ["php-fpm"]
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 06 Mar 2024 16:28:12 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_VERSION=7.100
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.100.tar.gz
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_MD5=e1e0963944555bee14bf54af5467192a
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f897572fdb0807137a76cab817abd60a161327c5d138611fa6f8060fb682bd99`  
		Last Modified: Sat, 16 Mar 2024 06:57:13 GMT  
		Size: 2.8 MB (2768091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a846157c6fa19794b64707b10dbb8a75987a57c45cf63601f1631ede934205`  
		Last Modified: Sat, 16 Mar 2024 06:57:13 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a69b4d780d64beeba4090b102a9d5c1c555acfb75602a0b576e0480391db42`  
		Last Modified: Sat, 16 Mar 2024 06:57:13 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf11c95498f940868b1941b01e7fd168a504792183807a04fff057750e4d47b6`  
		Last Modified: Fri, 10 May 2024 23:10:22 GMT  
		Size: 12.1 MB (12114779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2f719abc9c7bd8e4e87fced8d572d121d26c3487db54e360e54b77c2e71b4c`  
		Last Modified: Fri, 10 May 2024 23:10:21 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d288f1e81ac82ccb8623a38974de20b10e0f5a82f76a4cee4139010f19a04d11`  
		Last Modified: Fri, 10 May 2024 23:10:42 GMT  
		Size: 15.5 MB (15478911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21c9cbefb4f56fb63a7bbf6d736b41119ed271f9973b97f72b0ee9685dd7407f`  
		Last Modified: Fri, 10 May 2024 23:10:39 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6432fd6cca236248af16eb1241c87775850113160999cc69841c77c850411a9`  
		Last Modified: Fri, 10 May 2024 23:10:39 GMT  
		Size: 18.7 KB (18738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c33b6a4ca856aac42136f8102250c398976856c83e137db90bcbdcc6d014260`  
		Last Modified: Fri, 10 May 2024 23:10:39 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a716a69e7c51ad3e9aca0b706e252b450bb2975276ad703d3809dd71783f89`  
		Last Modified: Sat, 11 May 2024 02:39:41 GMT  
		Size: 2.3 MB (2258260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16948f693bdf6165ba09c92beea0a5f84ff9653d89c593eb73acd93cb238b652`  
		Last Modified: Sat, 11 May 2024 02:39:41 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8abe26e0fc6b3936489b00f8e2c34007fd7b0606480e3f89b1afed1ad9c6369`  
		Last Modified: Sat, 11 May 2024 02:39:41 GMT  
		Size: 3.4 MB (3425996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-fpm-alpine3.18` - unknown; unknown

```console
$ docker pull drupal@sha256:cdbeb60f38505f30a86e244250d583c9e3adc24106f22c0c02c534ea3ec51c74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.4 KB (285359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4b878e1ebe780c500774c22473e9c2b7bd402db2073f17ce7ab3b0e8a3e0606`

```dockerfile
```

-	Layers:
	-	`sha256:7449e3b28bc8e4f577babe5f3f0be417d013c44a392fbd5b7537c0417f5e8829`  
		Last Modified: Sat, 11 May 2024 02:39:39 GMT  
		Size: 262.4 KB (262413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f34d23896e37f31115cc2b87541fd3ebb0cbd55d731c4f26ba7f788a119062a6`  
		Last Modified: Sat, 11 May 2024 02:39:39 GMT  
		Size: 22.9 KB (22946 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.2-fpm-alpine3.18` - linux; s390x

```console
$ docker pull drupal@sha256:610a2c53d1e7c36d3bda8be0f3f8c997d96186f3474796bd50889406a12f244d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.7 MB (37726319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bcdec872cead237e86f1d9b566d06bd6d30caf8db99d2e1457a6b9f67890fb4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 06 Mar 2024 16:28:12 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 06 Mar 2024 16:28:12 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_VERSION=8.2.19
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.19.tar.xz.asc
# Wed, 06 Mar 2024 16:28:12 GMT
ENV PHP_SHA256=aecd63f3ebea6768997f5c4fccd98acbf897762ed5fc25300e846197a9485c13
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 06 Mar 2024 16:28:12 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 06 Mar 2024 16:28:12 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 06 Mar 2024 16:28:12 GMT
RUN docker-php-ext-enable sodium
# Wed, 06 Mar 2024 16:28:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 Mar 2024 16:28:12 GMT
WORKDIR /var/www/html
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 06 Mar 2024 16:28:12 GMT
STOPSIGNAL SIGQUIT
# Wed, 06 Mar 2024 16:28:12 GMT
EXPOSE 9000
# Wed, 06 Mar 2024 16:28:12 GMT
CMD ["php-fpm"]
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 06 Mar 2024 16:28:12 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_VERSION=7.100
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_URL=https://ftp.drupal.org/files/projects/drupal-7.100.tar.gz
# Wed, 06 Mar 2024 16:28:12 GMT
ENV DRUPAL_MD5=e1e0963944555bee14bf54af5467192a
# Wed, 06 Mar 2024 16:28:12 GMT
RUN set -eux; 	curl -fSL "$DRUPAL_URL" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4088d295136a43f57db649bdd26ccbaac0662fd64d2ec39fe32b09232de5c4b`  
		Last Modified: Sat, 16 Mar 2024 14:20:21 GMT  
		Size: 2.8 MB (2792799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46f46b31f919af053c5b1a8211f26d6f9705dec9c62ba4c514ba7cdabf63e144`  
		Last Modified: Sat, 16 Mar 2024 14:20:21 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8db3ceeff0eb576f4d982a7f70af546d2559ab23dae9a7d82247a4ff98fd44`  
		Last Modified: Sat, 16 Mar 2024 14:20:21 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b6b443282ab3a54786c803a6667212504e32d90571d7c788525ce241324d4e7`  
		Last Modified: Sat, 11 May 2024 00:37:34 GMT  
		Size: 12.1 MB (12114789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d6bb1750adf955695cdb5a798d312c0a70a2ca965295efc453a157fb44e4cc`  
		Last Modified: Sat, 11 May 2024 00:37:34 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ec6da4698ce79df69dd513cdf7933a40bf9730d3d2e290be0039737df3b3fc`  
		Last Modified: Sat, 11 May 2024 00:37:50 GMT  
		Size: 14.1 MB (14142544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51fd749f65fe2ddaceb87e49579ed1e64bbbada8b8fe974f33507ff6b7ea0ccb`  
		Last Modified: Sat, 11 May 2024 00:37:47 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b99bff86f4b8b2682344a867ccc56e3f280bc38d80c13864f517c1d2b5746f3`  
		Last Modified: Sat, 11 May 2024 00:37:47 GMT  
		Size: 18.8 KB (18796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:423f7feddd3f3e651db77fc574bd6baf71459a2369fc99b4189401701b0fabed`  
		Last Modified: Sat, 11 May 2024 00:37:47 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37878cd1193fca6d2537bd51bc9e16f548ec280c4d97ff0b39026b74fe1957b1`  
		Last Modified: Sat, 11 May 2024 03:22:15 GMT  
		Size: 2.0 MB (1999898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e06609374f9fef1171cefb000c0e56f04e8345bec8b26a14ded04da604a4ac`  
		Last Modified: Sat, 11 May 2024 03:22:15 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967ebf5bb8e03127096365fc0e7496c2f7e05670bf18b4e3e28811bf086b55c0`  
		Last Modified: Sat, 11 May 2024 03:22:16 GMT  
		Size: 3.4 MB (3425994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.2-fpm-alpine3.18` - unknown; unknown

```console
$ docker pull drupal@sha256:82208456320253be7acac678d725970c573575041e5d788bba299a31438b5c88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.3 KB (285307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b8d59c3628dba66bae94ec6ebd3ddf5563fe56f368abc3fb6de0000ead3066`

```dockerfile
```

-	Layers:
	-	`sha256:3a80f40f0b4644af5c205bccef0a8191d1ec9b64fbc4eed6ddb32c671ffb03b2`  
		Last Modified: Sat, 11 May 2024 03:22:13 GMT  
		Size: 262.4 KB (262391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b8261986ef356f7bdec174c696af12247d83baa77225b6d6fb88c83f19ff9b3`  
		Last Modified: Sat, 11 May 2024 03:22:13 GMT  
		Size: 22.9 KB (22916 bytes)  
		MIME: application/vnd.in-toto+json
