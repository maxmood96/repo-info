## `drupal:11-fpm-alpine3.21`

```console
$ docker pull drupal@sha256:009449a30e1eb41446a2a15f87e1704a3cdb8b09eb736998423aba6cf0ec9dd2
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

### `drupal:11-fpm-alpine3.21` - linux; amd64

```console
$ docker pull drupal@sha256:b4c8439ae8670f5f4063f7da64d179bd68569fb0d1f126abc51966bf00713d3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.5 MB (55456017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb073b7fc0aa050122d211dda618d232708187594df4d1e9027ec02306eb15aa`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86_64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 16 Dec 2024 22:27:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Dec 2024 22:27:38 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_VERSION=8.3.15
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Dec 2024 22:27:38 GMT
WORKDIR /var/www/html
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
STOPSIGNAL SIGQUIT
# Mon, 16 Dec 2024 22:27:38 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 16 Dec 2024 22:27:38 GMT
CMD ["php-fpm"]
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV DRUPAL_VERSION=11.1.0
# Mon, 16 Dec 2024 22:27:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 16 Dec 2024 22:27:38 GMT
WORKDIR /opt/drupal
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:38a8310d387e375e0ec6fabe047a9149e8eb214073db9f461fee6251fd936a75`  
		Last Modified: Thu, 05 Dec 2024 21:56:24 GMT  
		Size: 3.6 MB (3644443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2981ee43f7920f748d4bece3e7abb474adcaadc3c1baf9d29477f60226cd935d`  
		Last Modified: Fri, 20 Dec 2024 21:35:23 GMT  
		Size: 3.3 MB (3336062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b5d407c468a2e1f0c35fdc3ed7ee58ce09fed59d194f1cc3ff412ef225713ec`  
		Last Modified: Fri, 20 Dec 2024 21:35:05 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492eeffe85eda81e1086b30ef62a18c99280333c82422a03e28e18aaa6ab1fef`  
		Last Modified: Fri, 20 Dec 2024 21:35:23 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e328f9fa3fbdd485355f3bd7514e1dc56995801fcc3ffe84fac7f3ce0cc2af51`  
		Last Modified: Fri, 20 Dec 2024 21:35:23 GMT  
		Size: 12.5 MB (12545941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63268d19f741e517bb845664e1f97c60a13350e784628b60fe33c9dcbfef75fc`  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a4c1dc04937765eae654284af1e8228b5833a57f019131e703a31a932e5289`  
		Last Modified: Fri, 20 Dec 2024 21:35:24 GMT  
		Size: 13.2 MB (13200626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6f461a2073e3e50bbaa22a462e1766521cf2ed6d43dcff03fb20a7ec735056`  
		Last Modified: Fri, 20 Dec 2024 21:35:24 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1009e3a6117286bd335b8bb43d3276a3e5fad5771a14bd58a439608dd104f3d0`  
		Last Modified: Fri, 20 Dec 2024 21:35:24 GMT  
		Size: 20.1 KB (20064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff6b83b58755429dc58208289d5ac99eb408af7878f8839d44b9aa1374c1d315`  
		Last Modified: Fri, 20 Dec 2024 21:35:24 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcfc6d7669b7faa85389be6d27f8b869c4a715657c98fdb92d465253d37a3579`  
		Last Modified: Fri, 20 Dec 2024 23:13:08 GMT  
		Size: 1.9 MB (1921929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098aed1814a8ac04d22d7f76c3d046d1d66e48740e603a62cfaa70723d8e8325`  
		Last Modified: Fri, 20 Dec 2024 23:13:08 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88ba0f57d9ae422edee877cb95f525d5e088ea056b67e4a5513a42adf838f7e`  
		Last Modified: Fri, 20 Dec 2024 23:13:08 GMT  
		Size: 742.2 KB (742237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c20af71355106c40d01a9ca9c651199c60fe8c55dc7c34266a452e9faa0ebc8a`  
		Last Modified: Fri, 20 Dec 2024 23:13:08 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb02d104480ed84616579b991c162518e02e29229554ff9d76aa8665ef3e84ba`  
		Last Modified: Fri, 20 Dec 2024 23:13:09 GMT  
		Size: 20.0 MB (20030987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:cddb858eaab91d32c35b9bf18366613345958374e3b261a662166f03325be617
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.4 KB (402354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ff2eca2d10e35908e03cc1ea22b66f00d36f5f47f2045d212d0750088ea17e`

```dockerfile
```

-	Layers:
	-	`sha256:203c4b4964f391e5969fe08ba0272cb18e56cef64c0ed08777d513e566c3a0b0`  
		Last Modified: Fri, 20 Dec 2024 23:13:08 GMT  
		Size: 366.1 KB (366115 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a177f8de2b5f2027c2a0d22316dfcb4768a2fdabb4625d4b44a848189bb4175`  
		Last Modified: Fri, 20 Dec 2024 23:13:08 GMT  
		Size: 36.2 KB (36239 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-alpine3.21` - linux; arm variant v6

```console
$ docker pull drupal@sha256:93a269223909d6d40782d0766aa1da4bcc01ac9062a6d4e40f5368bd79f32ab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.8 MB (53820357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734bb842e1467259be85292cd44f25e5f8c58cf8aa958f28a7429100eeee04c3`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armhf.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 16 Dec 2024 22:27:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Dec 2024 22:27:38 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_VERSION=8.3.15
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Dec 2024 22:27:38 GMT
WORKDIR /var/www/html
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
STOPSIGNAL SIGQUIT
# Mon, 16 Dec 2024 22:27:38 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 16 Dec 2024 22:27:38 GMT
CMD ["php-fpm"]
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV DRUPAL_VERSION=11.1.0
# Mon, 16 Dec 2024 22:27:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 16 Dec 2024 22:27:38 GMT
WORKDIR /opt/drupal
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:f2148afcbc6cd4497527fc652f65872130774bf9baace0e1e6a85cad9da5f62e`  
		Last Modified: Thu, 05 Dec 2024 22:17:29 GMT  
		Size: 3.4 MB (3367182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b736a50b989ce147c8a50cd4eff3990052fbae41313316dd15bdd3ae41bb055`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 3.3 MB (3302897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:520076a7063b8a800f7aeb276beb6363fa2c2192a17d803ee3f5fa20b0b0b211`  
		Last Modified: Wed, 11 Dec 2024 23:33:48 GMT  
		Size: 945.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065854d8dae5a225e01a05809bd10528e215d02290cc6d9f51d4bc29dc1ac134`  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c3015bc8c172f12cc4fe09a12da51e00e780513b39e265561ecdf83d600100`  
		Last Modified: Fri, 20 Dec 2024 22:07:15 GMT  
		Size: 12.5 MB (12545966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373e3d546cbde8439a8d33b94b4dd43b562e1d7c7e7a91409739d55c42ed2b03`  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb80e80c0330fa80d6105fe73cf9b8112dfd5a6966adc10ad082e40796c09a30`  
		Size: 12.4 MB (12403370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d54625d0cec0ed6173f57d2deb7f36f1836db6eba30f1631709339abf12ed4`  
		Last Modified: Fri, 20 Dec 2024 22:12:45 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4871ed599a983e8f274dcad4bbb5421856b5e4f6e2d41029a509ba54a67ed3cc`  
		Last Modified: Fri, 20 Dec 2024 22:12:46 GMT  
		Size: 19.9 KB (19888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccedcad885a243169d01c9a486d7ff2ad32a246cf88ecf72cd997c9d80d3251`  
		Last Modified: Fri, 20 Dec 2024 22:12:46 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dcbd2d428a7b2624db5750bcc92d1379dad59a64d4e2a4dc02955137c25d68c`  
		Last Modified: Fri, 20 Dec 2024 23:19:23 GMT  
		Size: 1.4 MB (1394140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08caf27db20e957284b3d2bfb3e527955242cccf76297117c11a34c569e909cd`  
		Last Modified: Fri, 20 Dec 2024 23:19:23 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043a70046e577b7d204f1d6cc9b557779cbc11bba2be2b563b2598379ea832a2`  
		Last Modified: Fri, 20 Dec 2024 23:19:23 GMT  
		Size: 742.2 KB (742237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7480e13c602c8b6812f811b6966ba056c91620d2e58ff631ecd9398af9a0d3`  
		Last Modified: Fri, 20 Dec 2024 23:19:23 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70bcb0b0e5bbea289704acc9d81961caa5f9e5a6fa453861cb3ed9e055f840f9`  
		Last Modified: Fri, 20 Dec 2024 23:19:25 GMT  
		Size: 20.0 MB (20030942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:f0178e80addc750d362cb05537816506f989fe396f85f8bf47bf6991241d789e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.2 KB (36244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce6b7191255248c08d4de6be2ed7852604e869b2ae8cc79f9200cc5300bc3dd3`

```dockerfile
```

-	Layers:
	-	`sha256:2ff5c66c8a61b0d356e20c9d30a9ff8208f2ed4c6463302457b86877bc6b1f8c`  
		Last Modified: Fri, 20 Dec 2024 23:19:23 GMT  
		Size: 36.2 KB (36244 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-alpine3.21` - linux; arm variant v7

```console
$ docker pull drupal@sha256:1eff7ae92d158812ff651fd875c15d4637f654cfd12d28e81266dd99912c7d8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52554664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a4409f0a2c13bcc2770a2738ebe18576b195bc101a7af06985e3b5a6bce2286`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-armv7.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 16 Dec 2024 22:27:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Dec 2024 22:27:38 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_VERSION=8.3.15
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Dec 2024 22:27:38 GMT
WORKDIR /var/www/html
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
STOPSIGNAL SIGQUIT
# Mon, 16 Dec 2024 22:27:38 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 16 Dec 2024 22:27:38 GMT
CMD ["php-fpm"]
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV DRUPAL_VERSION=11.1.0
# Mon, 16 Dec 2024 22:27:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 16 Dec 2024 22:27:38 GMT
WORKDIR /opt/drupal
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:39ad020c297459aff9281e5c635286218011e335f3460834ae8397a771bfec55`  
		Last Modified: Thu, 05 Dec 2024 22:17:38 GMT  
		Size: 3.1 MB (3100035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e58a80555964d79b4c54d0bc69d1ac3c99d92bfa41dc077ad9039581c976fe1`  
		Last Modified: Wed, 11 Dec 2024 23:35:20 GMT  
		Size: 3.1 MB (3128235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30daf13605f2d1179f6005fb32926b33b8626b9ceb92de019df902d09cedf935`  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7365fc515397f6962469f3d1c8654b5801822a766158bca2e8a9fa961d78db8`  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394c1cab161152681c4a4923ba5640453fb36651c5d406e1461e78fefca0ff9e`  
		Last Modified: Fri, 20 Dec 2024 23:11:53 GMT  
		Size: 12.5 MB (12545977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6990a988b6908cb902b7b7a84eabefcad3f8564ccfc05aa272984fe5cfb8bef`  
		Last Modified: Fri, 20 Dec 2024 23:11:53 GMT  
		Size: 496.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edcbc81f0ecaf0ea0f2c085b8e8a597757bdac44152166383e29ddee33c99f14`  
		Last Modified: Fri, 20 Dec 2024 23:15:35 GMT  
		Size: 11.7 MB (11683753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2efc2a5fb23eb7991af83cfa6efeaf0fe754b457dc9b64ab4a446a53af99873`  
		Last Modified: Fri, 20 Dec 2024 23:15:34 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3d570b1f188630b1108f81fab18a1b2edb5d7ffc684efa24176a3e4e28e255`  
		Last Modified: Fri, 20 Dec 2024 23:15:35 GMT  
		Size: 19.9 KB (19903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:879bca6ede7b4638a6fea24b70c80b9afb3f8d9be83b86c49f263c0260744826`  
		Last Modified: Fri, 20 Dec 2024 23:15:35 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f1315cf1c41daf7d97e1478535cac922dd7b72ce02529b20604d89c1cd24129`  
		Last Modified: Sat, 21 Dec 2024 02:22:22 GMT  
		Size: 1.3 MB (1289830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1698e879951da7bdb98fcfab0a418a4e12ad6e7b72c4305c89ea5f49bbc635`  
		Last Modified: Sat, 21 Dec 2024 02:22:22 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac862919ec6319cb42f64fe2a94ccc0bb7458d5ec85ac9462ee7939f38389a08`  
		Last Modified: Sat, 21 Dec 2024 02:22:22 GMT  
		Size: 742.2 KB (742239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13134ca089c732390fd4055015557a17af9c506b8c4f79d4d3aee30c564a513a`  
		Last Modified: Sat, 21 Dec 2024 02:22:22 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d706f63ef2324bf0d453836e85446fc36116cc7e2c9db0c7b7d610f13e0ec0a5`  
		Last Modified: Sat, 21 Dec 2024 02:22:23 GMT  
		Size: 20.0 MB (20030953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:4cfb297d7b82be802b18a3635dd6cc28d7fdf01d8efca6706cd9e0133eb70d17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.9 KB (399893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c5db55dc654839626ef1c4452fb29eb033a9f8b3912d170f72b980cf7801d7`

```dockerfile
```

-	Layers:
	-	`sha256:e36932ba5f60ab21c282a022f9b3c38bcb4ed9a9ac062b1be7d3cf09cfa57f30`  
		Size: 363.4 KB (363434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cefd9dfdc6fbea9e82bd1ff643d69518c3949ef8745317fcc668a32806c1d44`  
		Size: 36.5 KB (36459 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:6cc248cccae907eb40c10fee168786e39ca1656fd53163e7fbabb01a130f152c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56540017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06b5ea12cdfc2b43f78b02179e9871bc65e5248942c2a544aaedb543baf3861a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-aarch64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 16 Dec 2024 22:27:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Dec 2024 22:27:38 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_VERSION=8.3.15
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Dec 2024 22:27:38 GMT
WORKDIR /var/www/html
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
STOPSIGNAL SIGQUIT
# Mon, 16 Dec 2024 22:27:38 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 16 Dec 2024 22:27:38 GMT
CMD ["php-fpm"]
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV DRUPAL_VERSION=11.1.0
# Mon, 16 Dec 2024 22:27:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 16 Dec 2024 22:27:38 GMT
WORKDIR /opt/drupal
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:cb8611c9fe5154550f45e284cf977cda4e2b2fee3478552eee31d84be3c95003`  
		Last Modified: Thu, 05 Dec 2024 22:17:35 GMT  
		Size: 4.0 MB (3993186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02eb691f526c59a4feade4837dd3c26533d9fe4c9306da60dc23a30620af346`  
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
	-	`sha256:abdd784aa3aa9333198dc46c8715a262b645c7e812b668343a6f8907ec3a1148`  
		Last Modified: Fri, 20 Dec 2024 22:56:13 GMT  
		Size: 12.5 MB (12545959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca86c163e8e53a33f4164c153a4aff9feed1c3820307c6126f0b0885d15669a0`  
		Last Modified: Fri, 20 Dec 2024 22:56:12 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f2ed91ebf2a94e75de814d21306756c7f0f771545c9c159997e66eb8c29765`  
		Last Modified: Fri, 20 Dec 2024 23:01:22 GMT  
		Size: 13.7 MB (13672364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40636246d4c25465f1c8c095a26c4c1ce1fd022f2f1c54553655f98d0d3c4a42`  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d8fc0f3006cf1a9ebda082fe22e187bc1df7bc395d00acbed5deb7e04905d76`  
		Last Modified: Fri, 20 Dec 2024 23:01:22 GMT  
		Size: 19.9 KB (19893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9e595f567ac627689b98f0cd97cfe51f90324d7961aa34e58415ebc305ef06`  
		Last Modified: Fri, 20 Dec 2024 23:01:22 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42a20e3ee01a88e021eb57cd52acbf7536fa0e3b1fb3ad7465de8d0c6022a465`  
		Last Modified: Sat, 21 Dec 2024 05:17:36 GMT  
		Size: 2.2 MB (2190158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554722f7d903f1f88d4327128a6d7eccf532b7da6653385ca49179f6135afd76`  
		Last Modified: Sat, 21 Dec 2024 05:17:35 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:495389664c0df1b83f19ab52266b177ccccd52fbeae5edfbcc2de90ffa47116a`  
		Size: 742.2 KB (742236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe66fe2b6712af345411456c19e724ef68539ab776c957b5c91941540f254be`  
		Last Modified: Sat, 21 Dec 2024 05:17:36 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50c45e5e364bed75d6f04e40a46c0e3d89edc84844c05ed125da1af2e91c6208`  
		Last Modified: Sat, 21 Dec 2024 05:17:37 GMT  
		Size: 20.0 MB (20030894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:938bcb0ba168b360e2891e67f9d80f8e75e5efb80f30a14c25942bae7db7246c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.0 KB (400044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35fa35be1d270e28f3c175bdf892941f071ca241730b947e39e77f885088ee03`

```dockerfile
```

-	Layers:
	-	`sha256:c905e8eb24f6b0f555b8d362d1db41704693bdf26d5faa021ce6a20c7440698b`  
		Last Modified: Sat, 21 Dec 2024 05:17:35 GMT  
		Size: 363.5 KB (363502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34c9b401d21b9534f5c743407d816859547d91813c734dbfbc808630ee8c52fd`  
		Last Modified: Sat, 21 Dec 2024 05:17:35 GMT  
		Size: 36.5 KB (36542 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-alpine3.21` - linux; 386

```console
$ docker pull drupal@sha256:7ba0f87c773d56d50a252d7f201b116af10650c5daf74b381e78971cccebf4d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.7 MB (55685609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dfd40496b0afb3ff0055d4925ddb59a01287cbf61a5a37787849cfc99cd4685`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-x86.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 16 Dec 2024 22:27:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Dec 2024 22:27:38 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_VERSION=8.3.15
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Dec 2024 22:27:38 GMT
WORKDIR /var/www/html
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
STOPSIGNAL SIGQUIT
# Mon, 16 Dec 2024 22:27:38 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 16 Dec 2024 22:27:38 GMT
CMD ["php-fpm"]
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV DRUPAL_VERSION=11.1.0
# Mon, 16 Dec 2024 22:27:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 16 Dec 2024 22:27:38 GMT
WORKDIR /opt/drupal
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:8e5e849a30a22d7386238d38bd56dd5564638f4856bee415fad2bc5852c31989`  
		Last Modified: Thu, 05 Dec 2024 22:17:33 GMT  
		Size: 3.5 MB (3466081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a41742cdeb2f0681a5356ffa552913f128ab77d2e3e40a615057f406a6608a97`  
		Last Modified: Fri, 20 Dec 2024 21:37:01 GMT  
		Size: 3.4 MB (3376584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79041d0d94e5a6e2ba763089ec2e6d5ee0f5a15c5723ae2f0090dad1b7338b81`  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca27fda8dd6fcfd8c4aa922d62f22349e8027645f13b28c1b15da463c008032`  
		Last Modified: Fri, 20 Dec 2024 21:37:01 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fd821165e2b5cfb5e91b8f6a4ea99ddcc996468cafd9a6c52ac1e6a8cb28d6`  
		Last Modified: Fri, 20 Dec 2024 21:37:02 GMT  
		Size: 12.5 MB (12545930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a4ca6f6764f2a8e85a431058fd711691ac9f3c89012104a53d1167a78cffce8`  
		Last Modified: Fri, 20 Dec 2024 21:37:02 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cb4ce3c9a2484c4134e96bfb2f738eb90cfcf2930ddf38c43899935af4b853`  
		Last Modified: Fri, 20 Dec 2024 21:37:03 GMT  
		Size: 13.5 MB (13505404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d77825521eb7dee1b9c82d71ae29688eece3be6264ec9ad0fd508616a04db4a`  
		Last Modified: Fri, 20 Dec 2024 21:37:02 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3de4adc1166e756eca5d52e8ac1938a2d4f21ecff30398c97b96e4642866511`  
		Last Modified: Fri, 20 Dec 2024 21:37:03 GMT  
		Size: 20.1 KB (20073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2acb52fae92c9a1c753a6ad0cd0d49623bc0bb2d5d8c913cd6d71a7e6ec1698`  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f0835ef3ca90107b4ec9c110383f1a582b310aa084db7e669dbc2a7be0c80e`  
		Last Modified: Sat, 21 Dec 2024 00:11:56 GMT  
		Size: 2.0 MB (1984627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54b13fcad3f1cb5083a9f4dc153231e77b1b83a83637c79e253ffa139fbe0c7`  
		Last Modified: Sat, 21 Dec 2024 00:11:56 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2981bb5873a8cf789d580ff7c17c78bf08e64b2d7625c6e0fa4ddb24d50671f`  
		Last Modified: Sat, 21 Dec 2024 00:11:56 GMT  
		Size: 742.2 KB (742240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3318ea152faaca6f4bd5aed4008ea6bf3c25e0693ddc73199b45096932fbe07d`  
		Last Modified: Sat, 21 Dec 2024 00:11:56 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91323b0002fd823104e6bec755a70719ad1b762b59fe7333975e553b42384f00`  
		Last Modified: Sat, 21 Dec 2024 00:11:57 GMT  
		Size: 20.0 MB (20030938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:7f7f93cdc45d0b88577d14aec45635c49a1c4c6aae886e159027e19c96a84195
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.2 KB (402166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbe67e4985c4e251f747a1bbcb87a826f70d7c7b8455682195d51154edf19ea1`

```dockerfile
```

-	Layers:
	-	`sha256:8b2e183ef56034de403413fb6a1e8792299d67d9e10c09c89bdad0966a4ea133`  
		Last Modified: Sat, 21 Dec 2024 00:11:56 GMT  
		Size: 366.0 KB (366030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:725662d0eff767bcd7f185011c22c955aef7f951d0a6897cfda92f5e7127e564`  
		Size: 36.1 KB (36136 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-alpine3.21` - linux; ppc64le

```console
$ docker pull drupal@sha256:488fe398be50ff862d23dbfc9c11d9c0b5deef2650daeea371817203c624d25f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56257059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29b3cdc5e7a075582d0a743a5a837860aa12f7bc7a3ccf6d2dc74d3f99432afa`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-ppc64le.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 16 Dec 2024 22:27:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Dec 2024 22:27:38 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_VERSION=8.3.15
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Dec 2024 22:27:38 GMT
WORKDIR /var/www/html
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
STOPSIGNAL SIGQUIT
# Mon, 16 Dec 2024 22:27:38 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 16 Dec 2024 22:27:38 GMT
CMD ["php-fpm"]
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV DRUPAL_VERSION=11.1.0
# Mon, 16 Dec 2024 22:27:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 16 Dec 2024 22:27:38 GMT
WORKDIR /opt/drupal
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:a12ff663c50b78339bd273940ba035e29d8220954846a4c35a5f79080b37a3d3`  
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
	-	`sha256:24d40603d4b850df238e35dbc6816a13b2e6235c3102fed1724294ce15efefcb`  
		Last Modified: Fri, 20 Dec 2024 22:24:50 GMT  
		Size: 12.5 MB (12545962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5d5810e908afeb19def92ea6df97eae826289a0f43bf9898a15337b467aa50b`  
		Last Modified: Fri, 20 Dec 2024 22:24:49 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7285436c421faa1ca0e751ce703308066a5a1e0f69e75c3e04ad0030a9c13775`  
		Last Modified: Fri, 20 Dec 2024 22:28:22 GMT  
		Size: 14.2 MB (14160911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f02e4ba87cb6cea0c3eaa88a4d6c377fddeefe2684e037970ed0f93c006ae4`  
		Last Modified: Fri, 20 Dec 2024 22:28:21 GMT  
		Size: 2.4 KB (2445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df2347ea3c703c6b84b706275d2baee82427e09c8d2a5586538f80a5f87d9405`  
		Size: 19.9 KB (19897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3149db3f1553e27f3b1362e40bf09f47e5598fdaf78d5bc97818896b5e698bf7`  
		Last Modified: Fri, 20 Dec 2024 22:28:21 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df14c2d6583d27a62998d3e6e6b0acf6d58e1569de0122f064e9773c7854ed41`  
		Last Modified: Sat, 21 Dec 2024 02:55:19 GMT  
		Size: 1.7 MB (1691979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adf3b53037be9ad72572ad72edac141141ca6b79c122a0463a017e8dd47a7cb6`  
		Last Modified: Sat, 21 Dec 2024 02:55:19 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:619086fd63ece8f6623b7301b0bc3ae99800d91dba9faaf0537339286f41cca8`  
		Last Modified: Sat, 21 Dec 2024 02:55:19 GMT  
		Size: 742.2 KB (742238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6288e169b14113f356d083e4859f9c63a2658cce0cef81e0921cecf99145b5a`  
		Last Modified: Sat, 21 Dec 2024 02:55:19 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203d51ed0afdac59c1aca62271511645edebf9118dfe3051aba4754b3b39a431`  
		Last Modified: Sat, 21 Dec 2024 02:55:21 GMT  
		Size: 20.0 MB (20030961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:b8e50aad12327bb549315383d00eac0d96721e99cae799a6323bd818c5d4f7cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.8 KB (397826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc55de80c170a50c3b5b167f627b1a8f5b32083121bd8fcfb0260bf37ea9c62f`

```dockerfile
```

-	Layers:
	-	`sha256:601b67c48e834f7eca27e7b971b6d754fdb3179cd99e670c624d5eeccafd30df`  
		Size: 361.5 KB (361457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da0e76927561469b52cfa7f86d687283c6b1b35dbab2c423798d1b5aa8e50f02`  
		Size: 36.4 KB (36369 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-alpine3.21` - linux; riscv64

```console
$ docker pull drupal@sha256:8f3cf9e6da1d3cc540c4f5e31b8fd10f78fcc1d97c181061f401491a5495bf99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.8 MB (54813465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed5c5339465158c2a6b1ad7ed2bec8643efa2b33010e65e09c0552394ea1f63b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-riscv64.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 16 Dec 2024 22:27:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Dec 2024 22:27:38 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_VERSION=8.3.15
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Dec 2024 22:27:38 GMT
WORKDIR /var/www/html
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
STOPSIGNAL SIGQUIT
# Mon, 16 Dec 2024 22:27:38 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 16 Dec 2024 22:27:38 GMT
CMD ["php-fpm"]
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV DRUPAL_VERSION=11.1.0
# Mon, 16 Dec 2024 22:27:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 16 Dec 2024 22:27:38 GMT
WORKDIR /opt/drupal
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:a6d4526e72329f3572a607f27b44cacf8e150856b24a0178c889732b00471eb3`  
		Last Modified: Thu, 05 Dec 2024 22:19:03 GMT  
		Size: 3.4 MB (3354022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f4d72319026451a2551d3aadef8d677694387fab55cabeb9cbfc0eb4e3dea03`  
		Last Modified: Thu, 12 Dec 2024 02:34:49 GMT  
		Size: 3.4 MB (3445761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca9c93fa8ac38e6017fe5251627d738084239fbab425319ead8bdece897e493`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 946.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011fcd924c23dea0d5c69cc213494734a9bd1dc4cba0284c8b817cd82ff126a6`  
		Last Modified: Thu, 12 Dec 2024 02:34:48 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480f55a34db1d920fdb0fde2a7db7b9921e9c3037a184e705b537b59acbba255`  
		Size: 12.5 MB (12545944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ec58601b0f7a00ee0a722ab084eb9dd5ff3a8be49ce3ad70df14cbaab554eb`  
		Last Modified: Sat, 21 Dec 2024 04:07:15 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11b1f931a6f37ee831a17be3bf5d6641bab60244f9bace237fe02d2ce9dd1822`  
		Last Modified: Sat, 21 Dec 2024 05:02:49 GMT  
		Size: 13.2 MB (13180780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914443008895b62b8fb11d43caa8f2b31b8811c7f299ef52aa1fee9a06723108`  
		Last Modified: Sat, 21 Dec 2024 05:02:46 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf011b88caafc3cd9722ad9e0558db1b9db8bb6968edcecec6d5bd398900a2d0`  
		Last Modified: Sat, 21 Dec 2024 05:02:47 GMT  
		Size: 19.9 KB (19882 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270db71f14920874c2aa4c7b7ad2afe56b7e09418c0c3367fded85dfe466ce59`  
		Last Modified: Sat, 21 Dec 2024 05:02:47 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419175e45548776d9ec79da83672fc2382c19826fd7b3962392bb9de162885a1`  
		Last Modified: Sat, 21 Dec 2024 18:17:01 GMT  
		Size: 1.5 MB (1480147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5863f6a469aebc75ed8b53d78c478cca162c5839d3b6caa78d8b9571d60b0687`  
		Last Modified: Sat, 21 Dec 2024 18:17:01 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2458aa61f8b4788b1d584f3a1b6061640c2be90d9a56a813bd96327c000fb1`  
		Last Modified: Sat, 21 Dec 2024 18:17:02 GMT  
		Size: 742.2 KB (742240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0224d8b3ab70570153e4164afff91b229a6cea6ebf5dd0c6d3d6bb9ae869fa15`  
		Last Modified: Sat, 21 Dec 2024 18:17:01 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f6a000aefb554fcf8c079110c6293bd9550b2e3a29709b1ce9b336e6ca76df`  
		Last Modified: Sat, 21 Dec 2024 18:17:05 GMT  
		Size: 20.0 MB (20030936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:03f6db6ddf2bca45d1b54525d878db2b5f01472dc9b9e658b2d5019a329462fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.8 KB (397822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2ea17f01aec216917504ae750c4ec5b27cf354dea45706a1f2821b385b2227c`

```dockerfile
```

-	Layers:
	-	`sha256:9f90fee47186178eca7c607c1516b03fd99a660412a7628aa9a5008e590ebc04`  
		Last Modified: Sat, 21 Dec 2024 18:17:01 GMT  
		Size: 361.5 KB (361453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aac031ed217d75108db5c0c649b9647a9707fc5fff8d6bb32ec1a8d302e24e96`  
		Last Modified: Sat, 21 Dec 2024 18:17:01 GMT  
		Size: 36.4 KB (36369 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:11-fpm-alpine3.21` - linux; s390x

```console
$ docker pull drupal@sha256:01447c28e91726868079bff2fa1a2c1da9ffe912e076b01f6e03ee6facba401e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55648010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a56eca746dd8374b44ba5fb0463acfb2b1d667d5b7d993f14af12fe2ec91b5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 05 Dec 2024 12:49:04 GMT
ADD alpine-minirootfs-3.21.0-s390x.tar.gz / # buildkit
# Thu, 05 Dec 2024 12:49:04 GMT
CMD ["/bin/sh"]
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Mon, 16 Dec 2024 22:27:38 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 16 Dec 2024 22:27:38 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_VERSION=8.3.15
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Mon, 16 Dec 2024 22:27:38 GMT
WORKDIR /var/www/html
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
STOPSIGNAL SIGQUIT
# Mon, 16 Dec 2024 22:27:38 GMT
EXPOSE map[9000/tcp:{}]
# Mon, 16 Dec 2024 22:27:38 GMT
CMD ["php-fpm"]
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV DRUPAL_VERSION=11.1.0
# Mon, 16 Dec 2024 22:27:38 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Mon, 16 Dec 2024 22:27:38 GMT
WORKDIR /opt/drupal
# Mon, 16 Dec 2024 22:27:38 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Mon, 16 Dec 2024 22:27:38 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
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
	-	`sha256:91c11d6f86ca7437fe4a6a209590a8ca3973436d40c816d6a4753ea1e31df310`  
		Last Modified: Fri, 20 Dec 2024 22:34:58 GMT  
		Size: 12.5 MB (12545971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e07bf1e01ae20cef8eb7176641bf854d4835230837db97c3bcf55b91998ecae`  
		Last Modified: Fri, 20 Dec 2024 22:34:57 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:635be795b2eb720fd5916a88d5f50dca0b6c75325b77868505450c0a762cb69e`  
		Last Modified: Fri, 20 Dec 2024 22:38:47 GMT  
		Size: 13.7 MB (13652462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d65f0d5339973da6a7a4dbea603cf5e3f51d0e191d154a9a2d95ce382f296f`  
		Last Modified: Fri, 20 Dec 2024 22:38:47 GMT  
		Size: 2.4 KB (2442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257fd3539759724f5ddf273730427f31660fb0aaef252ac254360f8960b6cd02`  
		Last Modified: Fri, 20 Dec 2024 22:38:47 GMT  
		Size: 19.9 KB (19894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e30cb1ac3ac1fd6b9e105903bfe4b6de56cc91fcdc33c8d7fe9ad168ead682b9`  
		Last Modified: Fri, 20 Dec 2024 22:38:47 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3aba4a1f0037ae1dc96343d3a3ab3bf1d799e07d48a89457b058da0d6110d67`  
		Size: 1.6 MB (1611525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c5c58dec87261674021de22d23f8cf41fd4c17208b641f7fb9b20bbb496227`  
		Last Modified: Sat, 21 Dec 2024 03:12:32 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b3a6359e6ba6c867189d1b64790cedc21f101e1f5fa825e87ede923e011a1d`  
		Last Modified: Sat, 21 Dec 2024 03:12:32 GMT  
		Size: 742.2 KB (742240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea552a231fad900f4ac5940ff70210ef08fb933761c09eec23cfa0fd4cf4e40a`  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f29d264571a810f2704613494bed296a6d27691ea77744d165df8d9094c8d13`  
		Last Modified: Sat, 21 Dec 2024 03:12:34 GMT  
		Size: 20.0 MB (20030914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:11-fpm-alpine3.21` - unknown; unknown

```console
$ docker pull drupal@sha256:bb5aeb6af4282ad5e69d9f236e1c4e4cc733c28bb6c9851895f0e5e2348c3457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.6 KB (397590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e83addaf693100e19af89be4da3b409f3652b246857265eb9b87605ad6fcf50d`

```dockerfile
```

-	Layers:
	-	`sha256:d86f920998937a7d4e4ca622a3e09f7a05024f57c9dd2af7ca07ac49f0fd37b6`  
		Last Modified: Sat, 21 Dec 2024 03:12:31 GMT  
		Size: 361.4 KB (361351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ac4731ab409d83cdda0e3eecfa343fc53239e5636e93dc4668e8f98f12ac7e0a`  
		Last Modified: Sat, 21 Dec 2024 03:12:31 GMT  
		Size: 36.2 KB (36239 bytes)  
		MIME: application/vnd.in-toto+json
