## `drupal:php8.3-fpm-alpine3.20`

```console
$ docker pull drupal@sha256:bcfb0984b0b161a8f6950049a9d7509685a36403e0347cba3a80d32245260fa8
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

### `drupal:php8.3-fpm-alpine3.20` - linux; amd64

```console
$ docker pull drupal@sha256:4c6bbeca5afdbfdc6b23dc6c27167ab59ede1199e6abe1dd4aeb119560e31202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.2 MB (56207305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c58ea93915772d26cea73ef2561a6ada294af915e7f16f1fce5c13a905b2424b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 04 Jul 2024 15:27:17 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Jul 2024 15:27:17 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Jul 2024 15:27:17 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_VERSION=8.3.9
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.9.tar.xz.asc
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_SHA256=bf4d7b8ea60a356064f88485278bd6f941a230ec16f0fc401574ce1445ad6c77
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 04 Jul 2024 15:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 04 Jul 2024 15:27:17 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 04 Jul 2024 15:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 04 Jul 2024 15:27:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Jul 2024 15:27:17 GMT
EXPOSE 9000
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["php-fpm"]
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV DRUPAL_VERSION=10.3.1
# Thu, 04 Jul 2024 15:27:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /opt/drupal
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ae0d9dfc4dada15e6a030ba7b9c9a3b16f9f5a7597a4d46ff24226e91b91db7`  
		Last Modified: Tue, 23 Jul 2024 03:55:04 GMT  
		Size: 3.3 MB (3272601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce295ca8623e5dc914104e970c5496db996db5f2abb336389bcbadd10465d21d`  
		Last Modified: Tue, 23 Jul 2024 03:55:03 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d3eb99f3c122bc8d6c22107602ed9c22fce771289b54bb2598142d1626f693`  
		Last Modified: Tue, 23 Jul 2024 03:55:03 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5da48d7a5e0690b25131025f4187cd876e3ef774226b1565897b1d8a7bd5e5dd`  
		Last Modified: Tue, 23 Jul 2024 03:58:16 GMT  
		Size: 12.5 MB (12491144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e142cb738903ef1899d23399f4e2e6300c8874a2c664604ec9b2775ef9e258`  
		Last Modified: Tue, 23 Jul 2024 03:58:15 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57abc6237edfae6af619240030abce2ea786ba6a536c8cd76cc8947b52af6bb3`  
		Last Modified: Tue, 23 Jul 2024 03:58:54 GMT  
		Size: 13.1 MB (13091089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd2f0795fbbeafef3b0615fc26f6abaa589c1883b1a89d6dd2ede88784193873`  
		Last Modified: Tue, 23 Jul 2024 03:58:52 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d6fe16d961db4871ad38617c0220a7b01e72a0aa02bbb376d67f99482e9a00`  
		Last Modified: Tue, 23 Jul 2024 03:58:52 GMT  
		Size: 19.7 KB (19697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22748174a5ce41806b1670b426462968ac413748ddb396e236458171671fbf17`  
		Last Modified: Tue, 23 Jul 2024 03:58:52 GMT  
		Size: 9.2 KB (9176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56204f681a5ee6e6dbf8e8ce5a77af924a6e4527f7f60a34e8715d3293f02173`  
		Last Modified: Tue, 23 Jul 2024 07:19:10 GMT  
		Size: 1.9 MB (1900638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a46bfe63ce49b8cfa3fd7241eef964f5a7d6d6bf50379e6c7617fe04c633cbc`  
		Last Modified: Tue, 23 Jul 2024 07:19:10 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6500e24b04e4ebdf24cd279e2de3b41d73e086444d23e256aa638ff2da4ff0b6`  
		Last Modified: Tue, 23 Jul 2024 07:19:10 GMT  
		Size: 726.3 KB (726325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94aab8e5589468072170708523744eb2823f8c5ab19a2626147e78b9db9b87ef`  
		Last Modified: Tue, 23 Jul 2024 07:19:08 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18ac58a92e76f9d6beb293278e70c00504febfe1fba7710ebe281fc241141964`  
		Last Modified: Tue, 23 Jul 2024 07:19:10 GMT  
		Size: 21.1 MB (21069210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:536dd195d845c0f5dfd5cd558384453ee9a63009da009a60fc1e184fee15516c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.5 KB (381452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097e99281ebbf614e8df6da2f3e96646433cef8a44b6afcbad86a26a6704db3a`

```dockerfile
```

-	Layers:
	-	`sha256:cd0ed18e2266cd412626ac35f316dd31d4510d81b64790e99fb68a8356a479fb`  
		Last Modified: Tue, 23 Jul 2024 07:19:10 GMT  
		Size: 348.8 KB (348769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:533e4f262c2232194048e3f4ac7e562e39daca72387cc0d601894f8289757e0c`  
		Last Modified: Tue, 23 Jul 2024 07:19:09 GMT  
		Size: 32.7 KB (32683 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-alpine3.20` - linux; arm variant v6

```console
$ docker pull drupal@sha256:746bba57a9b92232b3fbb9ecc1269e0ca2ec997a058f3b429dafd98db4022087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54739196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:034b55d30eb337471c74bd97a048f23c15ba4467be26df6983ce52f47ee7e1ab`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 04 Jul 2024 15:27:17 GMT
ADD file:85f927c1895bee1d0b095b2905c8d47ada8773f13e03fd4a201f718103ef7958 in / 
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Jul 2024 15:27:17 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Jul 2024 15:27:17 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_VERSION=8.3.10
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.10.tar.xz.asc
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_SHA256=a0f2179d00931fe7631a12cbc3428f898ca3d99fe564260c115af381d2a1978d
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 04 Jul 2024 15:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 04 Jul 2024 15:27:17 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 04 Jul 2024 15:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 04 Jul 2024 15:27:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Jul 2024 15:27:17 GMT
EXPOSE 9000
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["php-fpm"]
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV DRUPAL_VERSION=10.3.1
# Thu, 04 Jul 2024 15:27:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /opt/drupal
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:ae2458422e4465e718700cd0c5970c709804ded4caa7b7f317eada5d16878e29`  
		Last Modified: Mon, 22 Jul 2024 21:49:42 GMT  
		Size: 3.4 MB (3365189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b041a1a670328abed5fe2b73e068aba477e969ddbfe65c606c8054a4c36067b2`  
		Last Modified: Tue, 23 Jul 2024 01:00:35 GMT  
		Size: 3.3 MB (3263638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51daa6109cd19af541c6fc2600ad5a2f2382e50d3938e2b51f30d24df583fee`  
		Last Modified: Tue, 23 Jul 2024 01:00:33 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b57c8706e4f06f42a10294d5c9eef985613e48298dedb390c6e6816b60a8f78`  
		Last Modified: Tue, 23 Jul 2024 01:00:33 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7b5c8cff50f2b7d154a233e950b9d09158300b31e85557b8b38114e43f07cb`  
		Last Modified: Thu, 01 Aug 2024 19:32:23 GMT  
		Size: 12.5 MB (12505862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d80f66cfff4943c95c3397f600f5ed3b0e3285737ba87d8c82063ca58c1fb14`  
		Last Modified: Thu, 01 Aug 2024 19:32:22 GMT  
		Size: 498.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:096088067074af413e340f14463577ec3d036a30c4b67363dfabcc33007d690c`  
		Last Modified: Thu, 01 Aug 2024 19:33:06 GMT  
		Size: 12.4 MB (12390594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e63bbea3286cfd23ba94d0a7a0ffc8e4163a6aff496c444bc2897a5f43ca49dd`  
		Last Modified: Thu, 01 Aug 2024 19:33:03 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855c0821e70635405767e8f4fa35f3ec9a1daa3f313e52690f9d787d268f6479`  
		Last Modified: Thu, 01 Aug 2024 19:33:03 GMT  
		Size: 19.5 KB (19502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec0c737eafe5d572fe9dfd1e86e4b88d071faea971fda19d7a2c9c698617c88`  
		Last Modified: Thu, 01 Aug 2024 19:33:03 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdb261694257b34feb9c9e08d73749428cd85fc909a3d5515f092d2ade65b19b`  
		Last Modified: Thu, 01 Aug 2024 22:02:10 GMT  
		Size: 1.4 MB (1384992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe97450c795e760c0210c23eeae346cb6e7f144c3562c8ee749e71a37f93441`  
		Last Modified: Thu, 01 Aug 2024 22:02:10 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9203bedd490fac4310532e5b1626b3c7405bc4fd0f601fa8cf720fc574db9d72`  
		Last Modified: Thu, 01 Aug 2024 22:02:10 GMT  
		Size: 726.3 KB (726334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f4cdd57ba6182baacc4b3297b98f40c4c5749b77fdf8d619103c6f8a49acc11`  
		Last Modified: Thu, 01 Aug 2024 22:02:10 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c75f6bf7d06fac1a531921f0065124fd8c6b78ff55126f14b1b6c78d00078e`  
		Last Modified: Thu, 01 Aug 2024 22:37:28 GMT  
		Size: 21.1 MB (21069370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:3af4e2b1aa3b73938859d17b4b28c75812b7f2e9693ee35f01f574e170295606
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **32.6 KB (32640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:426979695928c6f603455bbb0749c62c658c026d94c46c9f3acb34c93aeb70a5`

```dockerfile
```

-	Layers:
	-	`sha256:d740268d843ffdf4ebdc6e96cf28381a7a8af33876ff806cb5b1085d21ac1dc7`  
		Last Modified: Thu, 01 Aug 2024 22:37:27 GMT  
		Size: 32.6 KB (32640 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-alpine3.20` - linux; arm variant v7

```console
$ docker pull drupal@sha256:ee6f6fb6ad9a43fddf61ac5676d5477be1c173fef754158950c534b30e69068b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.4 MB (53385146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9db429603059a0fe37b7b2a4e409fb91855ab7f68113b241b630d38aef721269`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 04 Jul 2024 15:27:17 GMT
ADD file:816da1ff7b962e1f52c650dfd66caeb2b88f3ab9fadc249c30f86ebe5372538c in / 
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Jul 2024 15:27:17 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Jul 2024 15:27:17 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_VERSION=8.3.10
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.10.tar.xz.asc
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_SHA256=a0f2179d00931fe7631a12cbc3428f898ca3d99fe564260c115af381d2a1978d
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 04 Jul 2024 15:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 04 Jul 2024 15:27:17 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 04 Jul 2024 15:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 04 Jul 2024 15:27:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Jul 2024 15:27:17 GMT
EXPOSE 9000
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["php-fpm"]
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV DRUPAL_VERSION=10.3.1
# Thu, 04 Jul 2024 15:27:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /opt/drupal
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:9c6652a37da7fb600faac56897745bdde89a4f9bd260a082b6bf4a0d173b5906`  
		Last Modified: Mon, 22 Jul 2024 22:00:23 GMT  
		Size: 3.1 MB (3094960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57db3d4836535044109c42cf341df21ab1def6a06fecbaf98ffac833b47f15b`  
		Last Modified: Tue, 23 Jul 2024 01:14:20 GMT  
		Size: 3.1 MB (3073093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7991e70be4838afae3979e2bef4b2a7682dffac44793431e072ffbc9fc1686e5`  
		Last Modified: Tue, 23 Jul 2024 01:14:19 GMT  
		Size: 943.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3967a6fef2cedd5f47096963a74875b542f5e4f6667543712aa16505b281dcf7`  
		Last Modified: Tue, 23 Jul 2024 01:14:19 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ee7fab1c6e45e49a530fb41053c616b6c4654ff85741408c2daa8103629db9`  
		Last Modified: Thu, 01 Aug 2024 20:08:43 GMT  
		Size: 12.5 MB (12505870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52be183bb835b7ee911798b48dbca91dee024087a7e36afe13fc1f8484649d6b`  
		Last Modified: Thu, 01 Aug 2024 20:08:42 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c54b192ced76774746c8ec9698e4700f2bbdaac1339aa84b2a629990670d2eee`  
		Last Modified: Thu, 01 Aug 2024 20:09:26 GMT  
		Size: 11.6 MB (11607118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca9e8ba35f98945ea8c1e78a598028dcdf7ec28e462365803f13447f6c6112b`  
		Last Modified: Thu, 01 Aug 2024 20:09:24 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e36873ef9a5eaf73aaa05d4f35d1e974ed6b8338b4aae716d7a4b27c17d5d58`  
		Last Modified: Thu, 01 Aug 2024 20:09:24 GMT  
		Size: 19.5 KB (19501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90b830e49da34553a94bda5d316abf5e3798b8e1c11bf066afeb6e3f4eeb1a7`  
		Last Modified: Thu, 01 Aug 2024 20:09:21 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ed8a6224030b44a17a106d7771788ad6e6a96c48051b28f495bb04e6e53678`  
		Last Modified: Fri, 02 Aug 2024 02:46:00 GMT  
		Size: 1.3 MB (1275364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1373a56f01327c6ed488499402dfb3d1a4ba7d97d750b2966734ec9614d08e1f`  
		Last Modified: Fri, 02 Aug 2024 02:46:00 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6e27022a4140fcfa9bc761ac96452f7fe0ff893361a333aa53e6a84e524fe8`  
		Last Modified: Fri, 02 Aug 2024 02:46:00 GMT  
		Size: 726.3 KB (726334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7bb92f3540cd96539470b8161def4cd826ecd1e2c72daf017f34bb4ab89a66d`  
		Last Modified: Fri, 02 Aug 2024 02:46:00 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a5ac3e61a1f0a329904d4ad0bb67e26007321fce8817b70d61a429b31fb2908`  
		Last Modified: Fri, 02 Aug 2024 02:56:13 GMT  
		Size: 21.1 MB (21069191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:9293656599df0aef3a245e84044463bd8c25d25ca21465559ab0b036f0795aec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.8 KB (378835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7adfbdf1dd969aa2bc69d956d64b3249f31fa2cbf36bd8fa639254341080e011`

```dockerfile
```

-	Layers:
	-	`sha256:924744319f7947761d3e7c214a0cb7537d1d07052aeca7ab7410b2aefe94b58e`  
		Last Modified: Fri, 02 Aug 2024 02:56:11 GMT  
		Size: 346.0 KB (345977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8af6e3dcc25fc52363cd6cfda1f6e5904cfce24c3e53e3c1a42d3d8d4e5edb6b`  
		Last Modified: Fri, 02 Aug 2024 02:56:11 GMT  
		Size: 32.9 KB (32858 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:cace87c7a7130b8350211f07e9765eb9bf0e5ebff30a38bbfb385f5df4b8d534
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57551891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5f4147b5414593375bf57c3a145880a3a9e2c3b5a4b56fbf1bea4066af3271c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 04 Jul 2024 15:27:17 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Jul 2024 15:27:17 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Jul 2024 15:27:17 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_VERSION=8.3.10
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.10.tar.xz.asc
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_SHA256=a0f2179d00931fe7631a12cbc3428f898ca3d99fe564260c115af381d2a1978d
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 04 Jul 2024 15:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 04 Jul 2024 15:27:17 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 04 Jul 2024 15:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 04 Jul 2024 15:27:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Jul 2024 15:27:17 GMT
EXPOSE 9000
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["php-fpm"]
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV DRUPAL_VERSION=10.3.1
# Thu, 04 Jul 2024 15:27:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /opt/drupal
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f069fb86c015646c4497d6fa3beaf8bd3f9f04d8f77a1a865ff47fc9922c27e3`  
		Last Modified: Tue, 23 Jul 2024 02:00:05 GMT  
		Size: 3.3 MB (3324720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:298458c1fe168646ba7edf3e03804ff1a01f1fac6b41ef2a94ef5bf333311f2b`  
		Last Modified: Tue, 23 Jul 2024 02:00:05 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f71c5e072e5141e780c5bbd4c1e2a34f9248a4b4a0983717a6c98be7560b899`  
		Last Modified: Tue, 23 Jul 2024 02:00:04 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0ca8306920cf340c871469010d72334d7d7b19a2b2832066d3a361bfbd8491`  
		Last Modified: Thu, 01 Aug 2024 19:49:40 GMT  
		Size: 12.5 MB (12505868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5428c467d398c1ea31f8f201c7865f041033b556e31c7e3c601f530e684f1704`  
		Last Modified: Thu, 01 Aug 2024 19:49:39 GMT  
		Size: 501.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698c91c8820e3c664296c7dcc80968f744d13946ead46ed2603c7622e10454c2`  
		Last Modified: Thu, 01 Aug 2024 19:50:18 GMT  
		Size: 13.6 MB (13628037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d343185248bb4443172b45d722efcc33937c788d6eb3995c56ad0df42ad2923`  
		Last Modified: Thu, 01 Aug 2024 19:50:16 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8f867c709a4bf6d43bb91b1bb04015c3b423f802c803934c79e640a87b7ceab`  
		Last Modified: Thu, 01 Aug 2024 19:50:17 GMT  
		Size: 19.5 KB (19492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c677eef28c51a7f91d13a5ccefaa5465165bf4b70c85edfcfa94be8fba03be9`  
		Last Modified: Thu, 01 Aug 2024 19:50:17 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b232ae98558d168b9e5b77bc1f8a620e1398c1ad082074f558b61a20d2795735`  
		Last Modified: Fri, 02 Aug 2024 05:16:41 GMT  
		Size: 2.2 MB (2177277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19a11bfeba1055e173331f845376ccb1959cf98996c02bc0d533b93cd9a84166`  
		Last Modified: Fri, 02 Aug 2024 05:16:41 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1910efd754db8d928d5cf93c4ed0a0d119b7b117c0cf5c1bc12fefde60a93da`  
		Last Modified: Fri, 02 Aug 2024 05:16:41 GMT  
		Size: 726.3 KB (726333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b90185c8134395e74bf5c552d52899464b70b62d69ad11bc9d646187165370e`  
		Last Modified: Fri, 02 Aug 2024 05:16:41 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593f97ae3934c93c338d746365f9b825cf9c13c78a8125e19f481927bbb413fe`  
		Last Modified: Fri, 02 Aug 2024 05:26:46 GMT  
		Size: 21.1 MB (21069518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:f2511eb109473e97fd2cba085e81db55ec3ed9f5a532e98d1c8f56ef2e7b4676
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.4 KB (379404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e7f2938f2718b0795ff546bbf467cd9aa49bca7b846fe7cb373587314ad636b`

```dockerfile
```

-	Layers:
	-	`sha256:cb7ff1e36b69ecbe12b80b4c0a77d5bd6e19bc16a73a95b3b055c3927741e5e1`  
		Last Modified: Fri, 02 Aug 2024 05:26:45 GMT  
		Size: 346.0 KB (346013 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ccf91bfd7fb9d6a0792893642cb3734699bf1bca5a67861e5c698319bbbc25a`  
		Last Modified: Fri, 02 Aug 2024 05:26:45 GMT  
		Size: 33.4 KB (33391 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-alpine3.20` - linux; 386

```console
$ docker pull drupal@sha256:385e2095b4bfc4f3a6b1ffaa4bd9729ff2f584b4c96a031c34b04b9f1a34a60c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56497603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd9e92663c834de5399276fc61117edb1cb1d45de5971a5cd0100c013117610c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 04 Jul 2024 15:27:17 GMT
ADD file:e5b77b9337c5f89df9a65f8c439736a6d79e68274100ab1a1d7d61359a9abf5d in / 
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Jul 2024 15:27:17 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Jul 2024 15:27:17 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_VERSION=8.3.9
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.9.tar.xz.asc
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_SHA256=bf4d7b8ea60a356064f88485278bd6f941a230ec16f0fc401574ce1445ad6c77
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 04 Jul 2024 15:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 04 Jul 2024 15:27:17 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 04 Jul 2024 15:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 04 Jul 2024 15:27:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Jul 2024 15:27:17 GMT
EXPOSE 9000
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["php-fpm"]
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV DRUPAL_VERSION=10.3.1
# Thu, 04 Jul 2024 15:27:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /opt/drupal
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:2585500d54afa42a6b579f9ed6f62b49c5fb21c2653f79194342804bde8770fe`  
		Last Modified: Mon, 22 Jul 2024 21:38:55 GMT  
		Size: 3.5 MB (3468071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3702ede31b739c37f265c096aaa90041a249a222cf13f8141408974d1da345`  
		Last Modified: Tue, 23 Jul 2024 02:14:27 GMT  
		Size: 3.3 MB (3322587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd32fd053b31656313ffe5c4d6a711c2bdfbac32689ec3ed4eb1993c89d7c5cf`  
		Last Modified: Tue, 23 Jul 2024 02:14:26 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c734d1f76ba06cf1de68095cf88223f8aecf6242e60ae0985e4b555bd937308d`  
		Last Modified: Tue, 23 Jul 2024 02:14:26 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8809eabb483bc5c67a1bcbe6b092cc84c09e8c07c3f68ceaeeadc70e1273aff`  
		Last Modified: Tue, 23 Jul 2024 02:18:04 GMT  
		Size: 12.5 MB (12491139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2348f8b19e856fcaae860d9ed870cebf7eef570d28f5780f99f5ae40199524b4`  
		Last Modified: Tue, 23 Jul 2024 02:18:02 GMT  
		Size: 497.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a26eafdbb9c641cb795207e0152291cdd53fe928b5c23368d39f89784c0dcd4c`  
		Last Modified: Tue, 23 Jul 2024 02:18:44 GMT  
		Size: 13.4 MB (13425342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2664c321ed236aa93fdeeabcb91469b9f08e1fbed2348aef59a4226d8d89d125`  
		Last Modified: Tue, 23 Jul 2024 02:18:41 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38f04ae9d0e030b3bfcbb7acd3d83ab19e34dd9703a2579f43c26b25c272d4ad`  
		Last Modified: Tue, 23 Jul 2024 02:18:41 GMT  
		Size: 19.7 KB (19700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88de5cf09cabdfbd40214e33d9ad696484086f46a92c30664c20696a658da24e`  
		Last Modified: Tue, 23 Jul 2024 02:18:41 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abebbdf3ba1006db43df81f3563580fa2356455add8a9d2c936549e75b3917dd`  
		Last Modified: Tue, 23 Jul 2024 06:09:45 GMT  
		Size: 2.0 MB (1961263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e2180c0c3f8fd0fcb58ed41cf95c85f91959ef3cff37ac2cdd238a31d4795bb`  
		Last Modified: Tue, 23 Jul 2024 06:09:45 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cfcdc7ade398cba0429991c0ee985fa0f0e124576f6aeef56c696e5434cae2`  
		Last Modified: Tue, 23 Jul 2024 06:09:45 GMT  
		Size: 726.3 KB (726331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee13c822239b59a9e04bcf6d01d7c8d6c065d4fa8a02ad7bdcb77fc9873a8605`  
		Last Modified: Tue, 23 Jul 2024 06:09:45 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96be894ff83e43ad992911c607d48aa4b9319457400beb65020b1623a59da95b`  
		Last Modified: Tue, 23 Jul 2024 06:09:46 GMT  
		Size: 21.1 MB (21069457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:c151136afe38c3760f573f81d1c6414d945c6f55928070bfe9d810fb3a065448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.3 KB (381263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfefc4bf1f9b219ced5ea8f9b0c8f5e6475909dea1fedc3e8fffcd6274953b6d`

```dockerfile
```

-	Layers:
	-	`sha256:73343f0e98f269aec74b92cb87a44b2f3a548b8ffdb581a6fb419286c03d19d4`  
		Last Modified: Tue, 23 Jul 2024 06:09:45 GMT  
		Size: 348.7 KB (348724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c5b4db05d28f8b7f977f292b6807e8d0af45ae5143430cd2325787b7f57929e`  
		Last Modified: Tue, 23 Jul 2024 06:09:45 GMT  
		Size: 32.5 KB (32539 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-alpine3.20` - linux; ppc64le

```console
$ docker pull drupal@sha256:7fdfe160b6dddea1fd60ee79f2dd0c91a40a4d727edd3b83cac4957c6811ccd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.6 MB (56562472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02938d411dad8b1ab98ccd6041341fc1d021328f0604b33d2159d2995dd480a2`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 04 Jul 2024 15:27:17 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Jul 2024 15:27:17 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Jul 2024 15:27:17 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_VERSION=8.3.9
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.9.tar.xz.asc
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_SHA256=bf4d7b8ea60a356064f88485278bd6f941a230ec16f0fc401574ce1445ad6c77
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 04 Jul 2024 15:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 04 Jul 2024 15:27:17 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 04 Jul 2024 15:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 04 Jul 2024 15:27:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Jul 2024 15:27:17 GMT
EXPOSE 9000
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["php-fpm"]
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV DRUPAL_VERSION=10.3.1
# Thu, 04 Jul 2024 15:27:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /opt/drupal
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3b3ac21bbea54c953ea1f2d18929d69c201c50acbb70a6157944a16d881644`  
		Last Modified: Mon, 22 Jul 2024 23:40:54 GMT  
		Size: 3.4 MB (3400973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ab89bd2c65997355b0f8d6c170e8ada77fc5d87ae04f4e525032aad1d1c519`  
		Last Modified: Mon, 22 Jul 2024 23:40:53 GMT  
		Size: 942.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d9ea05d06440c67793ed8359925d4dcf5e15c76e0e78b5d20fad34b553a253f`  
		Last Modified: Mon, 22 Jul 2024 23:40:53 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2298a0635b24808ca33801fc6591bee31abc336cc00659919d267d6b2dc12024`  
		Last Modified: Mon, 22 Jul 2024 23:44:07 GMT  
		Size: 12.5 MB (12491148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed3c88984fa2f5172e314ab9e3e0ca346b7bbb0164f19c329a25c2cb2542e7e`  
		Last Modified: Mon, 22 Jul 2024 23:44:07 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa23ab923f9dfbc1f35d1b08d3e876b5406fe2f0a20e8f057d283fb6382676c`  
		Last Modified: Mon, 22 Jul 2024 23:44:46 GMT  
		Size: 13.6 MB (13590133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26843a240acb5d00367a257344d40f1aad52c4cd0bcaeb6f9a1bb9dcdf12d70a`  
		Last Modified: Mon, 22 Jul 2024 23:44:43 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:558dfbb0e5e6325e4de7717bad4ab8bfe8efaaec3ae8bfe12603b2159ab4eb04`  
		Last Modified: Mon, 22 Jul 2024 23:44:43 GMT  
		Size: 19.5 KB (19484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96c71a162fb234e1c1ca5fdb9ac46486ffcdb67b8b012e1f1ab9929ec6e7fba`  
		Last Modified: Mon, 22 Jul 2024 23:44:43 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0e767128db0e527941117b875c8eafbdcb9d6c8419500f3c5695216d195939`  
		Last Modified: Wed, 24 Jul 2024 12:50:06 GMT  
		Size: 1.7 MB (1679578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eabcbf83addbcb0e85897cbf0dda8f90d35e78a745d4e44d4e96b5a0b8e90ad8`  
		Last Modified: Wed, 24 Jul 2024 12:50:06 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8189270bfb3db99189e7e1e44b7a108f1db82e0ee2d5328e6d3449204189a2`  
		Last Modified: Wed, 24 Jul 2024 12:50:06 GMT  
		Size: 726.3 KB (726340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6911b5997cdfb3e600748c76811bf09a9b08b0e6eefdd4225e0adb2744ed46de`  
		Last Modified: Wed, 24 Jul 2024 12:50:07 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0074322d0bfb0fb647e82c081255dd3cb172482e02ddec0e37f18958a3dbdaea`  
		Last Modified: Wed, 24 Jul 2024 13:09:10 GMT  
		Size: 21.1 MB (21069542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:aca5153bf0e86ef2d680de648323bf5209cc31519c4ff81a5c2f0230305cff93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.8 KB (376786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8aeaa77f22faa3297088e65e100eccfe36343d694903c5f31337e005c673f718`

```dockerfile
```

-	Layers:
	-	`sha256:cf2e029b3203c26c658bbc4e85aaf9bed72853f76eabe28f2e56ee2ba8a0baf4`  
		Last Modified: Wed, 24 Jul 2024 13:09:09 GMT  
		Size: 344.0 KB (344009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4b0491b59eb66037c4b34d170cde0ecff349702913b23141f197f76fc19e34a`  
		Last Modified: Wed, 24 Jul 2024 13:09:09 GMT  
		Size: 32.8 KB (32777 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-alpine3.20` - linux; riscv64

```console
$ docker pull drupal@sha256:88ece35ddeee9d68886ca5406b083ed924f855983f15204ffb5b9dc6282fa006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.2 MB (55242756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5ef75c60c7cec651c66d047761ee0bd666882cc4a4e4aa27aa33d9f6cf41c2`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 04 Jul 2024 15:27:17 GMT
ADD file:cdf7088bbd70519f0f5d7b4249df34386e40f0194752f45842b3d85f2d331cf5 in / 
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Jul 2024 15:27:17 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Jul 2024 15:27:17 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_VERSION=8.3.10
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.10.tar.xz.asc
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_SHA256=a0f2179d00931fe7631a12cbc3428f898ca3d99fe564260c115af381d2a1978d
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 04 Jul 2024 15:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 04 Jul 2024 15:27:17 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 04 Jul 2024 15:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 04 Jul 2024 15:27:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Jul 2024 15:27:17 GMT
EXPOSE 9000
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["php-fpm"]
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV DRUPAL_VERSION=10.3.1
# Thu, 04 Jul 2024 15:27:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /opt/drupal
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:faf447acae27573624c0613a79c4bcf1f9bc46d29f523140352abfd3f7691282`  
		Last Modified: Mon, 22 Jul 2024 22:21:18 GMT  
		Size: 3.4 MB (3370673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2d0e03d7a4d4766a64c04a50abfb02e217be153dd68888273b46568c4cac04`  
		Last Modified: Tue, 23 Jul 2024 12:29:02 GMT  
		Size: 3.4 MB (3397181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56268c2d820d6bf5bbf0e86c5bc55e50edc209a552c0844c6a9f787a880a2c6`  
		Last Modified: Tue, 23 Jul 2024 12:28:58 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f05d3b9188b0e4a61167b2493ce280347bad9dfe72e9ecf4c18c5572f2cb6719`  
		Last Modified: Tue, 23 Jul 2024 12:28:58 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17cb76992d32d9cdb0561153daa1513a30cad594b5114d7ea2ccd5803d9924a8`  
		Last Modified: Thu, 01 Aug 2024 22:47:06 GMT  
		Size: 12.5 MB (12505868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6a0a6fc99f199e401f3df122305bf5f8186ce1a6163e6371cf3c1c5e5d5212a`  
		Last Modified: Thu, 01 Aug 2024 22:47:01 GMT  
		Size: 499.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f463729d5cbf4e53c1fa8f81dcae57d90b0dbb115e48544ef30e8929bea4da`  
		Last Modified: Thu, 01 Aug 2024 22:48:17 GMT  
		Size: 12.7 MB (12656975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68808b933c41a24e62ba203cfca19e4c3f158c2cd400327eed33492ab598b1ac`  
		Last Modified: Thu, 01 Aug 2024 22:48:05 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6e5ef092c76869a04ad88ad85193e1d3b3eef8ef9e66063d88f046b24f809e`  
		Last Modified: Thu, 01 Aug 2024 22:48:05 GMT  
		Size: 19.5 KB (19488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c45c5a9345785014215a19d39bdf836921991f22ba20b09f2dfdd2816724ed5`  
		Last Modified: Thu, 01 Aug 2024 22:48:05 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796b9a25196886c1acb35e7ff4eba756a602038e9584a4043ca333823cb6d0ca`  
		Last Modified: Fri, 02 Aug 2024 06:10:52 GMT  
		Size: 1.5 MB (1482230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edc20d1a429a590dea3c372193cb3228363f5a703a92089391981096ec44f19a`  
		Last Modified: Fri, 02 Aug 2024 06:10:51 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6464873f8aecdd1b486da40ba112ad0c7272ca85aa6bbe3738b6b09bc561fd1e`  
		Last Modified: Fri, 02 Aug 2024 06:10:52 GMT  
		Size: 726.3 KB (726335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d9aa6cc92824b0b7f9ebbb913cfa988fb27f85e2fac149a5c78c484188f340`  
		Last Modified: Fri, 02 Aug 2024 06:10:51 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dfffb4e7d21630020b21443cd436aecbc5cca2365f4c4f430563ccf44962339`  
		Last Modified: Fri, 02 Aug 2024 06:17:28 GMT  
		Size: 21.1 MB (21070281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:38c4616391fa91154d8fec65733316f76a3886fdba218f5d9fee77b89e98a3f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.8 KB (376795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f35b593be54d493985e4c1712b49f5a7737ad07e1590fa7473710356aaa0974d`

```dockerfile
```

-	Layers:
	-	`sha256:b09cf4298917ce4e91a9299a67b5f651ec108c230dfd81b4b48a461216a43c0a`  
		Last Modified: Fri, 02 Aug 2024 06:17:24 GMT  
		Size: 344.0 KB (344009 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12cd8f537b65897260ae7e9ef0ff4481e14089ec02c3fb3b2337880a485e580b`  
		Last Modified: Fri, 02 Aug 2024 06:17:24 GMT  
		Size: 32.8 KB (32786 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-alpine3.20` - linux; s390x

```console
$ docker pull drupal@sha256:99d28ebb2c465571bb4cd85f03be8bc9e8d90444875eed9557700d23f5f5ad9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55902736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c3a416959364264cbbb769a3a791891e122301861703ef154f2570eb77d7d5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 04 Jul 2024 15:27:17 GMT
ADD file:63d382fb7a431c57868274a368a659bde32a60ae0cd05c8af34c3d6a57066a77 in / 
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["/bin/sh"]
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Thu, 04 Jul 2024 15:27:17 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 04 Jul 2024 15:27:17 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_VERSION=8.3.9
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.9.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.9.tar.xz.asc
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_SHA256=bf4d7b8ea60a356064f88485278bd6f941a230ec16f0fc401574ce1445ad6c77
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 04 Jul 2024 15:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 04 Jul 2024 15:27:17 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 04 Jul 2024 15:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 04 Jul 2024 15:27:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Jul 2024 15:27:17 GMT
EXPOSE 9000
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["php-fpm"]
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV DRUPAL_VERSION=10.3.1
# Thu, 04 Jul 2024 15:27:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /opt/drupal
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:834c666d55eae0e308600077be061a01680e7cd02b579be887d9469075f0d943`  
		Last Modified: Mon, 22 Jul 2024 21:51:06 GMT  
		Size: 3.5 MB (3461066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bee85c5a5fc33ed0d0f61a077ed76c922b87c42c5cb3a4dbba408dd62a64def`  
		Last Modified: Tue, 23 Jul 2024 00:56:03 GMT  
		Size: 3.5 MB (3467756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1505ad7d669e91b715e2a1bc7ec0c52dd53433332ad45653571cbe2c3643d5`  
		Last Modified: Tue, 23 Jul 2024 00:56:02 GMT  
		Size: 941.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87d87c5417e12df9b44287d4f554dd37d0b5b446d100409e5c49a17ac509a5b2`  
		Last Modified: Tue, 23 Jul 2024 00:56:02 GMT  
		Size: 220.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0798d5d0f94584ef0fd49afb25bb51d262348b1d10f193e292b75236019b40`  
		Last Modified: Tue, 23 Jul 2024 00:58:32 GMT  
		Size: 12.5 MB (12491136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a87fcaab65a2d28ba5531aea62a826c3c223da11c8ca853aca5f13a7e620383`  
		Last Modified: Tue, 23 Jul 2024 00:58:32 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1f7e3ee533eb57720a80b403c267c19223b2404b2e8b033dcc46089a34bcaea`  
		Last Modified: Tue, 23 Jul 2024 00:59:00 GMT  
		Size: 13.1 MB (13057608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27736685ad6d2f39eb44f77ffcaa226e93ce8e174a348d1a70319e9f5372df0`  
		Last Modified: Tue, 23 Jul 2024 00:58:58 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90f4a38ef076d056fd6c32764e3cfdacb32047c500af1d66a197047305c0822`  
		Last Modified: Tue, 23 Jul 2024 00:58:58 GMT  
		Size: 19.5 KB (19483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09511e2f6844a88289701d854d95eae16177f306045631f657749b664166f3ab`  
		Last Modified: Tue, 23 Jul 2024 00:58:58 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ec4e29f3bb344971279824f67eacabb34767101771d139ec850ce78ae5a808`  
		Last Modified: Wed, 24 Jul 2024 12:23:12 GMT  
		Size: 1.6 MB (1596511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed49647d7f54202c2f4990b01a93e6ef510c987561a0f8bfeab47c67a7fe24ad`  
		Last Modified: Wed, 24 Jul 2024 12:23:12 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e0d6ddbfb98565d67a84c45f222cc171c314ac5b851c59b62f6a5c3d25cf13`  
		Last Modified: Wed, 24 Jul 2024 12:23:12 GMT  
		Size: 726.3 KB (726348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bf752f0c2545a69f5607d413c99c9d2f5cc7bf5e012dd075dbf760d8d109da`  
		Last Modified: Wed, 24 Jul 2024 12:23:12 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b29389388b665c25ca8b52273e087dbd855b6cdb37659b97923179d3ebedf50`  
		Last Modified: Wed, 24 Jul 2024 12:52:06 GMT  
		Size: 21.1 MB (21069115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-alpine3.20` - unknown; unknown

```console
$ docker pull drupal@sha256:4b5606c150967ad58c979dba6fd89c6eefecf37bc37ba11a869311e1d2a7d7a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.7 KB (376652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f207570184e8235c5dc042877581e6acf2432cb87996cbc1fe392d8878e03308`

```dockerfile
```

-	Layers:
	-	`sha256:2fa840f002854dc7596f78b374d3a9c00d6c762530f28c437d58e5697a8259b8`  
		Last Modified: Wed, 24 Jul 2024 12:52:05 GMT  
		Size: 344.0 KB (343951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9358b9a62760303d0da5550a0d20311bb52ff59f28a604fc498ab7e2a62dfca2`  
		Last Modified: Wed, 24 Jul 2024 12:52:05 GMT  
		Size: 32.7 KB (32701 bytes)  
		MIME: application/vnd.in-toto+json
