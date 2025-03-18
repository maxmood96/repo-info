## `backdrop:fpm`

```console
$ docker pull backdrop@sha256:4be888f1c3dc7f12ec8127f2b999ee765f97cb4469b115cfb247e42598c286a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:b50428e2fd1b36cf43346258044e9c25be4fd62fd12244e95e493d4272e2fd75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.4 MB (187429753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5650c622d5d1939636f59556367bb745ea4efcf0cb628481ce7ed47fc1b5c12a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 07 Mar 2025 19:02:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 07 Mar 2025 19:02:00 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_VERSION=8.3.19
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
STOPSIGNAL SIGQUIT
# Fri, 07 Mar 2025 19:02:00 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["php-fpm"]
# Fri, 07 Mar 2025 19:02:00 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_VERSION=1.30.1
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_MD5=8117080cf35711087376410f85a65646
# Fri, 07 Mar 2025 19:02:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ba0c13e0a380d1066144c01cfba2ab859d271383069f8c2b442f6141a93b518`  
		Last Modified: Mon, 17 Mar 2025 23:18:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59086e1f0cf9b61be62079647cdc4eb36b89cea5edff168417222bb22b103614`  
		Last Modified: Mon, 17 Mar 2025 23:18:09 GMT  
		Size: 104.3 MB (104329136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf44beef353412043b2b3904037068ca43282275644dc9b25bab39318df2e2f`  
		Last Modified: Mon, 17 Mar 2025 23:18:07 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c6f0658675ec128165643f91dc72a063ebc6ddff00c2fa1a0a30e21bceafa9`  
		Last Modified: Mon, 17 Mar 2025 23:18:08 GMT  
		Size: 12.7 MB (12670866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c52b4d55386b4eb029ceb7084de7fd0755bb27068f7e5386d09191500cf532`  
		Last Modified: Mon, 17 Mar 2025 23:18:08 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd31f0048a04f2deacdfa04e90000a90da078da75b8b711b6c82eef396b3934`  
		Last Modified: Mon, 17 Mar 2025 23:18:09 GMT  
		Size: 27.8 MB (27828243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e79a7d807db4cf18efb8c69c13baefe71d1794e42bad07fa2f1d5d4e27b867`  
		Last Modified: Mon, 17 Mar 2025 23:18:09 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:789f3e28059cc460aa7b42e702b9031ae9a8be7a6c5f9a1cdef49b8fcfa5edbc`  
		Last Modified: Mon, 17 Mar 2025 23:18:09 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79abfc0ffe8fae80874cefe1dc5a68e73f7d831fb061e7f0adc8e6c0729c376`  
		Last Modified: Mon, 17 Mar 2025 23:18:10 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3a50659b9d6949bd73a7423e49d53e7615839c6090753685671927d4ad2737`  
		Last Modified: Tue, 18 Mar 2025 00:17:06 GMT  
		Size: 5.6 MB (5588002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9af74eb1ddb5c4f4102c3401b1979197f8c3ae0cbadbcfa3e7088be7257982`  
		Last Modified: Tue, 18 Mar 2025 00:17:06 GMT  
		Size: 8.8 MB (8794824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e4b96a5d219cafc293b68f995eea0528b3369efd25a46e311d24555ce8af1c1`  
		Last Modified: Tue, 18 Mar 2025 00:17:06 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:ce7da6f5dbee9cccee7a374cef703a1f6d58e7c6ceb44277befeb7b342f0ba7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6451388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dacadaa8e05016a6b0fa31f1eb111451d528b113d2048ba7506c60117c8f576`

```dockerfile
```

-	Layers:
	-	`sha256:41bb2cc6c12011a90b448e68cdab8cd47650effb3b281a708bb90450d2bd2045`  
		Last Modified: Tue, 18 Mar 2025 00:17:06 GMT  
		Size: 6.4 MB (6429804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2521730d2f4f9a7008aca3edcf3cbd555ea40389be2b67f105dfab454cc1cc16`  
		Last Modified: Tue, 18 Mar 2025 00:17:06 GMT  
		Size: 21.6 KB (21584 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:3d454b9bb282fc4b224560916df60eccaebb709ec5c12d51636cf2e0f0f269fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.0 MB (181032490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b5d72e237511d698382d62204c8899137f9dc69cbf0d44e74997414f8b3098`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 07 Mar 2025 19:02:00 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_VERSION=8.3.19
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Fri, 07 Mar 2025 19:02:00 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
STOPSIGNAL SIGQUIT
# Fri, 07 Mar 2025 19:02:00 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["php-fpm"]
# Fri, 07 Mar 2025 19:02:00 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
WORKDIR /var/www/html
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_VERSION=1.30.1
# Fri, 07 Mar 2025 19:02:00 GMT
ENV BACKDROP_MD5=8117080cf35711087376410f85a65646
# Fri, 07 Mar 2025 19:02:00 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 07 Mar 2025 19:02:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 07 Mar 2025 19:02:00 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31676cd976ed7c1a1f79275ef2602fefb67765b353e429d88aab3fd76863e399`  
		Last Modified: Tue, 25 Feb 2025 03:03:46 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6e69341e71d07089c45827b72bbbf8ca0698042a25ca2375d9c71797edd77e`  
		Last Modified: Tue, 25 Feb 2025 03:03:49 GMT  
		Size: 98.1 MB (98130460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ee28dda6888ebc4fc51f7f52c135986c07171dad8ce5a8fafed9d2f65d62ec`  
		Last Modified: Tue, 25 Feb 2025 03:03:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f19612df6c8b11eab84a5bb5b44627e00dda3eb5c29a447f494160d040a65be`  
		Last Modified: Fri, 14 Mar 2025 02:35:35 GMT  
		Size: 12.7 MB (12670786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1e86b8a62be947487f7600d97973fd3bec39aa741065ac318f924584c42f4fa`  
		Last Modified: Fri, 14 Mar 2025 02:35:34 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e31dd5ed02f9eea3f69b028908cc3bb42a7802cbfcb9e7c4b650706fd5e00eb`  
		Last Modified: Fri, 14 Mar 2025 02:40:25 GMT  
		Size: 27.8 MB (27772449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0d59bb902b97b58e0ca6f094a7cded9325884cdc29dd3cd8ec38cf7a5381eb`  
		Last Modified: Fri, 14 Mar 2025 02:40:24 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1f1b487ac17f877a44f7dd3f30e241e0823150253e7a38f462acaf8ef2112c5`  
		Last Modified: Fri, 14 Mar 2025 02:40:24 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98067ac8cbae75bbf2f044327990c759767da17c105c01cfb95c3374ee99e453`  
		Last Modified: Fri, 14 Mar 2025 02:40:25 GMT  
		Size: 9.2 KB (9188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14531b3ef2cef9e184f53e2b7e4e7c9e8248ca64ece49f4fd54af8a0f223d07f`  
		Last Modified: Fri, 14 Mar 2025 20:35:21 GMT  
		Size: 5.6 MB (5601721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:019b906ba031f251bf0ef0a242f4e60886a554e681d095c997810f7435e91cf8`  
		Last Modified: Fri, 14 Mar 2025 20:35:21 GMT  
		Size: 8.8 MB (8794808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa73c8576bf52489b87209e8f870c9359d00a83dbf0e12cdbbfe63c8553cb1d3`  
		Last Modified: Fri, 14 Mar 2025 20:35:20 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:359a6d0257f11f723c53d31702f41c9b18f79212f4170a16c0a6c41bde36ee4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6479902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:892c7f595224b74c8817efa0a8c1b10c0f457dcce703e928cbe73604961603b3`

```dockerfile
```

-	Layers:
	-	`sha256:7f9e77adf90b5eb89666b262a468cb6059d123e31bd2659de464d7b6b6809161`  
		Last Modified: Fri, 14 Mar 2025 20:35:20 GMT  
		Size: 6.5 MB (6458204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb5334c6c7f7762ea59823ab0c8ff88b62b37a0760af0c6edc25aeb90d8d6c59`  
		Last Modified: Fri, 14 Mar 2025 20:35:20 GMT  
		Size: 21.7 KB (21698 bytes)  
		MIME: application/vnd.in-toto+json
