## `drupal:php8.2-fpm-alpine`

```console
$ docker pull drupal@sha256:7f1ee0a4f898f7d74b4350c795f09d09fff2a8aef60596ed7d688b635c6203e4
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

### `drupal:php8.2-fpm-alpine` - linux; amd64

```console
$ docker pull drupal@sha256:b1cbe84fee71e2a7145eb49c4ae9d30fbc411f34970bdf6f70f948fa0c61f186
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53350561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2053454b69f1728676fada49812b310c13a642fd93b054c58f60f94b6821e147`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 17 Jan 2024 22:53:51 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Wed, 17 Jan 2024 22:53:51 GMT
CMD ["/bin/sh"]
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 17 Jan 2024 22:53:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Jan 2024 22:53:51 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_VERSION=8.2.15
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 17 Jan 2024 22:53:51 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 17 Jan 2024 22:53:51 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 17 Jan 2024 22:53:51 GMT
RUN docker-php-ext-enable sodium
# Wed, 17 Jan 2024 22:53:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 17 Jan 2024 22:53:51 GMT
WORKDIR /var/www/html
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 17 Jan 2024 22:53:51 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jan 2024 22:53:51 GMT
EXPOSE 9000
# Wed, 17 Jan 2024 22:53:51 GMT
CMD ["php-fpm"]
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
ENV DRUPAL_VERSION=10.2.2
# Wed, 17 Jan 2024 22:53:51 GMT
WORKDIR /opt/drupal
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9ef19a461f9d419fc91c59399a9daa1f3302d30f099065a185a8bfeea3c9a8`  
		Last Modified: Sat, 27 Jan 2024 05:36:08 GMT  
		Size: 2.8 MB (2761515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2fc49c6a93ebf520a5ecba9c061dbdd22083df74d0de9dcac9011f3f927d9f`  
		Last Modified: Sat, 27 Jan 2024 05:36:08 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a4aa92ed6361a95da0e916e30e661754a1edf38c0b8b15bee6872d055e3603`  
		Last Modified: Sat, 27 Jan 2024 05:36:08 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bdde487d2c3c481b0aa4cd0406254b43519751c01aa878faabca1606841a70b`  
		Last Modified: Sat, 27 Jan 2024 05:38:36 GMT  
		Size: 12.1 MB (12096363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:243db39c4f41b17d1f4c981d29228b0eb61f114ae253a3f4f129690393294e2e`  
		Last Modified: Sat, 27 Jan 2024 05:38:36 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53efed4e67e9e058bf4248baae909225e8465dce9c5b817f002aaf6ec44ca830`  
		Last Modified: Sat, 27 Jan 2024 05:39:19 GMT  
		Size: 12.8 MB (12848982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea1e3b7a6c96ad81accc89f994fd1703472ee8c09610defadf7413dd14a84b4`  
		Last Modified: Sat, 27 Jan 2024 05:39:17 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a808721a61eca53c289206c4a2077823696d71938aa6303f8de9b54394e062c9`  
		Last Modified: Sat, 27 Jan 2024 05:39:17 GMT  
		Size: 19.3 KB (19288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a3cc5a1024bad9c8ddf1e09b9099dbf48cffbb02da3f524161f7b3a52a470f`  
		Last Modified: Sat, 27 Jan 2024 05:39:18 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcef1955b8e15899425a0fc5fc4948ec1ff5bf195e246ab58ab6b1bc2be42c3f`  
		Last Modified: Sat, 27 Jan 2024 11:54:54 GMT  
		Size: 2.3 MB (2281653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84090c961bc8520bc421ccdcdebe54e2d327a8614df88f71fead9acdeba7c1c`  
		Last Modified: Sat, 27 Jan 2024 11:54:53 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47be01fe1a0e85d5634e030e7d2ad6faa01b6eb8cb5907470d50cecb477eb022`  
		Last Modified: Sat, 27 Jan 2024 11:54:53 GMT  
		Size: 705.2 KB (705204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e7fe98d21f1335eb18ae0c831bfc3731af68b5f8ba69e32bf0bef9d95a2061`  
		Last Modified: Sat, 27 Jan 2024 11:54:53 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba98d6c031d68ca248406ef9c85241dd1b18d1d9b96a69af44f19ad1d1ef5f18`  
		Last Modified: Sat, 27 Jan 2024 11:54:55 GMT  
		Size: 19.2 MB (19214750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:e7a34d7960cd08c0230e6ac6ea74c0e784ffefe9b34d41da472ee2a2937ee726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.6 KB (326613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56c56fecfdd4a1d71855d09ecd2687abf1ad7bc603e310c2c704229d7bdd938a`

```dockerfile
```

-	Layers:
	-	`sha256:c9c849a9a8f0c0a08e2aac314195ea694037b236bb8033304e4e408e7a3a02ba`  
		Last Modified: Sat, 27 Jan 2024 11:54:53 GMT  
		Size: 288.2 KB (288223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70b2da155cdb9673d6c5e85d566deff2e16cfd2dcf27ab1e94da89f1aed3a77c`  
		Last Modified: Sat, 27 Jan 2024 11:54:53 GMT  
		Size: 38.4 KB (38390 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.2-fpm-alpine` - linux; arm variant v6

```console
$ docker pull drupal@sha256:cb70d0bbb33f03352f050feda86d68c1a09e7853e2b4ec1e6501d4a0aef538cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51412681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acfda750a431ed88cc7108cd18d980c67c2ab7de7b1ad14a5aae9e8f3e7bae7d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 17 Jan 2024 22:53:51 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Wed, 17 Jan 2024 22:53:51 GMT
CMD ["/bin/sh"]
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 17 Jan 2024 22:53:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Jan 2024 22:53:51 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_VERSION=8.2.15
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 17 Jan 2024 22:53:51 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 17 Jan 2024 22:53:51 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 17 Jan 2024 22:53:51 GMT
RUN docker-php-ext-enable sodium
# Wed, 17 Jan 2024 22:53:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 17 Jan 2024 22:53:51 GMT
WORKDIR /var/www/html
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 17 Jan 2024 22:53:51 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jan 2024 22:53:51 GMT
EXPOSE 9000
# Wed, 17 Jan 2024 22:53:51 GMT
CMD ["php-fpm"]
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
ENV DRUPAL_VERSION=10.2.2
# Wed, 17 Jan 2024 22:53:51 GMT
WORKDIR /opt/drupal
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6147d01edb253ab7eff347bb08482a430759361f869152a4c0a0ecdd946e0d17`  
		Last Modified: Sat, 27 Jan 2024 06:44:23 GMT  
		Size: 2.8 MB (2764487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b42f6e9b3a3a721beed37ea494f71a49e981f945e849780a3cc6a57bf1c0ed9`  
		Last Modified: Sat, 27 Jan 2024 06:44:22 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7136267c1932cb42af7ae697ecc07c459f4c5a75f3adf037cdfff9774f183ff3`  
		Last Modified: Sat, 27 Jan 2024 06:44:22 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55005ed483beb1ca337359ab17a9675e229b931426997399767cc9d13937a3ad`  
		Last Modified: Sat, 27 Jan 2024 06:46:51 GMT  
		Size: 12.1 MB (12096382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aedab67bb2ee246ae317cf484a9d5751a7fe4e6b2b339dedaa0cac726c5f706`  
		Last Modified: Sat, 27 Jan 2024 06:46:50 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6ccdb14914594e3628577188a6abab005164d7a4d2693b4221f6e7f929f00d`  
		Last Modified: Sat, 27 Jan 2024 06:47:17 GMT  
		Size: 11.7 MB (11693476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f82c42b68ca4f7920ec45aee2afe77286c2034a2d6d39adaa6b82e87724f997`  
		Last Modified: Sat, 27 Jan 2024 06:47:14 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3c06177b0de9717f3d106277b69e1f907e80d34b2b7f9cdaeffe0a38d2b3a9`  
		Last Modified: Sat, 27 Jan 2024 06:47:15 GMT  
		Size: 19.1 KB (19133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76346ff4270699ce5621489a14f91f2659156895337742c85457fb76cf476dd0`  
		Last Modified: Sat, 27 Jan 2024 06:47:15 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b1b9872af53bdc63e4b74e4eebf678f0446204457f4f9723843708c7bdac86`  
		Last Modified: Mon, 29 Jan 2024 17:12:24 GMT  
		Size: 1.7 MB (1739741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2344c8264ce113c75a75f54078e6d064378ec0822ec6281d08a2fe8bd8700919`  
		Last Modified: Mon, 29 Jan 2024 17:12:24 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:260f398639daa51812026da5df4c8be2fb28f07ecec369dd63a48beecc9a79bc`  
		Last Modified: Mon, 29 Jan 2024 17:12:24 GMT  
		Size: 705.2 KB (705205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e556ca88e60671eccf3f54eba31549fde1f9eae67a7e8c3892dee84add43de86`  
		Last Modified: Mon, 29 Jan 2024 17:12:24 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a11ee193ece9cfd65bc238a3a2efd635da81abcda84cf1939c96911285b6e94`  
		Last Modified: Mon, 29 Jan 2024 17:12:26 GMT  
		Size: 19.2 MB (19214791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:e8dadd853bd7fb50f4b73d4217e502c96f3c76c66de5c66076c91c2d61dda335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 KB (36111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3cefc181eabf5b5fe6516b137dfc58282644b1c5ebedf62c9c27a74fe1cfe93`

```dockerfile
```

-	Layers:
	-	`sha256:0faa19657cf2e094bfb6c9786dceed980c58d283a5b52c6a0e33fa3873c2b3d8`  
		Last Modified: Mon, 29 Jan 2024 17:12:22 GMT  
		Size: 36.1 KB (36111 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.2-fpm-alpine` - linux; arm variant v7

```console
$ docker pull drupal@sha256:106c9e387981a9a27dcd0e414ed0531ed8dccec7153185c0fa11d4cc8ff54052
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50150977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888a8819a2d9b626693f11680cbda88b58ba8f8584195b46479adf54152013d6`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 17 Jan 2024 22:53:51 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Wed, 17 Jan 2024 22:53:51 GMT
CMD ["/bin/sh"]
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 17 Jan 2024 22:53:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Jan 2024 22:53:51 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_VERSION=8.2.15
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 17 Jan 2024 22:53:51 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 17 Jan 2024 22:53:51 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 17 Jan 2024 22:53:51 GMT
RUN docker-php-ext-enable sodium
# Wed, 17 Jan 2024 22:53:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 17 Jan 2024 22:53:51 GMT
WORKDIR /var/www/html
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 17 Jan 2024 22:53:51 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jan 2024 22:53:51 GMT
EXPOSE 9000
# Wed, 17 Jan 2024 22:53:51 GMT
CMD ["php-fpm"]
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
ENV DRUPAL_VERSION=10.2.2
# Wed, 17 Jan 2024 22:53:51 GMT
WORKDIR /opt/drupal
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fad4c06f9510d8c219b7fe261aa66aed178abd7a1c84deb7c27194f902386d7`  
		Last Modified: Sat, 27 Jan 2024 07:33:08 GMT  
		Size: 2.6 MB (2612619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53b84d0418e4ec14c0677d1849ef32a6fc29b8ff5271474a5fc99e97086db728`  
		Last Modified: Sat, 27 Jan 2024 07:33:07 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ae368cea0e62724a4b01ec73e9ff3a02291ca0fd945c2ae68057812a20aaa69`  
		Last Modified: Sat, 27 Jan 2024 07:33:07 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65dd81ce9f474926537159466ea61163cd5e0d8208708b276b446c4e937010eb`  
		Last Modified: Sat, 27 Jan 2024 07:35:35 GMT  
		Size: 12.1 MB (12096377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d966a63805a474d73af865d3d61bf83cb3046119d26647714d0f5985fe4f6a`  
		Last Modified: Sat, 27 Jan 2024 07:35:34 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd323e5b2ac241d76d5d733babb7a3a4a7dde658edc58290b02e9fa63c11a123`  
		Last Modified: Sat, 27 Jan 2024 07:35:59 GMT  
		Size: 11.0 MB (10965754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ed4bdfe230b50d193cb9f10007a1d9fff2649889a9193e9be5b0c23eb6f67a`  
		Last Modified: Sat, 27 Jan 2024 07:35:57 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b7ac3c56cb7d7124ad8521f17e32db106e10e84fe34782b3d9e0c80cc87566`  
		Last Modified: Sat, 27 Jan 2024 07:35:57 GMT  
		Size: 19.1 KB (19103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:367dc860c71a9e3a24408b5c68e457e214e06cbacf3ca8725f7fa026d2bdec5f`  
		Last Modified: Sat, 27 Jan 2024 07:35:57 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c904ef86e1a18c9149336d5af62d6639c68f076a620e34f9097bf5f6af704b3`  
		Last Modified: Sat, 27 Jan 2024 21:37:01 GMT  
		Size: 1.6 MB (1604327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb395ef9702465bc345b6d0020ebebb85b5d70e9124840e2a6dd12478a4dcd0`  
		Last Modified: Sat, 27 Jan 2024 21:37:00 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35529736d80659ddc71a55cc2d6dac78162152c3c8cd0b378f1f304d46eeb70`  
		Last Modified: Sat, 27 Jan 2024 21:37:01 GMT  
		Size: 705.2 KB (705202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2428dd0905f6a6c5f4ac8d436f1bca211b82a00634474da51b46d386287b5732`  
		Last Modified: Sat, 27 Jan 2024 21:37:01 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:003b74832891cc9fc457334ed9ffc66e105ce4e39dbf7d11c013c783718b056d`  
		Last Modified: Sat, 27 Jan 2024 21:37:03 GMT  
		Size: 19.2 MB (19214621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:0a5ea86d81ffbdba1ffa91044f7f975ae4c9d47f8f13a51bf9a484e26534ad59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.2 KB (322209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e6c8691324903e53354dbbf6309afd5a68664a689540448a762dfdb63ab1ab2`

```dockerfile
```

-	Layers:
	-	`sha256:7b20dba8c691506b2e71f260f9e6ee638b0d001d9f53fce054005b154c3f234f`  
		Last Modified: Sat, 27 Jan 2024 21:36:59 GMT  
		Size: 285.9 KB (285883 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c543313d7a26fe21899a9227b0ac1276dc699692f3f12e0ee51b8f1cea096534`  
		Last Modified: Sat, 27 Jan 2024 21:36:59 GMT  
		Size: 36.3 KB (36326 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.2-fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:c7ff0d211f5c75546bbd0436b1f9ee4b5760fd74ecabd417989080af0689ef0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53676593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cba7cce63e6caeb661cd2adb270ed1b8513a98c52fef583a255e1a8b0c6129d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 17 Jan 2024 22:53:51 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Wed, 17 Jan 2024 22:53:51 GMT
CMD ["/bin/sh"]
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 17 Jan 2024 22:53:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Jan 2024 22:53:51 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_VERSION=8.2.15
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 17 Jan 2024 22:53:51 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 17 Jan 2024 22:53:51 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 17 Jan 2024 22:53:51 GMT
RUN docker-php-ext-enable sodium
# Wed, 17 Jan 2024 22:53:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 17 Jan 2024 22:53:51 GMT
WORKDIR /var/www/html
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 17 Jan 2024 22:53:51 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jan 2024 22:53:51 GMT
EXPOSE 9000
# Wed, 17 Jan 2024 22:53:51 GMT
CMD ["php-fpm"]
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
ENV DRUPAL_VERSION=10.2.2
# Wed, 17 Jan 2024 22:53:51 GMT
WORKDIR /opt/drupal
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f072bab4d3b766550992c322a39fcd900b329ffbe17cdcb1a7d74010688b23ec`  
		Last Modified: Sat, 27 Jan 2024 08:40:23 GMT  
		Size: 2.8 MB (2815760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537d23c253bc777c8630b1470aee1d7857122cbdf09144b5cb061bde634e0fbd`  
		Last Modified: Sat, 27 Jan 2024 08:40:22 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65cde09541f81b6406c9aa0f33cd98ae9716bc8c625290248755e374475bda3`  
		Last Modified: Sat, 27 Jan 2024 08:40:22 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7635cf7aef4c63fed820cf1a7d4016022d00a0480ceb121fb03561da21ed4c16`  
		Last Modified: Sat, 27 Jan 2024 08:42:44 GMT  
		Size: 12.1 MB (12096388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acdb20c879b0f1f0e303192e729f69ee98706f083dd82eb93e38de241a74bed`  
		Last Modified: Sat, 27 Jan 2024 08:42:44 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffde6eec435e25aa53b0067ead3bd5314467757f6e43cdee2f32dd82befa4052`  
		Last Modified: Sat, 27 Jan 2024 08:43:07 GMT  
		Size: 12.9 MB (12910806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea6f640d6c7975cd9e94e989db6ac71fa97a651c18bfbf72ffb65da53583596`  
		Last Modified: Sat, 27 Jan 2024 08:43:05 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:514d668a5c83dbca5542a242a3c9350431b9fcd194bb47c2e3f22e2d00e5d2f2`  
		Last Modified: Sat, 27 Jan 2024 08:43:05 GMT  
		Size: 19.1 KB (19085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9997ebf78f09b231338f3c151603fdedc673a84e9340cef8300b5aa9432c4174`  
		Last Modified: Sat, 27 Jan 2024 08:43:05 GMT  
		Size: 9.2 KB (9175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9302de508def1f5dd39975d5104aa9c279e0d142a8847d249f48044d030f2ff7`  
		Last Modified: Sat, 27 Jan 2024 18:42:41 GMT  
		Size: 2.6 MB (2552941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d3287220c5b64fddd36ef353b83175afb1675efefa5f28fce590cfee1dd20ff`  
		Last Modified: Sat, 27 Jan 2024 18:42:41 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f290b3f5113a9d3b15c4e92d229448f2dc6e258da8b33afdf9848ad1b2d05875`  
		Last Modified: Sat, 27 Jan 2024 18:42:41 GMT  
		Size: 705.2 KB (705207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca269ba29ce663c2fa2f3b14797de47d93c9abca16467930cf5477e4ac5699a5`  
		Last Modified: Sat, 27 Jan 2024 18:42:42 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f9196985f51d80ef32d843b3085de0db93927872bfcb8b210b456809fbda9f`  
		Last Modified: Sat, 27 Jan 2024 18:42:43 GMT  
		Size: 19.2 MB (19214618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:9de3e154c73a2c3600d31747dc94d1f27b6fd9ebd058699658cd67a1d09a89c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.9 KB (321936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36892dcc06cd2515b8642d4008d4c7f1175a6ece9e4009474d28f0a2df09dda`

```dockerfile
```

-	Layers:
	-	`sha256:35e525fe0ddda2e8b8f5a7b91e1444b0a79b791a0445bf7984a8f702889942d7`  
		Last Modified: Sat, 27 Jan 2024 18:42:39 GMT  
		Size: 285.8 KB (285786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c885ea1887e259190445a1b58d6da9a8363188bf1f6f21aa6b2f66f17ada843e`  
		Last Modified: Sat, 27 Jan 2024 18:42:39 GMT  
		Size: 36.1 KB (36150 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.2-fpm-alpine` - linux; 386

```console
$ docker pull drupal@sha256:b51480ba1dc3aacec6cb60d06a33f99bef87983c9315e5bc83f46649f90ecec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53630511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80320c7cd0152107921e4d69e6d951deca9b8d7f8a65d9b578e166c33d001feb`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 17 Jan 2024 22:53:51 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Wed, 17 Jan 2024 22:53:51 GMT
CMD ["/bin/sh"]
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 17 Jan 2024 22:53:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Jan 2024 22:53:51 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_VERSION=8.2.15
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 17 Jan 2024 22:53:51 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 17 Jan 2024 22:53:51 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 17 Jan 2024 22:53:51 GMT
RUN docker-php-ext-enable sodium
# Wed, 17 Jan 2024 22:53:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 17 Jan 2024 22:53:51 GMT
WORKDIR /var/www/html
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 17 Jan 2024 22:53:51 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jan 2024 22:53:51 GMT
EXPOSE 9000
# Wed, 17 Jan 2024 22:53:51 GMT
CMD ["php-fpm"]
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
ENV DRUPAL_VERSION=10.2.2
# Wed, 17 Jan 2024 22:53:51 GMT
WORKDIR /opt/drupal
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf91a7316d2e2098b1a91882947964b19bab201421576e249c440063e956bcab`  
		Last Modified: Sat, 27 Jan 2024 06:46:12 GMT  
		Size: 2.8 MB (2825332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a5caaf92a60154c94967702a2fdee5954dec8352f776f8abc87659c4de67f6`  
		Last Modified: Sat, 27 Jan 2024 06:46:11 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d170158e1d1cffac62a145eb90dbbfd417840d1e2a9a4ae707cafa0bcc2781`  
		Last Modified: Sat, 27 Jan 2024 06:46:11 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b705d96a822720c651828184408f1a6c9eea23d8197c63f104bccb6e1d73ba73`  
		Last Modified: Sat, 27 Jan 2024 06:49:03 GMT  
		Size: 12.1 MB (12096383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87bce88821860841ad9fb8f2aa35e55484bf761143949eab88642252b79cad41`  
		Last Modified: Sat, 27 Jan 2024 06:49:02 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ed75cac09ec5f9766a622ae1979291bcfa3db20e87749b8b96bdf1ce9fa7344`  
		Last Modified: Sat, 27 Jan 2024 06:49:31 GMT  
		Size: 13.2 MB (13195968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a9ed1af92f7cd9d4833f43b5ec3fda659b5fcda099579bd9b1157f8fb3d7593`  
		Last Modified: Sat, 27 Jan 2024 06:49:28 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ec9b7459eb3fb9025e10bfa088ab0bd24e214c524d477abddd714fe74a22da`  
		Last Modified: Sat, 27 Jan 2024 06:49:28 GMT  
		Size: 19.3 KB (19292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcd34332b4b5e6c9f8687d99b6d843b070f7aa9e20d70d6cf3b3dd2fe11b6964`  
		Last Modified: Sat, 27 Jan 2024 06:49:28 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb1e1527910feca7a4d4ea5e218ea2ebc41074375c537015729c1f840bc0523`  
		Last Modified: Sat, 27 Jan 2024 09:54:57 GMT  
		Size: 2.3 MB (2315793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5d39d3a643760488b54b919aeb3985e2c67d0e1ad06c275a67ad7e8ff7c01e`  
		Last Modified: Sat, 27 Jan 2024 09:54:57 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b651771b6c2c5495213f5eccf37ef7563ec013062d89bc5eeb12920498596db2`  
		Last Modified: Sat, 27 Jan 2024 09:54:57 GMT  
		Size: 705.2 KB (705206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22e96496ead079947759f8210936f64dca2e8ca3806b83d95eb0e3a40b7947c`  
		Last Modified: Sat, 27 Jan 2024 09:54:57 GMT  
		Size: 111.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e7a125f1b0f7292b096781235bfdac813b956e61efa9174c01c3ae369474c85`  
		Last Modified: Sat, 27 Jan 2024 09:54:58 GMT  
		Size: 19.2 MB (19214378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:c1fcb753d8545095956c8052323175ebd82ae7feb9c00f43c7eb62ca38c3d262
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.4 KB (326432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d082bed6e1218ffb9534cdf1350133b729f4e9662d2736ac2ec839da0e074210`

```dockerfile
```

-	Layers:
	-	`sha256:a27c4bd9b9daacfc47eed1dec6932ee248eca203a291ea317e6688359b00e793`  
		Last Modified: Sat, 27 Jan 2024 09:54:57 GMT  
		Size: 288.1 KB (288138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f02d50f2b83d085585e8ae8634fa8f787594478eccfee22317536fcb3f559bc`  
		Last Modified: Sat, 27 Jan 2024 09:54:57 GMT  
		Size: 38.3 KB (38294 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.2-fpm-alpine` - linux; ppc64le

```console
$ docker pull drupal@sha256:e64a2dd8e58ebbc4f0452111aee0754d03406da91a29b881af9d19c657fc5057
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53694240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c5b9899c072dea9b226d7972df482f606da6956ff23071f3ea0e5b42e1950f`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 17 Jan 2024 22:53:51 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Wed, 17 Jan 2024 22:53:51 GMT
CMD ["/bin/sh"]
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 17 Jan 2024 22:53:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Jan 2024 22:53:51 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_VERSION=8.2.15
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 17 Jan 2024 22:53:51 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 17 Jan 2024 22:53:51 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 17 Jan 2024 22:53:51 GMT
RUN docker-php-ext-enable sodium
# Wed, 17 Jan 2024 22:53:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 17 Jan 2024 22:53:51 GMT
WORKDIR /var/www/html
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 17 Jan 2024 22:53:51 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jan 2024 22:53:51 GMT
EXPOSE 9000
# Wed, 17 Jan 2024 22:53:51 GMT
CMD ["php-fpm"]
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
ENV DRUPAL_VERSION=10.2.2
# Wed, 17 Jan 2024 22:53:51 GMT
WORKDIR /opt/drupal
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa8953adc2ed89719cf332d6841a33f5396f09790ebe287db3934fd2327d14b7`  
		Last Modified: Sat, 27 Jan 2024 04:21:21 GMT  
		Size: 2.8 MB (2842838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a412c6f832e805dac7f8f5eb85b03e9340bde010929c469a7aa203611edf867d`  
		Last Modified: Sat, 27 Jan 2024 04:21:21 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ad5c29bf6c410c283dc6e7c4619fb7570382a7860ef5d8b6a00e3228ea8a03`  
		Last Modified: Sat, 27 Jan 2024 04:21:21 GMT  
		Size: 268.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91dfc65a6989d02faf8ba64268e70055439b4184c1af31338fcc69df9aa4f4b4`  
		Last Modified: Sat, 27 Jan 2024 04:24:19 GMT  
		Size: 12.1 MB (12096378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc874be9fcdd85b468fdcd00a7ac26557a1dfa6ce3d214db4870df31d7669dd`  
		Last Modified: Sat, 27 Jan 2024 04:24:18 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee81264d77cbed5dd874c4a761f4e67f0318331456d87eddcfe8d4e300d3248`  
		Last Modified: Sat, 27 Jan 2024 04:24:48 GMT  
		Size: 13.3 MB (13338992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f291bcd4f88be6c7991d439cc1a391b19dac2294394a49112b4f5b107ee2b3d0`  
		Last Modified: Sat, 27 Jan 2024 04:24:46 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6b9d2ddd88902f6fb0a5c19a8b7ef7e3e5ba6782d74407d0345c3974feb779`  
		Last Modified: Sat, 27 Jan 2024 04:24:45 GMT  
		Size: 19.1 KB (19105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ce7c07f8ad7e826f226f530b811bd96fc32d55f47f15f89d99bb5a51c051e6`  
		Last Modified: Sat, 27 Jan 2024 04:24:45 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc28c1a54fdb4e99aa72e8a4d762289d92987a1c4e9ceecb2c4892d22309e86`  
		Last Modified: Sat, 27 Jan 2024 12:15:39 GMT  
		Size: 2.1 MB (2104503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b8b71ef7cc7cd30db609547aa658878907e15a9ec207d6e94a59c66af057ec`  
		Last Modified: Sat, 27 Jan 2024 12:15:38 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d8162265f1596dbb3a0febb5c82b249353c124e383fc05232b71c829e8ed8a`  
		Last Modified: Sat, 27 Jan 2024 12:15:39 GMT  
		Size: 705.2 KB (705207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9926f1e1474a93ff64b81e1d7ed30171b9dda455e823bc629eeb38299c5898`  
		Last Modified: Sat, 27 Jan 2024 12:15:38 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9388f1d8798ed1c4011ed9d39d62cb3e559a17d9ce77f5ab02e73791c051a2f`  
		Last Modified: Sat, 27 Jan 2024 12:15:40 GMT  
		Size: 19.2 MB (19214790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:5237b567a9203ec29066ae17517f6ffee524102a5cd29be966715044fcb5adaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.5 KB (320457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4efbcb1ee396e0d31425e383a8a6917d604ffb083c61d1bd37e2ea3d4c94cf8d`

```dockerfile
```

-	Layers:
	-	`sha256:e0ab480d3a12298758cfbd50b96cd3ca5dd2ad3487c7a88f73cc27b96c1941d7`  
		Last Modified: Sat, 27 Jan 2024 12:15:36 GMT  
		Size: 284.2 KB (284221 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d5b91fabc8be8861f3de6455d2eb5cce66fe4ac5f84e61a6a4efaa6b31dad7c`  
		Last Modified: Sat, 27 Jan 2024 12:15:36 GMT  
		Size: 36.2 KB (36236 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.2-fpm-alpine` - linux; s390x

```console
$ docker pull drupal@sha256:027da9c05858d27c9365e61b9c0b2de02fad1d3191091cd3b25dae7d15ee79a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52827926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce12bac93238c01c4970397df0afa87d5468ea1548736ea99c049e8d0581675d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 17 Jan 2024 22:53:51 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Wed, 17 Jan 2024 22:53:51 GMT
CMD ["/bin/sh"]
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Wed, 17 Jan 2024 22:53:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 17 Jan 2024 22:53:51 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_VERSION=8.2.15
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.15.tar.xz.asc
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PHP_SHA256=eca5deac02d77d806838275f8a3024b38b35ac0a5d9853dcc71c6cbe3f1f8765
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Wed, 17 Jan 2024 22:53:51 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-musl' && echo '--without-pcre-jit') 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 17 Jan 2024 22:53:51 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Wed, 17 Jan 2024 22:53:51 GMT
RUN docker-php-ext-enable sodium
# Wed, 17 Jan 2024 22:53:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 17 Jan 2024 22:53:51 GMT
WORKDIR /var/www/html
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Wed, 17 Jan 2024 22:53:51 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jan 2024 22:53:51 GMT
EXPOSE 9000
# Wed, 17 Jan 2024 22:53:51 GMT
CMD ["php-fpm"]
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
ENV DRUPAL_VERSION=10.2.2
# Wed, 17 Jan 2024 22:53:51 GMT
WORKDIR /opt/drupal
# Wed, 17 Jan 2024 22:53:51 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 17 Jan 2024 22:53:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a6de5ae65e656b2b4fa74ec7767361eaadc5cd5fe084c14430793caa205b914`  
		Last Modified: Sat, 27 Jan 2024 13:01:18 GMT  
		Size: 2.9 MB (2940559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22ae336f1db4cf8874ad7a1c11fdd671f8cfec2f2870323c9d69be5c95f4dc84`  
		Last Modified: Sat, 27 Jan 2024 13:01:17 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:641172590360f4af57f25f7e5069c42671cce55bb70bee9d82d9b5fb865e3edb`  
		Last Modified: Sat, 27 Jan 2024 13:01:17 GMT  
		Size: 269.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a462cee53e581fac0e8347d52eed10b734f2a96ee657bf3cc72d33a361e73044`  
		Last Modified: Sat, 27 Jan 2024 13:03:39 GMT  
		Size: 12.1 MB (12096382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae86ccd47b275d52ff8c597ac07ba00821d6a49f6a160672da08626ffb3e4ee`  
		Last Modified: Sat, 27 Jan 2024 13:03:38 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a6ba7dd265c8e072c655641baac3d3c8207b14989b48f9530d7f6e466a1e3d`  
		Last Modified: Sat, 27 Jan 2024 13:04:01 GMT  
		Size: 12.6 MB (12597111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a1fc6b555c1bf94facd39821f1301332cc3716571dd766868cf4428635638c8`  
		Last Modified: Sat, 27 Jan 2024 13:03:58 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92fb3222089f4ec15592befdafef43dd0fe5b0370e8e110922dfcf455bdbd413`  
		Last Modified: Sat, 27 Jan 2024 13:03:57 GMT  
		Size: 19.1 KB (19096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05da8d383b0b4509103b709fb6d0219680ca89038b861f3286d79a0b18d404a0`  
		Last Modified: Sat, 27 Jan 2024 13:03:57 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59bc23ed2fc7a229cbe73aaf48d646f668b5a00b76d3623f64f385ccdf1204f2`  
		Last Modified: Sun, 28 Jan 2024 00:26:21 GMT  
		Size: 2.0 MB (1998226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2444fac2513f381fc2268458becb67c13e40c65faf0aefacea806ee3fc807e5`  
		Last Modified: Sun, 28 Jan 2024 00:26:21 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:949e600aebd091c6a005562f52c0264f3220878f42b27bb1bee56a158e6412cc`  
		Last Modified: Sun, 28 Jan 2024 00:26:21 GMT  
		Size: 705.2 KB (705210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662c720cdf85207147469a4bbfd0fc7a1c9550dcbc3acf29904ce1a3f5681b7a`  
		Last Modified: Sun, 28 Jan 2024 00:26:21 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f86b4cecf8459a7581d262e68af3c65025f4c9f507ce8fcd4d0df462d14cb2f6`  
		Last Modified: Sun, 28 Jan 2024 00:26:22 GMT  
		Size: 19.2 MB (19214630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.2-fpm-alpine` - unknown; unknown

```console
$ docker pull drupal@sha256:c16623ce5a54fafa1fd975093fe13ef44746fe16ccdd367cec06aace4ab0eeb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.2 KB (320233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83aae8a5ead0a2eb7547b5e21fbb44ffa0df4e9ed0a199ff2f04dd2d7af477f`

```dockerfile
```

-	Layers:
	-	`sha256:93a5c9c6c5e8d95f80591068f912b42450c01286e6332ce54638caa920980dc6`  
		Last Modified: Sun, 28 Jan 2024 00:26:19 GMT  
		Size: 284.1 KB (284115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ade5123932b7e0e36ca030bb88c1ba51a17c6bf13c259cadc59a34fe1db2fe92`  
		Last Modified: Sun, 28 Jan 2024 00:26:19 GMT  
		Size: 36.1 KB (36118 bytes)  
		MIME: application/vnd.in-toto+json
