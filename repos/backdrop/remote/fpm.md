## `backdrop:fpm`

```console
$ docker pull backdrop@sha256:79381e558b865faf19a81bb06afe1cbc02aadb9d6ff567345a66abd88bf4adbd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:d657a0c3a9b30da11db75b375c7a64f6aaccb0b4daecd068e93807486ff1996c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.7 MB (187704325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b125370f23ab9a41716a3856c6a42091e5da92dc13cc3220c7e81c523210cec`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 16 May 2025 15:29:55 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 May 2025 15:29:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_VERSION=8.3.25
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 16 May 2025 15:29:55 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 May 2025 15:29:55 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["php-fpm"]
# Fri, 16 May 2025 15:29:55 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_VERSION=1.31.0
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_MD5=0204d479a71ac692039a9f7b1e50409f
# Fri, 16 May 2025 15:29:55 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c436dd6a4e0df2f6f99442f95627769e29be264803069601602a8717ef1cee2a`  
		Last Modified: Mon, 08 Sep 2025 21:45:54 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bf577e05081f5219d270419b699e5d5a11daa891626a9c71edeff4dfbda4f1`  
		Last Modified: Mon, 08 Sep 2025 21:46:08 GMT  
		Size: 117.8 MB (117836402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67c41c4b65cd3b5ed6f9d7c2330f92a3c0201c8570ba5454cc1113280856e992`  
		Last Modified: Mon, 08 Sep 2025 21:45:51 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fedace43d9fe59159008d52231f3af49c4ee1feede95cf172c10b15bff3c17e`  
		Last Modified: Mon, 08 Sep 2025 21:45:52 GMT  
		Size: 12.7 MB (12731010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf21a6390c6b4f338547642090a57f97740bfe2f82e2d4562827281e60ccd007`  
		Last Modified: Mon, 08 Sep 2025 21:45:51 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aca112d35ba6e81f8e4ab5c209c817e82d2bf44319ca333342b2b8b9c4250b3c`  
		Last Modified: Mon, 08 Sep 2025 21:45:53 GMT  
		Size: 11.9 MB (11892967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c7d791e20ad100274137f081f763787ad9869d338da110da9f7b45dd93896af`  
		Last Modified: Mon, 08 Sep 2025 21:45:50 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9a9b8def36b84357ba2d08d56d709be0642b3477e7f79b39c643db9bd09a83`  
		Last Modified: Mon, 08 Sep 2025 21:45:50 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f8011a0b6b4b2b559f6a07bf2ed7be106051508a3bb2916f5a323580b8bea6`  
		Last Modified: Mon, 08 Sep 2025 21:45:49 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25089592a83257371648a3411054a7439e2fa2b97a477e81433a663f5e3e1ec1`  
		Last Modified: Mon, 08 Sep 2025 21:45:49 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf73c246b04c7d55814439bf5f77229d6e9475986ec7131098e09ee741ee81bc`  
		Last Modified: Mon, 08 Sep 2025 22:49:34 GMT  
		Size: 6.5 MB (6538048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8716d99bc4c5a8fa25117801b36bd6653929fb94df02424da2ebb9e46d59d836`  
		Last Modified: Mon, 08 Sep 2025 22:49:44 GMT  
		Size: 8.9 MB (8918324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:463eae99109def435292d55bcc610f6839c0f38e80cedfe0699ef7a76914e6a2`  
		Last Modified: Mon, 08 Sep 2025 22:44:14 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:6e848ffb1d23d8931002e472d625e6d2b0cc03f5b0a4bde74c41aeff3df5bc96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6960075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d2506a4ee05176d451f6019c3bd933083547e1570f5cdb335c80489ef0487b9`

```dockerfile
```

-	Layers:
	-	`sha256:7d8e5eaf6f1d552de50eb4c2633f5aad89e99ad8318bddc7f66ed3489673d876`  
		Last Modified: Tue, 09 Sep 2025 00:26:31 GMT  
		Size: 6.9 MB (6937721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:629b6d6ae1e6b16c3ceb5d1c221c43ccd14b1d3f00d9438508c39e38b7539cea`  
		Last Modified: Tue, 09 Sep 2025 00:26:32 GMT  
		Size: 22.4 KB (22354 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:3da37235a968fdb1df6f30e360e14703b977148b78630b1f9579e5c2df9d0a34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.0 MB (181048592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f581a3a8462832f87a52d48e0c27ca301d1ebe6998ef01a5c2894f9703693eb3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 16 May 2025 15:29:55 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 16 May 2025 15:29:55 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_VERSION=8.3.25
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.25.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.25.tar.xz.asc
# Fri, 16 May 2025 15:29:55 GMT
ENV PHP_SHA256=187b61bb795015adacf53f8c55b44414a63777ec19a776b75fb88614506c0d37
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 16 May 2025 15:29:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 16 May 2025 15:29:55 GMT
STOPSIGNAL SIGQUIT
# Fri, 16 May 2025 15:29:55 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["php-fpm"]
# Fri, 16 May 2025 15:29:55 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 16 May 2025 15:29:55 GMT
WORKDIR /var/www/html
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_VERSION=1.31.0
# Fri, 16 May 2025 15:29:55 GMT
ENV BACKDROP_MD5=0204d479a71ac692039a9f7b1e50409f
# Fri, 16 May 2025 15:29:55 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Fri, 16 May 2025 15:29:55 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 16 May 2025 15:29:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 16 May 2025 15:29:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1ee6d029e615fa2b873890f1011a42f1c5f78b2d100eaed3bc1df5bb73d212`  
		Last Modified: Thu, 14 Aug 2025 22:21:29 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a472e922e809f2164e7de33f1a04d157980da1614d66407be60d248980ca8453`  
		Last Modified: Thu, 14 Aug 2025 22:21:38 GMT  
		Size: 110.2 MB (110160334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48fe053e93cb40a6c44acd9d0ab0ee960880abe08bd106a21947710df1e0399e`  
		Last Modified: Thu, 14 Aug 2025 22:21:29 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cdcce6740fd6a8f3c41d30131d51a6ea809e5b01656fe975508e1d7a60aa997`  
		Last Modified: Thu, 28 Aug 2025 19:10:51 GMT  
		Size: 12.7 MB (12743739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:022365ce08bc77832d0e359d376cc74be2903d14d71021eef7081f1bd3c844f8`  
		Last Modified: Thu, 28 Aug 2025 19:10:50 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ebb3945344283e1146f3d391636fc74cae40a02bff23b637ba79596f8feb98`  
		Last Modified: Thu, 28 Aug 2025 19:23:36 GMT  
		Size: 11.9 MB (11918818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c7923fe2edb0be90b4c8c2850712b3748d6a4be6fe4d5276c607e4d791cb00`  
		Last Modified: Thu, 28 Aug 2025 19:23:35 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:524d5ed5ce087e680bda122c3cb8e8826c47bd9463a4e8f1fb0f5f1d13d474c9`  
		Last Modified: Thu, 28 Aug 2025 19:23:35 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419186009e6c8dc2a15ea13708c78146b1043adf14fbbaa1adad3715b49e2e22`  
		Last Modified: Thu, 28 Aug 2025 19:23:35 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09c0fb3bbb08418a367136de5625e44c994e2f697981639852a559385bdaaa4`  
		Last Modified: Thu, 28 Aug 2025 19:23:35 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a73b540549c89ad0587ca133f3a681d8321118e057bd2dbd0056cf5cd24233`  
		Last Modified: Thu, 28 Aug 2025 20:58:33 GMT  
		Size: 7.2 MB (7157237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964f028d353c045cee7ce5d3b4af04da6ae50c261741390846fcc8056df6c432`  
		Last Modified: Thu, 28 Aug 2025 20:58:33 GMT  
		Size: 8.9 MB (8918334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203d9d8a053d379a139388e37bd69105d51bc5685d5aa3124c9a6c2eddbfd77a`  
		Last Modified: Thu, 28 Aug 2025 20:58:32 GMT  
		Size: 949.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:e964904b50b596845496d3075ea173d18a4962faa2d3c3062282d712a27ffa80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7056589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1f5841daa517e4bfa9d50f78e5196e12e9c915b36ee8f22b91698c28837b00`

```dockerfile
```

-	Layers:
	-	`sha256:532bd2c9fd1d1a02fec6a679eb65c523259d9be01bc66c99b2ff2ea011647828`  
		Last Modified: Thu, 28 Aug 2025 21:26:47 GMT  
		Size: 7.0 MB (7034117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a931fc9fc39f157ed2df67c9ba500d9f9461c549ca51a737f36e34c9e5cb9320`  
		Last Modified: Thu, 28 Aug 2025 21:26:48 GMT  
		Size: 22.5 KB (22472 bytes)  
		MIME: application/vnd.in-toto+json
