## `drupal:10-fpm-alpine3.20`

```console
$ docker pull drupal@sha256:a1245839316728ef08a6deaf47b48ce92d323092f39e2d339113756958bb6b0c
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

### `drupal:10-fpm-alpine3.20` - linux; amd64

```console
$ docker pull drupal@sha256:0f72601f0467fe2ec02b8e01765da33a26ec5bcd4fa51f0b38f4b04ed6461699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 MB (53790658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131b3ff2805823a86ca1a4a18a98cb38b339416a51c5da3ba85f780de4a1660a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 22 May 2024 18:18:11 GMT
ADD file:e3abcdba177145039cfef1ad882f9f81a612a24c9f044b19f713b95454d2e3f6 in / 
# Wed, 22 May 2024 18:18:12 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 22:49:37 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 29 May 2024 22:49:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 29 May 2024 22:49:39 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 29 May 2024 22:49:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 29 May 2024 22:49:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 29 May 2024 22:49:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 22:49:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 22:49:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 06 Jun 2024 02:42:28 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_VERSION=8.2.20
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.20.tar.xz.asc
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_SHA256=4474cc430febef6de7be958f2c37253e5524d5c5331a7e1765cd2d2234881e50
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 06 Jun 2024 10:04:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 06 Jun 2024 10:04:54 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
RUN docker-php-ext-enable sodium
# Thu, 06 Jun 2024 10:04:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Jun 2024 10:04:54 GMT
WORKDIR /var/www/html
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 06 Jun 2024 10:04:54 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Jun 2024 10:04:54 GMT
EXPOSE 9000
# Thu, 06 Jun 2024 10:04:54 GMT
CMD ["php-fpm"]
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
ENV DRUPAL_VERSION=10.2.7
# Thu, 06 Jun 2024 10:04:54 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Jun 2024 10:04:54 GMT
WORKDIR /opt/drupal
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:d25f557d7f31bf7acfac935859b5153da41d13c41f2b468d16f729a5b883634f`  
		Last Modified: Wed, 22 May 2024 18:18:35 GMT  
		Size: 3.6 MB (3622094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014df3980fae18c782aea9d0723608f946d6d6e8f6125728c16633b2d972368c`  
		Last Modified: Wed, 29 May 2024 23:20:58 GMT  
		Size: 3.3 MB (3267768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:336cedf37d159d49eef4060e02027c6d7a25eee6a23e0cebe098dd2df627e02c`  
		Last Modified: Wed, 29 May 2024 23:20:58 GMT  
		Size: 971.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7c0de909185a283d5194786f7c61bf2d3fa30ebc0cff2e7d21c1258f445f6e5`  
		Last Modified: Wed, 29 May 2024 23:20:57 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aa5a51cc359c7dc05b69e876bc11d7aacd94fdb2ad347848db4475dc95dd7ec`  
		Last Modified: Thu, 06 Jun 2024 22:18:28 GMT  
		Size: 12.1 MB (12118893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc21de623aad8be787aeb6de5a93d9650da55d94416136220a4976c6b1d7423`  
		Last Modified: Thu, 06 Jun 2024 22:18:27 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c973bf2f379c168c41d4fbe2f3a912a8bd1e58f81fd7d547d2f1f929ea8df345`  
		Last Modified: Thu, 06 Jun 2024 22:18:53 GMT  
		Size: 12.9 MB (12864129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:987d8b47c1bc8f5744bd1be304f04fb5098c94ab7a1c07dd1e8f1f464b1a46e9`  
		Last Modified: Thu, 06 Jun 2024 22:18:51 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a7bff2034a0c89b74e4a12b544e59ff63f6806293fefaa0f10cc78d93ddbbad`  
		Last Modified: Thu, 06 Jun 2024 22:18:51 GMT  
		Size: 19.7 KB (19681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97ab48817ef3af029ae0e073f18b1c1eaf9483af35dc4a304d097aa0b2ca4bd4`  
		Last Modified: Thu, 06 Jun 2024 22:18:51 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3101e6d29427b4f55ec6a6f4a9c91035f9e6d08437aa1d0cea7450351d3cca`  
		Last Modified: Fri, 07 Jun 2024 01:04:01 GMT  
		Size: 1.9 MB (1897714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf3be96e0105b5696c7e4d81c8e1f050fe876b0223ba85e818eef5b156f09e27`  
		Last Modified: Fri, 07 Jun 2024 01:04:01 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58da6eb6b7da95e45f29b65d5a8c62e7704459419b15958f8ba0f02affade79f`  
		Last Modified: Fri, 07 Jun 2024 01:04:01 GMT  
		Size: 724.7 KB (724732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83e4b07d1a59b269b4291533b6555bba44be368296270bceb00cd9a9f0a71376`  
		Last Modified: Fri, 07 Jun 2024 01:04:01 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e250a5de3c3bc0ff2d03fa61756c8b193ae91f2191bfb67da80c8f1398926f21`  
		Last Modified: Fri, 07 Jun 2024 01:04:02 GMT  
		Size: 19.3 MB (19261862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:7c991ede24a37a6d836042288a42816f8a5e241890c9644f6d2871bd48803046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.0 KB (367963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a8243bc2a14fbd49cec882eae52f987f938aa2289370ceebab14d6b5d2ad46`

```dockerfile
```

-	Layers:
	-	`sha256:3deec1c5d1511382c6e15a7b6aefa55854766dda33619b3fafd06e12ff25ba58`  
		Last Modified: Fri, 07 Jun 2024 01:04:01 GMT  
		Size: 332.9 KB (332909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0fc700c0e6445fa408bb99e2302b5d59d3de8f4ad51455b94ac7d360b94754da`  
		Last Modified: Fri, 07 Jun 2024 01:04:01 GMT  
		Size: 35.1 KB (35054 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.20` - linux; arm variant v6

```console
$ docker pull drupal@sha256:6b2a19e649f0b9e3af07b049dd937095aa992ebe4ac8d9ea2ce0745d9059073c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51851778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fdd3cb18cd11050d7d882db3927e373e910ab02f8e894709d91009069c47470`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 22 May 2024 17:56:54 GMT
ADD file:5103c8a26cd2dfa76f84be7e1886df206b2131d04cf3079dfd1b6385cc796428 in / 
# Wed, 22 May 2024 17:56:55 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 21:50:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 29 May 2024 21:50:43 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 29 May 2024 21:50:44 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 29 May 2024 21:50:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 29 May 2024 21:50:45 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 29 May 2024 21:50:45 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 21:50:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 21:50:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 29 May 2024 22:26:16 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_VERSION=8.2.20
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.20.tar.xz.asc
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_SHA256=4474cc430febef6de7be958f2c37253e5524d5c5331a7e1765cd2d2234881e50
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 06 Jun 2024 10:04:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 06 Jun 2024 10:04:54 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
RUN docker-php-ext-enable sodium
# Thu, 06 Jun 2024 10:04:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Jun 2024 10:04:54 GMT
WORKDIR /var/www/html
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 06 Jun 2024 10:04:54 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Jun 2024 10:04:54 GMT
EXPOSE 9000
# Thu, 06 Jun 2024 10:04:54 GMT
CMD ["php-fpm"]
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
ENV DRUPAL_VERSION=10.2.7
# Thu, 06 Jun 2024 10:04:54 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Jun 2024 10:04:54 GMT
WORKDIR /opt/drupal
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:b0da55d51ed2f4a2e9c4e3ca1e420bac26a1a37098e2f1437841049c51df7320`  
		Last Modified: Wed, 22 May 2024 17:57:17 GMT  
		Size: 3.4 MB (3365055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22fbde2bc87fb1211abfaa9d742eb1626779b6e008e3910fc9e86d002d2c18b4`  
		Last Modified: Wed, 29 May 2024 22:46:54 GMT  
		Size: 3.3 MB (3256537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d3d57f281c14652f66f7ed738a118a66f8f9fe01923de337160db44abde6c2e`  
		Last Modified: Wed, 29 May 2024 22:46:53 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df4f95681943fb2de91ae5af31702772ccab2891b4971de5a53ad5b5f06489e`  
		Last Modified: Wed, 29 May 2024 22:46:53 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a922e65f3d83ee41fbad3cf5eddf0c301f7c4156f412e4f954e0ecb9b24036fb`  
		Last Modified: Thu, 06 Jun 2024 20:19:45 GMT  
		Size: 12.1 MB (12118899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b1e9d56dc15e28920aac538540951170444760842266104ee7e7c514a483f63`  
		Last Modified: Thu, 06 Jun 2024 20:19:44 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a865af112206543d9315d4fe8d37897317c8c6750c34be97ac76fe662dc86efe`  
		Last Modified: Thu, 06 Jun 2024 20:20:12 GMT  
		Size: 11.7 MB (11709119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89dec66560ac355555a040c634b9ea28da9f83b7f84da75a6dfa0080b5195f71`  
		Last Modified: Thu, 06 Jun 2024 20:20:10 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cc5d2a4f3dbba489909bab372fb15a6bf9db0aee6a3b359a95afc125c0b1b4a`  
		Last Modified: Thu, 06 Jun 2024 20:20:08 GMT  
		Size: 19.5 KB (19489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b4efddc2d4023ab20639839ea7d7eecb9596c33c61bf6d198640f345912971e`  
		Last Modified: Thu, 06 Jun 2024 20:20:08 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a85907d2443488929b4b8e698c67d0bdb9269e1c188dc54964b4d264b59a2a`  
		Last Modified: Thu, 06 Jun 2024 21:34:44 GMT  
		Size: 1.4 MB (1382269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb71c37bafdc55f39778d4e54da19adaed03dcf55d9f9314d7806ad1a362a505`  
		Last Modified: Thu, 06 Jun 2024 21:34:44 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416d29e25e77bad3c5e19b34b2048fadf6c13b17eea7fdf3d7564a0f48bb34ac`  
		Last Modified: Thu, 06 Jun 2024 21:34:44 GMT  
		Size: 724.7 KB (724734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9a4a12f0540c81e10b9dc8fb6c6e8dbcc9375f15aa16a7379ded3ede668f18`  
		Last Modified: Thu, 06 Jun 2024 21:34:44 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686d0e2c013d552f20a5055f7515da77b9d47c4a2cde9275ad68a30dea17b4c4`  
		Last Modified: Thu, 06 Jun 2024 22:01:59 GMT  
		Size: 19.3 MB (19261891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:99b3b548c7f3d1ec3b6933fc0f3c5ecaf520d8390f3fdeba159e3dcdea975042
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.0 KB (35043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deed9c05b18690aa5866831677e94c63276710d51c57bcf56d3e824161310f7b`

```dockerfile
```

-	Layers:
	-	`sha256:2269c1f78bbc7d78946c28ff62926fa610989c0f2cc099d66f8c68550d1fbb31`  
		Last Modified: Thu, 06 Jun 2024 22:01:58 GMT  
		Size: 35.0 KB (35043 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.20` - linux; arm variant v7

```console
$ docker pull drupal@sha256:d614449eb69896193e2b6fa345f544c57117c4e27ae8af8d2d008a9b85857445
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50547433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ab92426c13cfce16df95b834e940f6d416c5780d357cafc36f14bbea688383e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 22 May 2024 18:07:12 GMT
ADD file:d6a90589cd9e92525c68e44f296baf2a57e5bda9e32ed5f7d45d6ad9a6595e26 in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 22:44:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 29 May 2024 22:44:07 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 29 May 2024 22:44:08 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 29 May 2024 22:44:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 29 May 2024 22:44:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 29 May 2024 22:44:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 22:44:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 22:44:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 29 May 2024 23:12:50 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_VERSION=8.2.20
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.20.tar.xz.asc
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_SHA256=4474cc430febef6de7be958f2c37253e5524d5c5331a7e1765cd2d2234881e50
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 06 Jun 2024 10:04:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 06 Jun 2024 10:04:54 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
RUN docker-php-ext-enable sodium
# Thu, 06 Jun 2024 10:04:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Jun 2024 10:04:54 GMT
WORKDIR /var/www/html
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 06 Jun 2024 10:04:54 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Jun 2024 10:04:54 GMT
EXPOSE 9000
# Thu, 06 Jun 2024 10:04:54 GMT
CMD ["php-fpm"]
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
ENV DRUPAL_VERSION=10.2.7
# Thu, 06 Jun 2024 10:04:54 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Jun 2024 10:04:54 GMT
WORKDIR /opt/drupal
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:8b416cac0b22b1e77fbe2d8d5f2f70f44878497f7c24dd739d8e56b317931303`  
		Last Modified: Wed, 22 May 2024 18:07:30 GMT  
		Size: 3.1 MB (3094035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b726d2ea6325cbe2918171017f17d1d12ab778e5c1d68d663b22b061790803e5`  
		Last Modified: Wed, 29 May 2024 23:37:27 GMT  
		Size: 3.1 MB (3069336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2825cd15ae946086782a856b1d53fadaac330d395b11caf35413766a5903ab25`  
		Last Modified: Wed, 29 May 2024 23:37:26 GMT  
		Size: 970.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47ea0ff5951f7688d6fc2e3212eae4ff67224a3150942bba64e271e0e6878353`  
		Last Modified: Wed, 29 May 2024 23:37:25 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c271788df6c086d2e4f2645e068d723aea25e3fc13ddcce11b8eaffb1b62794`  
		Last Modified: Thu, 06 Jun 2024 21:44:59 GMT  
		Size: 12.1 MB (12118907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5c5fe3d9bd9758d56c7f8de838841a02587788fa3ba38d3946dc877e92e61a`  
		Last Modified: Thu, 06 Jun 2024 21:44:58 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade8991594cb805f832c07138ef1882995eb9b1382ef93350d95b984e11b2b82`  
		Last Modified: Thu, 06 Jun 2024 21:45:25 GMT  
		Size: 11.0 MB (10972192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37a5c1665cbb8ceccc8b9de800becc2f3842f562b4bbf8dcdef72c95d087093f`  
		Last Modified: Thu, 06 Jun 2024 21:45:23 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f9d13c09ad51351e29fd09b08ad986729db9d1b3300ef1089ca6645a36e5d5`  
		Last Modified: Thu, 06 Jun 2024 21:45:23 GMT  
		Size: 19.5 KB (19483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e81c22be8233c21f01f455e327e245c3452c872b85b57048f22c4f1298fbe966`  
		Last Modified: Thu, 06 Jun 2024 21:45:23 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea9d9c0c6146867bb572d691681a7d2e3b90a452928ca9c1f87f40a7c963188`  
		Last Modified: Fri, 07 Jun 2024 02:49:50 GMT  
		Size: 1.3 MB (1273192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4963b8d9a26647f074528519cf8dff964793fb84b57dc8134e21c17dd6729eb`  
		Last Modified: Fri, 07 Jun 2024 02:49:49 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b3af4396a6d198f4c702c06723ad292699067bbb4ffc7938129cbe804089f5`  
		Last Modified: Fri, 07 Jun 2024 02:49:50 GMT  
		Size: 724.7 KB (724732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e969db6054d6819153a50c2a5995734cd6fe53cd4ec6c6cafc98ab760cf7a89`  
		Last Modified: Fri, 07 Jun 2024 02:49:50 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe0cc6720125583b10452a51874f5430a2989d7e37bbf9ebcb18d753f844426`  
		Last Modified: Fri, 07 Jun 2024 03:10:25 GMT  
		Size: 19.3 MB (19261768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:27357c259156b52394727a4829e5c3c4a075432be51e5bb6a1b6ce6638a31327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.7 KB (365725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06763e9cef5d57874a1a477e8c3d4079449261d2e834584dbbdd112b0acdbd91`

```dockerfile
```

-	Layers:
	-	`sha256:f5903ff4d5fb674e8210180936497819c3be89aee2c2c0fed0b5b2654ed82b67`  
		Last Modified: Fri, 07 Jun 2024 03:10:23 GMT  
		Size: 330.5 KB (330463 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fbaed26d460ac3ce93f7e952b047ff5ced981a2c7362c209b899e982f9deae7`  
		Last Modified: Fri, 07 Jun 2024 03:10:23 GMT  
		Size: 35.3 KB (35262 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:5d472f524fd3dbbc296d060a439a65a38dc48ddd2b83d5d1417aa9722dc4bbd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.6 MB (54644877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb4a1f99c9185a465e05c93da79cd177ad1d1f513f6380eb3802123dc0b5958`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 22 May 2024 18:17:27 GMT
ADD file:ceadd994c6d8900884c4a44aa76cf187336921e29afeaa017c4a3d1fc066a6a3 in / 
# Wed, 22 May 2024 18:17:28 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 23:53:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 22 May 2024 23:53:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 22 May 2024 23:53:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 22 May 2024 23:53:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 May 2024 23:53:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 22 May 2024 23:53:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:53:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:53:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 May 2024 23:53:55 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 22 May 2024 23:53:55 GMT
ENV PHP_VERSION=8.2.19
# Wed, 22 May 2024 23:53:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.19.tar.xz.asc
# Wed, 22 May 2024 23:53:55 GMT
ENV PHP_SHA256=aecd63f3ebea6768997f5c4fccd98acbf897762ed5fc25300e846197a9485c13
# Wed, 22 May 2024 23:53:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 22 May 2024 23:53:55 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 22 May 2024 23:53:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 22 May 2024 23:53:55 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 22 May 2024 23:53:55 GMT
RUN docker-php-ext-enable sodium
# Wed, 22 May 2024 23:53:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 May 2024 23:53:55 GMT
WORKDIR /var/www/html
# Wed, 22 May 2024 23:53:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 22 May 2024 23:53:55 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 May 2024 23:53:55 GMT
EXPOSE 9000
# Wed, 22 May 2024 23:53:55 GMT
CMD ["php-fpm"]
# Wed, 22 May 2024 23:53:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 22 May 2024 23:53:55 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 May 2024 23:53:55 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 22 May 2024 23:53:55 GMT
ENV DRUPAL_VERSION=10.2.6
# Wed, 22 May 2024 23:53:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 22 May 2024 23:53:55 GMT
WORKDIR /opt/drupal
# Wed, 22 May 2024 23:53:55 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 22 May 2024 23:53:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:94747bd812346354fd5042870b6e44e5406880a4e6b5736a9cf9c753110df11b`  
		Last Modified: Wed, 22 May 2024 18:17:47 GMT  
		Size: 4.1 MB (4086776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:499c233d91e0b285ef0ee55a1f0788e53ee03c80e7d609f44dfb93d39b760d4b`  
		Last Modified: Wed, 29 May 2024 22:56:13 GMT  
		Size: 3.3 MB (3321187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86d2271fbac7611742e70ef3cf276070acf7876e4bcb10f6841029eb4f88f0f9`  
		Last Modified: Wed, 29 May 2024 22:56:12 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9701985de31ecc58dfb2496e5353c355dc9587a81cddc0dc9043524261c37c5`  
		Last Modified: Wed, 29 May 2024 22:56:12 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb438149249389606376a8ab521d91d96fe72e85cf929f8701e940f0e0b0d8b`  
		Last Modified: Thu, 06 Jun 2024 04:23:09 GMT  
		Size: 12.1 MB (12115115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4315f8265e543b4deb2558254e2059a867cdbc0caa4768a9dd886167ff39a4fa`  
		Last Modified: Thu, 06 Jun 2024 04:23:08 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:358bc0cbbee8550b34b2890cbe1cd2c4056716cfdb68f074e1286946d77a59ab`  
		Last Modified: Thu, 06 Jun 2024 04:23:31 GMT  
		Size: 12.9 MB (12928863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60405d4a5e08a109dccc9d57cf982c9ca82a990704a7b88911807fbeba31e53`  
		Last Modified: Thu, 06 Jun 2024 04:23:29 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b524bfde4d30791673d3edd5a9d467111be95b8a1b4ff8b63f237137aa12b389`  
		Last Modified: Thu, 06 Jun 2024 04:23:29 GMT  
		Size: 19.5 KB (19473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a48e17de799d29b9f879aa34ab1419fdd48184687314561cf499d1b94a87fce`  
		Last Modified: Thu, 06 Jun 2024 04:23:29 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f217282a9068f368a2b0c1f198799dfbf62f864849b9fa86d98a87c26065e975`  
		Last Modified: Thu, 06 Jun 2024 08:23:52 GMT  
		Size: 2.2 MB (2173787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34c7fc55a64ad74cd8674c2314c74eeec547f2bdeaabbec8c3b9a0b6fa01c600`  
		Last Modified: Thu, 06 Jun 2024 08:23:52 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83927e023d0a31e3820c4fee71326808d2e23db95f97a33fe94c7fb6638c5191`  
		Last Modified: Thu, 06 Jun 2024 08:23:52 GMT  
		Size: 724.7 KB (724731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd3184a4f84ee575da247064f2867f41ed82b663e27f523af9e382109f011302`  
		Last Modified: Thu, 06 Jun 2024 08:23:52 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5445e81c740a94953b45d4ee93f98dbcdd097819aa3a9e73340272d3ccc84cfd`  
		Last Modified: Thu, 06 Jun 2024 08:40:59 GMT  
		Size: 19.3 MB (19261156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:df7663de7f2c49c04de22d3b133143e8301ae2326a7b69686c1b0dc587428e29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.0 KB (363994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a75ee8be7a1fc1ecc94699ef6c4ed786fca313de4b3b57a788b749687bbb253c`

```dockerfile
```

-	Layers:
	-	`sha256:35efe307d176676615c1aeb7f14cb4ecbc2edd5e11b2aadb12e5c88004f98fa3`  
		Last Modified: Thu, 06 Jun 2024 08:40:58 GMT  
		Size: 330.5 KB (330531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40dafc727e584707605abd0cb280d7d222941933bd47ede2b9da71b7c4113c67`  
		Last Modified: Thu, 06 Jun 2024 08:40:58 GMT  
		Size: 33.5 KB (33463 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.20` - linux; 386

```console
$ docker pull drupal@sha256:85eae990d2f0fe7d503969900eb470c0ab0eb1194b10ac696cc3818faf166b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54097126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:966a893f13d459e388c33cb36ac7071ea513cd0315d936f9d882193d07116fea`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 22 May 2024 18:05:50 GMT
ADD file:6a4a5e48a600b064b83b954a55f1ddd3352780d69a6fb0ad816258011f5a3e47 in / 
# Wed, 22 May 2024 18:05:51 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 22:27:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 29 May 2024 22:27:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 29 May 2024 22:27:10 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 29 May 2024 22:27:10 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 29 May 2024 22:27:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 29 May 2024 22:27:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 22:27:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 22:27:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 29 May 2024 23:28:55 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_VERSION=8.2.20
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.20.tar.xz.asc
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_SHA256=4474cc430febef6de7be958f2c37253e5524d5c5331a7e1765cd2d2234881e50
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 06 Jun 2024 10:04:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 06 Jun 2024 10:04:54 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
RUN docker-php-ext-enable sodium
# Thu, 06 Jun 2024 10:04:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Jun 2024 10:04:54 GMT
WORKDIR /var/www/html
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 06 Jun 2024 10:04:54 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Jun 2024 10:04:54 GMT
EXPOSE 9000
# Thu, 06 Jun 2024 10:04:54 GMT
CMD ["php-fpm"]
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
ENV DRUPAL_VERSION=10.2.7
# Thu, 06 Jun 2024 10:04:54 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Jun 2024 10:04:54 GMT
WORKDIR /opt/drupal
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:271acb68d2933b32dac564003959c5aea6d5d436c2779e253600ab35d7745465`  
		Last Modified: Wed, 22 May 2024 18:06:11 GMT  
		Size: 3.5 MB (3467181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00308a417566819cf13e2fb7bf876f51ca8fbd112253d246127bbc33958111f1`  
		Last Modified: Thu, 30 May 2024 00:14:44 GMT  
		Size: 3.3 MB (3318570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c7454942da668a8f495b1c84fba87d1e06bc62eaeeb69a615a9c479fa0c391`  
		Last Modified: Thu, 30 May 2024 00:14:43 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9c8ef20ed4a8301005b92779aeca9a7af8e5e2ba027ea76bf0ef3c9a5c7e3d3`  
		Last Modified: Thu, 30 May 2024 00:14:43 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ba28bfd8587e32e9ef589a710a04c91914b152ca4b0dbbb62881a93c790bca`  
		Last Modified: Fri, 07 Jun 2024 00:14:20 GMT  
		Size: 12.1 MB (12118893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:916797e66273299b92de6deb18e377361716395f32d1e6eda3c1f4d0210c2816`  
		Last Modified: Fri, 07 Jun 2024 00:14:18 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a59b4cae6aba66823ac0e462aa55778b9e8b70fea2758e88a97a030758205a0`  
		Last Modified: Fri, 07 Jun 2024 00:14:48 GMT  
		Size: 13.2 MB (13214907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e838e2527a4fe966259d47fb5312ab922692e7afae23c1a09058627cc0af9ef8`  
		Last Modified: Fri, 07 Jun 2024 00:14:45 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551ce11a57ae1e3e427dd53002b87310e1dd058c77817dd01990a9c75350ddb8`  
		Last Modified: Fri, 07 Jun 2024 00:14:45 GMT  
		Size: 19.7 KB (19703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544210d3284a1ed0478f4f0be1e4b667d2e8d7343c7991ee4a0c13bba157162e`  
		Last Modified: Fri, 07 Jun 2024 00:14:45 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9c4905bb1ba2536ad3d188bec78d4e9ec2fb7c97b5bc00ca816b42d1d76dfbd`  
		Last Modified: Fri, 07 Jun 2024 01:57:08 GMT  
		Size: 2.0 MB (1957620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c76ca67485006d8701efdc9cbbc91a8d83fc24056e2d7eb6a48eff41fdfd786`  
		Last Modified: Fri, 07 Jun 2024 01:57:07 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bed5ce515bb7d6eb11dab95296ef0fa2770e7e474550f562661a9476668e757e`  
		Last Modified: Fri, 07 Jun 2024 01:57:08 GMT  
		Size: 724.7 KB (724731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0e8e3c1e0dba522dbefb4e97807e202097e7360127e2813c81ae990db59857e`  
		Last Modified: Fri, 07 Jun 2024 01:57:08 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e4ba790ba771e4a3839a0359b85ee0d06dea921b956f38da773ba7c1f796a61`  
		Last Modified: Fri, 07 Jun 2024 01:57:09 GMT  
		Size: 19.3 MB (19261806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:97e40ce1fe2209e89879891c7e628603b0bfb9c65918e53a80e15014f302fc60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.8 KB (367781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:177aa8674b4b764be0fa339c9fadbc671b6c8c32a2a66ea45b8fd358c03ecd86`

```dockerfile
```

-	Layers:
	-	`sha256:937c8543c4e64ba17ccdf884accbb2709796288614ac0f9e4ddf637706018647`  
		Last Modified: Fri, 07 Jun 2024 01:57:08 GMT  
		Size: 332.8 KB (332824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d53d5b790eb4f82955bc43dd86b0009cf3377800aed3c0892a90435aaf65865d`  
		Last Modified: Fri, 07 Jun 2024 01:57:07 GMT  
		Size: 35.0 KB (34957 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.20` - linux; ppc64le

```console
$ docker pull drupal@sha256:ef35052556b30cfbc611aac9c82de0453fcaa18e69a2ce3204d5005f422f7afd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54136207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891cf756b3b924a9d310b7e79b0bf053eb859a371b08f543ee8fd0fc0fdb962d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 22 May 2024 18:07:11 GMT
ADD file:023435caa2a1f2c4ffa6455de5b3dc6e19c43a35708671eeef36e0166c54eecd in / 
# Wed, 22 May 2024 18:07:12 GMT
CMD ["/bin/sh"]
# Wed, 22 May 2024 23:53:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 22 May 2024 23:53:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 22 May 2024 23:53:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 22 May 2024 23:53:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 May 2024 23:53:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 22 May 2024 23:53:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:53:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 May 2024 23:53:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 May 2024 23:53:55 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 22 May 2024 23:53:55 GMT
ENV PHP_VERSION=8.2.19
# Wed, 22 May 2024 23:53:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.19.tar.xz.asc
# Wed, 22 May 2024 23:53:55 GMT
ENV PHP_SHA256=aecd63f3ebea6768997f5c4fccd98acbf897762ed5fc25300e846197a9485c13
# Wed, 22 May 2024 23:53:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 22 May 2024 23:53:55 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 22 May 2024 23:53:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 22 May 2024 23:53:55 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 22 May 2024 23:53:55 GMT
RUN docker-php-ext-enable sodium
# Wed, 22 May 2024 23:53:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 May 2024 23:53:55 GMT
WORKDIR /var/www/html
# Wed, 22 May 2024 23:53:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 22 May 2024 23:53:55 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 May 2024 23:53:55 GMT
EXPOSE 9000
# Wed, 22 May 2024 23:53:55 GMT
CMD ["php-fpm"]
# Wed, 22 May 2024 23:53:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 22 May 2024 23:53:55 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 22 May 2024 23:53:55 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 22 May 2024 23:53:55 GMT
ENV DRUPAL_VERSION=10.2.6
# Wed, 22 May 2024 23:53:55 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 22 May 2024 23:53:55 GMT
WORKDIR /opt/drupal
# Wed, 22 May 2024 23:53:55 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 22 May 2024 23:53:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:fc0288db113f6df5dbde63eac62c59d28df80cd0602675f606e688d365d8bc6a`  
		Last Modified: Wed, 22 May 2024 18:07:33 GMT  
		Size: 3.6 MB (3569846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84e66b0d0146556fc91220949b5af15563e21b230bdaa3c9156ea6266199b48b`  
		Last Modified: Wed, 29 May 2024 23:50:37 GMT  
		Size: 3.4 MB (3395298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8756bd610d512641d28be2382de169df6603336d94be542bd8f86c973a2284d`  
		Last Modified: Wed, 29 May 2024 23:50:35 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57d93c90e46e8ace79138019ef1d9c98710d4629fcc6a574f108b62323e9686a`  
		Last Modified: Wed, 29 May 2024 23:50:35 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdfbf1f9649d2bcac7974b4be5a848903e9c1009d4cad24253acba5e4d84f20d`  
		Last Modified: Wed, 29 May 2024 23:54:33 GMT  
		Size: 12.1 MB (12115138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:196d08a68c174174fc4747bcf1335fad048d7f483f1e21e4ae90010747ac91a0`  
		Last Modified: Wed, 29 May 2024 23:54:33 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15e2832456186b278c8e136323f76f82b5e8ecd00d61f064feb31c32b2ede16`  
		Last Modified: Thu, 06 Jun 2024 03:18:29 GMT  
		Size: 13.4 MB (13357919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f5fe46563f7df71be9bf969d8a7e1df325c8726f67a5504ebcc92a9431d085`  
		Last Modified: Thu, 06 Jun 2024 03:18:27 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a178ee05476d59ba4a813a3202f12337a86f03b559fba2254a314267cf86ff7c`  
		Last Modified: Thu, 06 Jun 2024 03:18:27 GMT  
		Size: 19.5 KB (19476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3832125453b2d83ed6b6079dfa67ec46e21133b49be8b0b2c8af261c84ce48f`  
		Last Modified: Thu, 06 Jun 2024 03:18:27 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5313945b2a6be2a2181a5ee56a49994bbe752f4b14e2f6ad677ce0be0a88886`  
		Last Modified: Thu, 06 Jun 2024 07:32:37 GMT  
		Size: 1.7 MB (1678763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2336e942fb090bda3b3c6690fa0de985a88ec00dfa97c09ab88df53c2387b56a`  
		Last Modified: Thu, 06 Jun 2024 07:32:37 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1879d54d5ace56a8c139321e7b0c4ec09c0ee13466cc2624d34edf559ce2b8`  
		Last Modified: Thu, 06 Jun 2024 07:32:37 GMT  
		Size: 724.7 KB (724729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fa1729a2bb2f8cf6811460272c49adff325cb246f3cb7f0bf16c6e9041def5`  
		Last Modified: Thu, 06 Jun 2024 07:32:37 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e900bb60de502f9819750b2fd7b771244de8e8015ce720c5266c55938e8894`  
		Last Modified: Thu, 06 Jun 2024 07:57:45 GMT  
		Size: 19.3 MB (19261253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:e5f33d723455a4bfac5c13a952edaffea8506e292f2254e96d018ffe8e03f48f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.7 KB (363655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de538d7cc1ef22e8a46461ade90e1a5fed727debaaa5f23a915c5b37a5ff4012`

```dockerfile
```

-	Layers:
	-	`sha256:ec8a7f728a500b248a8af4ab6454abd0336f366b720fa74ab436228fc83bdc1a`  
		Last Modified: Thu, 06 Jun 2024 07:57:44 GMT  
		Size: 328.5 KB (328483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74e953211dcc2f862a365f1d6d113419cb015c8b34f7c3373f9aef1191b6b8b9`  
		Last Modified: Thu, 06 Jun 2024 07:57:43 GMT  
		Size: 35.2 KB (35172 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-alpine3.20` - linux; s390x

```console
$ docker pull drupal@sha256:ddaf45cfdae685460a8dd1e46f57865221b0eee3f8fb045d5db10cdc424ee8bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53486497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d654c02d6cd188c4608b14f1a8288d5566e645781bc62cb48fdbec589439168a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 22 May 2024 18:34:06 GMT
ADD file:97335440b04aac71ca64b9c889e64d1da1913c788e108b6481155248fc670f8b in / 
# Wed, 22 May 2024 18:34:07 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 22:13:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 29 May 2024 22:13:57 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 29 May 2024 22:13:57 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 29 May 2024 22:13:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 29 May 2024 22:13:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 29 May 2024 22:13:58 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 22:13:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 29 May 2024 22:13:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 06 Jun 2024 02:25:46 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_VERSION=8.2.20
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.20.tar.xz.asc
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PHP_SHA256=4474cc430febef6de7be958f2c37253e5524d5c5331a7e1765cd2d2234881e50
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 06 Jun 2024 10:04:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 06 Jun 2024 10:04:54 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 06 Jun 2024 10:04:54 GMT
RUN docker-php-ext-enable sodium
# Thu, 06 Jun 2024 10:04:54 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 06 Jun 2024 10:04:54 GMT
WORKDIR /var/www/html
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 06 Jun 2024 10:04:54 GMT
STOPSIGNAL SIGQUIT
# Thu, 06 Jun 2024 10:04:54 GMT
EXPOSE 9000
# Thu, 06 Jun 2024 10:04:54 GMT
CMD ["php-fpm"]
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
ENV DRUPAL_VERSION=10.2.7
# Thu, 06 Jun 2024 10:04:54 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 06 Jun 2024 10:04:54 GMT
WORKDIR /opt/drupal
# Thu, 06 Jun 2024 10:04:54 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 06 Jun 2024 10:04:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:3b8747b05489980f63da1d2b8e5a444c55777f69540394397b0bc1c76c3e41f2`  
		Last Modified: Wed, 22 May 2024 18:34:48 GMT  
		Size: 3.5 MB (3460340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e59aaf3957408d79830703dc723f179ea56d5e09b1b2358d2a1714ad397bd5f`  
		Last Modified: Wed, 29 May 2024 22:44:35 GMT  
		Size: 3.5 MB (3462557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4bd92d81aa824eaaf12fe4dc2b23834b92dfcb5f95ef3f980bbb78e812f400`  
		Last Modified: Wed, 29 May 2024 22:44:34 GMT  
		Size: 972.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4444860820a15536e66bf9ebb5b9ad505955c852e9a02a4a2aa1afae631eb1`  
		Last Modified: Wed, 29 May 2024 22:44:34 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ce355aafe4ac66d37a8ec2ba8ba7f76d4282d98b76aa3b135d7992437e3f03c`  
		Last Modified: Thu, 06 Jun 2024 22:05:08 GMT  
		Size: 12.1 MB (12118896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4d6d11bf124a1e02422e1a2b379f975de8d23caf963965f37632365e049c1b`  
		Last Modified: Thu, 06 Jun 2024 22:05:07 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313727a92fc3e39d60fa957fc76ddcb47ec127c612f459762b9c5f790466f2a0`  
		Last Modified: Thu, 06 Jun 2024 22:05:28 GMT  
		Size: 12.8 MB (12830083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95caa3c74dcce1c193cc69432d0b9a670d69003ac2ee7ed2e10b221134ea82ae`  
		Last Modified: Thu, 06 Jun 2024 22:05:25 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a60be280299cb6e55a56573f3fe09e1fae0c98f160b59837dd47cebd16b4507`  
		Last Modified: Thu, 06 Jun 2024 22:05:25 GMT  
		Size: 19.5 KB (19481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76021def48f753ac3dbeea5a62bd425d08fc86b8711d55fbc0f54a594acae872`  
		Last Modified: Thu, 06 Jun 2024 22:05:26 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b93535ea00dabbe8326b921a08893fa8d7774cd5a19fcc3b257060b4a3defcc`  
		Last Modified: Fri, 07 Jun 2024 02:39:45 GMT  
		Size: 1.6 MB (1594790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a582b1a3500b05c4ccc65aa09fe979b33594fc1e5f92c6c66ad00a6949d47b2b`  
		Last Modified: Fri, 07 Jun 2024 02:39:45 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0292242e9f932943c18be591816b54c88e37d43841b2fc341e240538287801a8`  
		Last Modified: Fri, 07 Jun 2024 02:39:45 GMT  
		Size: 724.7 KB (724733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:478312cf35b54a903df96adeb43c60fd56c6f0300fcc742c3e4a9376a1052e05`  
		Last Modified: Fri, 07 Jun 2024 02:39:45 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9111ab9f15ffb6a2c687fecae0e6e52c977b3eead1fd2ee52c303d2c89105c5d`  
		Last Modified: Fri, 07 Jun 2024 03:07:58 GMT  
		Size: 19.3 MB (19261820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:6cecc93864bc9c56396de27fdae0fc33d843b23a4e623d3be85e63803fb5551a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.1 KB (361148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c60a3e893d9305957e96aa2686d02a515d55e4c8e160795212786e911ec691`

```dockerfile
```

-	Layers:
	-	`sha256:fd83afeff0940d6ef5916b3bb7aa372bc18bbaff3e059034090bef8734d4c3a9`  
		Last Modified: Fri, 07 Jun 2024 03:07:57 GMT  
		Size: 328.4 KB (328377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9802d75a6042120995488a2d4ed5352ff953d42890ee90bdd133cce87638c9b`  
		Last Modified: Fri, 07 Jun 2024 03:07:57 GMT  
		Size: 32.8 KB (32771 bytes)  
		MIME: application/vnd.in-toto+json
