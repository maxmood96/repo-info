## `mediawiki:legacy-fpm-alpine`

```console
$ docker pull mediawiki@sha256:994b2c3bea0e1fc1619494e3b13d8de4d7a1c5b1b340f02e74bba6c42d4676d2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
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

### `mediawiki:legacy-fpm-alpine` - linux; amd64

```console
$ docker pull mediawiki@sha256:e243562e4581739c1ef8e4719932860672acee38654bdcc3d8c2b6cdce8908f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.3 MB (150291051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef4f364de0b4e7db4cedd04ad93f69183f097489bc7f910e1449b96231d8fda`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 11 Dec 2024 09:15:55 GMT
ADD alpine-minirootfs-3.21.2-x86_64.tar.gz / # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
CMD ["/bin/sh"]
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 11 Dec 2024 09:15:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 11 Dec 2024 09:15:55 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_VERSION=8.1.31
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 11 Dec 2024 09:15:55 GMT
WORKDIR /var/www/html
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
STOPSIGNAL SIGQUIT
# Wed, 11 Dec 2024 09:15:55 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 11 Dec 2024 09:15:55 GMT
CMD ["php-fpm"]
# Thu, 09 Jan 2025 11:23:56 GMT
RUN set -eux; 		apk add --no-cache 		git 		imagemagick 		python3 	; # buildkit
# Thu, 09 Jan 2025 11:23:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		icu-dev 		lua5.1-dev 		oniguruma-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.24; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .mediawiki-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 09 Jan 2025 11:23:56 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 09 Jan 2025 11:23:56 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Thu, 09 Jan 2025 11:23:56 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.42
# Thu, 09 Jan 2025 11:23:56 GMT
ENV MEDIAWIKI_VERSION=1.42.4
# Thu, 09 Jan 2025 11:23:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps 		bzip2 		gnupg 	; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	[ 1.42.4 = "1.42.4" ] && 		sed -i 's|wikimedia/parsoid": "0.19.0"|wikimedia/parsoid": "0.19.1"|' 			composer.json; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apk del --no-network .fetch-deps # buildkit
# Thu, 09 Jan 2025 11:23:56 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:1f3e46996e2966e4faa5846e56e76e3748b7315e2ded61476c24403d592134f0`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.6 MB (3641715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53743d5ee0af96cfd594ff58425ccc8fef420f66d081c88723b8c05b854b994d`  
		Last Modified: Tue, 14 Jan 2025 20:42:11 GMT  
		Size: 3.3 MB (3333598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c5269af5b972a0934c87f25d017702f8c1fb7f13c7cd325a9490d4362f8263`  
		Last Modified: Wed, 08 Jan 2025 18:12:09 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8549079a067cbbd3f9225681e6ad881d4c4147c270ef0209c6ef338bdd3d31`  
		Last Modified: Wed, 08 Jan 2025 18:12:09 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351a601157695f0ca720aa43cf2c02154b5117bb30c14aa49d0fbf859a12dd83`  
		Last Modified: Wed, 08 Jan 2025 18:12:10 GMT  
		Size: 11.9 MB (11938065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b123184127f88cd5ecd66520d1029fabad224f07e7e8dcff122fe39b8f50cd`  
		Last Modified: Tue, 14 Jan 2025 20:42:29 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d1ff2b8f246fe401264375eaa15f73e814af4e368c090813afc822755c87fd`  
		Last Modified: Tue, 14 Jan 2025 20:42:17 GMT  
		Size: 12.7 MB (12701550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:333cacbedb352cde44cf678e4c98de8d3cdc096ff13d026bd4b3b791f89c1442`  
		Last Modified: Tue, 14 Jan 2025 20:42:18 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95aa41a66db7f64cfda2609da1132cb2375cc0c2db2a1d3f2521b9c919e5f26`  
		Last Modified: Wed, 08 Jan 2025 18:12:11 GMT  
		Size: 20.0 KB (20032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f20ec2dc77b57dbe1bb8220c3854f0f3e0561fd2819224979eafee5cc31ebcff`  
		Last Modified: Wed, 08 Jan 2025 18:12:11 GMT  
		Size: 8.9 KB (8876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a66ac20faab86abfc72acd86166957fce820041623f4a1ce63cc1ee4aa2f16f3`  
		Last Modified: Thu, 09 Jan 2025 22:31:01 GMT  
		Size: 23.4 MB (23387928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf87e4c0922ab288f8b130aba3920e74b550ac01b547b127a8235c62f2d3bee`  
		Last Modified: Thu, 09 Jan 2025 22:31:00 GMT  
		Size: 4.8 MB (4841216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54813f9933d2e81cc5c3ecaa3294506200d60533c19635cd0a3b9c3319a1c3bc`  
		Last Modified: Thu, 09 Jan 2025 22:31:00 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2502a8d555c355a030d32044a73cdc2ba5dbc733a5c0a7b5d8b98bccf4468b90`  
		Last Modified: Thu, 09 Jan 2025 22:31:00 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc346178dd8efd43b579bb34dfd41507227f0fb466dccfbb5baba5364233fda`  
		Last Modified: Thu, 09 Jan 2025 22:31:04 GMT  
		Size: 90.4 MB (90413486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:legacy-fpm-alpine` - unknown; unknown

```console
$ docker pull mediawiki@sha256:c48b0ab970a22eb893e2895089c90cf2d6157e0db97644bc0df11243384f4473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 KB (32645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ee891e5994fec882a05fd2b2f7288ce53f08308516bb53fb32d8375c0175b9`

```dockerfile
```

-	Layers:
	-	`sha256:818939ad242e690db89619a0b79ec56f12d46e186cc37a708c0d96da96108ad9`  
		Last Modified: Thu, 09 Jan 2025 22:30:59 GMT  
		Size: 32.6 KB (32645 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:legacy-fpm-alpine` - linux; arm variant v6

```console
$ docker pull mediawiki@sha256:b6740346b23826940f089e13d30a33f85bb4b1ec7b5a71ab345494cd9878a802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147433734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee6281082af85b4b2db56e61d5b7546c03e8dda2c98381d5756e4dc98a232787`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 11 Dec 2024 09:15:55 GMT
ADD alpine-minirootfs-3.21.2-armhf.tar.gz / # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
CMD ["/bin/sh"]
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 11 Dec 2024 09:15:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 11 Dec 2024 09:15:55 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_VERSION=8.1.31
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 11 Dec 2024 09:15:55 GMT
WORKDIR /var/www/html
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
STOPSIGNAL SIGQUIT
# Wed, 11 Dec 2024 09:15:55 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 11 Dec 2024 09:15:55 GMT
CMD ["php-fpm"]
# Thu, 09 Jan 2025 11:23:56 GMT
RUN set -eux; 		apk add --no-cache 		git 		imagemagick 		python3 	; # buildkit
# Thu, 09 Jan 2025 11:23:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		icu-dev 		lua5.1-dev 		oniguruma-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.24; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .mediawiki-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 09 Jan 2025 11:23:56 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 09 Jan 2025 11:23:56 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Thu, 09 Jan 2025 11:23:56 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.42
# Thu, 09 Jan 2025 11:23:56 GMT
ENV MEDIAWIKI_VERSION=1.42.4
# Thu, 09 Jan 2025 11:23:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps 		bzip2 		gnupg 	; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	[ 1.42.4 = "1.42.4" ] && 		sed -i 's|wikimedia/parsoid": "0.19.0"|wikimedia/parsoid": "0.19.1"|' 			composer.json; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apk del --no-network .fetch-deps # buildkit
# Thu, 09 Jan 2025 11:23:56 GMT
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
	-	`sha256:90e50ca11f125bd1dcb0f79afd00b19f676d22d041beb05fc6d51993185dc777`  
		Last Modified: Wed, 08 Jan 2025 20:39:27 GMT  
		Size: 11.9 MB (11938079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e5fa41f96c53d1929f36713d5d1f8f89d2c468d2805f582d2c0d78a3ea73c28`  
		Last Modified: Wed, 08 Jan 2025 20:39:26 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9668a608eba0fad79d490bff9d5876259ae53691811f286e1f4103160ad15c3`  
		Last Modified: Wed, 08 Jan 2025 20:42:51 GMT  
		Size: 11.4 MB (11437088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44cfeebe2ea5aa467ca07934a90f3fe32d5b12bf8a9386939b3b301e1fefa10`  
		Last Modified: Wed, 08 Jan 2025 20:42:50 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf84e1cd2eade844d97efb12931d3697a2b5db5b58a4928044ce15e04cc602d`  
		Last Modified: Wed, 08 Jan 2025 20:42:50 GMT  
		Size: 19.8 KB (19848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7d4e4668fa25ef4c6edda1e82f7b4f9d548285f346d5d66e99dae3e040effc`  
		Last Modified: Wed, 08 Jan 2025 20:42:51 GMT  
		Size: 8.9 KB (8877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b257c30b86e261438a53544d184697b63f7e64582cbf3804eda42fbf7c63ac08`  
		Last Modified: Thu, 09 Jan 2025 09:44:47 GMT  
		Size: 22.6 MB (22646010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ac729a349858a271d35dd58e771e85da2e316d1aeead4d858e83ead5514e4d`  
		Last Modified: Thu, 09 Jan 2025 09:44:46 GMT  
		Size: 4.3 MB (4302253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03959834ddb6388d3cf646366f0ae8f8699b778f453988ac2ddd2de5604fee8b`  
		Last Modified: Thu, 09 Jan 2025 09:44:46 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31803a18c9d9e68ed5a564b600982c35def8161f9f03d6380f5b692aedc81fc2`  
		Last Modified: Thu, 09 Jan 2025 09:44:46 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e066211bb14083b3f98e3a931144abd58e01f450f29803f4eb5f89c455d15c21`  
		Last Modified: Thu, 09 Jan 2025 22:32:17 GMT  
		Size: 90.4 MB (90412619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:legacy-fpm-alpine` - unknown; unknown

```console
$ docker pull mediawiki@sha256:987ee635319ddfc5accbec0da4e1b4667cd810a435f00ad364e6e196658429b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 KB (32765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23eb3efc2160c5a6cb21d67b3848ff2bd6e7fca60e7f1d2129dd676b56ef0b10`

```dockerfile
```

-	Layers:
	-	`sha256:17e0192982615b9d4c7a25cf94c8fd79b1be00fa9940adae972e4c1730d0ab72`  
		Last Modified: Thu, 09 Jan 2025 22:32:14 GMT  
		Size: 32.8 KB (32765 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:legacy-fpm-alpine` - linux; arm variant v7

```console
$ docker pull mediawiki@sha256:ea05dcd3a13964701133d68851a51153eb338f5d5fe77a10f4e1354554349834
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.4 MB (145351259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa55020ea790706d7f689dbe0544a2ab5e20eb630616259195365990a3848aa`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 11 Dec 2024 09:15:55 GMT
ADD alpine-minirootfs-3.21.2-armv7.tar.gz / # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
CMD ["/bin/sh"]
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 11 Dec 2024 09:15:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 11 Dec 2024 09:15:55 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_VERSION=8.1.31
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 11 Dec 2024 09:15:55 GMT
WORKDIR /var/www/html
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
STOPSIGNAL SIGQUIT
# Wed, 11 Dec 2024 09:15:55 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 11 Dec 2024 09:15:55 GMT
CMD ["php-fpm"]
# Thu, 09 Jan 2025 11:23:56 GMT
RUN set -eux; 		apk add --no-cache 		git 		imagemagick 		python3 	; # buildkit
# Thu, 09 Jan 2025 11:23:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		icu-dev 		lua5.1-dev 		oniguruma-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.24; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .mediawiki-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 09 Jan 2025 11:23:56 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 09 Jan 2025 11:23:56 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Thu, 09 Jan 2025 11:23:56 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.42
# Thu, 09 Jan 2025 11:23:56 GMT
ENV MEDIAWIKI_VERSION=1.42.4
# Thu, 09 Jan 2025 11:23:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps 		bzip2 		gnupg 	; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	[ 1.42.4 = "1.42.4" ] && 		sed -i 's|wikimedia/parsoid": "0.19.0"|wikimedia/parsoid": "0.19.1"|' 			composer.json; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apk del --no-network .fetch-deps # buildkit
# Thu, 09 Jan 2025 11:23:56 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:824bc99f06f2c6bebc1172ff7e39d7a1cdbd077ec44632079a629f69e9db7abf`  
		Last Modified: Tue, 14 Jan 2025 20:33:57 GMT  
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
		Last Modified: Wed, 15 Jan 2025 00:11:56 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:106117df467bfb4880f17a8feb657b0a9ef961de6c28f9741096c34122ff0b89`  
		Last Modified: Wed, 08 Jan 2025 20:44:49 GMT  
		Size: 11.9 MB (11938077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd1ba85a4ceea7ad23e84562065513bffc9da62b5ad5d914da79d2507d6a2c6`  
		Last Modified: Wed, 08 Jan 2025 20:44:48 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e240b70ef85ddf1bafd491179535569b5d72ee5b4ee14be9bb6a81bf751f31`  
		Last Modified: Wed, 08 Jan 2025 20:48:21 GMT  
		Size: 10.8 MB (10775845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f384693dbc880eb3a1d54ee72fcaab8738e7dc807656f74d73df5a8c791de7b`  
		Last Modified: Wed, 08 Jan 2025 20:48:20 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93dac9a7c6bddf21de2886960e85f4bb9c8b5b2e271206bbaeeb508e0dafb363`  
		Last Modified: Wed, 08 Jan 2025 20:48:20 GMT  
		Size: 19.9 KB (19853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a8f7626a14c1f867b4fa1eab647c903058d24e3d85a4871f88fa2e2b224949`  
		Last Modified: Wed, 15 Jan 2025 05:02:11 GMT  
		Size: 8.9 KB (8876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7635c1bf4018deba70ffd17ec1f974ee097815a44688554e9215301ae219d9e7`  
		Last Modified: Thu, 09 Jan 2025 11:10:53 GMT  
		Size: 21.6 MB (21617472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e560e1006df3069fe7fa1f87be6d3255a5a7bef06775729e7cf96117dcfe7d`  
		Last Modified: Thu, 09 Jan 2025 11:10:52 GMT  
		Size: 4.4 MB (4361349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25320a4d9d381c062e6ebde31383df5fd5dd282360bca248951066a381fb9bb9`  
		Last Modified: Thu, 09 Jan 2025 11:10:52 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c8c5e448b315e30bb9396ef20d1a247e002486fdb67d34f2498fa98b69b0a70`  
		Last Modified: Thu, 09 Jan 2025 11:10:52 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b010768e266408fa093f1eafd96f3592d68d1487415152617daf7d671f025fc`  
		Last Modified: Thu, 09 Jan 2025 22:39:55 GMT  
		Size: 90.4 MB (90412722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:legacy-fpm-alpine` - unknown; unknown

```console
$ docker pull mediawiki@sha256:4150c2b2336a55304887645de7a9a061d7615299c68a64a8f7537aa32bc9cc5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 KB (32765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd4b74fd09a0546813a6de06430cf6a0e47c7e69a3381fd0e5102e9ec20821d2`

```dockerfile
```

-	Layers:
	-	`sha256:708ab57e53a62f71d984cf2dc7fc53b7573326b6f39e220e0fad369fe134b609`  
		Last Modified: Thu, 09 Jan 2025 22:39:52 GMT  
		Size: 32.8 KB (32765 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:legacy-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull mediawiki@sha256:dbee1c6a6b18cc6a18dc52f10b70e14cd8f31ff45e095e28e2d5b262c7a98c93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.7 MB (150672384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1d6849817e47a6a0ce9ee84eb728ad8ffc34ec7cdd0a203d0c0503bfcc345f3`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 11 Dec 2024 09:15:55 GMT
ADD alpine-minirootfs-3.21.2-aarch64.tar.gz / # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
CMD ["/bin/sh"]
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 11 Dec 2024 09:15:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 11 Dec 2024 09:15:55 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_VERSION=8.1.31
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 11 Dec 2024 09:15:55 GMT
WORKDIR /var/www/html
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
STOPSIGNAL SIGQUIT
# Wed, 11 Dec 2024 09:15:55 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 11 Dec 2024 09:15:55 GMT
CMD ["php-fpm"]
# Thu, 09 Jan 2025 11:23:56 GMT
RUN set -eux; 		apk add --no-cache 		git 		imagemagick 		python3 	; # buildkit
# Thu, 09 Jan 2025 11:23:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		icu-dev 		lua5.1-dev 		oniguruma-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.24; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .mediawiki-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 09 Jan 2025 11:23:56 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 09 Jan 2025 11:23:56 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Thu, 09 Jan 2025 11:23:56 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.42
# Thu, 09 Jan 2025 11:23:56 GMT
ENV MEDIAWIKI_VERSION=1.42.4
# Thu, 09 Jan 2025 11:23:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps 		bzip2 		gnupg 	; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	[ 1.42.4 = "1.42.4" ] && 		sed -i 's|wikimedia/parsoid": "0.19.0"|wikimedia/parsoid": "0.19.1"|' 			composer.json; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apk del --no-network .fetch-deps # buildkit
# Thu, 09 Jan 2025 11:23:56 GMT
CMD ["php-fpm"]
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
		Last Modified: Wed, 08 Jan 2025 18:47:47 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e06c334c2725cc400bba17c21a0380b9f9c970473c4959000a3921b22cdf4a8`  
		Last Modified: Wed, 08 Jan 2025 18:47:47 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8327454479c1dddeaa233e2026ba9c70bba411174fd97ef85cd4dd3e1504e9`  
		Last Modified: Wed, 08 Jan 2025 20:55:07 GMT  
		Size: 11.9 MB (11938110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e442e6af21ecc85b465fe48b5bf170e8ca38529858674dc7e384aa462613760`  
		Last Modified: Wed, 08 Jan 2025 20:55:06 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e654d000c3e7e93410373c7536dee827a5481dd7d7908fcde1da6805c5293d`  
		Last Modified: Tue, 14 Jan 2025 20:55:44 GMT  
		Size: 12.7 MB (12689445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ffa0a6ce646379cc875eb4a7b9dc36963ba2a9d014dc132ba65e49fd83f00a`  
		Last Modified: Tue, 14 Jan 2025 20:44:26 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000df38ea7b0456a7d1bb1214fcfb4d2a96aadbbfc613ba7e57a39147a018624`  
		Last Modified: Wed, 08 Jan 2025 20:59:44 GMT  
		Size: 19.8 KB (19848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9742fc1afbdb7ea1cf6ef3255eb16d33e7de7df649c0503775c0d99b56bcd78`  
		Last Modified: Wed, 08 Jan 2025 20:59:45 GMT  
		Size: 8.9 KB (8875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec63a4f6ba061d82a9158d4bd2062a7d72c26ff472651fd1e06d0bf4db077e8b`  
		Last Modified: Thu, 09 Jan 2025 07:51:43 GMT  
		Size: 23.2 MB (23165307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b40366787f798e5b965c3326d9efde28dc56bb87d58165ca59a20e3eb3f01c1d`  
		Last Modified: Thu, 09 Jan 2025 07:51:43 GMT  
		Size: 5.1 MB (5113295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eefdcb881b21e3cd0bf984eaed1a6a74c0139826db098f23d506f672d76ba8b`  
		Last Modified: Thu, 09 Jan 2025 07:51:42 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b055789e1c69f7036f227e8a4eb007fc66ef0bbb160096e10d548d54c11bdd`  
		Last Modified: Thu, 09 Jan 2025 07:51:42 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f8f11423bf6c41bc579729a2770b2174ba31c98bd82b14c77b785014a79c63`  
		Last Modified: Thu, 09 Jan 2025 22:37:38 GMT  
		Size: 90.4 MB (90412876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:legacy-fpm-alpine` - unknown; unknown

```console
$ docker pull mediawiki@sha256:ee153f9cff93ce8343a4ee6b7745b46c0a9077caacaae27508322f7433858c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.8 KB (32797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0514ef7c8952c849693b4321d2a4147203bfb6e7a87bffaa0f1a8df8f8cf54c`

```dockerfile
```

-	Layers:
	-	`sha256:d8358efa8225b6951be5bd41b2cfaa9792cc9139fa471e31d81bebb91c165e32`  
		Last Modified: Thu, 09 Jan 2025 22:37:36 GMT  
		Size: 32.8 KB (32797 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:legacy-fpm-alpine` - linux; 386

```console
$ docker pull mediawiki@sha256:64955217b461b065657733f42b0bcb6a960584a324c4c697acafbb8e3917417e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.0 MB (151000669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c606904b15a2e807c9be454e3574cc3d6c30ff41f6fa46c51b851094da024bb8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 11 Dec 2024 09:15:55 GMT
ADD alpine-minirootfs-3.21.2-x86.tar.gz / # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
CMD ["/bin/sh"]
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 11 Dec 2024 09:15:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 11 Dec 2024 09:15:55 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_VERSION=8.1.31
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 11 Dec 2024 09:15:55 GMT
WORKDIR /var/www/html
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
STOPSIGNAL SIGQUIT
# Wed, 11 Dec 2024 09:15:55 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 11 Dec 2024 09:15:55 GMT
CMD ["php-fpm"]
# Thu, 09 Jan 2025 11:23:56 GMT
RUN set -eux; 		apk add --no-cache 		git 		imagemagick 		python3 	; # buildkit
# Thu, 09 Jan 2025 11:23:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		icu-dev 		lua5.1-dev 		oniguruma-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.24; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .mediawiki-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 09 Jan 2025 11:23:56 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 09 Jan 2025 11:23:56 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Thu, 09 Jan 2025 11:23:56 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.42
# Thu, 09 Jan 2025 11:23:56 GMT
ENV MEDIAWIKI_VERSION=1.42.4
# Thu, 09 Jan 2025 11:23:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps 		bzip2 		gnupg 	; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	[ 1.42.4 = "1.42.4" ] && 		sed -i 's|wikimedia/parsoid": "0.19.0"|wikimedia/parsoid": "0.19.1"|' 			composer.json; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apk del --no-network .fetch-deps # buildkit
# Thu, 09 Jan 2025 11:23:56 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:dbaac2331104495e5df0818a1db05c402cfc13af140c75beccf51922d5f37ad5`  
		Last Modified: Wed, 08 Jan 2025 17:23:36 GMT  
		Size: 3.5 MB (3463126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5b5e4c28cd1b1f1f8dc2487bbe5947f81f0bc52f65e0fd53e8b4d73601f89fb`  
		Last Modified: Wed, 15 Jan 2025 05:01:54 GMT  
		Size: 3.4 MB (3373777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8127c5471982a35356238a98c6bc1eb23b4453a678b15d66ddd9eae13f6f6ad`  
		Last Modified: Wed, 08 Jan 2025 18:09:28 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1d8a9bc95946bdf3ce5e57266f0226d03fc3f96e6c368505617f20d9bcfb60`  
		Last Modified: Wed, 08 Jan 2025 18:09:28 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83b8e3f7c041be52ed8f6ff9c0c1d8fd8f27848abed0338aefe7330c8c25cdb4`  
		Last Modified: Wed, 08 Jan 2025 18:09:28 GMT  
		Size: 11.9 MB (11938049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d74965c1781b77a6ef75372092f12fe63cae02952d568294f81ff16af647860`  
		Last Modified: Wed, 08 Jan 2025 18:09:28 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f210f1126334c7fcd4dcbeef509cee687c4d20a3b767ea1908bce9c09a3123b`  
		Last Modified: Wed, 08 Jan 2025 18:09:29 GMT  
		Size: 13.0 MB (13009147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd57a87d8d3586cf65e6f490a6c207039ca5983b1bf68dd621dac1db26d10ddb`  
		Last Modified: Wed, 08 Jan 2025 18:09:29 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4477d16f474c06ef6a13efc54a84370f25974d5642c1f5cc908dc02e20dc5204`  
		Last Modified: Wed, 08 Jan 2025 18:09:29 GMT  
		Size: 20.0 KB (20027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31c68c87212bf28cd8ade7c7c71bc5ea1bf9fb1f194d199bf41ee95716beb92`  
		Last Modified: Wed, 08 Jan 2025 18:09:29 GMT  
		Size: 8.9 KB (8878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b90c458957079850d669c050cdd7677c2b797edf01f2e6c9075ec3a71843b18`  
		Last Modified: Thu, 09 Jan 2025 22:30:52 GMT  
		Size: 23.8 MB (23816800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8c1f6f374f221187340c7c2645304f5c0c1df78bf9dac978e39db1a861b3fb`  
		Last Modified: Thu, 09 Jan 2025 22:30:52 GMT  
		Size: 5.0 MB (4953402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6522a6aee06618ae0164ba12460a57d0919906c20a257dc4c4a5b505bb7b5655`  
		Last Modified: Thu, 09 Jan 2025 22:30:51 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fc0e5411b1466ad0cb6e18d22bbce229cb84b7a9dc4ce05bc96624858e8a987`  
		Last Modified: Thu, 09 Jan 2025 22:30:51 GMT  
		Size: 141.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9cfcd483d35b549294ee86e85ec9bc02d5363def05973ed90d14e9d0643fa80`  
		Last Modified: Thu, 09 Jan 2025 22:30:55 GMT  
		Size: 90.4 MB (90412878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:legacy-fpm-alpine` - unknown; unknown

```console
$ docker pull mediawiki@sha256:ef7982e5688f5a9db256d87079cc11b725ce8712caad66bf5582cbc13e409681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 KB (32610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35c88061895bb04cacd1eb39d85fc2e78e9479b90b4ea389b65e5bff7dc721ba`

```dockerfile
```

-	Layers:
	-	`sha256:146b456dae4c7d649b4f249df78e2b3169eea1bab44b35ed9818e97a753caa4a`  
		Last Modified: Thu, 09 Jan 2025 22:30:51 GMT  
		Size: 32.6 KB (32610 bytes)  
		MIME: application/vnd.in-toto+json

### `mediawiki:legacy-fpm-alpine` - linux; ppc64le

```console
$ docker pull mediawiki@sha256:ceb1b5ad0888104265c4e9f8d338085947c704e9231885da6c982023c72c016f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151291475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43b40c684459ad1aa51aa588db344ccc12e2e887816170cb6aa9ecab27b0aa17`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 11 Dec 2024 09:15:55 GMT
ADD alpine-minirootfs-3.21.2-ppc64le.tar.gz / # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
CMD ["/bin/sh"]
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 11 Dec 2024 09:15:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 11 Dec 2024 09:15:55 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_VERSION=8.1.31
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.31.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.31.tar.xz.asc
# Wed, 11 Dec 2024 09:15:55 GMT
ENV PHP_SHA256=c4f244d46ba51c72f7d13d4f66ce6a9e9a8d6b669c51be35e01765ba58e7afca
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		patch 		patchutils 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	curl -fL 'https://github.com/php/php-src/commit/577b8ae4226368e66fee7a9b5c58f9e2428372fc.patch?full_index=1' -o 11678.patch; 	echo '6edc20c3bb3e7cc13515abce7f2fffa8ebea6cf7469abfbc78fcdc120350b239 *11678.patch' | sha256sum -c -; 	patch -p1 < 11678.patch; 	rm 11678.patch; 	curl -fL 'https://github.com/php/php-src/commit/67259e451d5d58b4842776c5696a66d74e157609.patch?full_index=1' -o 14834.patch; 	echo 'ed10a1b254091ad676ed204e55628ecbd6c8962004d6185a1821cedecd526c0f *14834.patch' | sha256sum -c -; 	filterdiff -x '*/NEWS' 14834.patch | patch -p1; 	rm 14834.patch; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 11 Dec 2024 09:15:55 GMT
WORKDIR /var/www/html
# Wed, 11 Dec 2024 09:15:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 11 Dec 2024 09:15:55 GMT
STOPSIGNAL SIGQUIT
# Wed, 11 Dec 2024 09:15:55 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 11 Dec 2024 09:15:55 GMT
CMD ["php-fpm"]
# Thu, 09 Jan 2025 11:23:56 GMT
RUN set -eux; 		apk add --no-cache 		git 		imagemagick 		python3 	; # buildkit
# Thu, 09 Jan 2025 11:23:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		icu-dev 		lua5.1-dev 		oniguruma-dev 	; 		docker-php-ext-install -j "$(nproc)" 		calendar 		intl 		mbstring 		mysqli 		opcache 	; 		pecl install APCu-5.1.24; 	pecl install LuaSandbox-4.1.2; 	docker-php-ext-enable 		apcu 		luasandbox 	; 	rm -r /tmp/pear; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local/lib/php/extensions 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .mediawiki-phpext-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 09 Jan 2025 11:23:56 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 09 Jan 2025 11:23:56 GMT
RUN set -eux; 	mkdir -p /var/www/data; 	chown -R www-data:www-data /var/www/data # buildkit
# Thu, 09 Jan 2025 11:23:56 GMT
ENV MEDIAWIKI_MAJOR_VERSION=1.42
# Thu, 09 Jan 2025 11:23:56 GMT
ENV MEDIAWIKI_VERSION=1.42.4
# Thu, 09 Jan 2025 11:23:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .fetch-deps 		bzip2 		gnupg 	; 		curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz" -o mediawiki.tar.gz; 	curl -fSL "https://releases.wikimedia.org/mediawiki/${MEDIAWIKI_MAJOR_VERSION}/mediawiki-${MEDIAWIKI_VERSION}.tar.gz.sig" -o mediawiki.tar.gz.sig; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 		D7D6767D135A514BEB86E9BA75682B08E8A3FEC4 		441276E9CCD15F44F6D97D18C119E1A64D70938E 		F7F780D82EBFB8A56556E7EE82403E59F9F8CD79 		1D98867E82982C8FE0ABC25F9B69B3109D3BB7B0 		E059C034E7A430583C252F4AA8F734246D73B586 	; 	gpg --batch --verify mediawiki.tar.gz.sig mediawiki.tar.gz; 	tar -x --strip-components=1 -f mediawiki.tar.gz; 	[ 1.42.4 = "1.42.4" ] && 		sed -i 's|wikimedia/parsoid": "0.19.0"|wikimedia/parsoid": "0.19.1"|' 			composer.json; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" mediawiki.tar.gz.sig mediawiki.tar.gz; 	chown -R www-data:www-data extensions skins cache images; 		apk del --no-network .fetch-deps # buildkit
# Thu, 09 Jan 2025 11:23:56 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:244ac55e5ecd413dee99efe3ace7cb84420bfc9a727ec2327dae7805045d7470`  
		Last Modified: Wed, 08 Jan 2025 17:24:16 GMT  
		Size: 3.6 MB (3573601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e88c0bde0da532d37286f677138c7e480dcb6f566920007e98f5e5eb88d6d4`  
		Last Modified: Wed, 15 Jan 2025 04:47:37 GMT  
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
	-	`sha256:680af27d977f66a982c3a663ea37f70eec827f44b071b99ed93e0ace0148677b`  
		Last Modified: Wed, 08 Jan 2025 20:25:45 GMT  
		Size: 11.9 MB (11938118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b307d2c718b0e0069a2efa3c4145db228cb371cf9fa8b4c2bc62132343bd45`  
		Last Modified: Wed, 15 Jan 2025 05:02:21 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cd086589f1f3a86874d9980cf3e76b94641bdbacbd19b5182e4e2c52d871cf7`  
		Last Modified: Wed, 08 Jan 2025 20:29:19 GMT  
		Size: 13.1 MB (13099882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b00767fa17fd895d30b9b32080faadef7d2125d66add3f941a5d369863c43a`  
		Last Modified: Wed, 15 Jan 2025 05:02:21 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c98dc52f2c61e27c21e7cc21fd7d6ea8be5c48dbdd4059b1fbeb252b88cf2b97`  
		Last Modified: Wed, 15 Jan 2025 05:02:21 GMT  
		Size: 19.8 KB (19849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b15b138d667d59e0f4688c24477862a31478d281f92aee62b4a866362909d3a`  
		Last Modified: Wed, 08 Jan 2025 20:29:19 GMT  
		Size: 8.9 KB (8882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c635b62dbbfa8e8672f9ebbeb2416426ba969dd96fefe8e15bbfdd855e6ccbdc`  
		Last Modified: Thu, 09 Jan 2025 22:46:14 GMT  
		Size: 24.1 MB (24130189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a78b10d4d7e59fcc2cb662f36a3e10295112c51b05e5e401c2215e03c85bb5a`  
		Last Modified: Thu, 09 Jan 2025 22:46:14 GMT  
		Size: 4.6 MB (4626879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0a90ec0c2434d87975ec1723c067ec445ca31eae6bb7268c5e69e8c9512fbf`  
		Last Modified: Thu, 09 Jan 2025 22:46:13 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a62e5a9f3c2e4e08a381d4df945385332807a7c5710e9309567a059fe40d79`  
		Last Modified: Thu, 09 Jan 2025 22:46:13 GMT  
		Size: 140.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f6a60b7e24a8c3f4fc8ca6d8d48a331443b2eaa273956c0929836e9cedc72e4`  
		Last Modified: Thu, 09 Jan 2025 22:46:17 GMT  
		Size: 90.4 MB (90413133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `mediawiki:legacy-fpm-alpine` - unknown; unknown

```console
$ docker pull mediawiki@sha256:570c63842160a5a22893de186e42551d05d44b74078235087c4571eed50f9362
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.7 KB (32690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:361d4910ff87a1e3744172d837a1e3f6bef20aa0c5c7867927f208348baffc93`

```dockerfile
```

-	Layers:
	-	`sha256:10856b4a354d105400da1536dbdac232aacf591135296ee8a66aa16b3689b0fc`  
		Last Modified: Thu, 09 Jan 2025 22:46:13 GMT  
		Size: 32.7 KB (32690 bytes)  
		MIME: application/vnd.in-toto+json
