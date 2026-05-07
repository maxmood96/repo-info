## `matomo:fpm`

```console
$ docker pull matomo@sha256:f4320fd1657d1918fa32da640541ba583aea8760742a9ee9e0745e8ab1220855
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

### `matomo:fpm` - linux; amd64

```console
$ docker pull matomo@sha256:6737761dc532c7ac20279422487ced081294ef4383cb0becc0f73dd3b7b249b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.0 MB (198989292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3bd6bbe5ef55fde59e8a8efc1d15516b1d94495de506076133e7cd58a01ce7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Thu, 07 May 2026 16:39:52 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 07 May 2026 16:40:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 07 May 2026 16:40:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 07 May 2026 16:40:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 07 May 2026 16:40:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 07 May 2026 16:40:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:40:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:40:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 07 May 2026 16:40:09 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 07 May 2026 16:40:09 GMT
ENV PHP_VERSION=8.4.21
# Thu, 07 May 2026 16:40:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.21.tar.xz.asc
# Thu, 07 May 2026 16:40:09 GMT
ENV PHP_SHA256=7cf5d8ab12c3b2016875bcfaec71bef1ef0b07bed6148f2c447577074431f984
# Thu, 07 May 2026 16:40:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 07 May 2026 16:40:18 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:42:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 07 May 2026 16:42:41 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:42:41 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 07 May 2026 16:42:41 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 07 May 2026 16:42:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 May 2026 16:42:41 GMT
WORKDIR /var/www/html
# Thu, 07 May 2026 16:42:41 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 07 May 2026 16:42:41 GMT
STOPSIGNAL SIGQUIT
# Thu, 07 May 2026 16:42:41 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 07 May 2026 16:42:41 GMT
CMD ["php-fpm"]
# Thu, 07 May 2026 17:26:56 GMT
ENV PHP_MEMORY_LIMIT=256M
# Thu, 07 May 2026 17:26:56 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Thu, 07 May 2026 17:26:56 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 07 May 2026 17:26:56 GMT
ENV MATOMO_VERSION=5.10.0
# Thu, 07 May 2026 17:27:05 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Thu, 07 May 2026 17:27:05 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Thu, 07 May 2026 17:27:05 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 May 2026 17:27:05 GMT
VOLUME [/var/www/html]
# Thu, 07 May 2026 17:27:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 May 2026 17:27:05 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9436a18512c6a6fd0fc6da80fdc77fd6f6c2c031f4548c942fb4ef80ec7d462`  
		Last Modified: Thu, 07 May 2026 16:43:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8614c6a26345cec0d1eff1da4322794681eb2ec8821b7d60941e509d67039f16`  
		Last Modified: Thu, 07 May 2026 16:43:04 GMT  
		Size: 117.8 MB (117842191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a910d204a1d384d1f9e51eb93097899cd62386298304efee6ec716535c784edb`  
		Last Modified: Thu, 07 May 2026 16:43:00 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b75df37e18881ab50a8874a6f8388207cb4581c93bd6cbe3ab86ddbaf7e594c`  
		Last Modified: Thu, 07 May 2026 16:43:02 GMT  
		Size: 13.9 MB (13866436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b32ff8f299874574891b870eab85e772912f00ed34363281a37747fa8a53c270`  
		Last Modified: Thu, 07 May 2026 16:43:02 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d66fcac55c3cab87788dcad115ab5ca0c47fe13f3ba6d8b2ae88d427a8d89ba`  
		Last Modified: Thu, 07 May 2026 16:43:03 GMT  
		Size: 13.8 MB (13802221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88e7f4bdabf6fd10b633d256cbab09311edf48e809179b22501eaa20929d8ea`  
		Last Modified: Thu, 07 May 2026 16:43:03 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9043b01834233b96d87c8b191d16784a60ec2282939a754f5358d0aa3534880f`  
		Last Modified: Thu, 07 May 2026 16:43:03 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a422ab7b6ffa91dcce5b8e6d50d2edb8f18ae7b67d83e9c5d69a4b9e55851a7`  
		Last Modified: Thu, 07 May 2026 16:43:04 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a17d792a063dc4df86310d9cce154ca70fe2bc6bb567f479413d3a478ee13c`  
		Last Modified: Thu, 07 May 2026 16:43:05 GMT  
		Size: 9.3 KB (9270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1944036f6b54245366d83370b5b9c37ea7c15e3f0b689389aeb95b6eda2b598`  
		Last Modified: Thu, 07 May 2026 17:27:12 GMT  
		Size: 2.7 MB (2694057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f6e8ebe1a55c3e67939a62fd7e7e8d433766e60dbe242c8dc97d931e146cb1`  
		Last Modified: Thu, 07 May 2026 17:27:12 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe974ccad20099d3c680ba026f89864123ca5c16b43ece093b2707047ba2b052`  
		Last Modified: Thu, 07 May 2026 17:27:13 GMT  
		Size: 21.0 MB (20989532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b43b44c557d115a265c6cb1f048df69b5cd920d9bd39e8089c80499e0eac5ee`  
		Last Modified: Thu, 07 May 2026 17:27:12 GMT  
		Size: 340.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01f95bc75f0265a90d626f74e2b7d8935e5a7b2d48d1da31bd56560e20fca31a`  
		Last Modified: Thu, 07 May 2026 17:27:13 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:a638935da33dbf236da5f32758bc492c1861260e1825bba700b005bc06d9f152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 KB (33253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4b0330a91e7b3bb1fe5916306f241875d16a2d4027bd52f060ce82f72027932`

```dockerfile
```

-	Layers:
	-	`sha256:25f7c9b885827fbe53c756cca00cd4001fa60a9329627806cdd2f7713bd635c3`  
		Last Modified: Thu, 07 May 2026 17:27:12 GMT  
		Size: 33.3 KB (33253 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm` - linux; arm variant v5

```console
$ docker pull matomo@sha256:da3ead0a6ec8ae8c5d2a87a79f5fd407f00b8352fcc4e5b70e533ca88c09e83d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **172.5 MB (172536365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c3aed0218b9fd42596476f587773342d74587025dda22380b3edd4bc88baa11`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Thu, 07 May 2026 16:39:11 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 07 May 2026 16:39:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 07 May 2026 16:39:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 07 May 2026 16:39:34 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 07 May 2026 16:39:34 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 07 May 2026 16:39:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:39:34 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:39:34 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 07 May 2026 16:39:34 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 07 May 2026 16:39:34 GMT
ENV PHP_VERSION=8.4.21
# Thu, 07 May 2026 16:39:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.21.tar.xz.asc
# Thu, 07 May 2026 16:39:34 GMT
ENV PHP_SHA256=7cf5d8ab12c3b2016875bcfaec71bef1ef0b07bed6148f2c447577074431f984
# Thu, 07 May 2026 16:39:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 07 May 2026 16:39:49 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:42:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 07 May 2026 16:42:49 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:42:49 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 07 May 2026 16:42:49 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 07 May 2026 16:42:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 May 2026 16:42:49 GMT
WORKDIR /var/www/html
# Thu, 07 May 2026 16:42:50 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 07 May 2026 16:42:50 GMT
STOPSIGNAL SIGQUIT
# Thu, 07 May 2026 16:42:50 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 07 May 2026 16:42:50 GMT
CMD ["php-fpm"]
# Thu, 07 May 2026 17:24:38 GMT
ENV PHP_MEMORY_LIMIT=256M
# Thu, 07 May 2026 17:24:38 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Thu, 07 May 2026 17:24:38 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 07 May 2026 17:24:38 GMT
ENV MATOMO_VERSION=5.10.0
# Thu, 07 May 2026 17:24:56 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Thu, 07 May 2026 17:24:56 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Thu, 07 May 2026 17:24:56 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 May 2026 17:24:56 GMT
VOLUME [/var/www/html]
# Thu, 07 May 2026 17:24:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 May 2026 17:24:56 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6496d93bca0663211b9252da346044ecb734ee5b3ecaae5b1fbd230753faee2f`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 27.9 MB (27948180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8efa6b9478dc96b9a15913adf086bcb01d590eb2364575124c6894946827b67a`  
		Last Modified: Thu, 07 May 2026 16:43:08 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6747d2e9493ddcc601b6e06e67d2a29d12e76706a9e8e515ce1c2da256f767ff`  
		Last Modified: Thu, 07 May 2026 16:43:11 GMT  
		Size: 94.9 MB (94885428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:745ffb91096a1a8fffe98a0d4a838c4b94328219bc5575f91436b21150b3b427`  
		Last Modified: Thu, 07 May 2026 16:43:08 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1768739544b8cb2e4ce692d5681d9cf2ca8151f36849c4c098c3fa4ebccd0617`  
		Last Modified: Thu, 07 May 2026 16:43:09 GMT  
		Size: 13.9 MB (13863918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22954dfcfc48e6f3f83b95f9d47f2136506765b7e6ea05dd0da227d33dd093fb`  
		Last Modified: Thu, 07 May 2026 16:43:09 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5822ebd6a829586800905ad922617d59f5aaf614e05643ef535d08d6f2adc6`  
		Last Modified: Thu, 07 May 2026 16:43:10 GMT  
		Size: 12.3 MB (12319509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41df6208d0ae72c202453daa0fd375b5d2ed1fca75b31a84df0d8ded02e26764`  
		Last Modified: Thu, 07 May 2026 16:43:10 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57c3cc5f775a6bd1515c0bff03473a4a6fdd9c34c90e26bc872085bf1cdee6a`  
		Last Modified: Thu, 07 May 2026 16:43:11 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42741e7912312289512ffee4ba9c19a8a9910cc98f9d3d18e43b9b0c37d1a75a`  
		Last Modified: Thu, 07 May 2026 16:43:11 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:924f65e2396571854ca63db72d0d7c5bbfca081800d463a0b47eecf049591875`  
		Last Modified: Thu, 07 May 2026 16:43:12 GMT  
		Size: 9.3 KB (9267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baf584b66663843d9a54cfcab563131ad8bea95b9fd6d011746dbca324c523f5`  
		Last Modified: Thu, 07 May 2026 17:25:03 GMT  
		Size: 2.5 MB (2517328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aecfc9dab9290dd7816434190312addc1c140c98b8515aaab21bc7c1b3d326d`  
		Last Modified: Thu, 07 May 2026 17:25:03 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be9b11cd43e2feb4ea3e1c5a0c6a1d3dff88f628973e7e85093c2dcf1537965`  
		Last Modified: Thu, 07 May 2026 17:25:03 GMT  
		Size: 21.0 MB (20987331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a7299912ebfa553463b27a486af3abb90b3810b4df063d0c59fd6acea25c7e`  
		Last Modified: Thu, 07 May 2026 17:25:03 GMT  
		Size: 341.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51e1de064df378721597f06cfd96d1a6cda8e2347013e19e290f20a45619e3a1`  
		Last Modified: Thu, 07 May 2026 17:25:04 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:84213c835a194a66a7036458f3b8e722d01afd8c5bff0f7a4e0e2924ba3b8611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 KB (33353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3ef171c4d67ff54d7a1746064f9230776878af60347da288bce2f7f34bb12b6`

```dockerfile
```

-	Layers:
	-	`sha256:049997804c481b603089cf612ed24e3e4484bbe0cb9a8ee09707aa454bc507f7`  
		Last Modified: Thu, 07 May 2026 17:25:03 GMT  
		Size: 33.4 KB (33353 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm` - linux; arm variant v7

```console
$ docker pull matomo@sha256:ee52b0bd5890e431a1bdc8637fd7bbb60fadc954411faadc996e5ed2b9625766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.4 MB (161382004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06b2dffd64bbe53f5dedd155c0e01daa0eb1f3c3746883f95c45389fb23b4a4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Thu, 07 May 2026 16:39:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 07 May 2026 16:39:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 07 May 2026 16:39:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 07 May 2026 16:39:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 07 May 2026 16:39:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 07 May 2026 16:39:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:39:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:39:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 07 May 2026 16:39:59 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 07 May 2026 16:39:59 GMT
ENV PHP_VERSION=8.4.21
# Thu, 07 May 2026 16:39:59 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.21.tar.xz.asc
# Thu, 07 May 2026 16:39:59 GMT
ENV PHP_SHA256=7cf5d8ab12c3b2016875bcfaec71bef1ef0b07bed6148f2c447577074431f984
# Thu, 07 May 2026 16:40:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 07 May 2026 16:40:11 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:42:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 07 May 2026 16:42:55 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:42:55 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 07 May 2026 16:42:55 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 07 May 2026 16:42:55 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 May 2026 16:42:55 GMT
WORKDIR /var/www/html
# Thu, 07 May 2026 16:42:55 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 07 May 2026 16:42:55 GMT
STOPSIGNAL SIGQUIT
# Thu, 07 May 2026 16:42:55 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 07 May 2026 16:42:55 GMT
CMD ["php-fpm"]
# Thu, 07 May 2026 17:50:24 GMT
ENV PHP_MEMORY_LIMIT=256M
# Thu, 07 May 2026 17:50:24 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Thu, 07 May 2026 17:50:24 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 07 May 2026 17:50:24 GMT
ENV MATOMO_VERSION=5.10.0
# Thu, 07 May 2026 17:50:39 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Thu, 07 May 2026 17:50:39 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Thu, 07 May 2026 17:50:39 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 May 2026 17:50:39 GMT
VOLUME [/var/www/html]
# Thu, 07 May 2026 17:50:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 May 2026 17:50:39 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638b71c49869eacd22db7cad8170788031d3d8264843ea937213b410609d0e7a`  
		Last Modified: Thu, 07 May 2026 16:43:12 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea2fdbc5e846ee9c4bfafb4fd523658a01a5a504cdc760599263a0bb381810bf`  
		Last Modified: Thu, 07 May 2026 16:43:15 GMT  
		Size: 86.3 MB (86250405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e849c6f137131434523a0e680fad24b2410a1f51655557c3af155901b19f4d5`  
		Last Modified: Thu, 07 May 2026 16:43:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d61e5e89d6b1e85cbcaf3dd2314fa4f8d83cc2d48e8d52461bd819c12543e8cf`  
		Last Modified: Thu, 07 May 2026 16:43:13 GMT  
		Size: 13.9 MB (13864081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2249ec38afc83745737b58aa998f99e27901f23223186acef9872b8bd875b550`  
		Last Modified: Thu, 07 May 2026 16:43:13 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9766ca579bdb017d5847a6c5e6127687755ffdfbeb75b18d32da75fc97c43c91`  
		Last Modified: Thu, 07 May 2026 16:43:14 GMT  
		Size: 11.7 MB (11650662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d847e406190da7480def88b7df12ffea8bc488650d9b05681c3f2ce560c50970`  
		Last Modified: Thu, 07 May 2026 16:43:14 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f3159dfa44c30d2dec259462152314dcff2d8c6176abfc5eb2085202b41340`  
		Last Modified: Thu, 07 May 2026 16:43:14 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf3d42e974861fffdecc378bd43009be9fe6590ca0054368fc03189e1b4170e`  
		Last Modified: Thu, 07 May 2026 16:43:15 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e757feb1e12f32b311ba2bc9ae41b97ec4673bbdae25da6542492f3ef7194a1c`  
		Last Modified: Thu, 07 May 2026 16:43:16 GMT  
		Size: 9.3 KB (9269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ebbe05d47f28584747fd98b8dc4c35ad376a7a6ce80bd587836d6da48888bf`  
		Last Modified: Thu, 07 May 2026 17:50:46 GMT  
		Size: 2.4 MB (2399817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be46e27763ad4f5b93434576108219f994b6d5805f742b0ca6fc0449df562a7c`  
		Last Modified: Thu, 07 May 2026 17:50:46 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169019fa3303e9d0834b9be9537ccd7d9dd3c93231143a5a6cd11dccd887205a`  
		Last Modified: Thu, 07 May 2026 17:50:46 GMT  
		Size: 21.0 MB (20987516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125e21053cf6be3c3fd97f63f43a1a0474a3c832e1952e7547f0517f892dc209`  
		Last Modified: Thu, 07 May 2026 17:50:46 GMT  
		Size: 344.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ab904a54ca880760ffea88c6cda2403a0bce47f9eb724fb592034e80da03fb`  
		Last Modified: Thu, 07 May 2026 17:50:47 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:0f89d1bf0fa07174367150f49fedf8c3a3fbf06c811134ae7d4ca8edb30caf44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 KB (33353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:726d9d86ed339f75364fb9947acd01f55682a8a9da9e2081d986f7c352e3c78c`

```dockerfile
```

-	Layers:
	-	`sha256:4bdc2d2af13e49b20409da85a7b2c71f0bca441d4ed66b1a59e062492f186455`  
		Last Modified: Thu, 07 May 2026 17:50:45 GMT  
		Size: 33.4 KB (33353 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm` - linux; arm64 variant v8

```console
$ docker pull matomo@sha256:d4e7a7b5b8d4133ecc239b771904bb53bc67170c2aab9aded829ea69fac43ea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.3 MB (191319832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96b63b368263e0688fae7416458490e0aea6ba9aeeba98399f48e4a720361a03`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Thu, 07 May 2026 16:39:48 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 07 May 2026 16:40:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 07 May 2026 16:40:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 07 May 2026 16:40:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 07 May 2026 16:40:06 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 07 May 2026 16:40:06 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:40:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:40:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 07 May 2026 16:40:06 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 07 May 2026 16:40:06 GMT
ENV PHP_VERSION=8.4.21
# Thu, 07 May 2026 16:40:06 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.21.tar.xz.asc
# Thu, 07 May 2026 16:40:06 GMT
ENV PHP_SHA256=7cf5d8ab12c3b2016875bcfaec71bef1ef0b07bed6148f2c447577074431f984
# Thu, 07 May 2026 16:40:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 07 May 2026 16:40:15 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:43:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 07 May 2026 16:43:11 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:43:11 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 07 May 2026 16:43:11 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 07 May 2026 16:43:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 May 2026 16:43:11 GMT
WORKDIR /var/www/html
# Thu, 07 May 2026 16:43:11 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 07 May 2026 16:43:11 GMT
STOPSIGNAL SIGQUIT
# Thu, 07 May 2026 16:43:11 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 07 May 2026 16:43:11 GMT
CMD ["php-fpm"]
# Thu, 07 May 2026 17:30:38 GMT
ENV PHP_MEMORY_LIMIT=256M
# Thu, 07 May 2026 17:30:38 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Thu, 07 May 2026 17:30:38 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 07 May 2026 17:30:38 GMT
ENV MATOMO_VERSION=5.10.0
# Thu, 07 May 2026 17:30:49 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Thu, 07 May 2026 17:30:49 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Thu, 07 May 2026 17:30:49 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 May 2026 17:30:49 GMT
VOLUME [/var/www/html]
# Thu, 07 May 2026 17:30:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 May 2026 17:30:49 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d878bc5af8601feb571fc58cab6ad77212a7b1339fe2918213d512aa498e6826`  
		Last Modified: Thu, 07 May 2026 16:43:18 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2178a14224b82e3b35fa173c2b621d5c1465065481eb3114945c606ebfe50a69`  
		Last Modified: Thu, 07 May 2026 16:43:35 GMT  
		Size: 110.2 MB (110165493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb592e455b0d45d48fd63fd53f3ffee161306b3204dd56177af518be68380c6`  
		Last Modified: Thu, 07 May 2026 16:43:31 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a35c53b315a424df74a420f5a6bd5db713531aee868dc0a8b1e7868da99ba52`  
		Last Modified: Thu, 07 May 2026 16:43:33 GMT  
		Size: 13.9 MB (13865945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d3c36f87f09864c3dc99abfcf8fe67ef506c7394479f1c53352a85f21018487`  
		Last Modified: Thu, 07 May 2026 16:43:33 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f29652391c2a094a6781e7fd849ca0f0f54f9e9fbdf1b986974e2c3293d3ec`  
		Last Modified: Thu, 07 May 2026 16:43:33 GMT  
		Size: 13.5 MB (13465566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:625b6c63072d32afecd25bd8603fd8f244beffd3f4039c60d99740918df5412a`  
		Last Modified: Thu, 07 May 2026 16:43:34 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f5b2a324a9119bb6cf7c4eb86173e14ebae5934b8defb2cf0f935399efd58f`  
		Last Modified: Thu, 07 May 2026 16:43:35 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae802c4128d0b6ef6de5b396dc9bd9d62bb1015dfc33987eca9791345bc8a68a`  
		Last Modified: Thu, 07 May 2026 16:43:35 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce124849f314cd7b4d765c30a6b2d9965df2f69ae9bf304e41d174558305ca33`  
		Last Modified: Thu, 07 May 2026 16:43:35 GMT  
		Size: 9.3 KB (9265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a52323fea6237f1bd392837f7208eee39416753820addc9ff15dea9657b81ea2`  
		Last Modified: Thu, 07 May 2026 17:30:56 GMT  
		Size: 2.7 MB (2675113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8b96501f0c7d5390a0d92cc15f66d826e54988145544114b872b3a476d22b70`  
		Last Modified: Thu, 07 May 2026 17:30:56 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96f6abd483e785e03bc8737cf96dc8cec7ad19dc3b0a6390a0c34dc1f681790`  
		Last Modified: Thu, 07 May 2026 17:30:57 GMT  
		Size: 21.0 MB (20989440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77550235f3768fc6253090e0cfdbd93425fa1724b48f8d7e8bdd04782fa45eeb`  
		Last Modified: Thu, 07 May 2026 17:30:56 GMT  
		Size: 342.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a70bc66217765c9d8e22761a6062d0156bf174eb4e6900a100e9b8239382eb2`  
		Last Modified: Thu, 07 May 2026 17:30:57 GMT  
		Size: 823.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:e929e55fddf2da435f38e34157347461eb1e8da1cdcb50bc1318437e8fe065fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.4 KB (33386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f974a8b0a737e2f44bab37c5429e3fa28f688b6dbe6cf8b6cff6a9c39775e983`

```dockerfile
```

-	Layers:
	-	`sha256:eb62851ca7c6eb0ec927d76eeefd8459eea5a22a9fe934a66603e6badaed7b90`  
		Last Modified: Thu, 07 May 2026 17:30:56 GMT  
		Size: 33.4 KB (33386 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm` - linux; 386

```console
$ docker pull matomo@sha256:df19373c7a7380c1330364430a8860dd4173f77ae5ef685ac846204e07c3b766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.1 MB (199084321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2feecb99ff0814bf441e855e3a636176d1c35b6f37975e7943d6d9e96b8cd950`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Thu, 07 May 2026 16:39:29 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 07 May 2026 16:39:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 07 May 2026 16:39:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Thu, 07 May 2026 16:39:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 07 May 2026 16:39:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 07 May 2026 16:39:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:39:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 07 May 2026 16:39:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 07 May 2026 16:39:48 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 07 May 2026 16:39:48 GMT
ENV PHP_VERSION=8.4.21
# Thu, 07 May 2026 16:39:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.21.tar.xz.asc
# Thu, 07 May 2026 16:39:48 GMT
ENV PHP_SHA256=7cf5d8ab12c3b2016875bcfaec71bef1ef0b07bed6148f2c447577074431f984
# Thu, 07 May 2026 16:39:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 07 May 2026 16:39:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:43:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 07 May 2026 16:43:01 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 07 May 2026 16:43:01 GMT
RUN docker-php-ext-enable opcache # buildkit
# Thu, 07 May 2026 16:43:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 07 May 2026 16:43:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 07 May 2026 16:43:01 GMT
WORKDIR /var/www/html
# Thu, 07 May 2026 16:43:01 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 07 May 2026 16:43:01 GMT
STOPSIGNAL SIGQUIT
# Thu, 07 May 2026 16:43:01 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 07 May 2026 16:43:01 GMT
CMD ["php-fpm"]
# Thu, 07 May 2026 17:28:33 GMT
ENV PHP_MEMORY_LIMIT=256M
# Thu, 07 May 2026 17:28:33 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Thu, 07 May 2026 17:28:33 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 07 May 2026 17:28:33 GMT
ENV MATOMO_VERSION=5.10.0
# Thu, 07 May 2026 17:28:46 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Thu, 07 May 2026 17:28:46 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Thu, 07 May 2026 17:28:46 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Thu, 07 May 2026 17:28:46 GMT
VOLUME [/var/www/html]
# Thu, 07 May 2026 17:28:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 May 2026 17:28:46 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4189244079fc70665b568828523a214a8c83049e752a4c76fed5ee13355f9fb0`  
		Last Modified: Thu, 07 May 2026 16:43:21 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b03709c56d4cb0ce0036df4dd0f68952877823f479769f13a2ce9f640eef400`  
		Last Modified: Thu, 07 May 2026 16:43:25 GMT  
		Size: 116.1 MB (116144157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff41f9dc707f4d283cfbc207de4144321956be829beebb55c39d629b619c560a`  
		Last Modified: Thu, 07 May 2026 16:43:22 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:541566b9aa033d2ed3edebbb63b07fb616bab3de8c616047aa0a09649e2136d9`  
		Last Modified: Thu, 07 May 2026 16:43:22 GMT  
		Size: 13.9 MB (13865376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4797eb41ac391a66fad16b894e831343113effb72b1a4d4969e3efe46882baff`  
		Last Modified: Thu, 07 May 2026 16:43:23 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bdde4f9b2e382575cae2c918ded517e36aeb4007da4a05daf6aefe06f526dbc`  
		Last Modified: Thu, 07 May 2026 16:43:24 GMT  
		Size: 14.1 MB (14103798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549a98b1be2c1c134ef0b60665df2cd15bb90a813b02a35ebb5fea6acdb04a1e`  
		Last Modified: Thu, 07 May 2026 16:43:24 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfe2c74e6a29a02d7154f8054ac8a7cae8626ae887e71f30e93f37a8eeac0edc`  
		Last Modified: Thu, 07 May 2026 16:43:24 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e7d9f24635ea789c34079e1c98c7e962868d68d5f4470d1de06bda091644fe`  
		Last Modified: Thu, 07 May 2026 16:43:25 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca21df16c8a8f39410e2d3bd1c3b8e4cb406850c228fcdbb9c67086e0635f87`  
		Last Modified: Thu, 07 May 2026 16:43:25 GMT  
		Size: 9.3 KB (9266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b7efb59ffce9860fbb64104748e50da76bf1e0c9056584c7c4399aa34bc7854`  
		Last Modified: Thu, 07 May 2026 17:28:54 GMT  
		Size: 2.7 MB (2671199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d2ec1b24fc5323df52776ad97a5d730b837efa2de52e7770b8898571f425fa`  
		Last Modified: Thu, 07 May 2026 17:28:53 GMT  
		Size: 323.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aedbe468fa1c86f96279a39970abfe38950556e1a77b6014cd64b87d31a67be`  
		Last Modified: Thu, 07 May 2026 17:28:54 GMT  
		Size: 21.0 MB (20988808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab2dd3df1cf6161e73e6b227c93e14ad3a78e33eb8d1142f1bdbb344c962a81`  
		Last Modified: Thu, 07 May 2026 17:28:53 GMT  
		Size: 337.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1db98eafc2a2a81d2eac43d55ac8fcbe3a9ddaf9eeeae6c777219909cbd5b84`  
		Last Modified: Thu, 07 May 2026 17:28:54 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:e0be6a3ac65fdc1d4a0b0a436c38aeb1e67b956eb0f0d1a727d0c1c9e10be6e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 KB (33217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58093b0665037d7edc9f4b9c171ab1b759db8311a518d7754f2c3ad7d8750e8a`

```dockerfile
```

-	Layers:
	-	`sha256:a561704622be63afd71b2fca4aa3864dacddf1c9343083180cfd8eb5746912c1`  
		Last Modified: Thu, 07 May 2026 17:28:53 GMT  
		Size: 33.2 KB (33217 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm` - linux; ppc64le

```console
$ docker pull matomo@sha256:bb257670b361087a6c9d4d5ada5f3b7c22eb978f86293e67e777cfb1c30496e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.2 MB (195202072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0413e9d9de7b62cc76fa8df012be95f03e10cfc005e46f11e7e9b0c92aaf1f89`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:53:38 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:54:50 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:54:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:54:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:54:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:54:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:54:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:54:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:54:51 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:54:51 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:54:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:54:51 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 02:19:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 02:19:21 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:28:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 02:28:59 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:28:59 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 02:29:00 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 02:29:00 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 02:29:00 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 02:29:01 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 22 Apr 2026 02:29:01 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 Apr 2026 02:29:01 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 22 Apr 2026 02:29:01 GMT
CMD ["php-fpm"]
# Mon, 04 May 2026 21:18:44 GMT
ENV PHP_MEMORY_LIMIT=256M
# Mon, 04 May 2026 21:18:44 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Mon, 04 May 2026 21:18:45 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 04 May 2026 21:18:45 GMT
ENV MATOMO_VERSION=5.10.0
# Mon, 04 May 2026 21:19:17 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Mon, 04 May 2026 21:19:17 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Mon, 04 May 2026 21:19:18 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 21:19:18 GMT
VOLUME [/var/www/html]
# Mon, 04 May 2026 21:19:18 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 21:19:18 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec9edacdb8f24d449ea1be53da1f3932bc82a28fd406dd1c8475cd2914e5241`  
		Last Modified: Wed, 22 Apr 2026 01:59:54 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b71f6d43ed1a8d00b3f34912982730d421bfd59fc7192b9463baff89769b29b0`  
		Last Modified: Wed, 22 Apr 2026 01:59:58 GMT  
		Size: 109.6 MB (109599283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673e750ff637e0d2354924e824bffee749521f15eda887d7ff34983e1c535855`  
		Last Modified: Wed, 22 Apr 2026 01:59:54 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054b5847d95feef86743cbd49c633eb60f2ff5fe302e71093f49fbd2320e1d58`  
		Last Modified: Wed, 22 Apr 2026 02:24:03 GMT  
		Size: 13.8 MB (13833103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b8e5fda2efc50218998dd81d724b6628613051cf19a1910551da522c682a78`  
		Last Modified: Wed, 22 Apr 2026 02:24:02 GMT  
		Size: 485.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:982b00cc68c3293e74b57069ebee18bfb120fd36d88dbfebbf2b9a65911fa379`  
		Last Modified: Wed, 22 Apr 2026 02:29:21 GMT  
		Size: 14.2 MB (14216593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4c4a379ef2f399d72ca01f374eaa921c02a69167826bb2c3e0829d8906fac45`  
		Last Modified: Wed, 22 Apr 2026 02:29:21 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e895ecc092a768d556e7735d4ad08f7b02d9251191e053d07a267350128f47`  
		Last Modified: Wed, 22 Apr 2026 02:29:21 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3916d2e474ef6e91c9eebef2373811cf9ef128ca7891f0cdb6e790747598f41`  
		Last Modified: Wed, 22 Apr 2026 02:29:21 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f1fed36adf60cc812d5d5ac75e5173f419b3ee00d8175c70fe1248910c1870`  
		Last Modified: Wed, 22 Apr 2026 02:29:22 GMT  
		Size: 9.3 KB (9268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32abc89e964585b0d48e8ca3f099a2f5e07003658f617f5d0eef2bd54c776cba`  
		Last Modified: Mon, 04 May 2026 21:19:37 GMT  
		Size: 3.0 MB (2950825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915a02c412a8ecf700c9a1eddd0305da270d215ef0d0bc75942df8ef22898fe9`  
		Last Modified: Mon, 04 May 2026 21:19:37 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbeabc205d7250273bdca6f144fefc7a371bc13270d7541aa134e26c16fb17f0`  
		Last Modified: Mon, 04 May 2026 21:19:37 GMT  
		Size: 21.0 MB (20989552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3499e6b3fb87eb105dc5d8699e2c6030eb4f72c65ac23c6c607642c76916527d`  
		Last Modified: Mon, 04 May 2026 21:19:37 GMT  
		Size: 344.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf2707e903e4fef9f9e457ed9e290138fc251672e0ab049fae79ab76bf24e86`  
		Last Modified: Mon, 04 May 2026 21:19:38 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:41acff07b89fbda995113c218f83e3e2c26774fd65d379337917b2c69c52c3e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 KB (33301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c86e27b2328b5ae143951bf9de23726bd7c9b1924025b23aaf138fdc291d6c`

```dockerfile
```

-	Layers:
	-	`sha256:4327068b35482e817be1ee7b6c3c9740af59f88bf41dde0b7d0079f5efd71ffd`  
		Last Modified: Mon, 04 May 2026 21:19:36 GMT  
		Size: 33.3 KB (33301 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm` - linux; riscv64

```console
$ docker pull matomo@sha256:bae924da097eb4c86fa570bc415f1bd8b880e35d5100de90e7411dfcad56c770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.4 MB (225438956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:328ca10a4fde4ed180d66f7bce89edf18673521cc5a93bb43685633ffbc4bb7f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 14:28:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 14:30:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 14:30:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 14:30:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 14:30:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 14:30:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 14:30:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 14:30:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 14:30:22 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 14:30:22 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 14:30:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 14:30:22 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 18:38:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 18:38:27 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 21:29:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 21:29:33 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 21:29:34 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 21:29:34 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 21:29:34 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 21:29:34 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 21:29:35 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 22 Apr 2026 21:29:35 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 Apr 2026 21:29:35 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 22 Apr 2026 21:29:35 GMT
CMD ["php-fpm"]
# Mon, 04 May 2026 21:26:09 GMT
ENV PHP_MEMORY_LIMIT=256M
# Mon, 04 May 2026 21:26:09 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Mon, 04 May 2026 21:26:09 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 04 May 2026 21:26:09 GMT
ENV MATOMO_VERSION=5.10.0
# Mon, 04 May 2026 21:27:33 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Mon, 04 May 2026 21:27:34 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Mon, 04 May 2026 21:27:34 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 21:27:34 GMT
VOLUME [/var/www/html]
# Mon, 04 May 2026 21:27:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 21:27:34 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48840fceecc8e73012b670476b1f8c5f728f434774a763b7cc1269fce314564f`  
		Last Modified: Wed, 22 Apr 2026 15:33:18 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ac60e5404292aec444c5e71111c9196ffd4f75603b3203d43ed8034e0ec9a6c`  
		Last Modified: Wed, 22 Apr 2026 15:33:49 GMT  
		Size: 146.6 MB (146578956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56f266893967c3439d4e5dced7f7d20ba4b866ef794fb589fc2b6f367491933e`  
		Last Modified: Wed, 22 Apr 2026 15:33:18 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784ce129d3aae6536b28ac471ccda0c98087bfe7735be55d347ae25a9d780f80`  
		Last Modified: Wed, 22 Apr 2026 19:35:09 GMT  
		Size: 13.8 MB (13840277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ef03df3a749d52c9af83343d03fb3f7cd625870519c5130aa9f9d48a7cb788`  
		Last Modified: Wed, 22 Apr 2026 19:35:04 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de80aa7749ec88062d0380364de2d9ff07037200bc522f7b9c61d049bbe87f08`  
		Last Modified: Wed, 22 Apr 2026 21:32:34 GMT  
		Size: 13.1 MB (13145305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20b80d37a0dfb6c0e335a84dcfbf7e0340af84ed2b7982db03753effa68f3cc`  
		Last Modified: Wed, 22 Apr 2026 21:32:31 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8b54d66e3d7eb78596a18bcecc33b2e4006019d65a0ad0c5ad77fa2d53774e`  
		Last Modified: Wed, 22 Apr 2026 21:32:31 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a42b07bdb305ebd3c405f41dd7356ed149280f43c3fc4b6deeb81af9a563f281`  
		Last Modified: Wed, 22 Apr 2026 21:32:31 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4368f7dc0d3a123dcf82ca51c60d5bee947ac175795c75439829b82331ea8d44`  
		Last Modified: Wed, 22 Apr 2026 21:32:33 GMT  
		Size: 9.3 KB (9270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3133ed98578da62a03747b704d958443bfb66fbb11a001a73b893ef7c71ce26`  
		Last Modified: Mon, 04 May 2026 21:28:52 GMT  
		Size: 2.6 MB (2590431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08b72159f25aeaa7fde3075aa4b20c73202dce67870741a76dc5ba312cbcc15`  
		Last Modified: Mon, 04 May 2026 21:28:51 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86a195be3abc041470909928ddeeb902de49794c0a391fc985fe825f65207f04`  
		Last Modified: Mon, 04 May 2026 21:28:55 GMT  
		Size: 21.0 MB (20989106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848caf6eee25e84bb0a6790a576e177366d95b4d9e70c125d5c2262ed50474f7`  
		Last Modified: Mon, 04 May 2026 21:28:51 GMT  
		Size: 343.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681f86f3de0f8c528931cd88ad9e8eff156c0f870887687c2089505423be792c`  
		Last Modified: Mon, 04 May 2026 21:28:53 GMT  
		Size: 820.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:b7ce3b89128db4454225a472e48f29a428b982a505355660ca10b7ceefc8b21a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 KB (33301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb8b13d75b9e2c1cc72f27ce7d64915fd9c696176d94fca25658f321fbe86199`

```dockerfile
```

-	Layers:
	-	`sha256:30c34a039633c1aab67d95ba66b404390871029d58c3eb446b787dd589bdf893`  
		Last Modified: Mon, 04 May 2026 21:28:51 GMT  
		Size: 33.3 KB (33301 bytes)  
		MIME: application/vnd.in-toto+json

### `matomo:fpm` - linux; s390x

```console
$ docker pull matomo@sha256:6e7adc8978aed9a99fde615aec340e11213e0ed019d9a79770eca81854ee05d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.4 MB (173442137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf5dbbb6c0263d52c0b35d3370726bb055612cdd8029ce1ddd0d544eb0c2c30`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:22:01 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:22:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:22:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:22:21 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:22:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:22:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:22:21 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:22:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:22:21 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Wed, 22 Apr 2026 01:22:21 GMT
ENV PHP_VERSION=8.4.20
# Wed, 22 Apr 2026 01:22:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.20.tar.xz.asc
# Wed, 22 Apr 2026 01:22:21 GMT
ENV PHP_SHA256=e454c6f7c89a42f41ebb06dc5c3578e8c8b5f1a3f0da6675665affab04e221f7
# Wed, 22 Apr 2026 01:33:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:33:37 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:37:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:37:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:37:56 GMT
RUN docker-php-ext-enable opcache # buildkit
# Wed, 22 Apr 2026 01:37:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:37:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:37:56 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:37:56 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 22 Apr 2026 01:37:56 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 Apr 2026 01:37:56 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 22 Apr 2026 01:37:56 GMT
CMD ["php-fpm"]
# Mon, 04 May 2026 21:05:23 GMT
ENV PHP_MEMORY_LIMIT=256M
# Mon, 04 May 2026 21:05:23 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype-dev 		libjpeg-dev 		libldap2-dev 		libpng-dev 		libzip-dev 		procps 	; 		debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure gd --with-freetype --with-jpeg; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		gd 		bcmath 		ldap 		mysqli 		pdo_mysql 		zip 	; 		pecl install APCu-5.1.28; 	pecl install redis-6.3.0; 		docker-php-ext-enable 		apcu 		redis 	; 	rm -r /tmp/pear; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean # buildkit
# Mon, 04 May 2026 21:05:23 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=2'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 04 May 2026 21:05:23 GMT
ENV MATOMO_VERSION=5.10.0
# Mon, 04 May 2026 21:05:40 GMT
RUN set -ex; 	fetchDeps=" 		dirmngr 		gnupg 	"; 	apt-get update; 	apt-get install -y --no-install-recommends 		$fetchDeps 	; 		curl -fsSL -o matomo.tar.gz 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz"; 	curl -fsSL -o matomo.tar.gz.asc 		"https://builds.matomo.org/matomo-${MATOMO_VERSION}.tar.gz.asc"; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys F529A27008477483777FC23D63BB30D0E5D2C749; 	gpg --batch --verify matomo.tar.gz.asc matomo.tar.gz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" matomo.tar.gz.asc; 	tar -xzf matomo.tar.gz -C /usr/src/; 	rm matomo.tar.gz; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false $fetchDeps; 	apt-get dist-clean # buildkit
# Mon, 04 May 2026 21:05:40 GMT
COPY php.ini /usr/local/etc/php/conf.d/php-matomo.ini # buildkit
# Mon, 04 May 2026 21:05:41 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Mon, 04 May 2026 21:05:41 GMT
VOLUME [/var/www/html]
# Mon, 04 May 2026 21:05:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 04 May 2026 21:05:41 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757f702e0a9ae41a0668944dbb4c245387fe46a7b86e9158d6238a0a7a2e8d3b`  
		Last Modified: Wed, 22 Apr 2026 01:26:46 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c4485b6f62a7b6c400504342749f4784b13250b4a4923fa17548e35ec69126`  
		Last Modified: Wed, 22 Apr 2026 01:26:48 GMT  
		Size: 92.6 MB (92572845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f521371e2b81d32dcc512c19954776e0f6ba6f3e6d3ab464b138a9d29e2737a4`  
		Last Modified: Wed, 22 Apr 2026 01:26:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:895072f1915069db96de1e6cd2775cfc97d31d00723b0b58b689f76a62b114b4`  
		Last Modified: Wed, 22 Apr 2026 01:37:07 GMT  
		Size: 13.8 MB (13832213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382e06742a171f68cde5770d70c17567b9188ea34dedcf5227404e9cec8cb39c`  
		Last Modified: Wed, 22 Apr 2026 01:37:06 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:618e083a88d6c35da869cebae5f113b9d04739889d9759e66ea3a3ac03dbfd44`  
		Last Modified: Wed, 22 Apr 2026 01:38:14 GMT  
		Size: 13.5 MB (13462525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1f567e1ecc28a79a4def138b98f18610cdf8cbc4c52e98b56481eaae456cec`  
		Last Modified: Wed, 22 Apr 2026 01:38:14 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bc44b21c26e70bb61141c8e8efce2d9f0f970663295792c1e4aee3edd1056b`  
		Last Modified: Wed, 22 Apr 2026 01:38:14 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb3b2142ea31f473941f8b36e1138fb495ed25f97b049103d4bb8307d58dd432`  
		Last Modified: Wed, 22 Apr 2026 01:38:14 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02955ca59e915e77d99e4d867b1d53eabb24d3af4353fb49005525fc7de8a345`  
		Last Modified: Wed, 22 Apr 2026 01:38:15 GMT  
		Size: 9.3 KB (9265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f52786f1385a4f562f1d86d6b40c979c0f7e64a8a5647f02ad6f1d40cb069b1d`  
		Last Modified: Mon, 04 May 2026 21:05:52 GMT  
		Size: 2.7 MB (2731310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7efc05109dcf18ed21effe433d5c62ed34e5f19f7f976a86d16fc0cb3fa8d9ae`  
		Last Modified: Mon, 04 May 2026 21:05:52 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d34898edab7705d7e8e62638bbf533d51d27c16935d6587208a5b49cc48fade8`  
		Last Modified: Mon, 04 May 2026 21:05:52 GMT  
		Size: 21.0 MB (20988272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f2a9e32651b515b641c721e026bb4815fbb5af711a4293fa58fd260293e798`  
		Last Modified: Mon, 04 May 2026 21:05:52 GMT  
		Size: 343.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea3bedab59b7c4c370ddbce19f8ed01680a8fc8f4a0dfc2f083571a9dae32547`  
		Last Modified: Mon, 04 May 2026 21:05:53 GMT  
		Size: 824.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `matomo:fpm` - unknown; unknown

```console
$ docker pull matomo@sha256:c13c8385288357f3c0c838ba11e560b44063aeb3beab8c8d30846b5a87c58089
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 KB (33246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c09d83b2465d10c5f80c69a88892b497d4132a777b8364e71dd8ea2f78da79a`

```dockerfile
```

-	Layers:
	-	`sha256:a6bbacac4f012b40fd6285b145b86a79513d59b31e61fb571d87328526f1658e`  
		Last Modified: Mon, 04 May 2026 21:05:52 GMT  
		Size: 33.2 KB (33246 bytes)  
		MIME: application/vnd.in-toto+json
