## `yourls:fpm`

```console
$ docker pull yourls@sha256:f9a898462f1f89271885747973f410e920c4aa9edcf98c6fdbce192a731c7a44
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
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

### `yourls:fpm` - linux; amd64

```console
$ docker pull yourls@sha256:8c7f6296796b864e4a8c36cec6d151978e1bdb6c5787f203165ecabcface6f9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.8 MB (181830819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:271a3cf3d59b783d59f5d9376c871b2386ab1512e7d8eb616d9a55d383044ddf`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:06:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Nov 2025 04:06:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Nov 2025 04:06:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 04:06:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Nov 2025 04:06:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Nov 2025 04:06:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 04:06:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 04:06:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Nov 2025 04:06:56 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 04 Nov 2025 04:06:56 GMT
ENV PHP_VERSION=8.4.14
# Tue, 04 Nov 2025 04:06:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 04 Nov 2025 04:06:56 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 04 Nov 2025 04:07:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Nov 2025 04:07:05 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:09:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Nov 2025 04:09:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:09:49 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 04 Nov 2025 04:09:50 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Nov 2025 04:09:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Nov 2025 04:09:50 GMT
WORKDIR /var/www/html
# Tue, 04 Nov 2025 04:09:50 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 04 Nov 2025 04:09:50 GMT
STOPSIGNAL SIGQUIT
# Tue, 04 Nov 2025 04:09:50 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 04 Nov 2025 04:09:50 GMT
CMD ["php-fpm"]
# Tue, 04 Nov 2025 07:41:15 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Tue, 04 Nov 2025 07:41:15 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 04 Nov 2025 07:41:17 GMT
ARG YOURLS_VERSION=1.10.2
# Tue, 04 Nov 2025 07:41:17 GMT
ARG YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 04 Nov 2025 07:41:17 GMT
ENV YOURLS_VERSION=1.10.2
# Tue, 04 Nov 2025 07:41:17 GMT
ENV YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 04 Nov 2025 07:41:17 GMT
# ARGS: YOURLS_VERSION=1.10.2 YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Tue, 04 Nov 2025 07:41:17 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Tue, 04 Nov 2025 07:41:17 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 07:41:17 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Tue, 04 Nov 2025 07:41:17 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e5fe17e68f22f45b5b8289eaafad0866d4b8a753a7738d4fd4eede8a09550ab`  
		Last Modified: Tue, 04 Nov 2025 04:10:26 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2126dd8a88a0c19dfdb7ace2440b487f85f46cacd6337d1bdda976a0345da0f`  
		Last Modified: Tue, 04 Nov 2025 04:10:38 GMT  
		Size: 117.8 MB (117838528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b6a6224213173e6ed562cde77e7f237c488fb70337dcd7831edbcf7c202f36`  
		Last Modified: Tue, 04 Nov 2025 04:10:26 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f36fdf404142d1cc011b6702f8c923968a0a507817510bfb0b48b37d614cb38f`  
		Last Modified: Tue, 04 Nov 2025 04:10:27 GMT  
		Size: 13.8 MB (13791535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f936d0fbe2bd7d3c4a9d1e74773dfe27ea968af8f6b7fd41d8b38d9ed187f11e`  
		Last Modified: Tue, 04 Nov 2025 04:10:26 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad537b0b726d26581f48a05117800f6847772ef4627c87840e4d9ddfc5d744cf`  
		Last Modified: Tue, 04 Nov 2025 04:10:28 GMT  
		Size: 13.7 MB (13660455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff015b6369be72a3a7e8b2b4f0ac3db3e9beb496e3331a9d4617acb13ae52ce`  
		Last Modified: Tue, 04 Nov 2025 04:10:26 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb79f402ec0e1e1df3618ecab18a250f34d2b2d43b32c1c7d450f31bf9ba5e8f`  
		Last Modified: Tue, 04 Nov 2025 04:10:27 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:470a6d36fae127548e05f2ff4a781a4f0d5ff338a563d7ffb2ec8c6fd62f8232`  
		Last Modified: Tue, 04 Nov 2025 04:10:26 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef1e62e8161332189bafd5b7e27a1c7fa22f8564f5873313a07b29232896872`  
		Last Modified: Tue, 04 Nov 2025 04:10:26 GMT  
		Size: 9.2 KB (9198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad6b3288cbe02887efa9b2b72b9d44e09db54d30ff72ed3f2774ea14f0a1fa4b`  
		Last Modified: Tue, 04 Nov 2025 07:41:28 GMT  
		Size: 671.3 KB (671316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f355fc1033917d5057056c5aa0536e1b99d5d5aaa9d69e30511dca007d82d780`  
		Last Modified: Tue, 04 Nov 2025 07:41:28 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b683d42708179cf6457c513cfe07c77d5716eae6cf2ef10682cd288a6f36e5c`  
		Last Modified: Tue, 04 Nov 2025 07:41:30 GMT  
		Size: 6.1 MB (6073654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e925cdfea6032d224481611e5550fe026ca9ecd4810c606ef6c08ef05512f196`  
		Last Modified: Tue, 04 Nov 2025 07:41:28 GMT  
		Size: 2.1 KB (2094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065d3ef509e369a62574275d482828c3fbac30fa29920889aeaefdf22ff0fce3`  
		Last Modified: Tue, 04 Nov 2025 07:41:28 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:97c723b1a19695def72ceba1cf6013900fd972adba25466f8cb2edd9f7f9f01c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d1c265e16141478cfb39fd8409d89ead74cc706d4b3a3b18622e5024fe652b6`

```dockerfile
```

-	Layers:
	-	`sha256:2c5d171e9c543fb748aec016c641fb2dd8ec882a2e559cd766d462c4277acc10`  
		Last Modified: Tue, 04 Nov 2025 11:43:07 GMT  
		Size: 27.5 KB (27481 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:fpm` - linux; arm variant v5

```console
$ docker pull yourls@sha256:290b13406658c83a70c18dbcb36ed1ff579ee753cfb73362b7bed569c219c2e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155110125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6370e5472c3a2c8bdbce32b4bfd751cfda89fbea42a7019923492adcf3f41f6a`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 00:39:21 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Nov 2025 00:39:43 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Nov 2025 00:39:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 00:39:43 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Nov 2025 00:39:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Nov 2025 00:39:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 00:39:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 00:39:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Nov 2025 00:39:43 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 04 Nov 2025 00:39:43 GMT
ENV PHP_VERSION=8.4.14
# Tue, 04 Nov 2025 00:39:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 04 Nov 2025 00:39:43 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 04 Nov 2025 00:39:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Nov 2025 00:39:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:42:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Nov 2025 00:42:52 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 00:42:52 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 04 Nov 2025 00:42:52 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Nov 2025 00:42:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Nov 2025 00:42:52 GMT
WORKDIR /var/www/html
# Tue, 04 Nov 2025 00:42:52 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 04 Nov 2025 00:42:52 GMT
STOPSIGNAL SIGQUIT
# Tue, 04 Nov 2025 00:42:52 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 04 Nov 2025 00:42:52 GMT
CMD ["php-fpm"]
# Tue, 04 Nov 2025 02:50:53 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Tue, 04 Nov 2025 02:50:53 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 04 Nov 2025 02:50:55 GMT
ARG YOURLS_VERSION=1.10.2
# Tue, 04 Nov 2025 02:50:55 GMT
ARG YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 04 Nov 2025 02:50:55 GMT
ENV YOURLS_VERSION=1.10.2
# Tue, 04 Nov 2025 02:50:55 GMT
ENV YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 04 Nov 2025 02:50:55 GMT
# ARGS: YOURLS_VERSION=1.10.2 YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Tue, 04 Nov 2025 02:50:55 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Tue, 04 Nov 2025 02:50:55 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 02:50:55 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Tue, 04 Nov 2025 02:50:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:453afc2258d7bc5729fed5672fb95bafa092e30a933b4377a12034be940a671b`  
		Last Modified: Tue, 04 Nov 2025 00:13:12 GMT  
		Size: 27.9 MB (27946438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8ba2162334449c487b11cac0e0639d05692eaf747643d14add02e392876ed4`  
		Last Modified: Tue, 04 Nov 2025 00:43:26 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78da078236a0d3d57f73ad4a2d9108a368e7b224cbc46497817124d923960f32`  
		Last Modified: Tue, 04 Nov 2025 00:43:34 GMT  
		Size: 94.9 MB (94875563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c66c34d17f1b846cf1a2bd9eb3950044ebf34090737a0d46f32f6eafb8f5e76`  
		Last Modified: Tue, 04 Nov 2025 00:43:26 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a20802caf5491cc85c7a87fda2e3fd1c00801ee8788693f005febcb0cb3cd8b`  
		Last Modified: Tue, 04 Nov 2025 00:43:29 GMT  
		Size: 13.8 MB (13789172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28764cacec48d8d96b630b2181f78fc3d43bd70f6ce815bfd835d61ca8a1c3b8`  
		Last Modified: Tue, 04 Nov 2025 00:43:26 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49cad2168180eb1354001a5e0e2f95c0480079ac01ee2e1fad344ac40e6eec40`  
		Last Modified: Tue, 04 Nov 2025 00:43:28 GMT  
		Size: 12.2 MB (12233273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6cfa3a2340e6136ea63d7ccfb55ff88a01813d47fa4696eb78755f28f8948e5`  
		Last Modified: Tue, 04 Nov 2025 00:43:26 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d79a363b14c912f30701606c9320b86d3bdf2d2ce97e7e1a08e6e1f5b9750e`  
		Last Modified: Tue, 04 Nov 2025 00:43:26 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:833feeca67f5cd2628c86dbf7be0892213dfbcc3ff2958c57befaa028852db1c`  
		Last Modified: Tue, 04 Nov 2025 00:43:27 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a05e1559838b428564623e8e981fa7da293ec08f5555a40ddfcc83fdc071bc9`  
		Last Modified: Tue, 04 Nov 2025 00:43:27 GMT  
		Size: 9.2 KB (9199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2da5e68d1491ff73d42379e7d4319100cce1110768e76dfce451dd7804248c7`  
		Last Modified: Tue, 04 Nov 2025 02:51:05 GMT  
		Size: 174.8 KB (174781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:284f5543549a42da86940ac50a3d32619a91b85e35cf84cdcfb26e1024cef4d5`  
		Last Modified: Tue, 04 Nov 2025 02:51:05 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:321f34105c516cf6259e16f08ffa40cee3983d4010f07f6f584726b9169b7857`  
		Last Modified: Tue, 04 Nov 2025 02:51:06 GMT  
		Size: 6.1 MB (6073655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91179d2e1f60473dbf04a4d74a64657a9d75380f86a67939834bb496eadd7b67`  
		Last Modified: Tue, 04 Nov 2025 02:51:05 GMT  
		Size: 2.1 KB (2097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c0fc6a9c34b86fe3cb5aea06c8c1510b03e8bc70c8bbc4d867e891a30b646f`  
		Last Modified: Tue, 04 Nov 2025 02:51:05 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:8b59bb9cad1e6bcd63dfe9762f56d37099cd92cc955b1eae4792de88c2b97625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 KB (27581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44be0e2abcf3f3f0220259433998105da5ce11e07159c57aed3f65c27860e920`

```dockerfile
```

-	Layers:
	-	`sha256:91c007133a58ad226051667c02b6c52c769915315ec2dfa14e005dbd00ad2a7f`  
		Last Modified: Tue, 04 Nov 2025 08:42:48 GMT  
		Size: 27.6 KB (27581 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:fpm` - linux; arm variant v7

```console
$ docker pull yourls@sha256:860217767f1788eb84011d0c5cb8d033bc294416cbbdb41a4606b0a41e4fa754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144062637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dca1937169ec9cbf8f46deb5ca17552d067d900362d5f75a268c6fe802b51fb`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:09:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Nov 2025 02:09:40 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Nov 2025 02:09:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:09:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Nov 2025 02:09:40 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Nov 2025 02:09:40 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 02:09:40 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 02:09:40 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Nov 2025 02:09:40 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 04 Nov 2025 02:09:40 GMT
ENV PHP_VERSION=8.4.14
# Tue, 04 Nov 2025 02:09:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 04 Nov 2025 02:09:40 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 04 Nov 2025 02:09:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Nov 2025 02:09:50 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 02:12:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Nov 2025 02:12:32 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 02:12:33 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 04 Nov 2025 02:12:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Nov 2025 02:12:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Nov 2025 02:12:33 GMT
WORKDIR /var/www/html
# Tue, 04 Nov 2025 02:12:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 04 Nov 2025 02:12:33 GMT
STOPSIGNAL SIGQUIT
# Tue, 04 Nov 2025 02:12:33 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 04 Nov 2025 02:12:33 GMT
CMD ["php-fpm"]
# Tue, 04 Nov 2025 03:20:15 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Tue, 04 Nov 2025 03:20:15 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 04 Nov 2025 03:20:17 GMT
ARG YOURLS_VERSION=1.10.2
# Tue, 04 Nov 2025 03:20:17 GMT
ARG YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 04 Nov 2025 03:20:17 GMT
ENV YOURLS_VERSION=1.10.2
# Tue, 04 Nov 2025 03:20:17 GMT
ENV YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 04 Nov 2025 03:20:17 GMT
# ARGS: YOURLS_VERSION=1.10.2 YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Tue, 04 Nov 2025 03:20:17 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Tue, 04 Nov 2025 03:20:17 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 03:20:17 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Tue, 04 Nov 2025 03:20:17 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f514cf9237a39681c8ce234133379ed4ef8f74a01f406939c87b30e7a08ae08`  
		Last Modified: Tue, 04 Nov 2025 02:12:58 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e040a22d2dfd3ea294053d4d17be950e39f8768b36251faaa66929f8466e7fad`  
		Last Modified: Tue, 04 Nov 2025 02:13:08 GMT  
		Size: 86.2 MB (86245918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01213e8a92d2fe44916741e5c86b39794ad4b3c962fd1d7eb07082863e733dca`  
		Last Modified: Tue, 04 Nov 2025 02:12:58 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9179ac57796155178e2dcf91a54ea4ad107c408cd4800eb2db9403ae12d4513c`  
		Last Modified: Tue, 04 Nov 2025 02:13:00 GMT  
		Size: 13.8 MB (13789282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01800e7739dc51a39550c8a36e6dd7347c6960d8731da26b814bc7173624bdea`  
		Last Modified: Tue, 04 Nov 2025 02:12:58 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9e53914c3cefd95d79d7b2d56c87bff85fb1aeaa2d8405ec5ef4b4f5461916`  
		Last Modified: Tue, 04 Nov 2025 02:12:59 GMT  
		Size: 11.6 MB (11562150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abca587a618a59fca6420d568e5f826754460b026fef2fae18781a48b10ba53`  
		Last Modified: Tue, 04 Nov 2025 02:12:58 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4162d748e7e46c771ceecd80ecc6753d2c98f2edfc8a41b08f467d94ac493d`  
		Last Modified: Tue, 04 Nov 2025 02:12:58 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e41a02299fd7b46ec62c6d2b72766b17251d4f89a3c972f4b2bff4525260310c`  
		Last Modified: Tue, 04 Nov 2025 02:12:58 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25153f51bd066c29931583973e3cd08eb8e4edabe6f82328bdaff5de922a066`  
		Last Modified: Tue, 04 Nov 2025 02:12:58 GMT  
		Size: 9.2 KB (9196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cec96481d62cf6ad62245ec229697a97026316104b88bdef10b55bbd09d6f517`  
		Last Modified: Tue, 04 Nov 2025 04:03:20 GMT  
		Size: 161.4 KB (161391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9402ca43bbd25ec6e9f669c7bd9ab0b529d19ea19bdf54bebace0f329130e7aa`  
		Last Modified: Tue, 04 Nov 2025 04:03:20 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a233358b52b7edcfbfea3c9ee10dd4b12c7283c92ac530d39c4c5d52c9534c15`  
		Last Modified: Tue, 04 Nov 2025 11:43:52 GMT  
		Size: 6.1 MB (6073644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f38e7d8eca9728fd3159e3f038f6b345d0ae2b7e9cb97961127620f67b9ae92`  
		Last Modified: Tue, 04 Nov 2025 04:03:21 GMT  
		Size: 2.1 KB (2089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da45ad67fa5f7cff8128f017530d5763dd6c7384efb16e1a374be459340a9274`  
		Last Modified: Tue, 04 Nov 2025 04:03:20 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:fde86b136f8f3639da8d7a311c10c4ccf5cc5b5258af2f4dfed3d4ae3a30f137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 KB (27581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:023b7c2315968835af87726f54f9edf9f1bd8569dcb0566aa22993d9e78cf453`

```dockerfile
```

-	Layers:
	-	`sha256:493ccf439913cfd6204ca70b8b1ba827174e89a9bf45382b9a5c9d835e0946a9`  
		Last Modified: Tue, 04 Nov 2025 11:43:12 GMT  
		Size: 27.6 KB (27581 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:fpm` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:9b5625e50598775b669945b6ff366c05799ed6db4e064e984d8504a7267c4943
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.1 MB (174107711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:387fba55c1552140cbc0a5a2d8dc97997e3bf562badf9daaa32caf6abee2c09f`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:20:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Nov 2025 01:21:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Nov 2025 01:21:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 01:21:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Nov 2025 01:21:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Nov 2025 01:21:14 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 01:21:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 01:21:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Nov 2025 01:21:14 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 04 Nov 2025 01:21:14 GMT
ENV PHP_VERSION=8.4.14
# Tue, 04 Nov 2025 01:21:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 04 Nov 2025 01:21:14 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 04 Nov 2025 01:21:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Nov 2025 01:21:24 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:24:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Nov 2025 01:24:31 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:24:31 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 04 Nov 2025 01:24:31 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Nov 2025 01:24:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Nov 2025 01:24:31 GMT
WORKDIR /var/www/html
# Tue, 04 Nov 2025 01:24:31 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 04 Nov 2025 01:24:31 GMT
STOPSIGNAL SIGQUIT
# Tue, 04 Nov 2025 01:24:31 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 04 Nov 2025 01:24:31 GMT
CMD ["php-fpm"]
# Tue, 04 Nov 2025 02:19:23 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Tue, 04 Nov 2025 02:19:23 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 04 Nov 2025 02:19:25 GMT
ARG YOURLS_VERSION=1.10.2
# Tue, 04 Nov 2025 02:19:25 GMT
ARG YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 04 Nov 2025 02:19:25 GMT
ENV YOURLS_VERSION=1.10.2
# Tue, 04 Nov 2025 02:19:25 GMT
ENV YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 04 Nov 2025 02:19:25 GMT
# ARGS: YOURLS_VERSION=1.10.2 YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Tue, 04 Nov 2025 02:19:25 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Tue, 04 Nov 2025 02:19:25 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 02:19:25 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Tue, 04 Nov 2025 02:19:25 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a28af7603cdf6004d302424db9853fb489926eababed22cbe970346cb4a5e87`  
		Last Modified: Tue, 04 Nov 2025 01:25:01 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2731e5164d54ee6e46123f5188c4200070cceb2705e6dd407f33a6b9cb37699`  
		Last Modified: Tue, 04 Nov 2025 02:16:05 GMT  
		Size: 110.2 MB (110162764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b263042dc7dd327e9f48c2e5bf784f51e4a1c866753a34b8da411a649aa0e9b8`  
		Last Modified: Tue, 04 Nov 2025 01:25:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b3c84f2838cff64ff8bafbde54f4267231d7835dd6ce8d673695239bd8f5c4`  
		Last Modified: Tue, 04 Nov 2025 01:25:03 GMT  
		Size: 13.8 MB (13791188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d415c0a35ffcdcd2cdd9cbdfbbe4e8759207ff3dec7e32456acfcea3e607298`  
		Last Modified: Tue, 04 Nov 2025 01:25:01 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2952f26b621e51373a10b32d1730c92d9adb91d72b4c20bd8a35c5cc7c7e2e02`  
		Last Modified: Tue, 04 Nov 2025 01:25:03 GMT  
		Size: 13.3 MB (13328243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c97ad7844b63e2d81e4e0a4a6356bd62aa4149cbabc4b0438ee217b8e9d65a3b`  
		Last Modified: Tue, 04 Nov 2025 01:25:01 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ddcb1ce63088e30d61bf426cef5ce7b8ad1cf0e3cec1bdaaa4d7a0d8dd44ef`  
		Last Modified: Tue, 04 Nov 2025 01:25:01 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ca1bbcbfd2ecdd1d25a2cb18d209bcd52a86476da3f1d6db24e4080f2bfef2`  
		Last Modified: Tue, 04 Nov 2025 01:25:01 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a59d5459d17e4321f99c6aa9f1f8fc8a0c883b6340a11b0105f3f714c77588ba`  
		Last Modified: Tue, 04 Nov 2025 01:25:01 GMT  
		Size: 9.2 KB (9198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:893d3c298fbac3e7a8088b0e7ed51db41e1d0fa726e5eb9c6e0de2e7b502a7fc`  
		Last Modified: Tue, 04 Nov 2025 02:19:34 GMT  
		Size: 592.3 KB (592334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3372860f633d5b8a2657a378bd4546d8e6a9fb6ec7d555b9f234f082a2d6d3a8`  
		Last Modified: Tue, 04 Nov 2025 02:19:34 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608f6ab3f5bfcfdfb9294078d7754e528ac2bfaa82fbe2fa5c1884f0087681a3`  
		Last Modified: Tue, 04 Nov 2025 02:19:35 GMT  
		Size: 6.1 MB (6073654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc1f39c52f5e3dd840b92a19b00a188ceda4179c60d680307e9f78d8692f39db`  
		Last Modified: Tue, 04 Nov 2025 02:19:34 GMT  
		Size: 2.1 KB (2095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf8bbd39271b9e42eac195f02dab38f22146fc0a5ed3f011d332308d2337db8`  
		Last Modified: Tue, 04 Nov 2025 02:19:34 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:619be6e34a3427dbe2d3d567e33ab2ab9083ed1ff655083d33543cbb3e90f9e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 KB (27615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9127010cc35e53903cef7cd733534d4ac4353a4dc430ea56c6f632a21b33a51e`

```dockerfile
```

-	Layers:
	-	`sha256:b8007603c86e8ddf68ec6f71f0319507cd10fb0e6565a134a2c2f6446e720127`  
		Last Modified: Tue, 04 Nov 2025 11:43:15 GMT  
		Size: 27.6 KB (27615 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:fpm` - linux; 386

```console
$ docker pull yourls@sha256:94e9835c139b14530581c77a59dd1745194e378aabd9814254bada913c6b6b9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.0 MB (181968210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8495f5f2ce2d48128e52627f8ea8ab435d15804beda4e10c412ff4a2d8dd479`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:17:49 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 04 Nov 2025 01:18:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Nov 2025 01:18:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 01:18:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Nov 2025 01:18:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 04 Nov 2025 01:18:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 01:18:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Nov 2025 01:18:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Nov 2025 01:18:07 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 04 Nov 2025 01:18:07 GMT
ENV PHP_VERSION=8.4.14
# Tue, 04 Nov 2025 01:18:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 04 Nov 2025 01:18:07 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 04 Nov 2025 01:22:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 04 Nov 2025 01:22:22 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:25:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 04 Nov 2025 01:25:15 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 01:25:15 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 04 Nov 2025 01:25:15 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 04 Nov 2025 01:25:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Nov 2025 01:25:15 GMT
WORKDIR /var/www/html
# Tue, 04 Nov 2025 01:25:15 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 04 Nov 2025 01:25:15 GMT
STOPSIGNAL SIGQUIT
# Tue, 04 Nov 2025 01:25:15 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 04 Nov 2025 01:25:15 GMT
CMD ["php-fpm"]
# Tue, 04 Nov 2025 02:19:41 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Tue, 04 Nov 2025 02:19:41 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 04 Nov 2025 02:19:43 GMT
ARG YOURLS_VERSION=1.10.2
# Tue, 04 Nov 2025 02:19:43 GMT
ARG YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 04 Nov 2025 02:19:43 GMT
ENV YOURLS_VERSION=1.10.2
# Tue, 04 Nov 2025 02:19:43 GMT
ENV YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 04 Nov 2025 02:19:43 GMT
# ARGS: YOURLS_VERSION=1.10.2 YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Tue, 04 Nov 2025 02:19:43 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Tue, 04 Nov 2025 02:19:43 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 02:19:43 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Tue, 04 Nov 2025 02:19:43 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc20212c96bdc95ed31aa8da46f5114adb20d7818c6cec7bc6d4c0fc5b3c0e3e`  
		Last Modified: Tue, 04 Nov 2025 01:22:13 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac5aeb396423137c15bb282c86fc0326729028b17b04946aaa3f641d7d50555d`  
		Last Modified: Tue, 04 Nov 2025 01:22:28 GMT  
		Size: 116.1 MB (116138351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4854d175d1928040d3aee9a6918991a89bc7f5be2c517284578ddcf9f7924286`  
		Last Modified: Tue, 04 Nov 2025 01:22:13 GMT  
		Size: 221.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8253dcabd073888ed17a511430bf9fdecd805b9066db113b596ce8f6abb10cd`  
		Last Modified: Tue, 04 Nov 2025 01:25:34 GMT  
		Size: 13.8 MB (13790705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26541f36a3b89b0acdc57ba70c0373baac6f2e4a9761a5f709d670e1066fde2a`  
		Last Modified: Tue, 04 Nov 2025 01:25:33 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4016d656d1b3ca6a6d6ff99085c2ee9fe2a8d8156846cfdcc4dcc6fb65b78c1`  
		Last Modified: Tue, 04 Nov 2025 01:25:35 GMT  
		Size: 14.0 MB (13957305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e98a91d44c15cbee61fee1db9e00844616526b52899b6c02dbd7837f8f4c08`  
		Last Modified: Tue, 04 Nov 2025 01:25:33 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c619aa47839def92d079eecb2ee8f5ed62262f62ca4ab72ca95071b7cad89ab6`  
		Last Modified: Tue, 04 Nov 2025 01:25:33 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc2c858406a873d223fe50251aab03bf4aa0a118f814cb1424df703f8a1e90d9`  
		Last Modified: Tue, 04 Nov 2025 01:25:33 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a295856b6731c5eab7ac490311de9a2607f43b588e5958469e39cd73b82958`  
		Last Modified: Tue, 04 Nov 2025 01:25:33 GMT  
		Size: 9.2 KB (9194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522f599b6c695115984fd248821782c8c7fa9d5f7e6673a224fca85b85b3c214`  
		Last Modified: Tue, 04 Nov 2025 02:19:55 GMT  
		Size: 696.2 KB (696209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4b447ee6d977d55232358d8d1608d8fd710f3009ded842f132e9b95be5a98c`  
		Last Modified: Tue, 04 Nov 2025 02:19:54 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9488618380f37b7583425bab9b2fb1b6c69cf450c90530055ed3cadae0bad931`  
		Last Modified: Tue, 04 Nov 2025 02:19:55 GMT  
		Size: 6.1 MB (6073655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6214e1c3706f07c19192bb844f9751ade994e4a624f215507e91fa6a73e6e82d`  
		Last Modified: Tue, 04 Nov 2025 02:19:54 GMT  
		Size: 2.1 KB (2094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e647336d465d55479d57ac9a98c0eb2ad6ccfc537d9b3445c7e2ccc028952929`  
		Last Modified: Tue, 04 Nov 2025 02:19:54 GMT  
		Size: 1.7 KB (1689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:4d6a69d6ec3c0f2564f9efc495a10bafc5ecd2c51c26a2593c4af18a13ad34f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 KB (27445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78644350b557a7f2339d1069a583611d86b0f8255315f3bfe30864ffd039b0d2`

```dockerfile
```

-	Layers:
	-	`sha256:8f13ced2b3927bd5fcd53163163935a6c18d72802ed9454ae7e83977e5469fc8`  
		Last Modified: Tue, 04 Nov 2025 11:43:18 GMT  
		Size: 27.4 KB (27445 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:fpm` - linux; ppc64le

```console
$ docker pull yourls@sha256:319fa0b6a89931852b7075bff2484a05ba942469f80b9623625f534566f732d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.5 MB (177508349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83fda32e0a5538389e86fdb8f10782bf03fe07ec16d9c9713d228ec123ac424a`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 19 Aug 2025 10:14:17 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 Aug 2025 10:14:17 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_VERSION=8.4.14
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 Aug 2025 10:14:17 GMT
WORKDIR /var/www/html
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 Aug 2025 10:14:17 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["php-fpm"]
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ARG YOURLS_VERSION=1.10.2
# Tue, 19 Aug 2025 10:14:17 GMT
ARG YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 19 Aug 2025 10:14:17 GMT
ENV YOURLS_VERSION=1.10.2
# Tue, 19 Aug 2025 10:14:17 GMT
ENV YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 19 Aug 2025 10:14:17 GMT
# ARGS: YOURLS_VERSION=1.10.2 YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a9b4dd19a96be85b367998327f4288ed2fa8f174d1b3e8bea8ac7c2c626ec865`  
		Last Modified: Tue, 21 Oct 2025 00:26:55 GMT  
		Size: 33.6 MB (33598518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d9930d173c844c53a7c234fc6795612dd8a9cd3fa137cebec8570aa820f7779`  
		Last Modified: Tue, 21 Oct 2025 02:18:16 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf07ac4257b79ada16559cfa4a31502b1c711128c5199e235de1363c9bcbd2bf`  
		Last Modified: Tue, 21 Oct 2025 02:18:23 GMT  
		Size: 109.6 MB (109597844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87cff8614d84588c83a0d2abe18d46fc6b68b149ff9548d76e95cacef7b67548`  
		Last Modified: Tue, 21 Oct 2025 02:18:17 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7660a090dded77a1b74e83f8183f50673f4d16089f523d55b31064a05010151`  
		Last Modified: Fri, 24 Oct 2025 20:30:21 GMT  
		Size: 13.8 MB (13806094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e1c8fd8566ca6aa2f2ec65d080c82e6cde2a2b9fe9e1452a1159f214faddd0`  
		Last Modified: Fri, 24 Oct 2025 20:30:19 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:213deecbab5b04f31e8f790a775274e9956177ee128d2b331790c093647e6a80`  
		Last Modified: Fri, 24 Oct 2025 20:39:40 GMT  
		Size: 14.2 MB (14205686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7ad4fdea1f9ec7b24c6d570c1ccfd4cc83afe8376f2e47fbedf791d35d2c7b`  
		Last Modified: Fri, 24 Oct 2025 20:39:39 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af4e7ff20dc11ad21cf7ec15f8952b3b5c9fcf39e64e20b7f9398c99212db528`  
		Last Modified: Fri, 24 Oct 2025 20:39:39 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:388e8c2a09a29719ecb9c6ef7daf28d31ac9db20d97dca4e91a6a21134130d2c`  
		Last Modified: Fri, 24 Oct 2025 20:39:38 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b84b644399545f64ebda9d6d92ddabf163480c9d09753b010f0bfcb3c0b21fd2`  
		Last Modified: Fri, 24 Oct 2025 20:39:38 GMT  
		Size: 9.2 KB (9196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9aa164354de9fe4f6538f477da8533aebb4ef9e32a16d211086ac14b0face2c`  
		Last Modified: Sat, 25 Oct 2025 02:51:53 GMT  
		Size: 209.3 KB (209317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f11beed11ae9ee75d76f906ac87c04e6ea3c9e38746adf0146996f8c8081380`  
		Last Modified: Sat, 25 Oct 2025 02:51:53 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f304170a8d02f894fc1cfa7ebb2fc3d849336cfdf0e3c0162eeaad7b4dcd3946`  
		Last Modified: Sat, 25 Oct 2025 02:51:53 GMT  
		Size: 6.1 MB (6073648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b91cdd072b61a4b7848cca9b25cf3518e3d393503d3cbe94ec13fbe077604da`  
		Last Modified: Sat, 25 Oct 2025 02:51:53 GMT  
		Size: 2.1 KB (2096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c38b0a1bd5b55a7b3833f6f3db1f553f3995aa66ace97cef6fb74dd56e63b03`  
		Last Modified: Sat, 25 Oct 2025 02:51:53 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:2a78012a6c703c500386a3187c5c6e8447317aaa7e266d2a4a6335b1e203519c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 KB (27572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf6673e8f809a14b694210bb14821075f8d8f3e846e69447599df85bc2922e8`

```dockerfile
```

-	Layers:
	-	`sha256:c27684781c12fa1327de93b3bdd543d0a2d4eaf146f5951dbdef8d23dcc7ead2`  
		Last Modified: Sat, 25 Oct 2025 04:42:50 GMT  
		Size: 27.6 KB (27572 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:fpm` - linux; riscv64

```console
$ docker pull yourls@sha256:ea95d9cc178b2acc92102c2352a7e240b70d68b4c7d9f5e53c6892a908e0234e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.1 MB (208084168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:264925a461ecaefd6d12b2a8cd1616d007fd89e6be9a95ccbf0539d295b89215`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 19 Aug 2025 10:14:17 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 Aug 2025 10:14:17 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_VERSION=8.4.14
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 Aug 2025 10:14:17 GMT
WORKDIR /var/www/html
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 Aug 2025 10:14:17 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["php-fpm"]
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ARG YOURLS_VERSION=1.10.2
# Tue, 19 Aug 2025 10:14:17 GMT
ARG YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 19 Aug 2025 10:14:17 GMT
ENV YOURLS_VERSION=1.10.2
# Tue, 19 Aug 2025 10:14:17 GMT
ENV YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 19 Aug 2025 10:14:17 GMT
# ARGS: YOURLS_VERSION=1.10.2 YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10e23c0c73cc8f0a9cca6c3668230538af936622d758ae4720124e65d1901fb`  
		Last Modified: Tue, 21 Oct 2025 07:00:41 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a425a73dbb9980b18297b2dd5ae6470d5dd6bff4029928b3c47109bbcfc0163`  
		Last Modified: Tue, 21 Oct 2025 17:30:53 GMT  
		Size: 146.6 MB (146579498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0199b9324986716555eaee60a4139b64762a2ce7dc60435723ca0d60bbdcc8e7`  
		Last Modified: Tue, 21 Oct 2025 07:00:41 GMT  
		Size: 222.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca47e77a86254002ae83ffe25a0654bb2a501ce9a949dacbbeccc06160b52ab8`  
		Last Modified: Sat, 25 Oct 2025 16:06:43 GMT  
		Size: 13.8 MB (13806057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ecd0eda6a6b0b04f00a2df4218253b0abf6a3663c0a959146820ad62a2fff5`  
		Last Modified: Sat, 25 Oct 2025 16:06:41 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c3fff779e9ef018a302a1dc6cce838694a93c0bd40ca692d30fbf3414ce8655`  
		Last Modified: Sat, 25 Oct 2025 18:06:24 GMT  
		Size: 13.1 MB (13146939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2c33ae670d9442c831391f9eb25c9b3153a9ee8d07af4deaf771b99950d8ff`  
		Last Modified: Sat, 25 Oct 2025 18:06:22 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbad695038e7b3ab0dd8c4bb761cdd85b49e9087ad0ebffcd898521d094404f9`  
		Last Modified: Sat, 25 Oct 2025 18:06:22 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be0177b7e80a06a600fc281fc166ba5fea8415e579b4fb5c56183c21bc8c117`  
		Last Modified: Sat, 25 Oct 2025 18:06:22 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:251766f6070e2c3382c52ccfb814456c8be087d130d21304a0d77c3db3355079`  
		Last Modified: Sat, 25 Oct 2025 18:06:22 GMT  
		Size: 9.2 KB (9199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9bd13c6c56209a9408c8e88409ca08c3c641605eaa7d77ecf464945d5425e7`  
		Last Modified: Mon, 27 Oct 2025 04:55:50 GMT  
		Size: 185.1 KB (185146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b28c49f3493e0e7c993cf7af4585da1ce0c45abe85a59b4f8415bb7d93855f89`  
		Last Modified: Mon, 27 Oct 2025 04:55:50 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6101374755c29934063bfe3ab70a800c65b564bc0b01fb07fa9f861a7520862e`  
		Last Modified: Mon, 27 Oct 2025 04:55:52 GMT  
		Size: 6.1 MB (6073644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7076d6b2ff30cf14758841b19eb23461b6655f108d83b99fdbfe31001fef7a3`  
		Last Modified: Mon, 27 Oct 2025 04:55:51 GMT  
		Size: 2.1 KB (2094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0b641a8a942c6f9af93c185910fff50e0028c9542633a784b521536c0ef353`  
		Last Modified: Mon, 27 Oct 2025 04:55:50 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:5b3ebfac2551a3bae52d295be5ad6d9138a6dfd70d8d843088368d628ce7127e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 KB (27572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed9e82747beb960878f83d8ccb9a2a0d6023906c2fb4f7f6cad83f36f49f9039`

```dockerfile
```

-	Layers:
	-	`sha256:4595a8730e80bff9e4770caf270c830767928a83d5bcdc91610547d189ac41a5`  
		Last Modified: Mon, 27 Oct 2025 07:42:45 GMT  
		Size: 27.6 KB (27572 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:fpm` - linux; s390x

```console
$ docker pull yourls@sha256:14bbefe445b24dc8689cbef887130d54f058fbb1cc75b0c1ac18b736764d98c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (155956900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9870791cd267d746bb05cbdff5e227d3490b7ebe1849cbbbd10c5bc9b4dcf7c6`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 19 Aug 2025 10:14:17 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 19 Aug 2025 10:14:17 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_VERSION=8.4.14
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.14.tar.xz.asc
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_SHA256=bac90ee7cf738e814c89b6b27d4d2c4b70e50942a420837e1a22f5fd5f9867a3
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN docker-php-ext-enable opcache # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN docker-php-ext-enable sodium # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 19 Aug 2025 10:14:17 GMT
WORKDIR /var/www/html
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 Aug 2025 10:14:17 GMT
EXPOSE map[9000/tcp:{}]
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["php-fpm"]
# Tue, 19 Aug 2025 10:14:17 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ARG YOURLS_VERSION=1.10.2
# Tue, 19 Aug 2025 10:14:17 GMT
ARG YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 19 Aug 2025 10:14:17 GMT
ENV YOURLS_VERSION=1.10.2
# Tue, 19 Aug 2025 10:14:17 GMT
ENV YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Tue, 19 Aug 2025 10:14:17 GMT
# ARGS: YOURLS_VERSION=1.10.2 YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 19 Aug 2025 10:14:17 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Tue, 19 Aug 2025 10:14:17 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:71dc03f1fd788f9fc2bbb931d3df17cbfaf0b486bdfb19f4e3b8792a206689a1`  
		Last Modified: Tue, 21 Oct 2025 00:28:26 GMT  
		Size: 29.8 MB (29837255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6c3f4ad4e24c29ede95cbb6fb2aa2828df1b20348eed91dade18765579bc19`  
		Last Modified: Tue, 21 Oct 2025 02:12:15 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b339ad9eb2dd636ee49d09322a8cc6b6ddb681a1c9115d8fdbd520598d3213bc`  
		Last Modified: Tue, 21 Oct 2025 02:12:21 GMT  
		Size: 92.6 MB (92564172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40db4669097adb199a40f97fcd445c22549de3dc01b5d9f3374183cb691b12ad`  
		Last Modified: Tue, 21 Oct 2025 02:12:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf671578f9b7abbfb746c7eb3b201a5bdd829a19a317b694802c39b4a8bcb5d`  
		Last Modified: Fri, 24 Oct 2025 19:33:00 GMT  
		Size: 13.8 MB (13805613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813ec806095ff4476c06b17194fe24361c4503aaf1db5ab5913f709b53deaded`  
		Last Modified: Fri, 24 Oct 2025 19:32:58 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd09e285625b4fc0d731e8c0aabf9d7e816f85017b4b7dad6734d0ca6604ddd2`  
		Last Modified: Fri, 24 Oct 2025 19:40:37 GMT  
		Size: 13.5 MB (13458568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de2ac97f09589019b8b65aba84cc69ac4ec41181f90b775f3c0abeb56c79dbd`  
		Last Modified: Fri, 24 Oct 2025 19:40:27 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ebb53992444c16e553c4c948a2aa72a1a949d1c7abfe3fa335a175070af62b4`  
		Last Modified: Fri, 24 Oct 2025 19:40:27 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59275cfa71c6af7a514b975a8dc778fcd7f8c703ccd0099774bbbce5ca649e92`  
		Last Modified: Fri, 24 Oct 2025 19:40:27 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0044227cc19b5c82d1822f58e594b2778fba925b1ba7c3cd90f4d5129a22e4d`  
		Last Modified: Fri, 24 Oct 2025 19:40:27 GMT  
		Size: 9.2 KB (9197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2234f0b991dc03f90a2745b12abe9da6fdba3205905ed44e659beebd5721f0a4`  
		Last Modified: Sat, 25 Oct 2025 01:54:40 GMT  
		Size: 200.4 KB (200419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bfe42ddbb1abb1f71726635cb31cbd7c5f1748d8b89c960aeb5c3d5c0406964`  
		Last Modified: Sat, 25 Oct 2025 01:54:40 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8910374c3b5d7b076a6d517a648a9d3885da0ac8f348ac4e1f5abb5cfa6400c9`  
		Last Modified: Sat, 25 Oct 2025 01:54:41 GMT  
		Size: 6.1 MB (6073643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88559cd9ddc7818dc22ad2148f11a43e52435975787d104388222a78ffd8672`  
		Last Modified: Sat, 25 Oct 2025 01:54:41 GMT  
		Size: 2.1 KB (2097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67088d961b1e64917b103b03189da27e7115b221b3303617b39617abd87f4fe2`  
		Last Modified: Sat, 25 Oct 2025 01:54:40 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:bd119727034d71db4f90e0f69644bc6bba67ebee91b21d16967a2dedbbe92910
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a859eee385e5943d76a2a14fad7b4abf53c4433e09e5c7254d674daa144d93e`

```dockerfile
```

-	Layers:
	-	`sha256:788786eac4268b16d9d0027d3100e294ad69e23a753b8fab48d16934841ca951`  
		Last Modified: Sat, 25 Oct 2025 04:42:55 GMT  
		Size: 27.5 KB (27518 bytes)  
		MIME: application/vnd.in-toto+json
