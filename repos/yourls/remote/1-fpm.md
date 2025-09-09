## `yourls:1-fpm`

```console
$ docker pull yourls@sha256:3656f27c4a10aff5336d4c01ae285af0a857559ac3bfb0303373d18b18afbcf3
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

### `yourls:1-fpm` - linux; amd64

```console
$ docker pull yourls@sha256:19c38f346bf87fa50eb42c3f40ecdc48e654ecef5fe5e44135c1288554bfb334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182502581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cac6df31fe57b7af394693025a13bfd3be1d70c2e0dc65697dad3008b343f65e`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 19 Aug 2025 10:14:17 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
ENV PHP_VERSION=8.4.12
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
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
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f54bda37a0f3414da800aa09358db214706a9c41092cccd160ef85bd881cbd`  
		Last Modified: Mon, 08 Sep 2025 21:45:57 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82259e2cc78c6b7380ba09942db7af5255d8fa7f3da0059a61080325fa36653c`  
		Last Modified: Mon, 08 Sep 2025 21:46:05 GMT  
		Size: 117.8 MB (117835879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9193f06b445fe74131814fde6d3c7cb5a52eab17f173a9c9f20eb63b4a359e34`  
		Last Modified: Mon, 08 Sep 2025 21:45:55 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8c9225ef8a0bf2d67172537a54346a22cc4809acc5b7c139444a251206c41f9`  
		Last Modified: Mon, 08 Sep 2025 21:45:56 GMT  
		Size: 13.8 MB (13783972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6afc13381d01714452519ac7b7ef0b253c5430eb188185a859055c002db9af2b`  
		Last Modified: Mon, 08 Sep 2025 21:45:54 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a3488303e01f4139270dc55ccd4a469ca5df5a39fdaf143da0b793b7e70fe2`  
		Last Modified: Mon, 08 Sep 2025 21:45:57 GMT  
		Size: 14.3 MB (14346559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1da7985fc18c2eefcede4c373c00b3d0a81205f6be228fd11dae96678242aac3`  
		Last Modified: Mon, 08 Sep 2025 21:45:54 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bb60b8af5aad487cb92c5cc17f687d40be4b7933633cc220a4855eada8bc0eb`  
		Last Modified: Mon, 08 Sep 2025 21:45:53 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbfd55202c3ddb054ae394bc8f09b4104fe24014e87e3f65a11bcbfba211f5c`  
		Last Modified: Mon, 08 Sep 2025 21:45:53 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9650050d44dc7ecddabda2304815d9173cdf70953803643d8d031ad6b287e6c4`  
		Last Modified: Mon, 08 Sep 2025 21:45:53 GMT  
		Size: 9.2 KB (9197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20528644612c1ccda5910c02192fbe44d201e405e600e70e772f89981b21cc9`  
		Last Modified: Mon, 08 Sep 2025 22:16:47 GMT  
		Size: 671.8 KB (671808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aedbcc8dcf9272207c8c2ea9e837bbda4cee1cb478669ab0271e83f415c3dde`  
		Last Modified: Mon, 08 Sep 2025 22:16:50 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58bcd4e37254cd52319f3acd9971c8fcfaf4c671d4d25cdb9c634eb6d0e6afa1`  
		Last Modified: Mon, 08 Sep 2025 22:43:15 GMT  
		Size: 6.1 MB (6073643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b0ffe48353eb3a98f7ecb3a949c0d73090ac84c3231735e2dc01b838a36437`  
		Last Modified: Mon, 08 Sep 2025 22:16:53 GMT  
		Size: 2.1 KB (2092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a7ccfc653328ab666d51c6249c7e9134678d5d83bf68d3a7f4014e700a59c81`  
		Last Modified: Mon, 08 Sep 2025 22:16:56 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:f898e80444c448f4b0d9f69c7922ab03432387073918a457d1ac97279fdfe8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47ab8b1f17b7ddabd4895bb3ea8672bbf0f06b5ca07b7f2ddc4d62fcc808f158`

```dockerfile
```

-	Layers:
	-	`sha256:c1abc8b8501e0d4296f5615be2c4353b698f0c94fcf73d699d01ef7f6d4a6717`  
		Last Modified: Mon, 08 Sep 2025 22:42:45 GMT  
		Size: 27.5 KB (27524 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm` - linux; arm variant v5

```console
$ docker pull yourls@sha256:386eb82a53bbf63e42237c5fababf32fdd3dc59efc2bda6c195a683b5093ad36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.8 MB (155779830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f7d9f088aef84dff8d32716f2aeab97054a4946b03c75c09c4ac982d4c90b09`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 19 Aug 2025 10:14:17 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1757289600'
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
ENV PHP_VERSION=8.4.12
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
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
	-	`sha256:5d61fc20e756831552727f89a087e2b45b07dace604ad2cda0a2afa80ace388d`  
		Last Modified: Mon, 08 Sep 2025 21:13:29 GMT  
		Size: 27.9 MB (27941760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8956d940413107e8a587889282d89e7b056b270d4521a0fb94cd24b6b45cb9aa`  
		Last Modified: Mon, 08 Sep 2025 21:35:17 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54422b440865b387ae4ee5ebe83477e636240c0894f7885c2391dfc6a1d605ab`  
		Last Modified: Tue, 09 Sep 2025 00:02:29 GMT  
		Size: 94.9 MB (94872271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b5293bb11cae50ed59c799b4dd0ea0db2f1f717e070a56ccfd00bc4d87cee1`  
		Last Modified: Mon, 08 Sep 2025 21:35:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051baebb2b7d5391ca347707e9e0f24fd869bb7339f5ac724f9f64a200c44c1d`  
		Last Modified: Tue, 09 Sep 2025 00:02:32 GMT  
		Size: 13.8 MB (13781532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b7df078c62011cb3c0ea9d195c8327c0dca4fc7c68317583730f3ac9e7304d7`  
		Last Modified: Mon, 08 Sep 2025 21:35:23 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:575e7736797a10e20a001458febc60ff0e764668ed5f3b4662d71f4409bc5bf8`  
		Last Modified: Tue, 09 Sep 2025 00:02:34 GMT  
		Size: 12.9 MB (12918612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcae26b0724a9cd1db378dfdb7b574043357c761f4c196f735fba7e40514764b`  
		Last Modified: Mon, 08 Sep 2025 21:35:26 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0defe3bab8285766d7f3150451759934cd22d0f2ec8dfe43e051709a235ec9`  
		Last Modified: Mon, 08 Sep 2025 21:35:28 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc4e6507667159f68f0976883ff1bef2ec5b989327531ec3583e1b982c36b98`  
		Last Modified: Mon, 08 Sep 2025 21:35:32 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed00cb49697ab71c93d11a8bc6bac217f489d10bb2f8518529a37f970cd7ea3`  
		Last Modified: Mon, 08 Sep 2025 21:35:36 GMT  
		Size: 9.2 KB (9200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b28c5de0ec5540d25680f7f4743045306f58984b860b2552b328f60428251f`  
		Last Modified: Tue, 09 Sep 2025 02:10:27 GMT  
		Size: 174.8 KB (174777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ad2a1fb63a6f0b5a69e6f3996728405f2b6f57926196eaba60d8463c7b8afbf`  
		Last Modified: Tue, 09 Sep 2025 02:10:27 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:715fb86090fa4293394a39953965aadc2f1291996ce61013d51654e99f1f99f4`  
		Last Modified: Tue, 09 Sep 2025 02:21:18 GMT  
		Size: 6.1 MB (6073643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e68b0acd82a677a8beb8647af581e53ae88073f4c9bb67ec2c288367923df7`  
		Last Modified: Tue, 09 Sep 2025 02:10:27 GMT  
		Size: 2.1 KB (2095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f5c04823d440eee3aa9c7e802e3f27099370298378706509449e2fbf9d2f5a`  
		Last Modified: Tue, 09 Sep 2025 02:10:27 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:7b4908315d37ff1556cc5a9aca92db6459d3a50c0bd640275597de648b62c80e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 KB (27624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:733cfaf2d103b10288384c86fed9384752b94798cce8b2d78e9b4e29a6ad68ae`

```dockerfile
```

-	Layers:
	-	`sha256:717cb203bd9f11c57cb1cc4edf2407b244c8e7044f1db9ff8c2554adcaa5543c`  
		Last Modified: Tue, 09 Sep 2025 04:42:56 GMT  
		Size: 27.6 KB (27624 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm` - linux; arm variant v7

```console
$ docker pull yourls@sha256:5d8cf3ec64115f77b75d363b8acb13a3584724f56930ea733d9142b6bba842a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144736032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a790cabb80b66102e25bbf7940a9e5716c622d37142474dc3f2b030e8aa6ff97`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 19 Aug 2025 10:14:17 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
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
ENV PHP_VERSION=8.4.12
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
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
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170005e8e6b2785a58cdd86d5a05d68a9cc82b4d8846ed3f5456a9814275b203`  
		Last Modified: Mon, 08 Sep 2025 21:42:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:419eb2d7b1e735d456c74a84e6968a328f9ef7ca83b0a11e4e06114013863d43`  
		Last Modified: Tue, 09 Sep 2025 00:02:48 GMT  
		Size: 86.2 MB (86244716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e76699292edcf726849ca40ef1d4e203da4e9fe6b652bdfe326e2e916c7514`  
		Last Modified: Mon, 08 Sep 2025 21:42:58 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cd5e36b56e434746f82d914c5fcf6ccb75ab1064ece40ebf0902c3f04c026e8`  
		Last Modified: Tue, 09 Sep 2025 00:02:49 GMT  
		Size: 13.8 MB (13781633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3cfdff1a16c85f4a7634baa3e4cbfb7bb52624d5eee063d27dd64836af844d6`  
		Last Modified: Mon, 08 Sep 2025 21:43:03 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c686c9f7de12f4d5ca0e1df0619ee8568e909c16937e261650dd23838140017c`  
		Last Modified: Tue, 09 Sep 2025 00:02:52 GMT  
		Size: 12.2 MB (12249571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b35f80e4eaa7c5ec476e1144b9d562abb629a39ec3120dc560d6812ae6c7dc78`  
		Last Modified: Mon, 08 Sep 2025 21:43:07 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63be6006f58ba6c3e4147f460b80c2aa2efa395f6b83055e8c819b451e46e5ff`  
		Last Modified: Mon, 08 Sep 2025 21:43:10 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bb2f4961c54176b80f4bfa93d447265712ce48cbd2576ad9752f536e5f9cdf1`  
		Last Modified: Mon, 08 Sep 2025 21:43:14 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3b65579a3664bba24091a057d88213a92245d4bb02494e41741cf9804c32f9`  
		Last Modified: Mon, 08 Sep 2025 21:43:18 GMT  
		Size: 9.2 KB (9196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a1dd6e9bcba0ef4e4e5be8f080dc74bdb19e8b2895cd49cd52247b53e2e089`  
		Last Modified: Tue, 09 Sep 2025 04:11:41 GMT  
		Size: 161.4 KB (161398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6cdabcc30cc016217fba61a0debed740afbecd615f89622567576c26dde8932`  
		Last Modified: Tue, 09 Sep 2025 04:11:46 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d789e1a602b597b11f7e03c4bd02dc954dd7b20ee891ce63b801b9244e26e497`  
		Last Modified: Tue, 09 Sep 2025 04:43:02 GMT  
		Size: 6.1 MB (6073643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96c046cf857bcb9376a93423222185d8188a928fdc1f54478db4aa45207b7bc3`  
		Last Modified: Tue, 09 Sep 2025 04:11:41 GMT  
		Size: 2.1 KB (2095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:671148db2b48e7f862e2047e658a244b1126165b7f407af617bb89a8d6750772`  
		Last Modified: Tue, 09 Sep 2025 04:11:42 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:2137c18a967cd7e1dfa5535bf4745a57a2eedda5cb16cc1228e38bb2a997101a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 KB (27624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69f4bc4a8fee2429c24fe265fc74bd3aa4b3711f683771247fd9f4d7f8485a3d`

```dockerfile
```

-	Layers:
	-	`sha256:ca87b0d3dc24f6a42ca63310521e11292748ffab255752edc42eb906165953e5`  
		Last Modified: Tue, 09 Sep 2025 04:42:59 GMT  
		Size: 27.6 KB (27624 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:5e6abdfd5b2403fbd26e18452adc93ac59c12d90f89004879a7c75163c43af1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.8 MB (174761413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6189a2b1441a3832ac5fa11deceef1463d004b784ef4d84c9e4c9656503ae2`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 19 Aug 2025 10:14:17 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
ENV PHP_VERSION=8.4.12
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
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
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ece5e8db45df529c695354fb69a31fa35d96c6acc213193b3b8b0d91268c44d`  
		Last Modified: Mon, 08 Sep 2025 22:04:35 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5378f2f406c9f274e4864d2bf451a2bac770f09b6aee2189f9c71f82fca4c0c`  
		Last Modified: Mon, 08 Sep 2025 22:21:50 GMT  
		Size: 110.2 MB (110161802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f485dc7ef4bb46555035f16886a78f2132c0c38a70d1e435ca4d7f3bba5e00c`  
		Last Modified: Mon, 08 Sep 2025 22:04:35 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:326fe30853c1a8516d9302ce26e40c8099a67c692235b98270f603286ae5c84d`  
		Last Modified: Mon, 08 Sep 2025 22:21:44 GMT  
		Size: 13.8 MB (13783580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5713fbd7efe3ca97c7d8b0f818271d1db37632535db2ed5dab595b814e74e685`  
		Last Modified: Mon, 08 Sep 2025 22:12:46 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92ca1b1ce7ba77275f4de1d24e9266c9ee678cdcabee744cbef85850aa4af14d`  
		Last Modified: Mon, 08 Sep 2025 22:21:44 GMT  
		Size: 14.0 MB (14000848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbb6b6f9fa8f9ad902093c82331727e46d8dc23b71e24fcd060483df8f72ed0`  
		Last Modified: Mon, 08 Sep 2025 22:12:46 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67d0733b2713b952be3857caf807a6c40eb4b80ec309753dd553b094c801eb52`  
		Last Modified: Mon, 08 Sep 2025 22:12:46 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69bf7eb4717705271dd34326a04ab66650ac3cad5fceceee30d76bc2ac433ddc`  
		Last Modified: Mon, 08 Sep 2025 22:12:46 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6306d88fe57081174796dee2c24b38044097eaaebf5e2378879460bb1a4d3b1e`  
		Last Modified: Mon, 08 Sep 2025 22:12:47 GMT  
		Size: 9.2 KB (9196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1866b3cb4aa0b696e7b983adf92722df5399ff22f8f984dac175bb0c45574087`  
		Last Modified: Tue, 09 Sep 2025 02:18:10 GMT  
		Size: 587.7 KB (587673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aa037d1337b21238ce547e85140a95a105b871b490f2a47c181e4d0c8a687d1`  
		Last Modified: Tue, 09 Sep 2025 02:18:10 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dddd2e704497c2bc40ff81ad4be173161140613530319981b202b43aea61a7a`  
		Last Modified: Tue, 09 Sep 2025 02:32:49 GMT  
		Size: 6.1 MB (6073643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36a28054e27f9e082ccf50a194fc3726134def742101b1daa3d98ba85b972158`  
		Last Modified: Tue, 09 Sep 2025 02:18:10 GMT  
		Size: 2.1 KB (2096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04d60b613e5f135afdddf39e70837fdfe50730b1848bf6f0699f0a30e5edb8d`  
		Last Modified: Tue, 09 Sep 2025 02:18:10 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:a696b40e9921003bd194051e48bf525a11ebd7e0aaa23ae4db354284d9d718b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.7 KB (27658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2b525918251676a597842a8d331486833d1bc11625c3a6ab7dc3a04a7384a6c`

```dockerfile
```

-	Layers:
	-	`sha256:8670c774eec7866cc99d55098ecf2010d292419645d52ced415ba1110f67f04e`  
		Last Modified: Tue, 09 Sep 2025 04:43:02 GMT  
		Size: 27.7 KB (27658 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm` - linux; 386

```console
$ docker pull yourls@sha256:a4ccff9f8f8178f3caebdb39aa934e08527ced47ea792d435d3bc80ed710f9e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.6 MB (182630660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f3eaa31a0e690dfdefdc44db8498ab41004245634dd7bb93fffcc1c5700541a`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 19 Aug 2025 10:14:17 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
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
ENV PHP_VERSION=8.4.12
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
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
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14cb411c259f89ddfa2b2d033346731fa8204f13b8566958d0226a5c6480265a`  
		Last Modified: Mon, 08 Sep 2025 21:47:08 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a63beb9ee6a3fdea07f8c32c3607d65424cdfb91ca8772eaf59d823fcdd9b4`  
		Last Modified: Mon, 08 Sep 2025 21:54:52 GMT  
		Size: 116.1 MB (116136712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a9796ef33755d55869b309e8b523770eadbb6047e8d247abe2e5c0408f0d596`  
		Last Modified: Mon, 08 Sep 2025 21:47:11 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1713743cdf04b37ca4990461e374020ef533ae184ab96abed5f99f87889884`  
		Last Modified: Mon, 08 Sep 2025 21:54:05 GMT  
		Size: 13.8 MB (13782931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a13216c8f24cd0d92fb47da8778bd24fcb3e75f495f5747ec5923784a2b09bf`  
		Last Modified: Mon, 08 Sep 2025 21:47:14 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b70d33d5d346369d7a5c6a0a92b5b3a180e7c2105cbbc205c46863e37739177`  
		Last Modified: Mon, 08 Sep 2025 21:54:12 GMT  
		Size: 14.6 MB (14635212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:756c8f31b778ccabfd2fdb3b5f9828235efe859d42f00844636f2f9de876e4f3`  
		Last Modified: Mon, 08 Sep 2025 21:47:17 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0375f6d9ebb21e27d1c1c079186ac358237cdd01a1df533d30cc554ea3e9ef`  
		Last Modified: Mon, 08 Sep 2025 21:47:21 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c28d087a25847203d49ced394ba051be6137dc2a3bf0897c7d4c9fadd1d89b`  
		Last Modified: Mon, 08 Sep 2025 21:47:25 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c689d46e36c029bf626b75695eee1f7453fe475596ec194285a003c48b686e9`  
		Last Modified: Mon, 08 Sep 2025 21:47:31 GMT  
		Size: 9.2 KB (9197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc7b2d6fca7edccf27c633265f187476e705bc6b89f08c5ad67b65a5ea9513e5`  
		Last Modified: Mon, 08 Sep 2025 22:42:56 GMT  
		Size: 695.2 KB (695151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e14c2740c3dc23ef0fbb41cd16735e0ce34f9f27379b21773f6d8c7ff081a6`  
		Last Modified: Mon, 08 Sep 2025 22:42:55 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206ef6eed1d5ff5ce7e490d3a4012894106188721361dbd5182abd1a2de01859`  
		Last Modified: Mon, 08 Sep 2025 22:43:14 GMT  
		Size: 6.1 MB (6073642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d162db6717eb5c1a15325c7c317185b7c67d559270f9e9d037261255c8c29266`  
		Last Modified: Mon, 08 Sep 2025 22:42:55 GMT  
		Size: 2.1 KB (2094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdb2a71d263d70ca705a5d043dee9d7c4151ae59fb0754bb5d01efe7f47f3a4c`  
		Last Modified: Mon, 08 Sep 2025 22:42:56 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:61fc74bd992f451cb3066c45a197c356b8ae99f855eaec0b0698e8e4aaacc126
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74276cac27d395ca5c7cc31dae1ad80a72722cadd354ac2d2d8b2db9cd1785c5`

```dockerfile
```

-	Layers:
	-	`sha256:b9df788d7c13007e06d744553fe9afe68ec9356521896f2bc323d31af75564de`  
		Last Modified: Mon, 08 Sep 2025 22:42:56 GMT  
		Size: 27.5 KB (27488 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm` - linux; ppc64le

```console
$ docker pull yourls@sha256:657d3f91ab74e2a40168fc46591948e87aa3a4a418ced77815c2af7ab4086725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.2 MB (178173159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:062709bdc3ceae37e143d50a1acc5a34e23576b493a330d3e3e947edab01ec75`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 19 Aug 2025 10:14:17 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
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
ENV PHP_VERSION=8.4.12
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
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
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b92c5533102d377092f90a64ce96643efc2f90c8132806309f689ef1a0ff55f1`  
		Last Modified: Mon, 08 Sep 2025 22:47:15 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75c51011b81d61508b6739213b2956df239d3867fbd1b77eade087e74d53486`  
		Last Modified: Mon, 08 Sep 2025 23:13:00 GMT  
		Size: 109.6 MB (109596656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:169d6bf5057cf9cbf3d82654ad276e19db98dfaca1501852995c56026182bd5a`  
		Last Modified: Mon, 08 Sep 2025 22:47:18 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e4d5f8e44780ac25bebfa34d6191af197331f818be8ccd214b1b8164a3e93a`  
		Last Modified: Mon, 08 Sep 2025 23:35:09 GMT  
		Size: 13.8 MB (13783166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2508ca69d57915724e6d4016caa3a804666f309d53979798065874f5ad6414ff`  
		Last Modified: Mon, 08 Sep 2025 23:17:06 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:037899ea4e513825c44f9cc4d4e6433a43e1828cfaf473c485a12a70278d6bea`  
		Last Modified: Tue, 09 Sep 2025 13:12:59 GMT  
		Size: 14.9 MB (14898779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13339d4f3b05954836f1d1805de40e20114bacd544405c28bef0fadf2ea907e5`  
		Last Modified: Tue, 09 Sep 2025 13:12:56 GMT  
		Size: 2.5 KB (2455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ca1753bf30bd91f48a3b42d5ba7b8147ce31679418ab96d58ac56f0005d8f7c`  
		Last Modified: Tue, 09 Sep 2025 13:12:57 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87a722e7ddfb622cf1b08768e80e4d825a20ae2e5723f87685da461215bceed0`  
		Last Modified: Tue, 09 Sep 2025 13:12:57 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2586b93f56c90d64e96af6a51489c4c6156e17b91b5dac7f19349d54492e0036`  
		Last Modified: Tue, 09 Sep 2025 13:12:57 GMT  
		Size: 9.2 KB (9200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278687205dbc3885e9758d2f8c9713febe5998ad905a4fb2b895c2fa42a3e97b`  
		Last Modified: Tue, 09 Sep 2025 21:38:14 GMT  
		Size: 209.3 KB (209316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d660c1f310f84d72f93a5994de1cf3a12f18b1fa079cbc8b232d8e4a516eec9a`  
		Last Modified: Tue, 09 Sep 2025 21:38:19 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b59578e6f65f96dfb9a66fc3e8cc5206010287479149dc935195d138f69d4714`  
		Last Modified: Tue, 09 Sep 2025 22:08:57 GMT  
		Size: 6.1 MB (6073643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d34857000b822b6e8bc52eec60f76674a481d23717e86b04833b13f2a442ad`  
		Last Modified: Tue, 09 Sep 2025 21:38:23 GMT  
		Size: 2.1 KB (2098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ad3a18061d3a54181fd282c5277812323f93a9c2327aa1c88fec5f6a0337d05`  
		Last Modified: Tue, 09 Sep 2025 21:38:26 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:648249bf79c4596b97ecbc0274d4eb922896320b9d245fb66fb4061cd928696c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 KB (27571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03357804b648e13e89c117e4c8742e77d51d29f0c2b66973f48823977ee11aa`

```dockerfile
```

-	Layers:
	-	`sha256:56211f833a90a71ff397d38f6bdc07da30c86561c9b4d015c7a051f74e93bcce`  
		Last Modified: Tue, 09 Sep 2025 22:42:34 GMT  
		Size: 27.6 KB (27571 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm` - linux; riscv64

```console
$ docker pull yourls@sha256:4572b595ba0120ab9a32f47a861dbec2cfc57d10db2865594da2422048050daa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.7 MB (208745298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7997944b6af027128157fa1fb3c6023f187ee55cb37c1380cb3cee78ec6ad75b`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
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
ENV PHP_VERSION=8.4.12
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
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
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e74ecc2368ed7bf14f15784d294255a507b61c121584b8889b54497f586460`  
		Last Modified: Wed, 13 Aug 2025 11:14:45 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44ba9332bf4f75d23eae5411f58fe1a55971f98de6873eba08746a8a1042d175`  
		Last Modified: Wed, 13 Aug 2025 11:43:11 GMT  
		Size: 146.6 MB (146577824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c05acfa088a6e9eb3845fc5011b31ba6a62983f44944e2347f32361bf21d8f85`  
		Last Modified: Wed, 13 Aug 2025 11:14:48 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b6f12b0240e0dbf97c8e4e7dcd68de87e0574ef0a3f23092d507469bd287a7`  
		Last Modified: Thu, 28 Aug 2025 20:15:17 GMT  
		Size: 13.8 MB (13795967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04c460ecb1c90c1e778236105aed7163700500a98352ef0a0fc0ca5883f519ff`  
		Last Modified: Thu, 28 Aug 2025 20:14:18 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ab17b9b790bddf7dbc628a33ccaaa51a8fdb34ef653212b7481dc6d44e8d57`  
		Last Modified: Thu, 28 Aug 2025 21:22:45 GMT  
		Size: 13.8 MB (13823845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5f5c3198a56e140882802698f7790c169e98cb53bf274bf7c65694b723be4f6`  
		Last Modified: Thu, 28 Aug 2025 21:22:44 GMT  
		Size: 2.5 KB (2456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f819899f2a46b3af3292b9c55a3f827a8ea364a0db42778281293f7111043d5`  
		Last Modified: Thu, 28 Aug 2025 21:22:45 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bfec74d928323594efd185a50d2e951172758f7bfc69d5cfc30f4d5487d110a`  
		Last Modified: Thu, 28 Aug 2025 21:22:45 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2762a744bb5ca0534b988987159d987b16547c885864469823acc4fa74f91d8`  
		Last Modified: Thu, 28 Aug 2025 21:22:46 GMT  
		Size: 9.2 KB (9197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:069ac7b1e70350d39a8b4a5cab530b746f3a91df8b37f5295f6dccc40408cf84`  
		Last Modified: Sat, 30 Aug 2025 06:02:03 GMT  
		Size: 185.1 KB (185147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f974eb6565a64fac278e61f0faaf87ae9ceac75175c984466cd94c09f2dcbb`  
		Last Modified: Sat, 30 Aug 2025 06:02:03 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eb44da67192851c8c7e6143bca71f3c67dab8be42c51a33a55918419d8ff775`  
		Last Modified: Sat, 30 Aug 2025 06:02:03 GMT  
		Size: 6.1 MB (6073643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde381a62222b0ef651801141a43f3e0abbd25ff2524c601b426f97cfd91ebe3`  
		Last Modified: Sat, 30 Aug 2025 06:02:03 GMT  
		Size: 2.1 KB (2096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a265cc2be137b2a32efe67875c8a6c5049cfd0c2c0e62201c33110f6181a606`  
		Last Modified: Sat, 30 Aug 2025 06:02:03 GMT  
		Size: 1.7 KB (1695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:a4fef5033206925fd00f9f57b10d5b244d1f0b4aa7765ed2452f07c175b47ca1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 KB (27572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb15296155ab78015bc66b5132f9eb08e67b250f101b80cf6c3b640aa8006da`

```dockerfile
```

-	Layers:
	-	`sha256:31e8a3905347484a2cccd285ff306f7f4384802dd14482965aa12e1eed697497`  
		Last Modified: Sat, 30 Aug 2025 07:42:45 GMT  
		Size: 27.6 KB (27572 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm` - linux; s390x

```console
$ docker pull yourls@sha256:7e5081e32e8221b0e0f2a394b4e1eb70f2416d7ef6517a7989921cd58d8fa217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156910069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72db25e4aa6739fdf4ee137143dab074879747a9bb0747f6d1cf8918a7bce1e1`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 19 Aug 2025 10:14:17 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
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
ENV PHP_VERSION=8.4.12
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.12.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.12.tar.xz.asc
# Tue, 19 Aug 2025 10:14:17 GMT
ENV PHP_SHA256=c1b7978cbb5054eed6c749bde4444afc16a3f2268101fb70a7d5d9b1083b12ad
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
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b232e52aa98f49ca19e377e7da8d1acab05ee220da9d68dd81f728babf0c517`  
		Last Modified: Mon, 08 Sep 2025 21:55:17 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6478857e6e1b537f952dd40041dacfe05d27f69962e33a4c06fb4ff6381f540`  
		Last Modified: Mon, 08 Sep 2025 23:24:43 GMT  
		Size: 92.6 MB (92562517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa056e798e1e4f9bfdcf75b3f6f5791a4f0e696861934a12a910a510c2ac018d`  
		Last Modified: Mon, 08 Sep 2025 21:55:20 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6791b8b7b534a67db4c8aa2e1e8be2537fb2b5aa0e027b8fed33f973699b57e`  
		Last Modified: Mon, 08 Sep 2025 23:24:35 GMT  
		Size: 13.8 MB (13782379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:521ee8649b9b758d7d86588c9947141c2a79a9b036270f3aa1d15a6fa44f6762`  
		Last Modified: Mon, 08 Sep 2025 22:38:33 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce9a675f439e0b72a78878ec2625a075ee87e37c9636acaee6748ddf8078fc9`  
		Last Modified: Tue, 09 Sep 2025 00:03:37 GMT  
		Size: 14.4 MB (14440994 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6190611923c332027ad4d88dca29190e188f60295b7b87baf62a97840eeb6083`  
		Last Modified: Mon, 08 Sep 2025 22:38:37 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f962ff0a265900e274b6ad91acdb44e5a85cad1c8d00a46438b518d90c386b`  
		Last Modified: Mon, 08 Sep 2025 22:38:40 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3833d97bbcfda962f3e4753c3cf1edd880f08261a609ed6d7ddb14239a65ed`  
		Last Modified: Mon, 08 Sep 2025 22:38:43 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c2e95a8de72b4d5b5c946e9b63f0b968b4712b0bf165a50103176d4ddc03eca`  
		Last Modified: Mon, 08 Sep 2025 22:38:48 GMT  
		Size: 9.2 KB (9196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac913dbca84619e7418cc968a9934e124529ad6a7d4a9f9002baaad5b6ebc07e`  
		Last Modified: Tue, 09 Sep 2025 11:29:59 GMT  
		Size: 200.4 KB (200402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d94f7819cf90311976eaf33c27da104f3a25e300c100e82fdc6053467389123`  
		Last Modified: Tue, 09 Sep 2025 11:29:59 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e48f519c641204297161252eab5da1794315935b27e35c4253c4d63e1f1e7b1`  
		Last Modified: Tue, 09 Sep 2025 11:30:01 GMT  
		Size: 6.1 MB (6073643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b8142e6a954cbe6d4be1dfe5d224b0d91ecc482e302a42fad42d42da0a7c9bd`  
		Last Modified: Tue, 09 Sep 2025 11:29:59 GMT  
		Size: 2.1 KB (2092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f8cc9c9d4be917c9c76889d2bb8ef63e757520c6e997e99c468b4b213b9726f`  
		Last Modified: Tue, 09 Sep 2025 11:29:59 GMT  
		Size: 1.7 KB (1694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:34ffcec10333755d669ca4b91163fd963650334b89bc5c7e17e9f70f3590bb32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6574ac1d5add344981ffefb49acd28ecc36ffa8318242ab5543f37971637175`

```dockerfile
```

-	Layers:
	-	`sha256:e188a219ab2d11d2f9d288d8b820262a7a2aa75bd510ae6019374a46992b2949`  
		Last Modified: Tue, 09 Sep 2025 13:42:54 GMT  
		Size: 27.5 KB (27518 bytes)  
		MIME: application/vnd.in-toto+json
