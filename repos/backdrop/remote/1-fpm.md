## `backdrop:1-fpm`

```console
$ docker pull backdrop@sha256:41f81e2c629c68b83ef5422f3d898364d12e8098bb23bbb0a9675753dd4cc20f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:59044cd60b9c97903bb2d106cc002f22c416629117f06dfdcee55c86b405877f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.4 MB (187439434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cae9087e312477f111a0ad56a937516ab023580829f7cc889fc1704f8c30d759`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Jan 2025 03:55:56 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1740355200'
# Thu, 16 Jan 2025 03:55:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 16 Jan 2025 03:55:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 16 Jan 2025 03:55:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Jan 2025 03:55:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Jan 2025 03:55:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 16 Jan 2025 03:55:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Jan 2025 03:55:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Jan 2025 03:55:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 16 Jan 2025 03:55:56 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 16 Jan 2025 03:55:56 GMT
ENV PHP_VERSION=8.3.17
# Thu, 16 Jan 2025 03:55:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Thu, 16 Jan 2025 03:55:56 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Thu, 16 Jan 2025 03:55:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 16 Jan 2025 03:55:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 03:55:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 16 Jan 2025 03:55:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 03:55:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 16 Jan 2025 03:55:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 16 Jan 2025 03:55:56 GMT
WORKDIR /var/www/html
# Thu, 16 Jan 2025 03:55:56 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 16 Jan 2025 03:55:56 GMT
STOPSIGNAL SIGQUIT
# Thu, 16 Jan 2025 03:55:56 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 16 Jan 2025 03:55:56 GMT
CMD ["php-fpm"]
# Thu, 16 Jan 2025 03:55:56 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 16 Jan 2025 03:55:56 GMT
WORKDIR /var/www/html
# Thu, 16 Jan 2025 03:55:56 GMT
ENV BACKDROP_VERSION=1.30.0
# Thu, 16 Jan 2025 03:55:56 GMT
ENV BACKDROP_MD5=b4510de5df47fc277610f1eebceb7ac4
# Thu, 16 Jan 2025 03:55:56 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Thu, 16 Jan 2025 03:55:56 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Jan 2025 03:55:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Jan 2025 03:55:56 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:7cf63256a31a4cc44f6defe8e1af95363aee5fa75f30a248d95cae684f87c53c`  
		Last Modified: Tue, 25 Feb 2025 01:29:30 GMT  
		Size: 28.2 MB (28219301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc13aece20f33d2f2a5b061eb894bf5853409677da93284262aa65136e378e0d`  
		Last Modified: Tue, 25 Feb 2025 02:24:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4272f566deef911b3e789628e59b56ccc73946bc414ffb64aa5cdcaf737991`  
		Last Modified: Tue, 25 Feb 2025 02:24:51 GMT  
		Size: 104.3 MB (104345623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1375cb525613bd4f548e15f87666b848adbcc8324e3bf1cc654ff2e191982452`  
		Last Modified: Tue, 25 Feb 2025 02:24:49 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063d09a90e7c37c040c9198876ec1611b766047a93b958b564f8b64c024f5383`  
		Last Modified: Tue, 25 Feb 2025 02:24:51 GMT  
		Size: 12.7 MB (12650891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522ba3cca724b29e964c57f4f5a72b94d21700ad4c6686e2d046189738b06118`  
		Last Modified: Tue, 25 Feb 2025 02:24:50 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ae29a831c31d7afde4a21fb8159661e984847acb00be7104ca27cee07d86ae`  
		Last Modified: Tue, 25 Feb 2025 02:24:50 GMT  
		Size: 27.8 MB (27828364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcdf2effab82d99058cffbe200fd32c1edd3a609816c5761fb2db71341089037`  
		Last Modified: Tue, 25 Feb 2025 02:24:50 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39200e57518c59130d5a99eeec7de80d77d16c6fdca641ff19b2d73a3e338cf4`  
		Last Modified: Tue, 25 Feb 2025 02:24:51 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3e9ca325af0b12e67f643d90cc1ccf38ad57436e02c7fc9b2f049624b22528`  
		Last Modified: Tue, 25 Feb 2025 02:24:51 GMT  
		Size: 9.2 KB (9183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74799dc78f027405a90ba1569be12436d0c1af81982c47222599448107aa6fe6`  
		Last Modified: Tue, 25 Feb 2025 03:14:33 GMT  
		Size: 5.6 MB (5587426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21255c2bd7d060057ebbfde828f2e21e5af0f7bb365a26752b1f7b9d021e3ba7`  
		Last Modified: Tue, 25 Feb 2025 03:14:33 GMT  
		Size: 8.8 MB (8793999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74b69ef7e1b2d01845a7117bb6c963a745bfe35a063c82001fa25ae6f266eae`  
		Last Modified: Tue, 25 Feb 2025 03:14:33 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:4ae3cd2955d4d3b15f0929a41a723f5fc8fb8d7d11ed1f89c7209c36c3962e7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6451372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5790226c895968f4da0fb29e7200143a9392805b34f66797bcdef5e97375d50e`

```dockerfile
```

-	Layers:
	-	`sha256:095555ae7d84b9cfc86cc64f652ae0b60664efc68718812078d19367536b02c5`  
		Last Modified: Tue, 25 Feb 2025 03:14:33 GMT  
		Size: 6.4 MB (6429788 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2142b5d3829260a785c81728749910ecc0a23b7a626cb57784c8e32b7d44f955`  
		Last Modified: Tue, 25 Feb 2025 03:14:33 GMT  
		Size: 21.6 KB (21584 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:945bd31c234ee5fdb7140ca0fb58689ffdd3189df647c46c738120c51d1e023f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.0 MB (181003457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82389509827423e78c730c791ad89e0de12d66640e607893590026b761d94995`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Jan 2025 03:55:56 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Thu, 16 Jan 2025 03:55:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 16 Jan 2025 03:55:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 16 Jan 2025 03:55:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 16 Jan 2025 03:55:56 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Jan 2025 03:55:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 16 Jan 2025 03:55:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Jan 2025 03:55:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Jan 2025 03:55:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 16 Jan 2025 03:55:56 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 16 Jan 2025 03:55:56 GMT
ENV PHP_VERSION=8.3.17
# Thu, 16 Jan 2025 03:55:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.17.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.17.tar.xz.asc
# Thu, 16 Jan 2025 03:55:56 GMT
ENV PHP_SHA256=6158ee678e698395da13d72c7679a406d2b7554323432f14d37b60ed87d8ccfb
# Thu, 16 Jan 2025 03:55:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 16 Jan 2025 03:55:56 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 03:55:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 16 Jan 2025 03:55:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 16 Jan 2025 03:55:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 16 Jan 2025 03:55:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 16 Jan 2025 03:55:56 GMT
WORKDIR /var/www/html
# Thu, 16 Jan 2025 03:55:56 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 16 Jan 2025 03:55:56 GMT
STOPSIGNAL SIGQUIT
# Thu, 16 Jan 2025 03:55:56 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 16 Jan 2025 03:55:56 GMT
CMD ["php-fpm"]
# Thu, 16 Jan 2025 03:55:56 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Thu, 16 Jan 2025 03:55:56 GMT
WORKDIR /var/www/html
# Thu, 16 Jan 2025 03:55:56 GMT
ENV BACKDROP_VERSION=1.30.0
# Thu, 16 Jan 2025 03:55:56 GMT
ENV BACKDROP_MD5=b4510de5df47fc277610f1eebceb7ac4
# Thu, 16 Jan 2025 03:55:56 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Thu, 16 Jan 2025 03:55:56 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 16 Jan 2025 03:55:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 16 Jan 2025 03:55:56 GMT
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
	-	`sha256:7c1c4d6bf9e69519f60897ce4c9cb17b07e160bff393c08d5a63c4bbc9cd8465`  
		Last Modified: Tue, 25 Feb 2025 03:31:02 GMT  
		Size: 12.7 MB (12650793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc804e569d6ab7791891660bbf77785f5c4645f23a06e20667422a1776a1d816`  
		Last Modified: Tue, 25 Feb 2025 03:31:01 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b12ecd2f2fb50a6579221277167d86be68ae80f83b47abbcbd612b7c27fb669`  
		Last Modified: Tue, 25 Feb 2025 03:39:17 GMT  
		Size: 27.8 MB (27764205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e5253964a9be08eedf6dab9beffbb419a8c69f8600ae7b09476a52fe05689b`  
		Last Modified: Tue, 25 Feb 2025 03:39:16 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dbc850eab31ca269b1b4acb0029db851540c9baa174f2fb9a8cd9267c03731e`  
		Last Modified: Tue, 25 Feb 2025 03:39:16 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7afeba97b90193b385084cdb2a63e7db6ee5fe2b6ed1fa35ea343c60937de24b`  
		Last Modified: Tue, 25 Feb 2025 03:39:16 GMT  
		Size: 9.2 KB (9187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f7276dc362e36bb3f1c1ae61f0d1abb9c1e41af8a58a74205c9851101428812`  
		Last Modified: Tue, 25 Feb 2025 11:53:19 GMT  
		Size: 5.6 MB (5601741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c2d77d9478464fad24bbae7d5269dfe4d551676778db0a3aee7c309c0653aa8`  
		Last Modified: Tue, 25 Feb 2025 11:53:19 GMT  
		Size: 8.8 MB (8793997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d22f58dd6a0821ed5bfe1c316c6b63ef05265fe64b66ab35157f20c3ba8e43e`  
		Last Modified: Tue, 25 Feb 2025 11:53:19 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:78d6cd95b92641059eebe01424debc782a5f0ec47efe6ac0450a506cf9f5ecb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6479902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95dfbe0ed3aa3d0ecbcc9a25925fa8276a45dba3afedd984829442fd8a177808`

```dockerfile
```

-	Layers:
	-	`sha256:a47e5dfa36b2144b9df035f38c7bebb431ce338a4104c338f174f2f347569ee3`  
		Last Modified: Tue, 25 Feb 2025 11:53:19 GMT  
		Size: 6.5 MB (6458204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02b6bd45c3b022ea461044e34842729febc90a790fbb9d721877a57974358c3b`  
		Last Modified: Tue, 25 Feb 2025 11:53:18 GMT  
		Size: 21.7 KB (21698 bytes)  
		MIME: application/vnd.in-toto+json
