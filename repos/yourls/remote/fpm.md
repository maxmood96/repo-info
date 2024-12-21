## `yourls:fpm`

```console
$ docker pull yourls@sha256:d0640200e5bb96c9f789f424abffa5eb9fbc86c2550388a16e247ed4a03cf8a3
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `yourls:fpm` - linux; amd64

```console
$ docker pull yourls@sha256:59201e6cdbf6479a1094014a35a3227a9a7c29720b2e099b005659ef33589f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.4 MB (177447736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:630bd33c7f2e49170fce5487cde524e5c494296ebd4ee70dc76befa68fc5a107`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Apr 2024 21:17:33 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Apr 2024 21:17:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_VERSION=8.3.14
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.14.tar.xz.asc
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_SHA256=58b4cb9019bf70c0cbcdb814c7df79b9065059d14cf7dbf48d971f8e56ae9be7
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Apr 2024 21:17:33 GMT
WORKDIR /var/www/html
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Apr 2024 21:17:33 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
# ARGS: YOURLS_VERSION=1.9.2 YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ff6d89d3ef610dabc80f67546410c15d38e6c2e1c1b0c17e0bc9e723e73d9ef`  
		Last Modified: Tue, 03 Dec 2024 02:26:29 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f58c81aa650daba34415db72a2f7cf6806ca5c74df88746067ceaf4d7b734748`  
		Last Modified: Tue, 03 Dec 2024 02:26:32 GMT  
		Size: 104.2 MB (104150839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3939fcc93e45b0dfa23ab0cdd22a085bbcd10a850050c9835912dbeb47380ac6`  
		Last Modified: Tue, 03 Dec 2024 02:26:29 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d32ab61a2356a4b3569e1e9ac371ea80174c6a4998a7316f1f6ed5bbad4245`  
		Last Modified: Tue, 03 Dec 2024 02:26:30 GMT  
		Size: 12.6 MB (12629175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbb62ad600013e86e34b48d6b176b14265f2e274df07f12f9d7059a507920c7`  
		Last Modified: Tue, 03 Dec 2024 02:26:30 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27581b1affb6abf5a03956188fa9a903e4f7e4cedd7edb287cf6d43e31a11890`  
		Last Modified: Tue, 03 Dec 2024 02:26:31 GMT  
		Size: 27.8 MB (27818936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f4e845f2c4077e85902bf744a24f47c39beb0a4faa1f5350d29533df0724d7`  
		Last Modified: Tue, 03 Dec 2024 02:26:31 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7dcb2e06bbb9166c99b97e91ccbbbbc25bc1e96b5fd098344dada524dfdf7b9`  
		Last Modified: Tue, 03 Dec 2024 02:26:31 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fa982dd078a98ef2305c001b0eb6ad99a0c5133ba02a6978038a9284dbfb8f7`  
		Last Modified: Tue, 03 Dec 2024 02:26:32 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7210ce057d36082bdf58379d7b5f62e28df1e6bcc7b71f2d82d363a4052fd49`  
		Last Modified: Tue, 03 Dec 2024 03:17:23 GMT  
		Size: 526.9 KB (526948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143275a988e9c77020ac41aa53ef99ecdf6cc2394daca0f74cfd5cc8d5a4d6ad`  
		Last Modified: Tue, 03 Dec 2024 03:17:23 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ed2b831d8d2305c3dc4e534de95913b6f8594c9fb9a07d15fb72d8f60fc8e7`  
		Last Modified: Tue, 03 Dec 2024 03:17:23 GMT  
		Size: 4.1 MB (4073352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de23283b7290521f281e4fc46e45d4302fea843fa87d54890600563dda69d573`  
		Last Modified: Tue, 03 Dec 2024 03:17:23 GMT  
		Size: 2.0 KB (2049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ee704c6a8805be019f43d0d70a92b43c1ea10ac22bcfe28618715437a7abbd`  
		Last Modified: Tue, 03 Dec 2024 03:17:23 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:7a53c90451ef5c1015c91dd3307ba4220d23c04773993a1b1c05d9473034b8df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00faed5d86c8433a0277f01d52d8d5687b1e8361ef466e733eff4f5339ee5616`

```dockerfile
```

-	Layers:
	-	`sha256:8530b5e7b9653f38ec00cba882739373bed32bec3556cb81852eeaf9e471f28e`  
		Last Modified: Tue, 03 Dec 2024 03:17:22 GMT  
		Size: 26.4 KB (26449 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:fpm` - linux; arm variant v5

```console
$ docker pull yourls@sha256:1a52226182dbc3cf9c0df2f46bde3064afd99933f256846623287edc038e0403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.7 MB (150733563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a08d19b26c508f8fff664aa725524c672cc7bae16277a9a4ba35e39e99557dbb`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Apr 2024 21:17:33 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1733097600'
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Apr 2024 21:17:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_VERSION=8.3.15
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Apr 2024 21:17:33 GMT
WORKDIR /var/www/html
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Apr 2024 21:17:33 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
# ARGS: YOURLS_VERSION=1.9.2 YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:25d432086d20067bebfff2b163f22d49e7da8528782652615fe170bf8c39194d`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 25.8 MB (25754926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f38f689bfc81a80b77922476ec5fa4c66c3c95c18a88e0d5c163e4f88a3fa2`  
		Last Modified: Tue, 03 Dec 2024 02:47:24 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1391778530ecd6fb67099da1af9389d8c5e85a5bf4eda9154dc075982c5d03aa`  
		Last Modified: Tue, 03 Dec 2024 02:47:27 GMT  
		Size: 81.8 MB (81799353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1730374a8da7a42b29a8cb7308121c86932f17cf03f72bcbc1157654eab662c6`  
		Last Modified: Tue, 03 Dec 2024 02:47:24 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eaca6726ab4da45bb6f4571b0e1d65a67789b34f3c2aa35614411cec846f61a`  
		Last Modified: Fri, 20 Dec 2024 22:00:01 GMT  
		Size: 12.6 MB (12632571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1062d92037c52f50cf24a42680b3a97554a7be4224f5fc9b2eca72c2aaf8647d`  
		Last Modified: Fri, 20 Dec 2024 22:00:00 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc0786a87ef8802abcdd6ec069cd6e7b727f49f4cb10fce6d0132795c735108`  
		Last Modified: Fri, 20 Dec 2024 22:10:28 GMT  
		Size: 26.3 MB (26302102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ffc3e212e180560d108fb58f3121afbbdd57c7dd0c52afab6efec3fda63ff5`  
		Last Modified: Fri, 20 Dec 2024 22:10:27 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0660354018f19446100dda186ad119f9c264cd3ec2763ed5d750254f1bfcd802`  
		Last Modified: Fri, 20 Dec 2024 22:10:27 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f509a786825e26e6dd998534090321669aa93432dd8affdb7786fa63b1799ea3`  
		Last Modified: Fri, 20 Dec 2024 22:10:27 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca8f4fe717e967ccee4b3ddd20d9af5fdc01d52bf99ae8bc5a23306ecc691e9`  
		Last Modified: Fri, 20 Dec 2024 22:50:47 GMT  
		Size: 154.3 KB (154331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52261c99c2e1c5e936739acdf5eb8cb960d429ae70d02a5efa50bcba8e024156`  
		Last Modified: Fri, 20 Dec 2024 22:50:47 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf93b7919d7458e5e96967cf031ee7ff3bd741cc61be2bfd8d45fc3d8f4c7f33`  
		Last Modified: Fri, 20 Dec 2024 22:50:48 GMT  
		Size: 4.1 MB (4073352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1459029b496d6fc2933bc6d1c3975a026ae384cb843365d860fd17464ad82671`  
		Last Modified: Fri, 20 Dec 2024 22:50:47 GMT  
		Size: 2.0 KB (2050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a67422e61b4996409ce4afbd59e45c020147df84115df24abf062fefd281eed`  
		Last Modified: Fri, 20 Dec 2024 22:50:48 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:922c9e46ce89d99715b2026d7c04d5c265e03983b3b0864a41ca764a829ecd3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:679af0f3adca9c80513e4962846167cca5436678a741c4e515178bb826327e41`

```dockerfile
```

-	Layers:
	-	`sha256:10c3b0088d3568fbffe5f1fa781b4a09ca27c18c279e2d186bb3a7b8de842e91`  
		Last Modified: Fri, 20 Dec 2024 22:50:47 GMT  
		Size: 26.5 KB (26547 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:fpm` - linux; arm variant v7

```console
$ docker pull yourls@sha256:68bcdcdb5facf283466a25f8d77d21c0bbd8d15c1720958486109cb28957ee62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142167761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7d7f1c22c0ed6cc69370780b791b7ca20da8cd5696d9cac917310513173e4a7`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Apr 2024 21:17:33 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Apr 2024 21:17:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_VERSION=8.3.14
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.14.tar.xz.asc
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_SHA256=58b4cb9019bf70c0cbcdb814c7df79b9065059d14cf7dbf48d971f8e56ae9be7
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Apr 2024 21:17:33 GMT
WORKDIR /var/www/html
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Apr 2024 21:17:33 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
# ARGS: YOURLS_VERSION=1.9.2 YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:80b4fb4796cece09f69103235c60ffd0226a78c400a2953144b84c17de4df93d`  
		Last Modified: Tue, 03 Dec 2024 01:28:14 GMT  
		Size: 23.9 MB (23933588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc399a814abef0b215a25083103b4fcd6382c3040364b6565271bfaad3edcda`  
		Last Modified: Tue, 03 Dec 2024 02:45:44 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c111bef206c9990ed304a2c9e0dbc3e87552d4023cb73e5796908ce98c5a16`  
		Last Modified: Tue, 03 Dec 2024 02:45:47 GMT  
		Size: 76.0 MB (75969214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c345ebeb8ac614dcc4ff559e2cf2d693ff887d5cb958080625dc4d803abd018`  
		Last Modified: Tue, 03 Dec 2024 02:45:44 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ce390eb1d991785d3b488edc9aef2959bafb29bc022d6fb7107a9ff39dce42`  
		Last Modified: Tue, 03 Dec 2024 03:14:03 GMT  
		Size: 12.6 MB (12627555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4401073c044e6cb5c7f491839adf3752ef28ddf2460f73e2c697d998b4b862`  
		Last Modified: Tue, 03 Dec 2024 03:14:02 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5391fcdeb55cb3bc1cd6b106556e7515a0b8c802c87a0aafb449bea8102fd5be`  
		Last Modified: Tue, 03 Dec 2024 03:21:15 GMT  
		Size: 25.4 MB (25405525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea45ecd86ba99d12e3508a2c36eece9d1227e50c73a8765875e74a0c5a5fa866`  
		Last Modified: Tue, 03 Dec 2024 03:21:14 GMT  
		Size: 2.4 KB (2444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:055f9146098d2b284955ff9e9d92465f967785f1338129c3ecb8153e4d7f1f7d`  
		Last Modified: Tue, 03 Dec 2024 03:21:14 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681e51ae040e45ee24ee8cc79b8af56ea2c258ca11c60b4a66b035870ed9a999`  
		Last Modified: Tue, 03 Dec 2024 03:21:14 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eda5b8597fa02a8890a5d7caf337c555fa220d22738ffbe3edc7417d357e708`  
		Last Modified: Tue, 03 Dec 2024 17:14:58 GMT  
		Size: 141.6 KB (141613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24e440d951f94bcb8fd2126d11d34917c1c8947f78a69d3ccbf1ec4fe829f9e8`  
		Last Modified: Tue, 03 Dec 2024 17:14:58 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035ca34fd1b1047cbabe1c89519f8f0f8a07cb7b0d61661c3b3b80c31c2e55ad`  
		Last Modified: Tue, 03 Dec 2024 17:14:59 GMT  
		Size: 4.1 MB (4073362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dbd80629f443c74120bd5efedb2293e621666bef201a89bb163c69b6ec348b4`  
		Last Modified: Tue, 03 Dec 2024 17:14:58 GMT  
		Size: 2.1 KB (2051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4e727b04492a78b493ac161487ef1d47f9aa4511183f0af054def7b71aae5a`  
		Last Modified: Tue, 03 Dec 2024 17:14:59 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:43f05f0fb726ea26a8712aaf580ee6a3ff50c734da1bdf845a28510f3082c4b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46bc8e00d1d68b9f29cfb3af51d20a7dd00c83c27cb1fef33fd597a334817783`

```dockerfile
```

-	Layers:
	-	`sha256:cbc6d2f19843d90cb41d0988bd5fdb587340db672121ac8de25845e6e401bac4`  
		Last Modified: Tue, 03 Dec 2024 17:14:58 GMT  
		Size: 26.5 KB (26547 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:fpm` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:83266f6f523101d28a15df657b76400438a08bba62342c5c9cab923a2ea941fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.3 MB (171270188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce2f0e6fb3749ab26b3b0700ec00a98a01ee0377fdb071237e55efec84364d6c`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Apr 2024 21:17:33 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Apr 2024 21:17:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_VERSION=8.3.14
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.14.tar.xz.asc
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_SHA256=58b4cb9019bf70c0cbcdb814c7df79b9065059d14cf7dbf48d971f8e56ae9be7
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Apr 2024 21:17:33 GMT
WORKDIR /var/www/html
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Apr 2024 21:17:33 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
# ARGS: YOURLS_VERSION=1.9.2 YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:593b3b5e04c8b4e6110fb0e212055b9c7eb2aaa1cf8779fd681a2462f67111a8`  
		Last Modified: Tue, 03 Dec 2024 03:01:07 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc980920c054a940b9793a107341acd51b059aed873177ef237579d941f23ef`  
		Last Modified: Tue, 03 Dec 2024 03:01:11 GMT  
		Size: 97.9 MB (97936346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7130ec09764042703bb02f30348dab7ba0380d619963d04ab8ccc9678ca27470`  
		Last Modified: Tue, 03 Dec 2024 03:01:07 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14310aa309f408c03e58fedaf8744d3c2bba275fd52ed2d0356b6114113cf33f`  
		Last Modified: Tue, 03 Dec 2024 03:28:08 GMT  
		Size: 12.6 MB (12629089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b28bbb22eee1dcfe2b4467fc7f036eea805bc9d1d2fef18d22a6858d835453a`  
		Last Modified: Tue, 03 Dec 2024 03:28:06 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a612276995dd3f644935560ee3fabc5365d84dabaeb1f9ea06680ea307f1278a`  
		Last Modified: Tue, 03 Dec 2024 03:36:13 GMT  
		Size: 27.8 MB (27761327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20daf96a200a3b13203849382df4251b9880912a43cd562f34854cdc7a9eda92`  
		Last Modified: Tue, 03 Dec 2024 03:36:12 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04aea36c241d748664b15094addb188af06a236ee15cd153eab59b0a600f97d0`  
		Last Modified: Tue, 03 Dec 2024 03:36:12 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffff34a87b006c3ad9e95dcfa008d85875be28a4842117898f0024b35076289b`  
		Last Modified: Tue, 03 Dec 2024 03:36:12 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a6606a398e55ec5ddec0f8ef3d8d80c3412c9d53dd68cbec2994bf4f1c10ff3`  
		Last Modified: Tue, 03 Dec 2024 11:47:10 GMT  
		Size: 794.4 KB (794359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8570fe517feda67ff07f0aa294ed9ea4191229c3e5ffe9285b1358aaa8d25cb`  
		Last Modified: Tue, 03 Dec 2024 11:47:10 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230d8da86cd0990adc7d8fdc713ca44151132f87420e11b4c89d31966a45ead1`  
		Last Modified: Tue, 03 Dec 2024 11:47:10 GMT  
		Size: 4.1 MB (4073352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131ce2a72cc5d245d28b08f2b294e28d2e9203a82ed63bc31b791f15d942c8c8`  
		Last Modified: Tue, 03 Dec 2024 11:47:10 GMT  
		Size: 2.0 KB (2047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719baee1d1f5ac23e33b20ed393e704879d49788ef01481bfc68bd80e71c0f58`  
		Last Modified: Tue, 03 Dec 2024 11:47:11 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:da487770a70f1b0dd112bba9f187fc46a54dee980c6d4b2d7c48a8d2b1941974
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc43b2b114520310c1a82890655d30b96d9f3f5395bad7ff3de82455be7335f3`

```dockerfile
```

-	Layers:
	-	`sha256:27d814b82c7e53e5dd1f2a74dcf1877beddb2e5be9600f9f544f9d789b2a0a11`  
		Last Modified: Tue, 03 Dec 2024 11:47:09 GMT  
		Size: 26.6 KB (26579 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:fpm` - linux; 386

```console
$ docker pull yourls@sha256:1cb5d94706f03e49a8f3c612d847543a465e429073be83ef4cf438e542bf7efd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176087395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be2acc1a8180c7256a37fea1e76cb4c78557318f7404b2f08f7be26fc6c13cd2`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Apr 2024 21:17:33 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Apr 2024 21:17:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_VERSION=8.3.15
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.15.tar.xz.asc
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_SHA256=3df5d45637283f759eef8fc3ce03de829ded3e200c3da278936a684955d2f94f
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Apr 2024 21:17:33 GMT
WORKDIR /var/www/html
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Apr 2024 21:17:33 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
# ARGS: YOURLS_VERSION=1.9.2 YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b44713b9c3a4cd90f9143d8434f4ab863e0c4e2ce4c2b3064a132346fc7b0b`  
		Last Modified: Fri, 20 Dec 2024 21:34:34 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ce40d92aa6d76210640f1299db60d4dd445f0e1b11338632ac03c913f511fb`  
		Last Modified: Fri, 20 Dec 2024 21:35:19 GMT  
		Size: 101.3 MB (101319764 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041a02ce159eda1845178d6c6932587e1e6c87f26edac5aa2934267143b407ee`  
		Last Modified: Fri, 20 Dec 2024 21:34:34 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefd85e45ef8fcfba7f51b6e1dc1f889cbab954858500605c17b945e3765b4d3`  
		Last Modified: Fri, 20 Dec 2024 21:35:17 GMT  
		Size: 12.6 MB (12633469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af08658c6cbad6b6b8d0b20bb7b78b8d5c85ac7e5997a044f2df865c57072b90`  
		Last Modified: Fri, 20 Dec 2024 21:35:17 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7190e27e2e3233ce5054f5e5e564d3b1be8ed116e6ab4b0d5f1324aa18a73b4`  
		Last Modified: Fri, 20 Dec 2024 21:35:18 GMT  
		Size: 28.3 MB (28331443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:994f64c475a2cf26293f52aa6c04febb3c5ef773712c09441ed5a8ce534ca7b1`  
		Last Modified: Fri, 20 Dec 2024 21:35:17 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4039c6f50ad8700d3668e2d70a90b2e0406ca1ddccaa121ab1a1f96039e61e`  
		Last Modified: Fri, 20 Dec 2024 21:35:18 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a939c1487473fa46963f0d13ed73d4fabbee803f6fde77775d0e34752d4c902`  
		Last Modified: Fri, 20 Dec 2024 21:35:18 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1c6a63a480d80c71c69209a1e44321e8763f72ef6a126f80e46f5caada8c06`  
		Last Modified: Fri, 20 Dec 2024 22:31:05 GMT  
		Size: 507.0 KB (506952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09c1efa2a06a5fab30f18104ced11b83faa23c30efb3be010e505c7edb7da71`  
		Last Modified: Fri, 20 Dec 2024 22:31:05 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0cc5f2e7d69ef95e0437109c4419d0ec983271b4b3c7c836a374965bb714b0`  
		Last Modified: Fri, 20 Dec 2024 22:31:06 GMT  
		Size: 4.1 MB (4073358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b61d089f2ae5bc6395f18f4681bd6de64a6b59ed7675c74608c73bd5f9ce3b3`  
		Last Modified: Fri, 20 Dec 2024 22:31:05 GMT  
		Size: 2.0 KB (2050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b720b57c46fd24f8789d6f2f7626986dbc252b2a58283cb8d9e543682e5daf3`  
		Last Modified: Fri, 20 Dec 2024 22:31:06 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:f05308902858df111f479a7aa06dfbfcec4c24569caf1710ecadc0ebebabc855
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceedeae52be612102a5d7a84fc0d33e90d687f8dd05e68869c430fb79b0e4b63`

```dockerfile
```

-	Layers:
	-	`sha256:d22c15729dfa4697494d55f770ce24cea2875e53cf4395cbe3c6bc0fa15080f4`  
		Last Modified: Fri, 20 Dec 2024 22:31:05 GMT  
		Size: 26.4 KB (26415 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:fpm` - linux; mips64le

```console
$ docker pull yourls@sha256:e90ac96a11179f21e5589944b96f1224c5f7bee770f3e368dc1e08ef3d05195f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.8 MB (152759952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:421b149dfcce7a09b6215a3fdc1a9671052e22fd986a12e5bab0b2018dab0fc2`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Apr 2024 21:17:33 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1733097600'
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Apr 2024 21:17:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_VERSION=8.3.14
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.14.tar.xz.asc
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_SHA256=58b4cb9019bf70c0cbcdb814c7df79b9065059d14cf7dbf48d971f8e56ae9be7
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Apr 2024 21:17:33 GMT
WORKDIR /var/www/html
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Apr 2024 21:17:33 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
# ARGS: YOURLS_VERSION=1.9.2 YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:29ac4ae2849b0c84c0ef17659082268617abeb406402ef46b6fa9140e6d2064d`  
		Last Modified: Tue, 03 Dec 2024 01:28:15 GMT  
		Size: 28.5 MB (28505909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697b6f869e689f1f7935effcea7aef7505ad04025b0311ff3937b9103eef46fd`  
		Last Modified: Tue, 03 Dec 2024 04:22:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72b7f48524d255d2a114c61e2dea94f3576d2144432398eb626ed6bbb8da968d`  
		Last Modified: Tue, 03 Dec 2024 04:22:41 GMT  
		Size: 80.5 MB (80475126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7c3c34315ea9a93e65cc52bfdaf45d8f691045833035294baddeaa21df2439`  
		Last Modified: Tue, 03 Dec 2024 04:22:33 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cabe061a747ba3889f46b477245f159c783b67149ec1713b8cb349b6c8b70b78`  
		Last Modified: Tue, 03 Dec 2024 05:35:40 GMT  
		Size: 12.6 MB (12627286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40de77d6d506af5d9e347b5f8dc6f2d63e31cc5275e3cb688a398ab9c5e54003`  
		Last Modified: Tue, 03 Dec 2024 05:34:14 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db367d9d99dd78a368d6b87504b5fcc998cd56f26f1554a30168d757df52afe`  
		Last Modified: Tue, 03 Dec 2024 06:10:55 GMT  
		Size: 26.9 MB (26908391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aa6ee0bb97bc9cc50780440fc6e6471b208b0c5fcb74b8bbb026bbc6b2d603b`  
		Last Modified: Tue, 03 Dec 2024 06:10:52 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78231d3057287d8cca5ff9794bc2cca8a551e87bc13ec6ca2972d388bdb9c0e`  
		Last Modified: Tue, 03 Dec 2024 06:10:52 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd23532f4765aecd45eae0f4f805f316eaa14186bf7e6cfdb04e11f830e517ee`  
		Last Modified: Tue, 03 Dec 2024 06:10:52 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea03442e1d4c241e298566b678c48b275e1e8f0277142b9aa136f4c3ee6a4072`  
		Last Modified: Tue, 03 Dec 2024 23:19:24 GMT  
		Size: 153.0 KB (152967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b4c9ae6e1274b0873ea0a6b72e7b6b5afc9c75bfeda90d9eeb12b12d879b44`  
		Last Modified: Tue, 03 Dec 2024 23:19:24 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3fd2a55ec33fb25d79aea2ee6afb0272cbd2125b329d77768c8c260fd6ece4`  
		Last Modified: Tue, 03 Dec 2024 23:19:25 GMT  
		Size: 4.1 MB (4073352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626d73565b87950adcbc700b7f027a6785d313d233aae8875a5328afcc3a5585`  
		Last Modified: Tue, 03 Dec 2024 23:19:24 GMT  
		Size: 2.1 KB (2053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51dcdfc32449b0a4b45b5585fce8eebad8a91ce8f538823fa609a7ee51532035`  
		Last Modified: Tue, 03 Dec 2024 23:19:25 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:14d85bddcbfbc17da7b8972a027ed77a5dd2b8ec70706bba77dce5e40ee5f8ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89511d541c6b0d88050848b4f087648852f6a025c14a50f8d5b5b70f07a76969`

```dockerfile
```

-	Layers:
	-	`sha256:88e479cd600ae79e6b03fb04a25fb45134bb31b840959433e27eb742d537672c`  
		Last Modified: Tue, 03 Dec 2024 23:19:23 GMT  
		Size: 26.5 KB (26517 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:fpm` - linux; ppc64le

```console
$ docker pull yourls@sha256:738dc99cfb3f2aceccb078af216b2544278cfd1164213b4466d9d407966cac4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.0 MB (180977497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f2f47cc059215e8d8dcf8ab2e68179bd8cc59f542e39060cf03274f666f88c0`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Apr 2024 21:17:33 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Apr 2024 21:17:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_VERSION=8.3.14
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.14.tar.xz.asc
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_SHA256=58b4cb9019bf70c0cbcdb814c7df79b9065059d14cf7dbf48d971f8e56ae9be7
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Apr 2024 21:17:33 GMT
WORKDIR /var/www/html
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Apr 2024 21:17:33 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
# ARGS: YOURLS_VERSION=1.9.2 YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:e62b6946337cc6b72ec307008f1acc46e12a4f98e6f0e29c92b5538bbafd7ce6`  
		Last Modified: Tue, 03 Dec 2024 01:28:28 GMT  
		Size: 32.1 MB (32063265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dfd0832c6742842354605a68e1c37e01805dbd8dcb42bed521f3b5ffc9d6782`  
		Last Modified: Tue, 03 Dec 2024 03:01:38 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f8241edc102752205916990cef5c543934549ef471e4363e3f37b4d609359e`  
		Last Modified: Tue, 03 Dec 2024 03:01:42 GMT  
		Size: 103.1 MB (103128469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fe6a6422bc6eb2d0ecc0d78cfc1ccb6571b1ef03bf7b17f2384e77abef0c849`  
		Last Modified: Tue, 03 Dec 2024 03:01:38 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e1ab9e7e88301fc7c6ddfe49d65e6a71a83e20084b7b7bfe8bf3ed8711c02d3`  
		Last Modified: Tue, 03 Dec 2024 03:18:19 GMT  
		Size: 12.6 MB (12628806 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc32f346956291bbd935f441b41f0187b29c9deafecc66c48a23a53e3d1e2ad3`  
		Last Modified: Tue, 03 Dec 2024 03:18:18 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84c9f9e609eda4a36751cd44608141ece29d7db3743defaf5a1ada29eb4b2ba1`  
		Last Modified: Tue, 03 Dec 2024 03:27:02 GMT  
		Size: 28.9 MB (28878030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878a9f60b91797c0207e664f29f91a8ae4427183133f401bc5a61a2da5e7d988`  
		Last Modified: Tue, 03 Dec 2024 03:27:01 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac86af376c10889c4214d85942fa5a2bffa239441101a147f6cd6afa92bf6d4`  
		Last Modified: Tue, 03 Dec 2024 03:27:01 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09d6cccf1ecc5da7f7c355057744fd9e0877f5b6cb881c7f918a625dd9386ecc`  
		Last Modified: Tue, 03 Dec 2024 03:27:02 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13c9c50de0415de38bcecdce0dc34b678ce827e20de5b49854051aed71f370f`  
		Last Modified: Tue, 03 Dec 2024 09:40:25 GMT  
		Size: 188.7 KB (188657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8db7074a1748500558f0f8f9cd5e3bf8a1eb432644d6a8dfe56e76de5b043a54`  
		Last Modified: Tue, 03 Dec 2024 09:40:25 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a76738f0ccca77a17566a5e0b3749c2b4dea0bd82314737e7a4efc38a383f50`  
		Last Modified: Tue, 03 Dec 2024 09:40:26 GMT  
		Size: 4.1 MB (4073352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee34a19d5d3f9bde9a3fce7b7c354ef2c10185de60be3cdd456dfdc6a962b530`  
		Last Modified: Tue, 03 Dec 2024 09:40:25 GMT  
		Size: 2.0 KB (2050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112999a457fb8e6e6a841061bc94a0358f798ce4f32eba2fe04a84938ad42bdf`  
		Last Modified: Tue, 03 Dec 2024 09:40:26 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:beeb38a6f060e07e0b650e13f620dec90f80c927cbdb486654d29634a490744b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 KB (26498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03f85c58c52e09920bce355d63ce6cc9d66ef44ee43c92ebd21600424860aea9`

```dockerfile
```

-	Layers:
	-	`sha256:58be799e0ddc39e3643eef393cc3bd03b3071babcb905c163d496e04007fc974`  
		Last Modified: Tue, 03 Dec 2024 09:40:25 GMT  
		Size: 26.5 KB (26498 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:fpm` - linux; s390x

```console
$ docker pull yourls@sha256:8408951a4c2e2d586c89b36c669c78b2766f0b55bc45478072f7c1e2c13c1034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.3 MB (151302733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea23bf5620e0f16823bf4f9c8983dee35ed8de0d85db499e5f8f8222858505f7`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 18 Apr 2024 21:17:33 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 18 Apr 2024 21:17:33 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_VERSION=8.3.14
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.14.tar.xz.asc
# Thu, 18 Apr 2024 21:17:33 GMT
ENV PHP_SHA256=58b4cb9019bf70c0cbcdb814c7df79b9065059d14cf7dbf48d971f8e56ae9be7
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 18 Apr 2024 21:17:33 GMT
WORKDIR /var/www/html
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Apr 2024 21:17:33 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
# Thu, 18 Apr 2024 21:17:33 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ARG YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_VERSION=1.9.2
# Thu, 18 Apr 2024 21:17:33 GMT
ENV YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
# Thu, 18 Apr 2024 21:17:33 GMT
# ARGS: YOURLS_VERSION=1.9.2 YOURLS_SHA256=62a95ba766d62f3305d75944cbfe12d5a90c08c88fbf2f6e67150d36412b916f
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Apr 2024 21:17:33 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Thu, 18 Apr 2024 21:17:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9378ae44108012049addde60d193467e2b15a247b2f953ad5c27e073c4573d42`  
		Last Modified: Tue, 03 Dec 2024 01:28:18 GMT  
		Size: 26.9 MB (26878971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ff6d88ca75be60fd842318e38796161d90dc699ddefddb72e584661cafccbb5`  
		Last Modified: Tue, 03 Dec 2024 02:45:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12c1972b1cde205ce78e000379a6f103cc814e05cf048628db71370f4268b574`  
		Last Modified: Tue, 03 Dec 2024 02:45:10 GMT  
		Size: 80.6 MB (80624347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0df81e218837c9a0821f00169675df65b6dc92a07a5e60fb03eb1b30c73673`  
		Last Modified: Tue, 03 Dec 2024 02:45:09 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef556b18811311a80ab408553db09e1199e056d60a480d98855c056195b00223`  
		Last Modified: Tue, 03 Dec 2024 03:00:17 GMT  
		Size: 12.6 MB (12627988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d93b5ab4eb34ce3986ef55e1d77e95ba006883dcbe7ae1dadd1d5974bcf73ac`  
		Last Modified: Tue, 03 Dec 2024 03:00:16 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f5a3f975a48bc26ae180f395f08f8d89ec98675c0828692109973f802cc987`  
		Last Modified: Tue, 03 Dec 2024 03:07:27 GMT  
		Size: 26.9 MB (26919223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c4a552dc81bb6a7b3180d6f2fde3d91fcfbebfb5b20554ee9da9c3e3fc129ad`  
		Last Modified: Tue, 03 Dec 2024 03:07:27 GMT  
		Size: 2.4 KB (2443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4557106133e7ab5f1e8c4517fcd8d0a044a908862b29c1252f43e87c0407f81`  
		Last Modified: Tue, 03 Dec 2024 03:07:27 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c97889081d43397f12f13a3545db710dc6d4aece8cc688f4b3556392eb90c5`  
		Last Modified: Tue, 03 Dec 2024 03:07:27 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7cff2ccca28ab28e0045d82b2d24b3760821da77d7cb1ff563dd65e5c5f78be`  
		Last Modified: Tue, 03 Dec 2024 07:52:33 GMT  
		Size: 161.9 KB (161950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00473aa6b792efdda4ae0642ff2bf41650c508f551648c528cfa00dee112e449`  
		Last Modified: Tue, 03 Dec 2024 07:52:33 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3e7189221e28843f69776868539ee181807c16000460bbfb8bf268b50d18d33`  
		Last Modified: Tue, 03 Dec 2024 07:52:34 GMT  
		Size: 4.1 MB (4073352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397580055fda18dc50a482cb38ca13176b46a64db66ddf021a103ba2b59d9b35`  
		Last Modified: Tue, 03 Dec 2024 07:52:33 GMT  
		Size: 2.0 KB (2047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59cec573e785e0e6591d0613effc544990d5d3663c235c61a0711be7691832cb`  
		Last Modified: Tue, 03 Dec 2024 07:52:34 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:50adcaaaa4dd937090b8a1bda749ee1dc15512c88a7669dc1a4446f09b089380
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 KB (26445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cbec6a75ae21cf23e5fb8692eedd8d46040b105b02eca98fd033f0f8de39212`

```dockerfile
```

-	Layers:
	-	`sha256:733f749a854d897de565d985653f0a927647ef00a9efe2b7fde1c58e7fb329a1`  
		Last Modified: Tue, 03 Dec 2024 07:52:33 GMT  
		Size: 26.4 KB (26445 bytes)  
		MIME: application/vnd.in-toto+json
