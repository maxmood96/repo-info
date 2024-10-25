## `yourls:fpm-alpine`

```console
$ docker pull yourls@sha256:0bff4e6bbaf6756c3bbc3b5446aed11bc74584066fd34c79965fd532eb8acc76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `yourls:fpm-alpine` - linux; amd64

```console
$ docker pull yourls@sha256:80ca86538e18c084045176f2b9f88ffc1b56a1e9406ee7dde4b1e387fb7affb8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40948455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e522d3fca230fe2596a4d473ca7ecf62b4ba8d66de9173edd285084543527cc3`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 00:32:02 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 07 Sep 2024 00:32:03 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 07 Sep 2024 00:32:04 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 07 Sep 2024 00:32:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 07 Sep 2024 00:32:05 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 07 Sep 2024 00:32:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Sep 2024 00:32:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Sep 2024 00:32:05 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Sep 2024 00:58:16 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 25 Oct 2024 00:47:20 GMT
ENV PHP_VERSION=8.3.13
# Fri, 25 Oct 2024 00:47:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Fri, 25 Oct 2024 00:47:20 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Fri, 25 Oct 2024 00:47:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 25 Oct 2024 00:47:25 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 25 Oct 2024 00:55:44 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 25 Oct 2024 00:55:45 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 25 Oct 2024 00:55:46 GMT
RUN docker-php-ext-enable sodium
# Fri, 25 Oct 2024 00:55:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Oct 2024 00:55:46 GMT
WORKDIR /var/www/html
# Fri, 25 Oct 2024 00:55:47 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 25 Oct 2024 00:55:47 GMT
STOPSIGNAL SIGQUIT
# Fri, 25 Oct 2024 00:55:47 GMT
EXPOSE 9000
# Fri, 25 Oct 2024 00:55:47 GMT
CMD ["php-fpm"]
# Fri, 25 Oct 2024 03:16:42 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Fri, 25 Oct 2024 03:16:43 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 25 Oct 2024 03:16:44 GMT
RUN apk add --no-cache bash
# Fri, 25 Oct 2024 03:16:44 GMT
ARG YOURLS_VERSION=1.9.2
# Fri, 25 Oct 2024 03:16:44 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Fri, 25 Oct 2024 03:16:44 GMT
ENV YOURLS_VERSION=1.9.2
# Fri, 25 Oct 2024 03:16:44 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Fri, 25 Oct 2024 03:16:45 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Fri, 25 Oct 2024 03:16:46 GMT
COPY --chown=www-data:www-datafile:407fa98e3948ea07c2ff8bc30ad1b3b7b28a1c2b9b5d8e5ab87f9b317a2bac85 in /usr/src/yourls/user/ 
# Fri, 25 Oct 2024 03:16:46 GMT
COPY file:50b4d483341578e719ad63fd7aaea99a0d6d7cebfb7b43d6098a656a975ee0e3 in /usr/local/bin/ 
# Fri, 25 Oct 2024 03:16:46 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 25 Oct 2024 03:16:46 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb15916673af8229814dcc44164d4616a6141bc5b586ae9362e741d64c6e4c91`  
		Last Modified: Sat, 07 Sep 2024 02:15:12 GMT  
		Size: 3.3 MB (3282678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9feb3258c4c6a46b7e182fa372bfe03ff37fd0fdf7f6894ca97b564fc382d7d4`  
		Last Modified: Sat, 07 Sep 2024 02:15:11 GMT  
		Size: 943.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e436918c34ed4c536bdbaeace5213a8aaeb796ec65951fe681a10758ae2677`  
		Last Modified: Sat, 07 Sep 2024 02:15:11 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41457434eddc5cb99259de159d6a2dad43029452b1ab35975a3209703b9897f4`  
		Last Modified: Fri, 25 Oct 2024 02:16:38 GMT  
		Size: 12.5 MB (12504689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328056f851cc57837c30c7c30c8c1fba0e538db1bdb0f520508b064b7771388b`  
		Last Modified: Fri, 25 Oct 2024 02:16:37 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb6db2392ced3144f01adf1065fa477f696673ec741cb8b94970beb8ef5a9767`  
		Last Modified: Fri, 25 Oct 2024 02:17:18 GMT  
		Size: 16.4 MB (16397985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe723e0fc134010804cfde2c13338a9c9ecfc733d8c1802b1579f57dd61909f`  
		Last Modified: Fri, 25 Oct 2024 02:17:16 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d85690bf570916db0ae0b683aa665f8b81c753fd5c8667bc29a2d09cb2ed68`  
		Last Modified: Fri, 25 Oct 2024 02:17:16 GMT  
		Size: 19.7 KB (19728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e0c89a279bf5cf21eaf13ea569c6428aa0f994f34f7eb98c6114b41741aaaa`  
		Last Modified: Fri, 25 Oct 2024 02:17:16 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203e44e7cc2aa8d71d60fc4de1c35929840029097d908ccdd9b9fa5f8f5a62e7`  
		Last Modified: Fri, 25 Oct 2024 03:17:52 GMT  
		Size: 546.5 KB (546516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6863f2615425b342448dda7f0f0407a9bc2da7c20b4dcaba2a89552e50bcc44`  
		Last Modified: Fri, 25 Oct 2024 03:17:50 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13961d9db51847789ca2264078e42852347f6267f9c32637db5ba000e764d30f`  
		Last Modified: Fri, 25 Oct 2024 03:17:50 GMT  
		Size: 482.2 KB (482220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4fe7ffedc91c257eac36446d5f103a33a5cec1a1ab879848700fa9828135c9f`  
		Last Modified: Fri, 25 Oct 2024 03:17:50 GMT  
		Size: 4.1 MB (4073474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596ada7adc3c83d6d3ba59e96ed9925725efa02aa08b8b62ca3f75848844ac96`  
		Last Modified: Fri, 25 Oct 2024 03:17:49 GMT  
		Size: 2.0 KB (2047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5475e11a8e6333d075c89d38ac99199d5a39e11d34bd377ca46cd6113f2aa53d`  
		Last Modified: Fri, 25 Oct 2024 03:17:50 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm-alpine` - linux; arm variant v6

```console
$ docker pull yourls@sha256:1e88179fa29ff105d7dc63fbb6e7d82e4ce521474c1cc9ea516d482ffce8c894
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38818299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:020bc0cb22beda5c5cf617032d8e4d4942701b5203fad5d561f94a48fac3696a`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 22:49:23 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Fri, 06 Sep 2024 22:49:24 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:30:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 23:30:23 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 23:30:24 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 23:30:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 23:30:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 23:30:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:30:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:30:25 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Sep 2024 23:51:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 25 Oct 2024 00:19:03 GMT
ENV PHP_VERSION=8.3.13
# Fri, 25 Oct 2024 00:19:03 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Fri, 25 Oct 2024 00:19:03 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Fri, 25 Oct 2024 00:19:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 25 Oct 2024 00:19:08 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 25 Oct 2024 00:28:32 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 25 Oct 2024 00:28:33 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 25 Oct 2024 00:28:34 GMT
RUN docker-php-ext-enable sodium
# Fri, 25 Oct 2024 00:28:35 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Oct 2024 00:28:35 GMT
WORKDIR /var/www/html
# Fri, 25 Oct 2024 00:28:36 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 25 Oct 2024 00:28:36 GMT
STOPSIGNAL SIGQUIT
# Fri, 25 Oct 2024 00:28:36 GMT
EXPOSE 9000
# Fri, 25 Oct 2024 00:28:36 GMT
CMD ["php-fpm"]
# Fri, 25 Oct 2024 02:08:02 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Fri, 25 Oct 2024 02:08:03 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 25 Oct 2024 02:08:05 GMT
RUN apk add --no-cache bash
# Fri, 25 Oct 2024 02:08:05 GMT
ARG YOURLS_VERSION=1.9.2
# Fri, 25 Oct 2024 02:08:05 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Fri, 25 Oct 2024 02:08:05 GMT
ENV YOURLS_VERSION=1.9.2
# Fri, 25 Oct 2024 02:08:05 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Fri, 25 Oct 2024 02:08:07 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Fri, 25 Oct 2024 02:08:08 GMT
COPY --chown=www-data:www-datafile:407fa98e3948ea07c2ff8bc30ad1b3b7b28a1c2b9b5d8e5ab87f9b317a2bac85 in /usr/src/yourls/user/ 
# Fri, 25 Oct 2024 02:08:08 GMT
COPY file:50b4d483341578e719ad63fd7aaea99a0d6d7cebfb7b43d6098a656a975ee0e3 in /usr/local/bin/ 
# Fri, 25 Oct 2024 02:08:08 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 25 Oct 2024 02:08:08 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78c7a9de9941e89cd785fc3ad14f52410d858d2259f5c9b2a852fd144612520`  
		Last Modified: Sat, 07 Sep 2024 00:48:55 GMT  
		Size: 3.3 MB (3269770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddbf8fddbe2a872480c609959838de42e95d1f5d5d3d8daadf7a1e44e5c381a2`  
		Last Modified: Sat, 07 Sep 2024 00:48:54 GMT  
		Size: 943.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb2d88511b2a3086248129999917d9f1e5928426fda8f08edf40ab5bafa37a9`  
		Last Modified: Sat, 07 Sep 2024 00:48:53 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2913caf4eeb0b47e0a269d5500be80ad644b55b830987923b9b25d7c47b779b6`  
		Last Modified: Fri, 25 Oct 2024 01:12:37 GMT  
		Size: 12.5 MB (12504684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd40e2319cfc199b8ddae2c1022299e653810d5c8fcff021ecf9e71bc732119`  
		Last Modified: Fri, 25 Oct 2024 01:12:36 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a22bd48d8cd970d4d3abf524222b5af1cc44f622ea91cb6c04457b6fccaf6ab`  
		Last Modified: Fri, 25 Oct 2024 01:13:20 GMT  
		Size: 14.9 MB (14911759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2820c6b94ddaf1cfe93b1233a605eed5247758d2c2480b675cf4d245c7c924`  
		Last Modified: Fri, 25 Oct 2024 01:13:16 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b91f5ddf0231e9286b2035969b2e8d7ce898d929a8b6ea78c5bced453eeeadcb`  
		Last Modified: Fri, 25 Oct 2024 01:13:16 GMT  
		Size: 19.5 KB (19509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c698ffba2fada2b58d2c3104bc9da45a5204ed1c5683458ba97e51a1e5101c2`  
		Last Modified: Fri, 25 Oct 2024 01:13:16 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6646b21f91b529d0b956340dcf307e742259df264a169c071b21ef674a050931`  
		Last Modified: Fri, 25 Oct 2024 02:08:21 GMT  
		Size: 173.0 KB (172986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d68eaacef4de241a4053fa0a6882b3823f7ec58e665c814fe2515abaccd503`  
		Last Modified: Fri, 25 Oct 2024 02:08:19 GMT  
		Size: 323.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc53baf611f8e16ccbffb11d447c931aedbc6b982944b5d7c3cc88a19394f3bd`  
		Last Modified: Fri, 25 Oct 2024 02:08:20 GMT  
		Size: 482.3 KB (482258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1fe775cb4c6b6bdb3045b5466ceaad76dca0fc2eb6757257d80ba6e6618ecaa`  
		Last Modified: Fri, 25 Oct 2024 02:08:20 GMT  
		Size: 4.1 MB (4073478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6ff9cf317e9a50d0bcde4ec6f7942ce44a946213445d6171dba68d45ecd25e`  
		Last Modified: Fri, 25 Oct 2024 02:08:19 GMT  
		Size: 2.0 KB (2043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3705bb747911124479e1fd4f3e57a0c0315daea6e1e273f7f02c3d610e30592`  
		Last Modified: Fri, 25 Oct 2024 02:08:19 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm-alpine` - linux; arm variant v7

```console
$ docker pull yourls@sha256:b5b45ab7db43bb82ed584ab4c66940a15258697ce7a1f468203474294b0389ea
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.3 MB (37341199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c4795e2bac2ec3b321d0e00e0c03387904475acb6f63c962d466f1ad7ea10ad`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 22:29:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 22:29:09 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 22:29:10 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 22:29:10 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 22:29:10 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 22:29:10 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 22:29:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 22:29:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Sep 2024 22:47:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 25 Oct 2024 01:27:35 GMT
ENV PHP_VERSION=8.3.13
# Fri, 25 Oct 2024 01:27:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Fri, 25 Oct 2024 01:27:35 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Fri, 25 Oct 2024 01:27:40 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 25 Oct 2024 01:27:40 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 25 Oct 2024 01:33:38 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 25 Oct 2024 01:33:38 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 25 Oct 2024 01:33:39 GMT
RUN docker-php-ext-enable sodium
# Fri, 25 Oct 2024 01:33:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Oct 2024 01:33:39 GMT
WORKDIR /var/www/html
# Fri, 25 Oct 2024 01:33:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 25 Oct 2024 01:33:40 GMT
STOPSIGNAL SIGQUIT
# Fri, 25 Oct 2024 01:33:40 GMT
EXPOSE 9000
# Fri, 25 Oct 2024 01:33:40 GMT
CMD ["php-fpm"]
# Fri, 25 Oct 2024 03:05:37 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Fri, 25 Oct 2024 03:05:38 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 25 Oct 2024 03:05:39 GMT
RUN apk add --no-cache bash
# Fri, 25 Oct 2024 03:05:39 GMT
ARG YOURLS_VERSION=1.9.2
# Fri, 25 Oct 2024 03:05:39 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Fri, 25 Oct 2024 03:05:39 GMT
ENV YOURLS_VERSION=1.9.2
# Fri, 25 Oct 2024 03:05:40 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Fri, 25 Oct 2024 03:05:41 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Fri, 25 Oct 2024 03:05:41 GMT
COPY --chown=www-data:www-datafile:407fa98e3948ea07c2ff8bc30ad1b3b7b28a1c2b9b5d8e5ab87f9b317a2bac85 in /usr/src/yourls/user/ 
# Fri, 25 Oct 2024 03:05:41 GMT
COPY file:50b4d483341578e719ad63fd7aaea99a0d6d7cebfb7b43d6098a656a975ee0e3 in /usr/local/bin/ 
# Fri, 25 Oct 2024 03:05:41 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 25 Oct 2024 03:05:42 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f12c01d5f758f7fce28807153dec7a85ae2e307cf0d73f644d575cd875cb994a`  
		Last Modified: Fri, 06 Sep 2024 23:45:25 GMT  
		Size: 3.1 MB (3079568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c3e48f803b4ca0c1ec0b16f85f80f0a17b054845918112eb73b80eb9bd7297`  
		Last Modified: Fri, 06 Sep 2024 23:45:23 GMT  
		Size: 942.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff7c21bdd57d9b7548f08c79a56f0a75d4e14a705967ae55d0450a10f0c6c43e`  
		Last Modified: Fri, 06 Sep 2024 23:45:21 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93efe62db4f1f9f85f795e6cc1e7f8d835b0a8657d2a60143ba15d82d5863841`  
		Last Modified: Fri, 25 Oct 2024 02:37:26 GMT  
		Size: 12.5 MB (12504680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1204359c9c9eb5cb76578981a5c068e3fac227ce0e7df1a86096569dc1230c85`  
		Last Modified: Fri, 25 Oct 2024 02:37:25 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8988b5bf0a07fc37e38cc4d562bb42efb707d2b8386eb6eef3d7000622e4d43`  
		Last Modified: Fri, 25 Oct 2024 02:38:07 GMT  
		Size: 13.9 MB (13947713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b049572e0d13219dcd42d20089bd59d6860af37f2c9c0fe7c8a1e79774aa3375`  
		Last Modified: Fri, 25 Oct 2024 02:38:04 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de8112cd845766274a465b7aba29e08f38d21fa62445a41530e0794502690bc`  
		Last Modified: Fri, 25 Oct 2024 02:38:04 GMT  
		Size: 19.5 KB (19521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6bb294d616611f994756d0922816947e2fe904b62ed2fd97f4dfe87c61118ea`  
		Last Modified: Fri, 25 Oct 2024 02:38:04 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b8c2609aed247d0b7aaa7af416b162b5dc9793f30e4dbc8125668f218be01de`  
		Last Modified: Fri, 25 Oct 2024 03:06:36 GMT  
		Size: 161.0 KB (161014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f24796902ca624c5b91983c604d9dc04bea3ccb45c0374ccf340541ad7f9573`  
		Last Modified: Fri, 25 Oct 2024 03:06:34 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05738c2b5c9a91de69a34942a2033898c7c5ee7d4f228a2bf8dcf9dca26fc085`  
		Last Modified: Fri, 25 Oct 2024 03:06:34 GMT  
		Size: 442.4 KB (442372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58cdcc3e5b117f084c94a94f861d2934acdf7dc29460f07768cc18f4632c2da9`  
		Last Modified: Fri, 25 Oct 2024 03:06:35 GMT  
		Size: 4.1 MB (4073473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f9585bb6dd34e8bbed1619a4c73973977137488ee31d0ab49acf87cb6240f2d`  
		Last Modified: Fri, 25 Oct 2024 03:06:34 GMT  
		Size: 2.0 KB (2045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b502a47dccc53caca0d1f768324e590163de54a7fa53b8832f72531912e49fab`  
		Last Modified: Fri, 25 Oct 2024 03:06:34 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm-alpine` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:9ec105bc035c5c898c28f514e2ec181e3b35cea345ac439acb6828b303beefa5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42299159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95953bfcdaf5154c89aa862b4dcb2f002fe28892b617f354ba88959038aa2cb0`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Sat, 07 Sep 2024 00:43:30 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Sat, 07 Sep 2024 00:43:32 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Sat, 07 Sep 2024 00:43:32 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Sat, 07 Sep 2024 00:43:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 07 Sep 2024 00:43:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Sat, 07 Sep 2024 00:43:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Sep 2024 00:43:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 07 Sep 2024 00:43:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 07 Sep 2024 01:04:32 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 25 Oct 2024 00:52:20 GMT
ENV PHP_VERSION=8.3.13
# Fri, 25 Oct 2024 00:52:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Fri, 25 Oct 2024 00:52:20 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Fri, 25 Oct 2024 00:52:25 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 25 Oct 2024 00:52:25 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 25 Oct 2024 01:01:19 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 25 Oct 2024 01:01:19 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 25 Oct 2024 01:01:21 GMT
RUN docker-php-ext-enable sodium
# Fri, 25 Oct 2024 01:01:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Oct 2024 01:01:21 GMT
WORKDIR /var/www/html
# Fri, 25 Oct 2024 01:01:21 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 25 Oct 2024 01:01:21 GMT
STOPSIGNAL SIGQUIT
# Fri, 25 Oct 2024 01:01:21 GMT
EXPOSE 9000
# Fri, 25 Oct 2024 01:01:21 GMT
CMD ["php-fpm"]
# Fri, 25 Oct 2024 04:05:36 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Fri, 25 Oct 2024 04:05:36 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 25 Oct 2024 04:05:37 GMT
RUN apk add --no-cache bash
# Fri, 25 Oct 2024 04:05:38 GMT
ARG YOURLS_VERSION=1.9.2
# Fri, 25 Oct 2024 04:05:38 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Fri, 25 Oct 2024 04:05:38 GMT
ENV YOURLS_VERSION=1.9.2
# Fri, 25 Oct 2024 04:05:38 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Fri, 25 Oct 2024 04:05:39 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Fri, 25 Oct 2024 04:05:39 GMT
COPY --chown=www-data:www-datafile:407fa98e3948ea07c2ff8bc30ad1b3b7b28a1c2b9b5d8e5ab87f9b317a2bac85 in /usr/src/yourls/user/ 
# Fri, 25 Oct 2024 04:05:40 GMT
COPY file:50b4d483341578e719ad63fd7aaea99a0d6d7cebfb7b43d6098a656a975ee0e3 in /usr/local/bin/ 
# Fri, 25 Oct 2024 04:05:40 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 25 Oct 2024 04:05:40 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48ef8ad75958cd7eb0e453d0f85e72134ef3976f8351b5742370df35bc60ed42`  
		Last Modified: Sat, 07 Sep 2024 02:23:50 GMT  
		Size: 3.3 MB (3333388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f80c1299f6c626e7df88761199f03734cced725870be7a04dd95bf11e80104`  
		Last Modified: Sat, 07 Sep 2024 02:23:49 GMT  
		Size: 943.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb3615e2ca5466e128fbfbd9bfcaa4cc0a7c5935f1d980f13d765c6bfde9144`  
		Last Modified: Sat, 07 Sep 2024 02:23:49 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b324dba8535eea2357b994da9864afef849388a4c8e80235090810383253f31`  
		Last Modified: Fri, 25 Oct 2024 02:19:36 GMT  
		Size: 12.5 MB (12504686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e479347c3f32eee03df523edd0f1a869f7a7636702922f9d5db1ac9024ea211`  
		Last Modified: Fri, 25 Oct 2024 02:19:35 GMT  
		Size: 499.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23b04a5644c6d20e08059cccd97d6934147bebb18605c1dde72dd77c2a76455`  
		Last Modified: Fri, 25 Oct 2024 02:20:15 GMT  
		Size: 16.9 MB (16902093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7df40e793bac6573c663125ccfbeba7981561c44124f6fb6587c5a7b8254174`  
		Last Modified: Fri, 25 Oct 2024 02:20:12 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0990d1cc9efa7a886064d609af6f66ec31e70549b0a76e6e69d5a9901efc35ba`  
		Last Modified: Fri, 25 Oct 2024 02:20:12 GMT  
		Size: 19.5 KB (19500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997895c9b9ff476cc722581727f34c89230d1e2154be9e19517a382813e484af`  
		Last Modified: Fri, 25 Oct 2024 02:20:13 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51aad8f1c108c6a65a29dded51da9589f3d47509d8680300530c9ed53ced28ac`  
		Last Modified: Fri, 25 Oct 2024 04:06:42 GMT  
		Size: 816.1 KB (816093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a063f00d806d7f7bcbcf3b3c30005d620e04145842565621b2ff6d1256eac3`  
		Last Modified: Fri, 25 Oct 2024 04:06:39 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b2bba656a529dd2cffde142cfe0cbc4a4753a8444bc8d5c6173663891abc93`  
		Last Modified: Fri, 25 Oct 2024 04:06:40 GMT  
		Size: 544.9 KB (544916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1743ee3bcca52db6488719bf18669975f1ad99e939aa952df78d551e0636d21d`  
		Last Modified: Fri, 25 Oct 2024 04:06:40 GMT  
		Size: 4.1 MB (4073476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a976472ae8a2302ba8bbcf147d7b2b6d3f1e63feaace1551a55473547d4e083`  
		Last Modified: Fri, 25 Oct 2024 04:06:39 GMT  
		Size: 2.0 KB (2047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c92671ba4dd65fe1104c0ddfe29ece247e9a510aae186aecfea5f1631ea3654`  
		Last Modified: Fri, 25 Oct 2024 04:06:39 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm-alpine` - linux; 386

```console
$ docker pull yourls@sha256:ea2c47a322aed0ab1772c941b4bef8917a7048cbde6a101f2d504f8629f0eaaa
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.4 MB (38354793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd45d789ad65143cf43d4b591deaf495b6908a03ab834388874065c895890be6`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 22:57:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 22:57:51 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 22:57:52 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 22:57:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 22:57:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 22:57:52 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 22:57:53 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 22:57:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Sep 2024 23:42:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 26 Sep 2024 23:40:07 GMT
ENV PHP_VERSION=8.3.12
# Thu, 26 Sep 2024 23:40:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.12.tar.xz.asc
# Thu, 26 Sep 2024 23:40:07 GMT
ENV PHP_SHA256=f774e28633e26fc8c5197f4dae58ec9e3ff87d1b4311cbc61ab05a7ad24bd131
# Thu, 26 Sep 2024 23:40:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Sep 2024 23:40:13 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Sep 2024 23:53:44 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 26 Sep 2024 23:53:44 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 26 Sep 2024 23:53:45 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Sep 2024 23:53:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Sep 2024 23:53:46 GMT
WORKDIR /var/www/html
# Thu, 26 Sep 2024 23:53:46 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 26 Sep 2024 23:53:46 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Sep 2024 23:53:46 GMT
EXPOSE 9000
# Thu, 26 Sep 2024 23:53:47 GMT
CMD ["php-fpm"]
# Fri, 27 Sep 2024 05:06:44 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Fri, 27 Sep 2024 05:06:45 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 27 Sep 2024 05:06:46 GMT
RUN apk add --no-cache bash
# Fri, 27 Sep 2024 05:06:46 GMT
ARG YOURLS_VERSION=1.9.2
# Fri, 27 Sep 2024 05:06:46 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Fri, 27 Sep 2024 05:06:47 GMT
ENV YOURLS_VERSION=1.9.2
# Fri, 27 Sep 2024 05:06:47 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Fri, 27 Sep 2024 05:06:48 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Fri, 27 Sep 2024 05:06:49 GMT
COPY --chown=www-data:www-datafile:407fa98e3948ea07c2ff8bc30ad1b3b7b28a1c2b9b5d8e5ab87f9b317a2bac85 in /usr/src/yourls/user/ 
# Fri, 27 Sep 2024 05:06:49 GMT
COPY file:50b4d483341578e719ad63fd7aaea99a0d6d7cebfb7b43d6098a656a975ee0e3 in /usr/local/bin/ 
# Fri, 27 Sep 2024 05:06:49 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 27 Sep 2024 05:06:49 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17866811de1cdb9710f37a522dde62051d068230716118d22b6b987216e037ef`  
		Last Modified: Sat, 07 Sep 2024 01:49:46 GMT  
		Size: 3.3 MB (3331976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9513ca5d3e6e64e8e064f1b178ad39b5d375a65559181a7f4964c9471461ba8f`  
		Last Modified: Sat, 07 Sep 2024 01:49:45 GMT  
		Size: 942.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90338393c7a779c5576927d742c98b6841aa39aa84fe1b137708bd8f4d0ae68e`  
		Last Modified: Sat, 07 Sep 2024 01:49:45 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49780297be189a971be5de567fc77df4d1f028c473b0e4281317fe958ace0858`  
		Last Modified: Fri, 27 Sep 2024 03:26:41 GMT  
		Size: 12.5 MB (12514545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:507b27bb659f2115c30f2784b56ab81fae8b6bc12dc11cf49bff80725704b97f`  
		Last Modified: Fri, 27 Sep 2024 03:26:39 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7e12ccd68dba58910128ec0a50fa9721ee108e36b5523cfe01d362ae9b44ca`  
		Last Modified: Fri, 27 Sep 2024 03:27:25 GMT  
		Size: 13.9 MB (13909030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee97b32eb5e22727ff194106f632f0487d55d4e4f16dd1fa2be8f7a879bcb5d`  
		Last Modified: Fri, 27 Sep 2024 03:27:22 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409f402577af72398e7ab70eaca95e553aa6b51d4cdcfc1c96651a9bd715b3a7`  
		Last Modified: Fri, 27 Sep 2024 03:27:22 GMT  
		Size: 19.7 KB (19706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2411605fb9a5a2dc0f057fa28fbf87f75a3f4f95203a9a97db378f1ed14609bf`  
		Last Modified: Fri, 27 Sep 2024 03:27:22 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df594afce49f009e22d35db7ef304289a4234c789d3cc4da0dea1b09f8b0be90`  
		Last Modified: Fri, 27 Sep 2024 05:07:54 GMT  
		Size: 529.6 KB (529625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec3eafc42e29246c00f48a58102647a562ba6c16715b6973d0c6d34c1636485b`  
		Last Modified: Fri, 27 Sep 2024 05:07:52 GMT  
		Size: 324.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a288199265dce8fdd9f8c362471e0c3ad5930b08956ca82339e664e3ac81e21`  
		Last Modified: Fri, 27 Sep 2024 05:07:52 GMT  
		Size: 489.9 KB (489898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea849df1a483ad46fdcc35e5ac9a8d634d59675b82ea32780d2519642cd934d2`  
		Last Modified: Fri, 27 Sep 2024 05:07:53 GMT  
		Size: 4.1 MB (4073481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f449020fd2a40da56e4400b3474444bfccad4a4e10788166acaed72880dd549f`  
		Last Modified: Fri, 27 Sep 2024 05:07:52 GMT  
		Size: 2.1 KB (2052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e8bdc0cbba8f5a7c436a69b01a93f2f3768859acc2a1e941a1b9084c31efd6`  
		Last Modified: Fri, 27 Sep 2024 05:07:52 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm-alpine` - linux; ppc64le

```console
$ docker pull yourls@sha256:47ecc452658d74adc5404c12b690278894c40a3153536f45a22b863b142c1c9e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41146016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19404435c308cd2af3f6f4a0afcf4a771e042b07d52d83d845a2960700931985`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:15:52 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 23:15:54 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 23:15:56 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 23:15:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 23:15:57 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 23:15:57 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:15:58 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:15:58 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Sep 2024 23:59:12 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 25 Oct 2024 00:04:22 GMT
ENV PHP_VERSION=8.3.13
# Fri, 25 Oct 2024 00:04:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.13.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.13.tar.xz.asc
# Fri, 25 Oct 2024 00:04:23 GMT
ENV PHP_SHA256=89adb978cca209124fe53fd6327bc4966ca21213a7fa2e9504f854e340873018
# Fri, 25 Oct 2024 00:04:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Fri, 25 Oct 2024 00:04:29 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 25 Oct 2024 00:09:53 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 25 Oct 2024 00:09:54 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 25 Oct 2024 00:09:56 GMT
RUN docker-php-ext-enable sodium
# Fri, 25 Oct 2024 00:09:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 25 Oct 2024 00:09:56 GMT
WORKDIR /var/www/html
# Fri, 25 Oct 2024 00:09:57 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 25 Oct 2024 00:09:57 GMT
STOPSIGNAL SIGQUIT
# Fri, 25 Oct 2024 00:09:58 GMT
EXPOSE 9000
# Fri, 25 Oct 2024 00:09:58 GMT
CMD ["php-fpm"]
# Fri, 25 Oct 2024 01:19:44 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Fri, 25 Oct 2024 01:19:45 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 25 Oct 2024 01:19:46 GMT
RUN apk add --no-cache bash
# Fri, 25 Oct 2024 01:19:47 GMT
ARG YOURLS_VERSION=1.9.2
# Fri, 25 Oct 2024 01:19:47 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Fri, 25 Oct 2024 01:19:47 GMT
ENV YOURLS_VERSION=1.9.2
# Fri, 25 Oct 2024 01:19:48 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Fri, 25 Oct 2024 01:19:50 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Fri, 25 Oct 2024 01:19:50 GMT
COPY --chown=www-data:www-datafile:407fa98e3948ea07c2ff8bc30ad1b3b7b28a1c2b9b5d8e5ab87f9b317a2bac85 in /usr/src/yourls/user/ 
# Fri, 25 Oct 2024 01:19:50 GMT
COPY file:50b4d483341578e719ad63fd7aaea99a0d6d7cebfb7b43d6098a656a975ee0e3 in /usr/local/bin/ 
# Fri, 25 Oct 2024 01:19:51 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 25 Oct 2024 01:19:51 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9ac727a268c34206d27f9588c3acfc276afdaf0623dfdc19b7d210a7a881ee4`  
		Last Modified: Sat, 07 Sep 2024 01:44:58 GMT  
		Size: 3.4 MB (3408322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b564dcd8f1c226aa29a92bf07685b2a44ccb8ac47267a590bc34a56d25bbbcc4`  
		Last Modified: Sat, 07 Sep 2024 01:44:57 GMT  
		Size: 944.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e3867a87b0703f924c2a7915ce891a49d11c61af6d01613564e485431a9f78`  
		Last Modified: Sat, 07 Sep 2024 01:44:57 GMT  
		Size: 221.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8622608d41f825e14aa5bd26799c3251549bceef128cf2eae2f52f1ab78913e`  
		Last Modified: Fri, 25 Oct 2024 00:57:34 GMT  
		Size: 12.5 MB (12504690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b9b2cc7fa22223c46604afd8fd56f225e535ca1e7d006d545233f411a4a3c0`  
		Last Modified: Fri, 25 Oct 2024 00:57:33 GMT  
		Size: 497.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef8924f82b2625f8ef5e7542cf8df90a7ea23be0b16c0aba4eb7c33c1e1db88`  
		Last Modified: Fri, 25 Oct 2024 00:58:17 GMT  
		Size: 16.8 MB (16793437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:647cbae8e31365e26a7ccf044621ddbc54465f9788a82ff7a606cdcd2f3d2fd0`  
		Last Modified: Fri, 25 Oct 2024 00:58:14 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64837aa45d7b316149d05d385f9cf0d1242cc5f508dc01d54707975495ba636a`  
		Last Modified: Fri, 25 Oct 2024 00:58:14 GMT  
		Size: 19.5 KB (19493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c122d2282416fd41b44d88133833d1a36b36278e61186c0d6ee962ce2ef7c45c`  
		Last Modified: Fri, 25 Oct 2024 00:58:14 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8eccabc6f86b8bf8f2ead1f5c34c05c1f3e084739ce15236fc79bc3f48d5f4a`  
		Last Modified: Fri, 25 Oct 2024 01:20:48 GMT  
		Size: 208.6 KB (208626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53cafe8a8bfec88a04a2d740f6fb53227e5366ce380b24404e5185b3622f8ce`  
		Last Modified: Fri, 25 Oct 2024 01:20:46 GMT  
		Size: 325.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e31985a9e4d5b4dd327a58387e46c61a163f753dc32fb276045a4fa1d9ca15a`  
		Last Modified: Fri, 25 Oct 2024 01:20:46 GMT  
		Size: 548.2 KB (548203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28342485a34e01ecbdca99210d827a38c6b65da2e82262871117a3dec808de6c`  
		Last Modified: Fri, 25 Oct 2024 01:20:47 GMT  
		Size: 4.1 MB (4073469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8a35ec6d60984400b56fa501e2bdfa98395bab14de2e370adaa17c285c2abb`  
		Last Modified: Fri, 25 Oct 2024 01:20:46 GMT  
		Size: 2.0 KB (2047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68d70eeace420e07b213a5ec4aebe8ba28b7520adb438457fa3805873dbcc69`  
		Last Modified: Fri, 25 Oct 2024 01:20:46 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm-alpine` - linux; s390x

```console
$ docker pull yourls@sha256:69a070b85851666cf08410daddcbf8f463cdf23d08632ac883ea032fa1f8b606
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 MB (37827442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22bb1b16dcf078637d4cb72137d43084df0e66ae97c7896fab7295e7bfa979b0`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
CMD ["/bin/sh"]
# Fri, 06 Sep 2024 23:21:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev dpkg 		file 		g++ 		gcc 		libc-dev 		make 		pkgconf 		re2c
# Fri, 06 Sep 2024 23:21:08 GMT
RUN apk add --no-cache 		ca-certificates 		curl 		openssl 		tar 		xz
# Fri, 06 Sep 2024 23:21:09 GMT
RUN set -eux; 	adduser -u 82 -D -S -G www-data www-data
# Fri, 06 Sep 2024 23:21:09 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 06 Sep 2024 23:21:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Fri, 06 Sep 2024 23:21:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:21:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 06 Sep 2024 23:21:10 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 06 Sep 2024 23:42:29 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 26 Sep 2024 22:25:35 GMT
ENV PHP_VERSION=8.3.12
# Thu, 26 Sep 2024 22:25:35 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.12.tar.xz.asc
# Thu, 26 Sep 2024 22:25:35 GMT
ENV PHP_SHA256=f774e28633e26fc8c5197f4dae58ec9e3ff87d1b4311cbc61ab05a7ad24bd131
# Thu, 26 Sep 2024 22:25:39 GMT
RUN set -eux; 		apk add --no-cache --virtual .fetch-deps gnupg; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apk del --no-network .fetch-deps
# Thu, 26 Sep 2024 22:25:39 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 26 Sep 2024 22:32:07 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		$PHPIZE_DEPS 		argon2-dev 		coreutils 		curl-dev 		gnu-libiconv-dev 		libsodium-dev 		libxml2-dev 		linux-headers 		oniguruma-dev 		openssl-dev 		readline-dev 		sqlite-dev 	; 		rm -vf /usr/include/iconv.h; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv=/usr 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 						--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-cache $runDeps; 		apk del --no-network .build-deps; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 26 Sep 2024 22:32:08 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 26 Sep 2024 22:32:09 GMT
RUN docker-php-ext-enable sodium
# Thu, 26 Sep 2024 22:32:09 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 26 Sep 2024 22:32:09 GMT
WORKDIR /var/www/html
# Thu, 26 Sep 2024 22:32:10 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 26 Sep 2024 22:32:10 GMT
STOPSIGNAL SIGQUIT
# Thu, 26 Sep 2024 22:32:10 GMT
EXPOSE 9000
# Thu, 26 Sep 2024 22:32:10 GMT
CMD ["php-fpm"]
# Fri, 27 Sep 2024 02:35:54 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Fri, 27 Sep 2024 02:35:54 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 27 Sep 2024 02:35:55 GMT
RUN apk add --no-cache bash
# Fri, 27 Sep 2024 02:35:55 GMT
ARG YOURLS_VERSION=1.9.2
# Fri, 27 Sep 2024 02:35:55 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Fri, 27 Sep 2024 02:35:55 GMT
ENV YOURLS_VERSION=1.9.2
# Fri, 27 Sep 2024 02:35:56 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Fri, 27 Sep 2024 02:35:57 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Fri, 27 Sep 2024 02:35:57 GMT
COPY --chown=www-data:www-datafile:407fa98e3948ea07c2ff8bc30ad1b3b7b28a1c2b9b5d8e5ab87f9b317a2bac85 in /usr/src/yourls/user/ 
# Fri, 27 Sep 2024 02:35:57 GMT
COPY file:50b4d483341578e719ad63fd7aaea99a0d6d7cebfb7b43d6098a656a975ee0e3 in /usr/local/bin/ 
# Fri, 27 Sep 2024 02:35:57 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 27 Sep 2024 02:35:57 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9208ede8519d248128a660ad6cbef1b3a33b141374be176c946b5b17b2968ab4`  
		Last Modified: Sat, 07 Sep 2024 00:42:38 GMT  
		Size: 3.5 MB (3473993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabbdadb2babb53e22b8c60bffa37b66bacdd1495093eec38748ca15dabc8287`  
		Last Modified: Sat, 07 Sep 2024 00:42:37 GMT  
		Size: 943.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b2431f4d7c348124f66281fa6433fdcded6e6a093aedb9cdd6fa9c7d87a1407`  
		Last Modified: Sat, 07 Sep 2024 00:42:37 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36016ba9c526e5323d26d04a076ec5e3be849032b8a1a6974f74883a543d4391`  
		Last Modified: Fri, 27 Sep 2024 00:21:32 GMT  
		Size: 12.5 MB (12514557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640b952bffac3799480017b429663a8b55473ae133588ab65b79ac3dabb1a512`  
		Last Modified: Fri, 27 Sep 2024 00:21:31 GMT  
		Size: 498.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1272ce7d0e16ae48079cc29c6e57297ec551b964a42bd8de1a6bac249babd4c`  
		Last Modified: Fri, 27 Sep 2024 00:21:57 GMT  
		Size: 13.6 MB (13555084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf09d76621ca5efc78226bf04931fce6fa5e3e06925484a16ec1f623b4f423dc`  
		Last Modified: Fri, 27 Sep 2024 00:21:55 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2377a4ff1b53a8df636aef573506b1994b4cc10c9148a848979cda4dbdf6956d`  
		Last Modified: Fri, 27 Sep 2024 00:21:55 GMT  
		Size: 19.5 KB (19486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eddb2bda1e66cbb392555e7ad230fe93b1849b33f5409b7ec87ecebcd16330a6`  
		Last Modified: Fri, 27 Sep 2024 00:21:55 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6254031a79fadd1a62361b5e131503f715be1b8b9a08ac3b9e985746cc8f9a6b`  
		Last Modified: Fri, 27 Sep 2024 02:36:42 GMT  
		Size: 200.1 KB (200095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e689b210923061021533b2fb0b39167416d615ab4a43744ac0a1dacba7563b6b`  
		Last Modified: Fri, 27 Sep 2024 02:36:41 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c25bdc2e6b1c438483e5435d7bb3ae9ed6f109a7c27036053be146fec44469`  
		Last Modified: Fri, 27 Sep 2024 02:36:41 GMT  
		Size: 511.8 KB (511794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80374d9a0beaace2e0b861863ad1451cd5b5f389d43f0dc0fa4cea80bce273c`  
		Last Modified: Fri, 27 Sep 2024 02:36:41 GMT  
		Size: 4.1 MB (4073472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b37c11234b6b64d836c7371b2f7395193e0e47b4a9cd1eeb579e2ca3360303cd`  
		Last Modified: Fri, 27 Sep 2024 02:36:41 GMT  
		Size: 2.1 KB (2051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcfdc2acd36f2d2317b36ebb503ca048019ac8907f9f4245c071eb2455abb85b`  
		Last Modified: Fri, 27 Sep 2024 02:36:41 GMT  
		Size: 1.7 KB (1697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
