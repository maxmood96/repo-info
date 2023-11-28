## `drupal:7-php8.1-fpm-alpine3.17`

```console
$ docker pull drupal@sha256:1ff90588493357ad1285e2f171b0e872231a5ae1fd70756a24b6de0aaa0303b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 13
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
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

### `drupal:7-php8.1-fpm-alpine3.17` - linux; amd64

```console
$ docker pull drupal@sha256:92aa2ba4c7d325d57b83aca1364c5892e5f550f6cb467f30920672017647a9fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39855808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3fd0791fae959b9e90792dcdd76f403295c6f2eec9d535f6770bbbf1876512`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 14 Jun 2023 17:25:34 GMT
ADD file:6dd87346b8be240b21b4f4d9296253bf0d28b6579aa52d2118872e3936963b6b in / 
# Wed, 14 Jun 2023 17:25:34 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 14 Jun 2023 17:25:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 14 Jun 2023 17:25:34 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_VERSION=8.1.26
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.26.tar.xz.asc
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_SHA256=17f87133596449327451ad4b8d9911bfaea59ff5109f3a6f2bb679f967a8ea0f
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 14 Jun 2023 17:25:34 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 14 Jun 2023 17:25:34 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 14 Jun 2023 17:25:34 GMT
RUN docker-php-ext-enable sodium
# Wed, 14 Jun 2023 17:25:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 14 Jun 2023 17:25:34 GMT
WORKDIR /var/www/html
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 14 Jun 2023 17:25:34 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Jun 2023 17:25:34 GMT
EXPOSE 9000
# Wed, 14 Jun 2023 17:25:34 GMT
CMD ["php-fpm"]
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 14 Jun 2023 17:25:34 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 14 Jun 2023 17:25:34 GMT
ENV DRUPAL_VERSION=7.98
# Wed, 14 Jun 2023 17:25:34 GMT
ENV DRUPAL_MD5=4139f0feecb44a53645242194809b73a
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:9398808236ffac29e60c04ec906d8d409af7fa19dc57d8c65ad167e9c4967006`  
		Last Modified: Mon, 07 Aug 2023 19:21:08 GMT  
		Size: 3.4 MB (3378609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d409140a81c62f46aeb13593b4f71d44dfe26018d27aea968ccc0cf37ca63f0a`  
		Last Modified: Sat, 21 Oct 2023 06:27:11 GMT  
		Size: 4.0 MB (3966868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d975c886325f4cd819965bbfa3ee3a41d8635acbe5586307d01fd95204774c`  
		Last Modified: Sat, 21 Oct 2023 06:27:10 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c6b16bc660c086b6f1cb34456d304fa1062c10b31c12d3e0ac129b0f78b112`  
		Last Modified: Sat, 21 Oct 2023 06:27:10 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f36017b0684427442e8a513244d68c5f71abcfa2797595a7cdf146985276ee0`  
		Last Modified: Tue, 28 Nov 2023 00:22:50 GMT  
		Size: 11.8 MB (11829937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea48a27e1eaf38e10ae25f61c22261b84a4d85aec05ccb81f0552bcc0cbdf83c`  
		Last Modified: Tue, 28 Nov 2023 00:22:49 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae72462828ed69a9afeaac6327f71b1e93d713ec4dfc8a72059b7229a3c0c318`  
		Last Modified: Tue, 28 Nov 2023 00:23:08 GMT  
		Size: 15.0 MB (15030649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:534e7481c66811ce48a08a8072a4dd13f149bbff47dc3ac3de71ed6460ccd754`  
		Last Modified: Tue, 28 Nov 2023 00:23:05 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1425e92781c51e262ed035bd4ea8d8c36bca5b8c5fdbab69aa3440696f67c59f`  
		Last Modified: Tue, 28 Nov 2023 00:23:05 GMT  
		Size: 19.0 KB (18990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954d907dfaf09dbef1b7f738a3dad32169da06df2aa12637d5e7505463199404`  
		Last Modified: Tue, 28 Nov 2023 00:23:05 GMT  
		Size: 8.9 KB (8878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7836ec5cb5f3cc05e587f62ad9720c517928f9832c01445ec46794183a816e`  
		Last Modified: Tue, 28 Nov 2023 01:16:58 GMT  
		Size: 2.2 MB (2206793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f4c1f4044971fba959f4640656598c00987e2e75536efaa33700b08289315d`  
		Last Modified: Tue, 28 Nov 2023 01:16:58 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:377cae73c2e285c365ec86912ef893d5e0e29c228c8ff5ae0bb3b3ec7b3cfb14`  
		Last Modified: Tue, 28 Nov 2023 01:16:58 GMT  
		Size: 3.4 MB (3410296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1-fpm-alpine3.17` - unknown; unknown

```console
$ docker pull drupal@sha256:fd27a65e8100ccba5f5489bcc9767e42199001530d1a08a82ea8fbfdc9c7eb49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.9 KB (254944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc308c513067112e98ee93985a5b4643bb8733b4c8b3445796e131629b95278`

```dockerfile
```

-	Layers:
	-	`sha256:9421b93c357dd28636102f35ce96ee0e7b083adbb1b5cb8e4179aab3e0c906c4`  
		Last Modified: Tue, 28 Nov 2023 01:16:58 GMT  
		Size: 232.1 KB (232097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:265c2251d5567bee4de1d608bca963e9d2e91ce82de119e047a8c53e9dd1bbe5`  
		Last Modified: Tue, 28 Nov 2023 01:16:57 GMT  
		Size: 22.8 KB (22847 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.1-fpm-alpine3.17` - linux; arm variant v6

```console
$ docker pull drupal@sha256:a4a7e15dbe2bce58f0949e58217a26314af9d00af7fe1f893d4524ace377c78e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.2 MB (37163404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:554896f1040648bc9cb79561868bd255eae4938ab31e5d2a6082ea663fdd0ee4`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 14 Jun 2023 17:25:34 GMT
ADD file:cb3f59b0f701cb6ef552e7f8ada1707cf82747c95b69759924061ff9ac6dbe72 in / 
# Wed, 14 Jun 2023 17:25:34 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 14 Jun 2023 17:25:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 14 Jun 2023 17:25:34 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_VERSION=8.1.26
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.26.tar.xz.asc
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_SHA256=17f87133596449327451ad4b8d9911bfaea59ff5109f3a6f2bb679f967a8ea0f
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 14 Jun 2023 17:25:34 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 14 Jun 2023 17:25:34 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 14 Jun 2023 17:25:34 GMT
RUN docker-php-ext-enable sodium
# Wed, 14 Jun 2023 17:25:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 14 Jun 2023 17:25:34 GMT
WORKDIR /var/www/html
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 14 Jun 2023 17:25:34 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Jun 2023 17:25:34 GMT
EXPOSE 9000
# Wed, 14 Jun 2023 17:25:34 GMT
CMD ["php-fpm"]
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 14 Jun 2023 17:25:34 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 14 Jun 2023 17:25:34 GMT
ENV DRUPAL_VERSION=7.98
# Wed, 14 Jun 2023 17:25:34 GMT
ENV DRUPAL_MD5=4139f0feecb44a53645242194809b73a
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:342323bc858ed9706f7953ab06cbf6785b678c55ef2317577af748533d11165b`  
		Last Modified: Mon, 07 Aug 2023 19:49:53 GMT  
		Size: 3.1 MB (3112450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3615ead72921cc0e7d9b570fd1cbf98286500906c9e85157bc0f7f9215b4f62`  
		Last Modified: Sat, 21 Oct 2023 03:22:13 GMT  
		Size: 3.6 MB (3620887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ddcbcd062e3baf30ecfb665bd8957b2a308e0ea23338eab716e5c697cc3a81`  
		Last Modified: Sat, 21 Oct 2023 03:22:12 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6996322317f3e60398a7a63dcc220eabf2187328dca0c2c0eb96fcdd5d91984a`  
		Last Modified: Sat, 21 Oct 2023 03:22:12 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e920435952d34cb3b8f00c772b48ab8a28dfbc6e3cb3ea0f0d872571f19fd92`  
		Last Modified: Mon, 27 Nov 2023 22:33:47 GMT  
		Size: 11.8 MB (11829925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66bce0703e156b0fd8dbee0c69e2026b24f7a288fec203c5baf01a9be6e079e5`  
		Last Modified: Mon, 27 Nov 2023 22:33:46 GMT  
		Size: 496.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c9a99b5bb49f358e20a2da6aa97034617dcb5e647278c34c649903bd5e0535`  
		Last Modified: Mon, 27 Nov 2023 22:34:06 GMT  
		Size: 13.5 MB (13488874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73202e501f6e172d8ce2ae7ded29f0c3492ae55a8a3e25d06da599fb5726513`  
		Last Modified: Mon, 27 Nov 2023 22:34:03 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e5b94e6b144bd39de8b06aeb3ebb4a15b9072ef2ce4a4cca1c4a440c15e6f2`  
		Last Modified: Mon, 27 Nov 2023 22:34:03 GMT  
		Size: 18.8 KB (18780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a230abe69aa5028bf2a77dac2540b1571c6261e19ef4c10beb8840d1c8b50a6`  
		Last Modified: Mon, 27 Nov 2023 22:34:03 GMT  
		Size: 8.9 KB (8875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be65c34a51725e5fd7860b0a25b3dbfd5f8edbd486562ab77f62d7bea4f9ce1b`  
		Last Modified: Tue, 28 Nov 2023 00:17:15 GMT  
		Size: 1.7 MB (1668522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5421757bc9f4406c60c2eb46fdb0b52129173a61b0f83d2d657e9b8db15e5510`  
		Last Modified: Tue, 28 Nov 2023 00:17:14 GMT  
		Size: 312.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5772d5c848269fb9d1ed38077b6ae0e437fbf89ddd7a2e94be54da442edb1975`  
		Last Modified: Tue, 28 Nov 2023 00:25:31 GMT  
		Size: 3.4 MB (3410303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:7-php8.1-fpm-alpine3.17` - linux; arm variant v7

```console
$ docker pull drupal@sha256:3c20e8c9ae3591ca7fcb63f95b4824bf7ca4459ac3d9d43b407a4d30929d4d33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.7 MB (35688412 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbfe912290ae239a1bfcdf9d511107a0b24b770dfde20e3167d968ac9e055fda`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 14 Jun 2023 17:25:34 GMT
ADD file:7f36c30ba2b714d09a8650dba1545abdf892443dadbe9113b9a166b84ba7ac3f in / 
# Wed, 14 Jun 2023 17:25:34 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 14 Jun 2023 17:25:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 14 Jun 2023 17:25:34 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_VERSION=8.1.26
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.26.tar.xz.asc
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_SHA256=17f87133596449327451ad4b8d9911bfaea59ff5109f3a6f2bb679f967a8ea0f
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 14 Jun 2023 17:25:34 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 14 Jun 2023 17:25:34 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 14 Jun 2023 17:25:34 GMT
RUN docker-php-ext-enable sodium
# Wed, 14 Jun 2023 17:25:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 14 Jun 2023 17:25:34 GMT
WORKDIR /var/www/html
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 14 Jun 2023 17:25:34 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Jun 2023 17:25:34 GMT
EXPOSE 9000
# Wed, 14 Jun 2023 17:25:34 GMT
CMD ["php-fpm"]
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 14 Jun 2023 17:25:34 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 14 Jun 2023 17:25:34 GMT
ENV DRUPAL_VERSION=7.98
# Wed, 14 Jun 2023 17:25:34 GMT
ENV DRUPAL_MD5=4139f0feecb44a53645242194809b73a
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:b82e4fd40279a40aa2eecd301fabb2dca254727cc09daa8d0caf69ac28c44af1`  
		Last Modified: Mon, 07 Aug 2023 19:58:08 GMT  
		Size: 2.9 MB (2869425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266755729fd4b431e323998f3335d60c48ca5b6b1e495b1841084469413cdf31`  
		Last Modified: Sat, 21 Oct 2023 03:44:24 GMT  
		Size: 3.3 MB (3348109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e017575e43e4b32d3a5c7aa82e3964278cf4fbca4673ffa9821ad4ecb463c5`  
		Last Modified: Sat, 21 Oct 2023 03:44:24 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba28e04f456480646adaa0ccacf8b8f16d3071aa89bdbe881bcefb2036fea422`  
		Last Modified: Sat, 21 Oct 2023 03:44:23 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb3e883bff7051e1d63eb91882eb87f7ef6b0fe4965a6b2c1fb2b89576a59d4`  
		Last Modified: Mon, 27 Nov 2023 23:59:56 GMT  
		Size: 11.8 MB (11829921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f25e25a7474abf0f6e8f058472eaccc6766911a6a67946008145a466317dc0`  
		Last Modified: Mon, 27 Nov 2023 23:59:55 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b144267f00e413906adc15aa8758e450ebd133aaea148b448ba44049513730`  
		Last Modified: Tue, 28 Nov 2023 00:00:19 GMT  
		Size: 12.7 MB (12660830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b71dd008b3a7369c6fbd7d81127a9f14892b7e27cfe1295bc95df102144ea1`  
		Last Modified: Tue, 28 Nov 2023 00:00:16 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6092b1f7f59ebcef5a8b7bbf4d7a736b7a58d35b444aecbc944f9c131cc7f4f`  
		Last Modified: Tue, 28 Nov 2023 00:00:16 GMT  
		Size: 18.8 KB (18783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1df559c8186c25a0d57ab01c6bd1597f2fd36742ad085c576eddcc6db209294d`  
		Last Modified: Tue, 28 Nov 2023 00:00:16 GMT  
		Size: 8.9 KB (8877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a10fc5f127c3c57ff093a73f04551dedbf8adf21407494b83ad8cd189bbcef4`  
		Last Modified: Tue, 28 Nov 2023 03:44:23 GMT  
		Size: 1.5 MB (1537378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5424a8ce9b9a7df739894047a2aefe8bcca9d7459505a0a74fb4cd7f350ac2f9`  
		Last Modified: Tue, 28 Nov 2023 03:44:23 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb525d42aa77d3f73e1b532e7449a3f1631b22104e51195562a2d10cdf439b5`  
		Last Modified: Tue, 28 Nov 2023 04:07:02 GMT  
		Size: 3.4 MB (3410303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1-fpm-alpine3.17` - unknown; unknown

```console
$ docker pull drupal@sha256:00c122e33d651e5cd6534d1f1ef895141743a92b4996fec78fc9ed4cd506b5af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.9 KB (250948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:839e25e7d93973ac6588823d315803129ed64b5c83d4bd78faaad7b9dad93524`

```dockerfile
```

-	Layers:
	-	`sha256:5804db5e87d1d3cda6d4345579c6b81c04fbd2f8b6adcb994a56abb126b8d994`  
		Last Modified: Tue, 28 Nov 2023 04:07:01 GMT  
		Size: 229.6 KB (229645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7ba3e925e9af6a7777efae6e1f9eaafdb5ed1fd2563da180eb8b69cef1649eb`  
		Last Modified: Tue, 28 Nov 2023 04:07:01 GMT  
		Size: 21.3 KB (21303 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.1-fpm-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:51c46ca0f23fa7baab9f2dc67976f1cd1cac97ce0166a2d1587566d8845845a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39639661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d1b4d529a75dcc5b37e769cdc3e10eb187df6efebc522c172250b012028986`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 14 Jun 2023 17:25:34 GMT
ADD file:9e054a25c83111adc857a7f988336ee40eea5e1794ed30a80d465e8d472342e2 in / 
# Wed, 14 Jun 2023 17:25:34 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 14 Jun 2023 17:25:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 14 Jun 2023 17:25:34 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_VERSION=8.1.26
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.26.tar.xz.asc
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_SHA256=17f87133596449327451ad4b8d9911bfaea59ff5109f3a6f2bb679f967a8ea0f
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 14 Jun 2023 17:25:34 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 14 Jun 2023 17:25:34 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 14 Jun 2023 17:25:34 GMT
RUN docker-php-ext-enable sodium
# Wed, 14 Jun 2023 17:25:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 14 Jun 2023 17:25:34 GMT
WORKDIR /var/www/html
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 14 Jun 2023 17:25:34 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Jun 2023 17:25:34 GMT
EXPOSE 9000
# Wed, 14 Jun 2023 17:25:34 GMT
CMD ["php-fpm"]
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 14 Jun 2023 17:25:34 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 14 Jun 2023 17:25:34 GMT
ENV DRUPAL_VERSION=7.98
# Wed, 14 Jun 2023 17:25:34 GMT
ENV DRUPAL_MD5=4139f0feecb44a53645242194809b73a
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:4060ece20d7ac783f52cbe28a35fd5b06f90f7b4d773bae0d956024e85ff35b6`  
		Last Modified: Mon, 07 Aug 2023 19:39:59 GMT  
		Size: 3.3 MB (3258290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b34a0f55e243236a510d854843712a9aa7159ab999cfda1110aa86715d5379c2`  
		Last Modified: Sat, 21 Oct 2023 05:47:16 GMT  
		Size: 3.8 MB (3809798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4babc9015c2d2337c98044da97d8aa95024ab76852c6fcf6bf3ff14f02ab309`  
		Last Modified: Sat, 21 Oct 2023 05:47:15 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8990ce5d2eb593002dd6a3980d05121601226e231dc1b51ccd3ecdc06ebcd80e`  
		Last Modified: Sat, 21 Oct 2023 05:47:15 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c27f06dc70d9d1bfc78e0faf060722c0d311a3d8f935a50820109b6af3d774`  
		Last Modified: Mon, 27 Nov 2023 23:47:58 GMT  
		Size: 11.8 MB (11829930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a99de6047279c9262836a80dd58e86489594502c52e3c2468ece41d903b03d`  
		Last Modified: Mon, 27 Nov 2023 23:47:57 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de69f1825cd6e1a8f6bdec2630a606fdb7142c08b421558c0f13adf3789a76e9`  
		Last Modified: Mon, 27 Nov 2023 23:48:14 GMT  
		Size: 14.9 MB (14855519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa2a4376b3a02bf508e3a9517c2c5828c6e4d4c5f421f81f62ddb9305d548b59`  
		Last Modified: Mon, 27 Nov 2023 23:48:12 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8a6e5c35cf4eb65460e562a117f549329cc4b708d35637e9d739493fb0a06b`  
		Last Modified: Mon, 27 Nov 2023 23:48:12 GMT  
		Size: 18.8 KB (18787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c40ce1d8826ae3e579f49aaf81873fb08cb778e4b94f9f5dffcf086d6029c749`  
		Last Modified: Mon, 27 Nov 2023 23:48:12 GMT  
		Size: 8.9 KB (8875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f3340b36d1101212ff127443b5473531bfb52a7213ce29db856d0e9856ae0af`  
		Last Modified: Tue, 28 Nov 2023 04:08:10 GMT  
		Size: 2.4 MB (2443375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb666321e8617201d2af1c15bc476512e768b5113ed8333e3a6880d808602634`  
		Last Modified: Tue, 28 Nov 2023 04:08:10 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e12753c5d6e9fa34eff7f93b70c28111d61f4894b0e902dae507ffeb2276608`  
		Last Modified: Tue, 28 Nov 2023 04:23:56 GMT  
		Size: 3.4 MB (3410299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1-fpm-alpine3.17` - unknown; unknown

```console
$ docker pull drupal@sha256:a8da966c7bdaa011c4bee03d1e22d8456b8dd41234acfff0f2cdd8246efe9fc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.9 KB (250861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f3aa616b9256271ad4b8cbce8b67abf41318cf2e4a7a793096f6d720af79d7`

```dockerfile
```

-	Layers:
	-	`sha256:4e598b1e354cd726299ebb1f4158e4eecb895037ca7d78e37827dcd53f8c7c00`  
		Last Modified: Tue, 28 Nov 2023 04:23:56 GMT  
		Size: 229.6 KB (229632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6262f0d7dc41680cca4d7651812a42929c753be7aaf6f0bf2042f425142079cd`  
		Last Modified: Tue, 28 Nov 2023 04:23:55 GMT  
		Size: 21.2 KB (21229 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.1-fpm-alpine3.17` - linux; 386

```console
$ docker pull drupal@sha256:b9b2ffae67f0b2053dc8f1477ef4d155585cee992c64132a167153e412cf2935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40492017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7afe6cbe2c89a9d4ca88151e30ee578f605c6de12789d9e7bba3ba4e0a90368d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 14 Jun 2023 17:25:34 GMT
ADD file:437e2411fa3e4795a759f54507f41caa000169f0c32600ec49b4397313cd0884 in / 
# Wed, 14 Jun 2023 17:25:34 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 14 Jun 2023 17:25:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 14 Jun 2023 17:25:34 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_VERSION=8.1.25
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.25.tar.xz.asc
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_SHA256=66fdba064aa119b1463a7969571d42f4642690275d8605ab5149bcc5107e2484
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 14 Jun 2023 17:25:34 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 14 Jun 2023 17:25:34 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 14 Jun 2023 17:25:34 GMT
RUN docker-php-ext-enable sodium
# Wed, 14 Jun 2023 17:25:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 14 Jun 2023 17:25:34 GMT
WORKDIR /var/www/html
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 14 Jun 2023 17:25:34 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Jun 2023 17:25:34 GMT
EXPOSE 9000
# Wed, 14 Jun 2023 17:25:34 GMT
CMD ["php-fpm"]
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 14 Jun 2023 17:25:34 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 14 Jun 2023 17:25:34 GMT
ENV DRUPAL_VERSION=7.98
# Wed, 14 Jun 2023 17:25:34 GMT
ENV DRUPAL_MD5=4139f0feecb44a53645242194809b73a
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:ddc7d64c528fabaad61cc880e91abba829973f743d753415145211971f9ee10d`  
		Last Modified: Mon, 07 Aug 2023 19:39:10 GMT  
		Size: 3.4 MB (3413779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be77e393d6682467b55f831fba7245c492ff2ebb973f274c70a0599f86ae8320`  
		Last Modified: Sat, 21 Oct 2023 06:35:22 GMT  
		Size: 4.1 MB (4102087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf5db589daaa67b227ca91f01467309314a7bcaae01037a478e89635647e1d5`  
		Last Modified: Sat, 21 Oct 2023 06:35:21 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de995542458f5727da8d83e6d9736b6d9b159a7ff19fc5675533a8afa30602b`  
		Last Modified: Sat, 21 Oct 2023 06:35:21 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f3265a7ab75485d1bb8106fd16132c946494f3fa2d61d2579044cab29d123aa`  
		Last Modified: Sat, 28 Oct 2023 05:38:03 GMT  
		Size: 11.9 MB (11908747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89029fa01e3039ffbd0bb837c9bcf1b9716b495d8f1be26ec40d912a64047daf`  
		Last Modified: Sat, 28 Oct 2023 05:38:01 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9f728e7c7a4e2e5413be6c3487fc9e8181e3ea45daf530e2766cedd48414718`  
		Last Modified: Sat, 28 Oct 2023 05:38:23 GMT  
		Size: 15.3 MB (15338971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63f96e5a1e0842b69a4e117bf2e0c0beb2e38f1f75758c243452f9f26a2d158`  
		Last Modified: Sat, 28 Oct 2023 05:38:20 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af3b123c26204d45c5d3104f1b872c56cea937357f32c499703472e02b57270d`  
		Last Modified: Sat, 28 Oct 2023 05:38:20 GMT  
		Size: 19.0 KB (18986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e75cbe0e1ffaef43a52ca8918174b84fbbb77dfe46f77b9668fa5a70ff70bfac`  
		Last Modified: Sat, 28 Oct 2023 05:38:20 GMT  
		Size: 8.9 KB (8877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ab75a24f66e641a446009d8521049847f2e0dbc3a8a609564e39e9773200dd2`  
		Last Modified: Wed, 08 Nov 2023 20:25:46 GMT  
		Size: 2.3 MB (2285493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890b47804afae8da9a0bff8c5e9ac2cded26af93f6139029530697164a4f9c29`  
		Last Modified: Wed, 08 Nov 2023 20:25:46 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0820574936eac6604793b96c78b0b7e2fc22b5226f0c6a888f29c956f2c80b`  
		Last Modified: Wed, 08 Nov 2023 20:25:46 GMT  
		Size: 3.4 MB (3410294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1-fpm-alpine3.17` - unknown; unknown

```console
$ docker pull drupal@sha256:d8a83d1a19be0ea0d9367f7514ce137ded5ee0a148beca2c28e07ac311bd234a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 KB (22609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e9950990ef57d2594d4b35f5e62736493ed2201a546297ee2d44417f0e45d5`

```dockerfile
```

-	Layers:
	-	`sha256:229abedd074dbc6cdcdc1a7513ebbb59de541003b62c0644611841c8fbedfab0`  
		Last Modified: Wed, 08 Nov 2023 20:25:46 GMT  
		Size: 22.6 KB (22609 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.1-fpm-alpine3.17` - linux; ppc64le

```console
$ docker pull drupal@sha256:2a8c99ef9a866ded3f9ffc313d1836e6a646ff361dca35288f4a51bed6895301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.9 MB (39931299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51a86dd6a92415be199fda6883e47bb61492cc11189027d8bad69584bbcd40c9`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 14 Jun 2023 17:25:34 GMT
ADD file:52f28bcdd6e1c6f85b2b5d66ace37ed6cef0da8ce5c58e246549427361b64c1d in / 
# Wed, 14 Jun 2023 17:25:34 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 14 Jun 2023 17:25:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 14 Jun 2023 17:25:34 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_VERSION=8.1.26
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.26.tar.xz.asc
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_SHA256=17f87133596449327451ad4b8d9911bfaea59ff5109f3a6f2bb679f967a8ea0f
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 14 Jun 2023 17:25:34 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 14 Jun 2023 17:25:34 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 14 Jun 2023 17:25:34 GMT
RUN docker-php-ext-enable sodium
# Wed, 14 Jun 2023 17:25:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 14 Jun 2023 17:25:34 GMT
WORKDIR /var/www/html
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 14 Jun 2023 17:25:34 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Jun 2023 17:25:34 GMT
EXPOSE 9000
# Wed, 14 Jun 2023 17:25:34 GMT
CMD ["php-fpm"]
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 14 Jun 2023 17:25:34 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 14 Jun 2023 17:25:34 GMT
ENV DRUPAL_VERSION=7.98
# Wed, 14 Jun 2023 17:25:34 GMT
ENV DRUPAL_MD5=4139f0feecb44a53645242194809b73a
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:1e00d0a2a797866697ccca7b6307a9182e2852583b2b3be3928d196e4cb8ba3d`  
		Last Modified: Mon, 07 Aug 2023 20:17:39 GMT  
		Size: 3.4 MB (3391349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e873c5cf6843a39c83c213ecc24b0ce88d22c597cb59c1b30eaf91ee60983432`  
		Last Modified: Sat, 21 Oct 2023 03:16:15 GMT  
		Size: 4.0 MB (3995064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c74173d1cdae2d8dabd83394d41d1e351930fa23693f3d46bf78dbb89ca121`  
		Last Modified: Sat, 21 Oct 2023 03:16:14 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30228596168cc7b41cc835de78d55ba39b878894037e89ad156128301d96bad4`  
		Last Modified: Sat, 21 Oct 2023 03:16:14 GMT  
		Size: 270.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1664e6f8133843abac10eda0826735f4e3d7c2e648b625d455f87c020b67491a`  
		Last Modified: Tue, 28 Nov 2023 00:01:23 GMT  
		Size: 11.8 MB (11829933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f754a5f0ca040d39ad4fdcada862237ab3f480955569e9ab5d663a111dd0d406`  
		Last Modified: Tue, 28 Nov 2023 00:01:22 GMT  
		Size: 500.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dd0f7651f9f3b1dfbd9420ba474d28fa8e183983de8587089235f89ad3f5326`  
		Last Modified: Tue, 28 Nov 2023 00:01:43 GMT  
		Size: 15.3 MB (15347811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b66b8e331e960ecd13b6ed4713d1dce64e556c2ebdb010e7475dff885ae779`  
		Last Modified: Tue, 28 Nov 2023 00:01:40 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9cb666ef438c8629a0a26935f4f41a262efcf062d43b82ace26554f06a0874`  
		Last Modified: Tue, 28 Nov 2023 00:01:40 GMT  
		Size: 18.8 KB (18784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c3db433ba6453bfb41ef1bef689c80f98be01471e87d3b9269d70bf7308b111`  
		Last Modified: Tue, 28 Nov 2023 00:01:40 GMT  
		Size: 8.9 KB (8875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9392fdb621a3231e63310ecd1ba52abb98081a1b236d1983aa7057c8325931`  
		Last Modified: Tue, 28 Nov 2023 04:46:36 GMT  
		Size: 1.9 MB (1924401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f00694c561bfdc299ccaa685bda2fe5e761a199aaad5de760e10f1dbc39314`  
		Last Modified: Tue, 28 Nov 2023 04:46:36 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e14ee7105eb9570fd253179054a3c42ed93e10a0757a43aa9226b2cf8a7aecf`  
		Last Modified: Tue, 28 Nov 2023 04:46:36 GMT  
		Size: 3.4 MB (3410286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1-fpm-alpine3.17` - unknown; unknown

```console
$ docker pull drupal@sha256:f57857606a8430bc72dd2684372ef84a6f4610a48985e8464f14b513d9a89755
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.9 KB (250889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc713fc840543b261784ca403cb14580f295294f22f0825d07f405a3dfa7ac74`

```dockerfile
```

-	Layers:
	-	`sha256:bae25bf86866b89d0031ece97e38dcef9fcc264a1301bf13163641593f4f462a`  
		Last Modified: Tue, 28 Nov 2023 04:46:34 GMT  
		Size: 228.0 KB (228011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26ad3b4b1ba86d937a8f08ca28ab21abe88a97936d04632cc3006d97eebb6fe1`  
		Last Modified: Tue, 28 Nov 2023 04:46:34 GMT  
		Size: 22.9 KB (22878 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:7-php8.1-fpm-alpine3.17` - linux; s390x

```console
$ docker pull drupal@sha256:31c32abd24f829a47f0b65287ec361ca89ebcbcda341a09c5f5ca9b4021f22f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.9 MB (37932479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e26ff415a03b12ca0bb9448b8a259e69a3c668fc9342668d702b256ba8fe56d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 14 Jun 2023 17:25:34 GMT
ADD file:2e221805acb91c51e7afa6b926252ab2260cdf2e166f3d917a98384f3a157622 in / 
# Wed, 14 Jun 2023 17:25:34 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 14 Jun 2023 17:25:34 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		tar 		xz 		openssl
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 14 Jun 2023 17:25:34 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_VERSION=8.1.26
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.26.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.26.tar.xz.asc
# Wed, 14 Jun 2023 17:25:34 GMT
ENV PHP_SHA256=17f87133596449327451ad4b8d9911bfaea59ff5109f3a6f2bb679f967a8ea0f
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 14 Jun 2023 17:25:34 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 14 Jun 2023 17:25:34 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 14 Jun 2023 17:25:34 GMT
RUN docker-php-ext-enable sodium
# Wed, 14 Jun 2023 17:25:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 14 Jun 2023 17:25:34 GMT
WORKDIR /var/www/html
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 14 Jun 2023 17:25:34 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Jun 2023 17:25:34 GMT
EXPOSE 9000
# Wed, 14 Jun 2023 17:25:34 GMT
CMD ["php-fpm"]
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 14 Jun 2023 17:25:34 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 14 Jun 2023 17:25:34 GMT
ENV DRUPAL_VERSION=7.98
# Wed, 14 Jun 2023 17:25:34 GMT
ENV DRUPAL_MD5=4139f0feecb44a53645242194809b73a
# Wed, 14 Jun 2023 17:25:34 GMT
RUN set -eux; 	curl -fSL "https://ftp.drupal.org/files/projects/drupal-${DRUPAL_VERSION}.tar.gz" -o drupal.tar.gz; 	echo "${DRUPAL_MD5} *drupal.tar.gz" | md5sum -c -; 	tar -xz --strip-components=1 -f drupal.tar.gz; 	rm drupal.tar.gz; 	chown -R www-data:www-data sites modules themes # buildkit
```

-	Layers:
	-	`sha256:b69f31b9e61dae76a66eb3f9dd10f9f86d10116c6339347c47739dcf850af4d3`  
		Last Modified: Mon, 07 Aug 2023 19:42:48 GMT  
		Size: 3.2 MB (3175974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153856869a93ebfc3f61d3f5116b1550a1aebd971304ed195e66a4151a189042`  
		Last Modified: Sat, 21 Oct 2023 03:23:45 GMT  
		Size: 3.8 MB (3762212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef93127a61d902b0f6d7e810968191c39e1ae40f7e4314f70b295007af54e7f0`  
		Last Modified: Sat, 21 Oct 2023 03:23:45 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:823533547a7c859ffaad5a027c6b4f8adec6cbdbc7472544cd88f0360c6cae08`  
		Last Modified: Sat, 21 Oct 2023 03:23:45 GMT  
		Size: 267.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4833209b3581168644eef034cdb62f2286e0225f0b6c5a730674f78ea8e38c93`  
		Last Modified: Mon, 27 Nov 2023 23:34:13 GMT  
		Size: 11.8 MB (11829941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffbda412c306b98c77174d314c74db394f0820e280159d8c8b34237f25bf2452`  
		Last Modified: Mon, 27 Nov 2023 23:34:12 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba75988ad172ed8c334145d2772dd533f8232a92e6c984aaa1d9bd03d18175a`  
		Last Modified: Mon, 27 Nov 2023 23:34:27 GMT  
		Size: 13.9 MB (13918280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3192ed399a05dd0925b0eb27acea10a70af8fab8b0ac09e2091e1a7f28f4d2e9`  
		Last Modified: Mon, 27 Nov 2023 23:34:25 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce381e46e9b261e9e60764831e0e59174497dfbc708d98410f6519d23c40587`  
		Last Modified: Mon, 27 Nov 2023 23:34:25 GMT  
		Size: 18.8 KB (18816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4204785a7cf88bc027c9d0008d324b21c6482d99b870c6e5262516c99e1426a`  
		Last Modified: Mon, 27 Nov 2023 23:34:24 GMT  
		Size: 8.9 KB (8880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:688937d8ff8a4aea727d72510886b2f706cb0f56771cd93405f2882bc9ba1e8b`  
		Last Modified: Tue, 28 Nov 2023 02:01:52 GMT  
		Size: 1.8 MB (1803281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59714a15e07ee44803c2cf11c0cc84508b87a2b0cde8c3e83477a15c67d58ac6`  
		Last Modified: Tue, 28 Nov 2023 02:01:52 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3f0db377db7537e622352c394c145e09244227d12549e693c5a04a775af962`  
		Last Modified: Tue, 28 Nov 2023 02:32:46 GMT  
		Size: 3.4 MB (3410304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:7-php8.1-fpm-alpine3.17` - unknown; unknown

```console
$ docker pull drupal@sha256:2cdc94302af45ea541356a155f6bd01768cfd0fcdb66b0f07122fcc50626bc8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.2 KB (249212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e93ee6aee2cbbef5087ab5f7fce26266bd6b6929a02a54df2ee2e0019a7bc0`

```dockerfile
```

-	Layers:
	-	`sha256:a1819133457b23175b1c65d71ed092aaf58f0854afea4b67452f032f07b012c4`  
		Last Modified: Tue, 28 Nov 2023 02:32:46 GMT  
		Size: 228.0 KB (227989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89854344849d5640f62bdd5619597eff477228a6ce5023bb4b4bdd61924000ab`  
		Last Modified: Tue, 28 Nov 2023 02:32:46 GMT  
		Size: 21.2 KB (21223 bytes)  
		MIME: application/vnd.in-toto+json
