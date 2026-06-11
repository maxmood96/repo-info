## `drupal:php8.4-fpm-alpine3.22`

```console
$ docker pull drupal@sha256:a2e8b6f2f7ae2b0e48a384100194df85a5c896803d12f91c7b91f750c2d2eb16
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

### `drupal:php8.4-fpm-alpine3.22` - linux; amd64

```console
$ docker pull drupal@sha256:cc500940ab311512db55b22a613637a3e5cd3c07a96435be7dee6ee9bb461197
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62904288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1dfea0abdd04133dc68f833abb7fff58998e7270c41a9a80029c6a814f83e20`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 05 Jun 2026 22:42:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 05 Jun 2026 22:42:28 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 05 Jun 2026 22:42:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 05 Jun 2026 22:42:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Jun 2026 22:42:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 05 Jun 2026 22:42:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 22:42:28 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 22:42:28 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Jun 2026 22:42:28 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 05 Jun 2026 22:42:28 GMT
ENV PHP_VERSION=8.4.22
# Fri, 05 Jun 2026 22:42:28 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Fri, 05 Jun 2026 22:42:28 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Fri, 05 Jun 2026 22:42:32 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 05 Jun 2026 22:42:32 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:45:11 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 22:45:11 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:45:12 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 05 Jun 2026 22:45:12 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 22:45:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 22:45:12 GMT
WORKDIR /var/www/html
# Fri, 05 Jun 2026 22:45:13 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 05 Jun 2026 22:45:13 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Jun 2026 22:45:13 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 05 Jun 2026 22:45:13 GMT
CMD ["php-fpm"]
# Wed, 10 Jun 2026 23:10:44 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 10 Jun 2026 23:10:44 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 10 Jun 2026 23:10:44 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 23:10:44 GMT
ENV DRUPAL_VERSION=11.3.11
# Wed, 10 Jun 2026 23:10:44 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 10 Jun 2026 23:10:44 GMT
WORKDIR /opt/drupal
# Wed, 10 Jun 2026 23:10:55 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 10 Jun 2026 23:10:55 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99c9342f8dd1a5744816181620f0f6f64ca635071e7f7ea0e1c118c50245bfdd`  
		Last Modified: Fri, 05 Jun 2026 22:45:19 GMT  
		Size: 3.5 MB (3464896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b6c1799c444be8232213809719c740b246b252cfeb88a0f03d4c752d31f45a`  
		Last Modified: Fri, 05 Jun 2026 22:45:19 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47b24ddcc51d4885000654df9377d88192df902a8cf37d533d359e4075abae90`  
		Last Modified: Fri, 05 Jun 2026 22:45:19 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b39703d6d57ee586219bfd431733cf7fa450887266b707671495540bc4e0383`  
		Last Modified: Fri, 05 Jun 2026 22:45:19 GMT  
		Size: 13.8 MB (13752971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6cc846f92dda43bdd903ee51fd5a265a4ce7d979d1b6ec5e64d6e61c0f3818c`  
		Last Modified: Fri, 05 Jun 2026 22:45:20 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102985ad71f713e8a2c4928f0afb875a92d05462164d2fffc995f3147a701d3d`  
		Last Modified: Fri, 05 Jun 2026 22:45:20 GMT  
		Size: 15.2 MB (15179274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c68c110c1701b8ddebeee47da1b224ab244e9a58c59a33e373f2279f0e3fe2`  
		Last Modified: Fri, 05 Jun 2026 22:45:20 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b24d155337d040ed5a7b9adbbc5bc901e0a689403c05c1ab97b31d184fc4ab4`  
		Last Modified: Fri, 05 Jun 2026 22:45:21 GMT  
		Size: 20.0 KB (20025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b21936aa3ed1faada1e57afcad5cffc27cbc0884f564879af9ab5ff6646ffe19`  
		Last Modified: Fri, 05 Jun 2026 22:45:21 GMT  
		Size: 20.0 KB (20020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a08c8286ac6337a1b53d09be86388445d4312628088e37d4efc64ebb773540`  
		Last Modified: Fri, 05 Jun 2026 22:45:22 GMT  
		Size: 9.3 KB (9265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed1be8c861f8b773d7e950d96383e529afbaff37251c60310ea1fc1209b1191`  
		Last Modified: Wed, 10 Jun 2026 23:11:07 GMT  
		Size: 4.4 MB (4449849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bfac7b62b18294e5ba32504844029e48b47b82f65fa19ba106f5cf755e5e4f`  
		Last Modified: Wed, 10 Jun 2026 23:11:07 GMT  
		Size: 311.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25b7446fc1adb78caa3df47680ff70fdb3f7307b0137b7b360ea2c7416a412e`  
		Last Modified: Wed, 10 Jun 2026 23:11:07 GMT  
		Size: 823.3 KB (823337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1bb7aba3341183e9f23e8d22164f693ab178ffe660a57d20533513454259050`  
		Last Modified: Wed, 10 Jun 2026 23:11:07 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54009f0047df10e946ce3da969b17aca5706130f7676dc917d3c5619d75d7e4e`  
		Last Modified: Wed, 10 Jun 2026 23:11:09 GMT  
		Size: 21.4 MB (21371917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:18ba77a99933cad47476909f534f8c41d3880bc4ecbfa85baa2aa97036a5dbf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.0 KB (410991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b813a15253171dc318bd82f91a46e926e25bf5104d5ed9ccdea745c47f566136`

```dockerfile
```

-	Layers:
	-	`sha256:c43f7d243573e57ff307a80c9576611591b7eb06052c8e85c851053b30d3a0f6`  
		Last Modified: Wed, 10 Jun 2026 23:11:07 GMT  
		Size: 376.7 KB (376677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b19b7a13e5c59c51ac91482d935a7c790e8b39f6cf89e04210dbc3a7ea68e4b4`  
		Last Modified: Wed, 10 Jun 2026 23:11:07 GMT  
		Size: 34.3 KB (34314 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine3.22` - linux; arm variant v6

```console
$ docker pull drupal@sha256:487931543992f5af27505fea680fac503668267bb178a50b564ffb19559452ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60517416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b119259a4b246c64d9787b6d9bd553e1051fd2b1428adcdcae9a1c56e11c8214`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Fri, 05 Jun 2026 22:39:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 05 Jun 2026 22:39:24 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 05 Jun 2026 22:39:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 05 Jun 2026 22:39:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Jun 2026 22:39:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 05 Jun 2026 22:39:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 22:39:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 22:39:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Jun 2026 22:39:24 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 05 Jun 2026 22:39:24 GMT
ENV PHP_VERSION=8.4.22
# Fri, 05 Jun 2026 22:39:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Fri, 05 Jun 2026 22:39:24 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Fri, 05 Jun 2026 22:39:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 05 Jun 2026 22:39:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:42:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 22:42:23 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:42:24 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 05 Jun 2026 22:42:24 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 22:42:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 22:42:24 GMT
WORKDIR /var/www/html
# Fri, 05 Jun 2026 22:42:24 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 05 Jun 2026 22:42:24 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Jun 2026 22:42:24 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 05 Jun 2026 22:42:24 GMT
CMD ["php-fpm"]
# Wed, 10 Jun 2026 23:13:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 10 Jun 2026 23:13:57 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 10 Jun 2026 23:13:57 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 23:13:57 GMT
ENV DRUPAL_VERSION=11.3.11
# Wed, 10 Jun 2026 23:13:57 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 10 Jun 2026 23:13:57 GMT
WORKDIR /opt/drupal
# Wed, 10 Jun 2026 23:14:06 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 10 Jun 2026 23:14:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:469021a5cbec91d20c98a32d83335319a0fbb42fe9c3f6f8236fea3d2b20dd0a`  
		Last Modified: Fri, 05 Jun 2026 22:42:30 GMT  
		Size: 3.4 MB (3428172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19c94ea4614964c90aba3af660f1e398e6aba22ab45aefce5af7ca02161d7e39`  
		Last Modified: Fri, 05 Jun 2026 22:42:29 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332287916e101bb78e80c25f3630089504aa768112044db49efe66e0d06c1007`  
		Last Modified: Fri, 05 Jun 2026 22:42:29 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a07bac2912e25787d73ee0dfe149ce4500b327ba0121ac2aa8c721a314b37481`  
		Last Modified: Fri, 05 Jun 2026 22:42:30 GMT  
		Size: 13.8 MB (13752990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db9dbf3d77bbab853bf701531bd8f0dd4d9808e25bb092a2a3ae97bf9ef5cda`  
		Last Modified: Fri, 05 Jun 2026 22:42:31 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02eadca9b13d178f75e21f53925988fc9ea24d7207dfb49e30f464a6cb3b266`  
		Last Modified: Fri, 05 Jun 2026 22:42:31 GMT  
		Size: 13.6 MB (13628395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695c798213a0830bab8fe9f2ccc7ab38ef999c881809354eb121511c91aa6371`  
		Last Modified: Fri, 05 Jun 2026 22:42:31 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c6fcd4e140e97b70d6e6a54b7c5d3d694807e7bd8ead78c331b859f56ccca84`  
		Last Modified: Fri, 05 Jun 2026 22:42:31 GMT  
		Size: 19.8 KB (19844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8104f0e57d63d48f465d864635331d32fd76d6cbe3807184dc4875068335a4e5`  
		Last Modified: Fri, 05 Jun 2026 22:42:32 GMT  
		Size: 19.8 KB (19836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7b6ebb4ac4c05fa48cb07e613d820966cbd4f54ca7c59449a892bcce2fa910`  
		Last Modified: Fri, 05 Jun 2026 22:42:32 GMT  
		Size: 9.3 KB (9265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8b26d80b0426e4f216980d7a8173b5160c43def1c17e9f66d6ff88ad7c37bfe`  
		Last Modified: Wed, 10 Jun 2026 23:14:14 GMT  
		Size: 4.0 MB (3951402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4649d3c5fbc9ba3e6c7a053fd13ba3b78e10a0ed58b3f3cb069af8c34ecef8`  
		Last Modified: Wed, 10 Jun 2026 23:14:13 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d4bea4084dd0e4782f6f2cf96a917a473d670e5aed86e7f3c210b18113fc1e9`  
		Last Modified: Wed, 10 Jun 2026 23:14:13 GMT  
		Size: 823.3 KB (823337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b91e4669b2948e441d328ac63b90b4c2dfe8f3aec2600230121744dd0b2ce9ad`  
		Last Modified: Wed, 10 Jun 2026 23:14:13 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57bfc3bb8c062906cee03d48bba5fd2d2e785cd87fdf9c1c4a4a28e70b9f3af3`  
		Last Modified: Wed, 10 Jun 2026 23:14:15 GMT  
		Size: 21.4 MB (21372239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:1324bf7de75d240b5cc3d7dff1e1810c1437469c772d7b869439e6ace5c426cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.3 KB (34254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a2168c5ecea0357d71e4bd6a6f26ae1b442260ecc3941e2eb314b9cf9d518d`

```dockerfile
```

-	Layers:
	-	`sha256:b6f9f617b267dff0bfa2640ad4f44a437056635a769c87a49fce3289dbd3ee47`  
		Last Modified: Wed, 10 Jun 2026 23:14:13 GMT  
		Size: 34.3 KB (34254 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine3.22` - linux; arm variant v7

```console
$ docker pull drupal@sha256:274a83b8889d8c183dd27965e61dd81aeefcedc21782495fd59bcde1b495600d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59010379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db1b944f4d9780f7834a9dac6aefe76cd12305fd33e0be2499f02864de1f31a5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Fri, 05 Jun 2026 22:46:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 05 Jun 2026 22:46:55 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 05 Jun 2026 22:46:55 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 05 Jun 2026 22:46:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Jun 2026 22:46:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 05 Jun 2026 22:46:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 22:46:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 22:46:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Jun 2026 22:46:55 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 05 Jun 2026 22:46:55 GMT
ENV PHP_VERSION=8.4.22
# Fri, 05 Jun 2026 22:46:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Fri, 05 Jun 2026 22:46:55 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Fri, 05 Jun 2026 22:46:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 05 Jun 2026 22:46:59 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:50:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 22:50:02 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:50:03 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 05 Jun 2026 22:50:04 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 22:50:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 22:50:04 GMT
WORKDIR /var/www/html
# Fri, 05 Jun 2026 22:50:04 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 05 Jun 2026 22:50:04 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Jun 2026 22:50:04 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 05 Jun 2026 22:50:04 GMT
CMD ["php-fpm"]
# Wed, 10 Jun 2026 23:16:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 10 Jun 2026 23:16:07 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 10 Jun 2026 23:16:07 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 23:16:07 GMT
ENV DRUPAL_VERSION=11.3.11
# Wed, 10 Jun 2026 23:16:07 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 10 Jun 2026 23:16:07 GMT
WORKDIR /opt/drupal
# Wed, 10 Jun 2026 23:16:19 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 10 Jun 2026 23:16:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990f57594c57aac0167bd27f8590490070679cb8dc943e5551c190ac0082c013`  
		Last Modified: Fri, 05 Jun 2026 22:50:10 GMT  
		Size: 3.2 MB (3244384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0b20a3cbc1340a1391cc713bcf64f451aa43b7dad9da284ce5fedbeb9f477f8`  
		Last Modified: Fri, 05 Jun 2026 22:50:10 GMT  
		Size: 937.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ed13a11dc14eaca1aacee99c74b109eea221cf7c0c858947d159975c20a1d9`  
		Last Modified: Fri, 05 Jun 2026 22:50:10 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65239daa3a1914a40d996a36f30b517640e239b4493d5f5c261f4fd25a6374f6`  
		Last Modified: Fri, 05 Jun 2026 22:50:11 GMT  
		Size: 13.8 MB (13752972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7320fbe935ae08f5c93c738601ac93db5bf9399330949e7d6102bc0b22f4e5ce`  
		Last Modified: Fri, 05 Jun 2026 22:50:11 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:493630f48d4983b9c80cc48608c7bd7d620ca5a1d7e479214da35e17c2d8fde1`  
		Last Modified: Fri, 05 Jun 2026 22:50:12 GMT  
		Size: 12.9 MB (12876370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db4747334f41deec849ad46488943a63d9c316022d325217b758f3e031b7ca2`  
		Last Modified: Fri, 05 Jun 2026 22:50:12 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d9100cc8b6d35f950524ab7d29cd3ecd1d8f330d559d20ae8d8498bd1a45a3`  
		Last Modified: Fri, 05 Jun 2026 22:50:12 GMT  
		Size: 19.8 KB (19822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a258f290a9c4e8d618b78ca67a38ec4f5d40af8751bf06d149fd6e8b4cc36f48`  
		Last Modified: Fri, 05 Jun 2026 22:50:12 GMT  
		Size: 19.8 KB (19820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab3aae9abf6a6a22c01583e27a55b06d697b7e9a62b98ea5abe6aca43befe8d4`  
		Last Modified: Fri, 05 Jun 2026 22:50:13 GMT  
		Size: 9.3 KB (9261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1755bdc743bdce3a7ac3f92dc3874a2a68e830aaee995d2f8e98ea21ebd1c0c2`  
		Last Modified: Wed, 10 Jun 2026 23:16:33 GMT  
		Size: 3.7 MB (3663477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2bcd8cbc71dac882f63c69a6b09ab01586e69a60571fe4be16470ae75dfea42`  
		Last Modified: Wed, 10 Jun 2026 23:16:33 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d83b5df5eca2adadfacbc47ee485d79766d0087995eabed8b7627bede69921cc`  
		Last Modified: Wed, 10 Jun 2026 23:16:33 GMT  
		Size: 823.3 KB (823335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f711b4f7e2e927044e8b04ca2d12911b8493f8c6d78f7fa2577d607e8a7e14e`  
		Last Modified: Wed, 10 Jun 2026 23:16:33 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f200d9aa506af407b45920215a5cede099f2e6d0667f2ed9ff4ad4c15ad7f1`  
		Last Modified: Wed, 10 Jun 2026 23:16:34 GMT  
		Size: 21.4 MB (21370565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:10df989c53eabf028fe805c0eefc8b36209d619c35ed802bbcb6d98ba3bc80ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.2 KB (408224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f39a6c391916907e841991608a38f05bfb067916b255883cf5ddff91fe27ffdc`

```dockerfile
```

-	Layers:
	-	`sha256:640a5016aa86ecb9bef5eea7b4281ad4b6635a1597e73ec0ee47bcc7eeb698de`  
		Last Modified: Wed, 10 Jun 2026 23:16:32 GMT  
		Size: 373.8 KB (373755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:614a0a8d1f87cb4655ad14dcae43bf1a5cb27e32a4cde2c14afb66936e167e4a`  
		Last Modified: Wed, 10 Jun 2026 23:16:32 GMT  
		Size: 34.5 KB (34469 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:ab39b7bca830705f5430b100fbc65c8c2de69197a770a2ae55b1c2e866661ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63143966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e580d4c070958903449fcd0c79c860b3814000ff101a360e746b146b7f8dca07`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 05 Jun 2026 22:42:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 05 Jun 2026 22:42:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 05 Jun 2026 22:42:51 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 05 Jun 2026 22:42:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Jun 2026 22:42:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 05 Jun 2026 22:42:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 22:42:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 22:42:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Jun 2026 22:42:51 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 05 Jun 2026 22:42:51 GMT
ENV PHP_VERSION=8.4.22
# Fri, 05 Jun 2026 22:42:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Fri, 05 Jun 2026 22:42:51 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Fri, 05 Jun 2026 22:42:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 05 Jun 2026 22:42:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:46:40 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 22:46:40 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:46:41 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 05 Jun 2026 22:46:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 22:46:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 22:46:42 GMT
WORKDIR /var/www/html
# Fri, 05 Jun 2026 22:46:42 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 05 Jun 2026 22:46:42 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Jun 2026 22:46:42 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 05 Jun 2026 22:46:42 GMT
CMD ["php-fpm"]
# Wed, 10 Jun 2026 23:10:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 10 Jun 2026 23:10:53 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 10 Jun 2026 23:10:53 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 23:10:53 GMT
ENV DRUPAL_VERSION=11.3.11
# Wed, 10 Jun 2026 23:10:53 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 10 Jun 2026 23:10:53 GMT
WORKDIR /opt/drupal
# Wed, 10 Jun 2026 23:11:05 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 10 Jun 2026 23:11:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e414d42e99aeb33af3177f0890aa9084ed66969e6ddd3ff7cd23274d8bf672b`  
		Last Modified: Fri, 05 Jun 2026 22:46:49 GMT  
		Size: 3.5 MB (3467693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a060574cc4607ef70cdaf7e8e9efa49e2f2b34a828cc368363d82a46df5223`  
		Last Modified: Fri, 05 Jun 2026 22:46:48 GMT  
		Size: 937.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eaeaf893acf4eef97a92f662729ca77de9461d5b81e56bf403447b8563fc277`  
		Last Modified: Fri, 05 Jun 2026 22:46:48 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:018c0f47f21fd719a817ca51063ee080c626e6c8e52e1bd478df19d0639a3c76`  
		Last Modified: Fri, 05 Jun 2026 22:46:49 GMT  
		Size: 13.8 MB (13752939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6071731e5aa4915ffdc37e80f340b2176504fe6944f22d898aae243aca28101`  
		Last Modified: Fri, 05 Jun 2026 22:46:50 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997e5cf8a1b495fc9cfe12298a73c7078ddf8f21bdb7647bb3138fe9c0acfbda`  
		Last Modified: Fri, 05 Jun 2026 22:46:50 GMT  
		Size: 14.8 MB (14807781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe181840ba768ae11c38842e680f0c00d90e1b289eba4c53185cbc2a4b6d892d`  
		Last Modified: Fri, 05 Jun 2026 22:46:50 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad93225b151b30b48b6d33be2ea0ea63469f73ccda0e426b9b0b2c526e60173d`  
		Last Modified: Fri, 05 Jun 2026 22:46:50 GMT  
		Size: 19.8 KB (19829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0044e52ab2c13fc3708b05744290fd9dae6d538c87a6c8dd770bbd9dd804ebb0`  
		Last Modified: Fri, 05 Jun 2026 22:46:51 GMT  
		Size: 19.8 KB (19823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01755add44dff94323865737f6cf8c393ecb735d2782af369e927113caba043`  
		Last Modified: Fri, 05 Jun 2026 22:46:51 GMT  
		Size: 9.3 KB (9265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a27c2d78abfe5e5ba3a457f8d1994349e5973027b2ddcd312411b85888b149`  
		Last Modified: Wed, 10 Jun 2026 23:11:18 GMT  
		Size: 4.7 MB (4725250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bf394b0046eb76928c0f5d64149b283cd05f606a7ff4bedfe262097d794c48`  
		Last Modified: Wed, 10 Jun 2026 23:11:18 GMT  
		Size: 309.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28f25c704f5b8398e2fd7ee3f74d527753429da47dfb622f57e21bd791a9719`  
		Last Modified: Wed, 10 Jun 2026 23:11:18 GMT  
		Size: 823.3 KB (823335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac4c2b33cf2a67fa105818d3d646752e643c595139f8b5d43c6c2b4c6cefc10a`  
		Last Modified: Wed, 10 Jun 2026 23:11:18 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b372547ccae41acac997203e8dbad467a6cf220690dfbfcd1e63169563a44e7c`  
		Last Modified: Wed, 10 Jun 2026 23:11:20 GMT  
		Size: 21.4 MB (21371614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:2bcff7de61d895acb7884761f446449b3adff9b1540271c834b19eb2dc235443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **408.3 KB (408307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f007dac798256fe564afae20c7346f6afb445b5bb5f36d2ca3e31cd6c7f54a50`

```dockerfile
```

-	Layers:
	-	`sha256:870e7cc55fe75247a7ebcdc937295d6849d86269efc438c42eaf6565d7bd16f4`  
		Last Modified: Wed, 10 Jun 2026 23:11:18 GMT  
		Size: 373.8 KB (373791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:170b9d8cbe6807e12c9cf104aa207a48b47237c02e485f39dc4ebb9134868c04`  
		Last Modified: Wed, 10 Jun 2026 23:11:18 GMT  
		Size: 34.5 KB (34516 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine3.22` - linux; 386

```console
$ docker pull drupal@sha256:3a32a69ebfdbde2e29c082e09b1ffb54396f7d87530c3b23e1b6270b6e385a7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63066596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28689bbff55dff937ea32945793f6e5deec450f71b10925c59723a56ab25a520`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 17 Apr 2026 02:42:29 GMT
ADD alpine-minirootfs-3.22.4-x86.tar.gz / # buildkit
# Fri, 17 Apr 2026 02:42:29 GMT
CMD ["/bin/sh"]
# Fri, 05 Jun 2026 22:42:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 05 Jun 2026 22:42:52 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 05 Jun 2026 22:42:52 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 05 Jun 2026 22:42:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 05 Jun 2026 22:42:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 05 Jun 2026 22:42:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 22:42:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 05 Jun 2026 22:42:52 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 05 Jun 2026 22:42:52 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 05 Jun 2026 22:42:52 GMT
ENV PHP_VERSION=8.4.22
# Fri, 05 Jun 2026 22:42:52 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Fri, 05 Jun 2026 22:42:52 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Fri, 05 Jun 2026 22:42:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 05 Jun 2026 22:42:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:45:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 22:45:54 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:45:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 05 Jun 2026 22:45:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 22:45:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 22:45:55 GMT
WORKDIR /var/www/html
# Fri, 05 Jun 2026 22:45:56 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 05 Jun 2026 22:45:56 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Jun 2026 22:45:56 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 05 Jun 2026 22:45:56 GMT
CMD ["php-fpm"]
# Wed, 10 Jun 2026 23:41:22 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Wed, 10 Jun 2026 23:41:22 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 10 Jun 2026 23:41:23 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 10 Jun 2026 23:41:23 GMT
ENV DRUPAL_VERSION=11.3.11
# Wed, 10 Jun 2026 23:41:23 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 10 Jun 2026 23:41:23 GMT
WORKDIR /opt/drupal
# Wed, 10 Jun 2026 23:41:34 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 10 Jun 2026 23:41:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:481dba1f7704181ddc1e2b499675e9651a93f972d4cd141a4933d44622cdc88a`  
		Last Modified: Fri, 17 Apr 2026 02:42:34 GMT  
		Size: 3.6 MB (3624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57826239ae09ddeab34e500d730319407245195ee77c96a33c5bdd7dfecb8238`  
		Last Modified: Fri, 05 Jun 2026 22:46:02 GMT  
		Size: 3.5 MB (3522699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66c2a86921bd2e0d6c28e399997fd64f5c3021da564b6e3c62fb14fe04c08550`  
		Last Modified: Fri, 05 Jun 2026 22:46:02 GMT  
		Size: 936.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a67ae70b06f3c4fb3943f1e1c43caeebdd032ea5d5c9f63b9c08a4c744edc00`  
		Last Modified: Fri, 05 Jun 2026 22:46:02 GMT  
		Size: 215.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baa971b2127e22b3097080183c2ea07388f0b77d4d73dcf0bce86b791e8e4baf`  
		Last Modified: Fri, 05 Jun 2026 22:46:03 GMT  
		Size: 13.8 MB (13752946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc99878a790ba4ad1f766abb7a730945af613a7bf6f5f66eea55a5f76b5df426`  
		Last Modified: Fri, 05 Jun 2026 22:46:03 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fd21e497fabde23e2137e65680e9ea93da2f3764f04102d8c1f04b3d3a85492`  
		Last Modified: Fri, 05 Jun 2026 22:46:03 GMT  
		Size: 15.6 MB (15581725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d3cd57fdf07c6235bab46d0a4d670c37e7c1ad1c5c1d2e52403eb2d1404ca0e`  
		Last Modified: Fri, 05 Jun 2026 22:46:04 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57cb5786b2c9f2ee517e39278a0fbeec771524b67dcd87187faa532212cddf4`  
		Last Modified: Fri, 05 Jun 2026 22:46:04 GMT  
		Size: 20.0 KB (20019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6aaef5baf673802418725e07423c02bba3465a33b49425ddcb9c09e89485c89`  
		Last Modified: Fri, 05 Jun 2026 22:46:04 GMT  
		Size: 20.0 KB (20015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71fabe61da56de0a883b8b2dedd82ab14f6c04c78377f2f97299105a90087e83`  
		Last Modified: Fri, 05 Jun 2026 22:46:05 GMT  
		Size: 9.3 KB (9265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7edc8dba03d45e57b673bde27626b071d76b1c79872ff7a3cbffb88f13e421`  
		Last Modified: Wed, 10 Jun 2026 23:41:47 GMT  
		Size: 4.3 MB (4335867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c61025ffa8460bb65226ad61a224e68686b51b45bf51576d94727189931186`  
		Last Modified: Wed, 10 Jun 2026 23:41:47 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b8e7e693e4566780d0d618fc47de027847c6cae26a32ed9c1a3be7a968c81e3`  
		Last Modified: Wed, 10 Jun 2026 23:41:47 GMT  
		Size: 823.3 KB (823340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753a5e050c4aeb0f22bdd3fb39e1dcfb7c1e9813019adce51fbfa96c3c98751a`  
		Last Modified: Wed, 10 Jun 2026 23:41:47 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa7dacb09ce099c421323c726d4f37fb55832eda6c895869363b3ade5656c85`  
		Last Modified: Wed, 10 Jun 2026 23:41:49 GMT  
		Size: 21.4 MB (21371453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:ee190fc485c9a7978cb869cd766abcb21235e6814f8507488a170d7b6f1c7abb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **410.9 KB (410887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca72078a07a78b26412ce531e16707d4fde3f8fd525006b03135a075b6cd91a`

```dockerfile
```

-	Layers:
	-	`sha256:947182759d678e7818e3bf9237e1bc5992a162d6fcefdc2e3cfc53c9ce85e1c4`  
		Last Modified: Wed, 10 Jun 2026 23:41:47 GMT  
		Size: 376.6 KB (376632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9aa5e9434d6a0033f7d8d4dec1ddf2d60a678d4e8cc0643a16acaeb207ebe7d`  
		Last Modified: Wed, 10 Jun 2026 23:41:47 GMT  
		Size: 34.3 KB (34255 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine3.22` - linux; ppc64le

```console
$ docker pull drupal@sha256:a611b805f8414cbf48209a193c66638cba57d60fe502f6bd46fd1eac2b2f4255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.9 MB (60901671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b71d1e15978ca7dc3cc091205f740962d562731008a6cec9ce84e3a10d1994ba`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:19:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 17 Apr 2026 00:19:27 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Fri, 17 Apr 2026 00:19:28 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Fri, 17 Apr 2026 00:19:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 17 Apr 2026 00:19:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 17 Apr 2026 00:19:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Apr 2026 00:19:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 17 Apr 2026 00:19:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 17 Apr 2026 00:19:29 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 17 Apr 2026 00:19:29 GMT
ENV PHP_VERSION=8.4.22
# Fri, 17 Apr 2026 00:19:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Fri, 17 Apr 2026 00:19:29 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Fri, 05 Jun 2026 23:07:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 05 Jun 2026 23:07:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 23:17:08 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 23:17:09 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 23:17:10 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 05 Jun 2026 23:17:12 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 23:17:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 23:17:12 GMT
WORKDIR /var/www/html
# Fri, 05 Jun 2026 23:17:12 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 05 Jun 2026 23:17:12 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Jun 2026 23:17:12 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 05 Jun 2026 23:17:12 GMT
CMD ["php-fpm"]
# Sat, 06 Jun 2026 00:26:53 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sat, 06 Jun 2026 00:26:59 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Sat, 06 Jun 2026 00:26:59 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 00:26:59 GMT
ENV DRUPAL_VERSION=11.3.11
# Sat, 06 Jun 2026 00:26:59 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Sat, 06 Jun 2026 00:26:59 GMT
WORKDIR /opt/drupal
# Sat, 06 Jun 2026 00:27:16 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Sat, 06 Jun 2026 00:27:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b158ada90b6cc8f44737ff5d95bedaf7f63979acc7eb3452859f5d0ace79a5`  
		Last Modified: Fri, 17 Apr 2026 00:25:56 GMT  
		Size: 3.6 MB (3615071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b99d415a1788bb58d298132317074efb0a3a7801f8a3fed0809ed39f6869175`  
		Last Modified: Fri, 17 Apr 2026 00:25:55 GMT  
		Size: 934.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9eb866ab296180559ca8a3add579c6854d381da1068c287f30bf1ddcaa1eaf8`  
		Last Modified: Fri, 17 Apr 2026 00:25:55 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfa7c298c256ba3dc3234aec5bf402adb1f91580e3c45c005d9c993a200f9079`  
		Last Modified: Fri, 05 Jun 2026 23:12:43 GMT  
		Size: 13.8 MB (13752988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e97cb4cefbaec7779091263c5b7dd22a7ef990b5de10b44e5ab7fde663c126d`  
		Last Modified: Fri, 05 Jun 2026 23:12:42 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf74b63cc59ec0a4f0d38591f3c35ad3d63320fd9af723d03a0e585a063d48c6`  
		Last Modified: Fri, 05 Jun 2026 23:17:26 GMT  
		Size: 15.9 MB (15932398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b3a65f5ae8d260f28e9044b4c3402f7bf3708c29bc2e3e57dd551f3d0e16082`  
		Last Modified: Fri, 05 Jun 2026 23:17:26 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:368f33f3c40301b28dc37e6959a5411606cbbdeb07bc15014859b8f21833b7bd`  
		Last Modified: Fri, 05 Jun 2026 23:17:26 GMT  
		Size: 19.8 KB (19844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69db0a2d73c1483240d6b300ff8e5f308185b0c5a0284f8496d0bca39247ca89`  
		Last Modified: Fri, 05 Jun 2026 23:17:26 GMT  
		Size: 19.8 KB (19839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2eff3e1586e890fd465ee486b14ea81ba405ee3c80b2dae484a5a1b9a70f83`  
		Last Modified: Fri, 05 Jun 2026 23:17:27 GMT  
		Size: 9.3 KB (9265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f586fc5ff2705d7b91597323b7abb05ab7cd85d3ec612dd8b14f8d79ecbef83`  
		Last Modified: Sat, 06 Jun 2026 00:27:44 GMT  
		Size: 1.6 MB (1616058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c07a843edbc20e6b2bb44537dadbd941d17c2af0cc41cbd7ad68d6ba17d8e5`  
		Last Modified: Sat, 06 Jun 2026 00:27:44 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1cf6243e26cabc9d683c89402420564b439e867f900dfb25134540409ac6393`  
		Last Modified: Sat, 06 Jun 2026 00:27:44 GMT  
		Size: 823.3 KB (823340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fc42b124a50bcaf21345d44f1ed48f9b7e1b19bb8f7cfbb99f21605f0e21dc2`  
		Last Modified: Sat, 06 Jun 2026 00:27:44 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9d164ef678d71c7ef185a03036370a359b95407c2f6f2d54123b2c324dc3b4`  
		Last Modified: Sat, 06 Jun 2026 00:27:46 GMT  
		Size: 21.4 MB (21371655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:39d48e3fd193d4787292eeaf02d009ada36223b692080c5c0ee2268d40dfcf21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.4 KB (406381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57bc3b47aeac1b8b8fdc831c5ea0f42debb2fa10ee6ade174b05546005ae10df`

```dockerfile
```

-	Layers:
	-	`sha256:840313d0267d315b4afea678fc79a2d89ed4e80ba775c86dd1787a89cf961117`  
		Last Modified: Sat, 06 Jun 2026 00:27:44 GMT  
		Size: 371.8 KB (371794 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76a2b0e1625a8926c8b95977ed8ece45c6d2f76d233c39d7e6e7490c30c1ee91`  
		Last Modified: Sat, 06 Jun 2026 00:27:44 GMT  
		Size: 34.6 KB (34587 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine3.22` - linux; riscv64

```console
$ docker pull drupal@sha256:c7e04ef6735fb5ab95f23902141e082501894f956c483f387a663b9261b018d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59340993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc8f5b82b9d15947c35840d93d7ecfd745b6fcd43e94cc41c1273416c7dd4f06`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 17 Apr 2026 07:18:45 GMT
ADD alpine-minirootfs-3.22.4-riscv64.tar.gz / # buildkit
# Fri, 17 Apr 2026 07:18:45 GMT
CMD ["/bin/sh"]
# Sat, 18 Apr 2026 11:02:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 18 Apr 2026 11:02:25 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Sat, 18 Apr 2026 11:02:26 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Sat, 18 Apr 2026 11:02:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 18 Apr 2026 11:02:26 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Sat, 18 Apr 2026 11:02:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Apr 2026 11:02:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 18 Apr 2026 11:02:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 18 Apr 2026 11:02:26 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Sat, 18 Apr 2026 11:02:26 GMT
ENV PHP_VERSION=8.4.22
# Sat, 18 Apr 2026 11:02:26 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Sat, 18 Apr 2026 11:02:26 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Sat, 06 Jun 2026 05:37:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Sat, 06 Jun 2026 05:37:42 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 07:33:46 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 06 Jun 2026 07:33:46 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 07:34:03 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 06 Jun 2026 07:34:09 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 06 Jun 2026 07:34:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 06 Jun 2026 07:34:09 GMT
WORKDIR /var/www/html
# Sat, 06 Jun 2026 07:34:09 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 06 Jun 2026 07:34:09 GMT
STOPSIGNAL SIGQUIT
# Sat, 06 Jun 2026 07:34:09 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 06 Jun 2026 07:34:09 GMT
CMD ["php-fpm"]
# Sat, 06 Jun 2026 14:53:03 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sat, 06 Jun 2026 14:53:03 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Sat, 06 Jun 2026 14:53:03 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 14:53:03 GMT
ENV DRUPAL_VERSION=11.3.11
# Sat, 06 Jun 2026 14:53:03 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Sat, 06 Jun 2026 14:53:03 GMT
WORKDIR /opt/drupal
# Sat, 06 Jun 2026 14:53:46 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Sat, 06 Jun 2026 14:53:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:fbc07c8b85a3c60e503ffd0cbe3e1b3947fd65764784e1bd9d943ac21097cce7`  
		Last Modified: Fri, 17 Apr 2026 07:19:08 GMT  
		Size: 3.5 MB (3520880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aba8e387b0f52a066bd16fc16548380bb5c1ba358c87f632f41bf0e1538804c`  
		Last Modified: Sat, 18 Apr 2026 12:03:48 GMT  
		Size: 3.6 MB (3600194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e0aef12c28ba880017fb96a48e3e22f4b4e363ee1be8f9a85075a131d12b72`  
		Last Modified: Sat, 18 Apr 2026 12:03:47 GMT  
		Size: 933.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6a7d02aa931427745ea3ec5ed71cd22b97056886e6224d2e88e3226411519f`  
		Last Modified: Sat, 18 Apr 2026 12:03:47 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6f38acda5950b3036fd46285524418e07271f3166e0ea5c174a39e019000ae`  
		Last Modified: Sat, 06 Jun 2026 06:35:49 GMT  
		Size: 13.8 MB (13752990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a73121ddc78b3b608507b8582b394a8d4d3380b6e434d63030d35971685acc`  
		Last Modified: Sat, 06 Jun 2026 06:35:45 GMT  
		Size: 495.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:defd603828dc10fa014af51e66c376e675d5425cb871c87069e7c88650a694aa`  
		Last Modified: Sat, 06 Jun 2026 07:35:02 GMT  
		Size: 14.8 MB (14801945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0abefe649df81423c0c247e59fa1bfcf2745620f2fb0bce99d8323f737752784`  
		Last Modified: Sat, 06 Jun 2026 07:35:00 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f20d6cffce4448836559000d1faf06ad871914c806d090eeace80472ca20dd1`  
		Last Modified: Sat, 06 Jun 2026 07:35:00 GMT  
		Size: 19.8 KB (19840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78eda71c2d004716198762e2fcc0eed2e98f8b8044b2a911af2b74baf584e871`  
		Last Modified: Sat, 06 Jun 2026 07:35:00 GMT  
		Size: 19.8 KB (19837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c473a086e273152110dbf58e9fdbcca4dfceb3889d995c2e83d263e139b455c`  
		Last Modified: Sat, 06 Jun 2026 07:35:02 GMT  
		Size: 9.3 KB (9266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a32eb6d6e46e0ed7dc6c54ac33e92b6bc79a7c29bbfd35699e28d5311441bac3`  
		Last Modified: Sat, 06 Jun 2026 14:56:14 GMT  
		Size: 1.4 MB (1415674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b94194b90656b4379ab53bfb04485dac1c110e619e41c1b8721fd480ab39a3`  
		Last Modified: Sat, 06 Jun 2026 14:56:14 GMT  
		Size: 310.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b915893147e9ebdd9e27a342612b77b1de2ea9f8986a663c504309bb938104c5`  
		Last Modified: Sat, 06 Jun 2026 14:56:14 GMT  
		Size: 823.3 KB (823338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e57726f8db16c3d314b4ea0b79beaa9fa5456a633cbd9dd1a556ff28d00594`  
		Last Modified: Sat, 06 Jun 2026 14:56:14 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291a75080707422d6d56d3efc5e0eaaabf8bac86faf75bd1567bd5749527bf98`  
		Last Modified: Sat, 06 Jun 2026 14:56:18 GMT  
		Size: 21.4 MB (21372470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:b0d45632045e17f24e93b3a269026aaca69361a7b60b4e71ce604f32666ae53c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.4 KB (406377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a58432f83704b354827408b0208a248f1d9088f4d01a3bf7657490a44a29abc9`

```dockerfile
```

-	Layers:
	-	`sha256:0a3ee581c7069252555b72f2a77f546cc3ccc7644f269d49a5f69764a2c7e762`  
		Last Modified: Sat, 06 Jun 2026 14:56:14 GMT  
		Size: 371.8 KB (371790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5edd1cc32cb72126298411b680b4cf6f729ab9cffbf978bdada26cc3ed808899`  
		Last Modified: Sat, 06 Jun 2026 14:56:13 GMT  
		Size: 34.6 KB (34587 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.4-fpm-alpine3.22` - linux; s390x

```console
$ docker pull drupal@sha256:7f2f9168c2f9baffae7b8f4a526eb3a3b7ebd9d22d100d14aaa02d8ef7fe8e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59930314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdd0835d14f660c464c8773d0c16baacddd5cde8f56dba9e00828acfdad5432d`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Tue, 02 Jun 2026 06:10:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Tue, 02 Jun 2026 06:10:41 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz # buildkit
# Tue, 02 Jun 2026 06:10:41 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data # buildkit
# Tue, 02 Jun 2026 06:10:41 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jun 2026 06:10:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 02 Jun 2026 06:10:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jun 2026 06:10:41 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jun 2026 06:10:41 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jun 2026 06:10:41 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 02 Jun 2026 06:10:41 GMT
ENV PHP_VERSION=8.4.22
# Tue, 02 Jun 2026 06:10:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.22.tar.xz.asc
# Tue, 02 Jun 2026 06:10:41 GMT
ENV PHP_SHA256=696c0f6ad92e94c59059c1eb6e300842b8d050934226efcdf00f2a413cb083cf
# Fri, 05 Jun 2026 22:54:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apk del --no-network .fetch-deps # buildkit
# Fri, 05 Jun 2026 22:54:25 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:59:30 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 05 Jun 2026 22:59:30 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 05 Jun 2026 22:59:31 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 05 Jun 2026 22:59:32 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 05 Jun 2026 22:59:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 05 Jun 2026 22:59:32 GMT
WORKDIR /var/www/html
# Fri, 05 Jun 2026 22:59:32 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 05 Jun 2026 22:59:32 GMT
STOPSIGNAL SIGQUIT
# Fri, 05 Jun 2026 22:59:32 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 05 Jun 2026 22:59:32 GMT
CMD ["php-fpm"]
# Sat, 06 Jun 2026 00:21:26 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		freetype-dev 		libjpeg-turbo-dev 		libpng-dev 		libwebp-dev 		libzip-dev 		postgresql-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr/include 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		pdo_mysql 		pdo_pgsql 		zip 	; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .drupal-phpexts-rundeps $runDeps; 	apk del --no-network .build-deps # buildkit
# Sat, 06 Jun 2026 00:21:26 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Sat, 06 Jun 2026 00:21:26 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Sat, 06 Jun 2026 00:21:26 GMT
ENV DRUPAL_VERSION=11.3.11
# Sat, 06 Jun 2026 00:21:26 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Sat, 06 Jun 2026 00:21:26 GMT
WORKDIR /opt/drupal
# Wed, 10 Jun 2026 23:14:06 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 10 Jun 2026 23:14:06 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c75735c7840576081d137f73c9e1d671fef683197275ebf98b3f89df2d6f047`  
		Last Modified: Tue, 02 Jun 2026 06:14:13 GMT  
		Size: 3.7 MB (3691317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6467f2db1ecdfa183e05296de22d16bef58101b59f959d209d6247d1f495d947`  
		Last Modified: Tue, 02 Jun 2026 06:14:13 GMT  
		Size: 935.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17247e4c91d7dc91ceb5e0d3f79b6712c2173b99d17a3c9edfbf048e100777ee`  
		Last Modified: Tue, 02 Jun 2026 06:14:13 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a808d9b2f335eff2903388f6a6a371a8d45a337f5cdbabb6012823133af8e79f`  
		Last Modified: Fri, 05 Jun 2026 22:59:45 GMT  
		Size: 13.8 MB (13753000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d823ec779d9cf5fabc743944798d3b80518119f0f6e59b9a3747a5e80af649b1`  
		Last Modified: Fri, 05 Jun 2026 22:59:44 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:801a04f338d6677e98032ce70eccf3dc953f843f8d8ac90166d40908b138e338`  
		Last Modified: Fri, 05 Jun 2026 22:59:45 GMT  
		Size: 15.0 MB (15042744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56fa7cc1d3818f2513b7ed4850453fcba9fc48c6055b22d2096fd9acf56651e`  
		Last Modified: Fri, 05 Jun 2026 22:59:44 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d93da80d11bc8190c9ae4c171d27570630fbac494491f033c28010a7aad053`  
		Last Modified: Fri, 05 Jun 2026 22:59:45 GMT  
		Size: 19.8 KB (19834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a37d05bf866e6529b85de15e1499d92e6301f1826ac342374a2ce34b1943d58`  
		Last Modified: Fri, 05 Jun 2026 22:59:45 GMT  
		Size: 19.8 KB (19830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77913f080c13adaab2c1fc8bc9b911a53cffee2b3da46a184709a3233a76139`  
		Last Modified: Fri, 05 Jun 2026 22:59:46 GMT  
		Size: 9.3 KB (9260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065e8e7bc1de36d908b2c7143145c57361402c478cf4d4f977a4b02fbeffc0cf`  
		Last Modified: Sat, 06 Jun 2026 00:21:59 GMT  
		Size: 1.5 MB (1540711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c518be3e414eb7342b8204219dde4724bbe40de8b2bcecd09b1928c2cfc4e5`  
		Last Modified: Sat, 06 Jun 2026 00:21:59 GMT  
		Size: 308.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e76387b369c739869683c91ec0e4882c64b2a1a2e6917e0b66608026acc81de`  
		Last Modified: Sat, 06 Jun 2026 00:21:59 GMT  
		Size: 823.3 KB (823335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dcd2dc62260342856c891df0d6dd18c487985022e1bd0ac3913307ba91b9a50`  
		Last Modified: Sat, 06 Jun 2026 00:21:59 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d327d1b8a1dd8f609799554838251c90024eec07468fbfbf3e3a367d09c976c7`  
		Last Modified: Wed, 10 Jun 2026 23:14:26 GMT  
		Size: 21.4 MB (21371857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.4-fpm-alpine3.22` - unknown; unknown

```console
$ docker pull drupal@sha256:58c04707b60d13eac4528a6f0d18bd6d0a13156991f2c4b8951496a356567af8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.1 KB (406051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1240ad417de131b835a0365198b545c5e8bb6d61a5ffb388f96d251f784c4ae7`

```dockerfile
```

-	Layers:
	-	`sha256:8f1f14d334229ac1784018372d20f3075de9245ac9eec860715aec460a0086db`  
		Last Modified: Wed, 10 Jun 2026 23:14:25 GMT  
		Size: 371.7 KB (371736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d34c2d0100d034eb79e1d30c0b1a84674530633d8a9d513a5f9077e143279b75`  
		Last Modified: Wed, 10 Jun 2026 23:14:25 GMT  
		Size: 34.3 KB (34315 bytes)  
		MIME: application/vnd.in-toto+json
