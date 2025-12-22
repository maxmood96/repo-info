## `yourls:fpm`

```console
$ docker pull yourls@sha256:0a3e5077d8a4698598f4a8193713e0483ef4071d372cd65c1ad5b87bce1b3cc2
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
$ docker pull yourls@sha256:c95c626363be15ee1ee666b3f9a2fa9eafb6762b2bad44dafab8dcffd9b6bb1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.9 MB (181854388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e6437bacedc304c77c3960bfb94352434444084c905321f2fd6826d0eec3a5e`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1765152000'
# Fri, 19 Dec 2025 01:26:02 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 19 Dec 2025 01:26:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 19 Dec 2025 01:26:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 19 Dec 2025 01:26:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Dec 2025 01:26:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Dec 2025 01:26:19 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 01:26:19 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 01:26:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Dec 2025 01:26:19 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Dec 2025 01:26:19 GMT
ENV PHP_VERSION=8.4.16
# Fri, 19 Dec 2025 01:26:19 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.16.tar.xz.asc
# Fri, 19 Dec 2025 01:26:19 GMT
ENV PHP_SHA256=f66f8f48db34e9e29f7bfd6901178e9cf4a1b163e6e497716dfcb8f88bcfae30
# Fri, 19 Dec 2025 01:26:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Dec 2025 01:26:28 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:29:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Dec 2025 01:29:06 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:29:06 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Dec 2025 01:29:06 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Dec 2025 01:29:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Dec 2025 01:29:06 GMT
WORKDIR /var/www/html
# Fri, 19 Dec 2025 01:29:06 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 19 Dec 2025 01:29:06 GMT
STOPSIGNAL SIGQUIT
# Fri, 19 Dec 2025 01:29:06 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 19 Dec 2025 01:29:06 GMT
CMD ["php-fpm"]
# Fri, 19 Dec 2025 02:13:29 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Fri, 19 Dec 2025 02:13:29 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 19 Dec 2025 02:13:31 GMT
ARG YOURLS_VERSION=1.10.2
# Fri, 19 Dec 2025 02:13:31 GMT
ARG YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Fri, 19 Dec 2025 02:13:31 GMT
ENV YOURLS_VERSION=1.10.2
# Fri, 19 Dec 2025 02:13:31 GMT
ENV YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Fri, 19 Dec 2025 02:13:31 GMT
# ARGS: YOURLS_VERSION=1.10.2 YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 19 Dec 2025 02:13:31 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 19 Dec 2025 02:13:31 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 02:13:31 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 19 Dec 2025 02:13:31 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:1733a4cd59540b3470ff7a90963bcdea5b543279dd6bdaf022d7883fdad221e5`  
		Last Modified: Mon, 08 Dec 2025 22:17:58 GMT  
		Size: 29.8 MB (29776496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d1aae793d16770b3925c0be51870e93f7d7edaacfebe7830e7d2600db2cc8be`  
		Last Modified: Fri, 19 Dec 2025 01:29:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f7906b34dac2a5ca14056324d58b38a1ce379ba48e79c07ff6d40529d2f1ba`  
		Last Modified: Fri, 19 Dec 2025 01:29:48 GMT  
		Size: 117.8 MB (117838519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b886a29d683272444529ef3b736f4df896325914c1a6edb3bfef460e654c7da`  
		Last Modified: Fri, 19 Dec 2025 01:29:35 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a49173761cfb322e6d171a7344fd9103db980a3efe562625c1946837122e680`  
		Last Modified: Fri, 19 Dec 2025 01:29:38 GMT  
		Size: 13.8 MB (13808375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820eb4ea0d8a23cf0d27c091858c39db3574889114f00bf3db7399e4b207dda9`  
		Last Modified: Fri, 19 Dec 2025 01:29:35 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5af9b442576e99a2ba8a211e7014513be795a90fa8c35e9aa77ff2820c8748`  
		Last Modified: Fri, 19 Dec 2025 01:29:38 GMT  
		Size: 13.7 MB (13665766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d0e8b3680671126068ff6a902ddacc4ee082f78099442646492db2fb1d859a4`  
		Last Modified: Fri, 19 Dec 2025 01:29:35 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8075445dc1d21bbb91858b9613815f6af72e513d88bba737891ff5afb170fc`  
		Last Modified: Fri, 19 Dec 2025 01:29:36 GMT  
		Size: 252.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b984c10e8a6afaabf756b862b516acfd57cbbf50d2c87d46fdaaf38f9b054d7`  
		Last Modified: Fri, 19 Dec 2025 01:29:36 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406b0473a46c7203eeb7d57ac13067a72ccd164067c65d26762a5d04a0d55520`  
		Last Modified: Fri, 19 Dec 2025 01:29:36 GMT  
		Size: 9.2 KB (9194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7aa81b1791c3592ba9a92d203ba5d1407346642cb3c84826ef28bb8e907da8`  
		Last Modified: Fri, 19 Dec 2025 02:13:41 GMT  
		Size: 674.3 KB (674342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5258899c64946e4ac7419a9195c0c1bbf8d20b82fac7bc695093581507b919f4`  
		Last Modified: Fri, 19 Dec 2025 02:13:41 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13b433c7ad2a8b2c053f9749782cf22a53b0dbdc12122c01df01a563c50e64d2`  
		Last Modified: Fri, 19 Dec 2025 02:13:41 GMT  
		Size: 6.1 MB (6073656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21da21685611807e61355c84a2233c8bad59598757712d619583a24bb6b9d13`  
		Last Modified: Fri, 19 Dec 2025 02:13:41 GMT  
		Size: 2.1 KB (2095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183240ec35bc58e8eb9bb6834d243cc0449d6af25421f3c90941769783a97d30`  
		Last Modified: Fri, 19 Dec 2025 02:13:41 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:cc284472e4770adab4fbe78b47d9ccc3db91c56c3d99d99cd68692025cefbb16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de0d0b15c9ae7e9a8dd0aaf6f0972c15503e4164f0362398d4805d39609af57`

```dockerfile
```

-	Layers:
	-	`sha256:0f852edffbf16f0d303813e8f24376beadb67a208dd9f3a96d5f5431c1497dab`  
		Last Modified: Fri, 19 Dec 2025 05:43:34 GMT  
		Size: 27.5 KB (27481 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:fpm` - linux; arm variant v5

```console
$ docker pull yourls@sha256:f4d425c4b7ee59b6571f011a029d63304f6ae62d152e5ff0864ce0d58d403143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155125935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79b87c303e6e5b6e73a86f4ebaa7133e367cfa9e7027fcf9b1872444ce43594e`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1765152000'
# Fri, 19 Dec 2025 01:29:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 19 Dec 2025 01:30:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 19 Dec 2025 01:30:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 19 Dec 2025 01:30:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Dec 2025 01:30:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Dec 2025 01:30:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 01:30:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 01:30:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Dec 2025 01:30:04 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Dec 2025 01:30:04 GMT
ENV PHP_VERSION=8.4.16
# Fri, 19 Dec 2025 01:30:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.16.tar.xz.asc
# Fri, 19 Dec 2025 01:30:04 GMT
ENV PHP_SHA256=f66f8f48db34e9e29f7bfd6901178e9cf4a1b163e6e497716dfcb8f88bcfae30
# Fri, 19 Dec 2025 01:30:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Dec 2025 01:30:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:33:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Dec 2025 01:33:19 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:33:19 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Dec 2025 01:33:19 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Dec 2025 01:33:19 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Dec 2025 01:33:19 GMT
WORKDIR /var/www/html
# Fri, 19 Dec 2025 01:33:19 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 19 Dec 2025 01:33:19 GMT
STOPSIGNAL SIGQUIT
# Fri, 19 Dec 2025 01:33:19 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 19 Dec 2025 01:33:19 GMT
CMD ["php-fpm"]
# Fri, 19 Dec 2025 02:15:09 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Fri, 19 Dec 2025 02:15:09 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 19 Dec 2025 02:15:10 GMT
ARG YOURLS_VERSION=1.10.2
# Fri, 19 Dec 2025 02:15:10 GMT
ARG YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Fri, 19 Dec 2025 02:15:10 GMT
ENV YOURLS_VERSION=1.10.2
# Fri, 19 Dec 2025 02:15:10 GMT
ENV YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Fri, 19 Dec 2025 02:15:10 GMT
# ARGS: YOURLS_VERSION=1.10.2 YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 19 Dec 2025 02:15:10 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 19 Dec 2025 02:15:10 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 02:15:10 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 19 Dec 2025 02:15:10 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d97bc71d0fa535127863fdab265dfddb07b3cda35b80de4dd2b9b67fe154c856`  
		Last Modified: Mon, 08 Dec 2025 22:16:59 GMT  
		Size: 27.9 MB (27944187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a05a50db64ecd34dce11bdece4252d1e0c8103e7b2155217e824d6feec4cf23`  
		Last Modified: Fri, 19 Dec 2025 01:33:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767c44a2b459cdf0e4a8748d3bae87d95cc16c135d04c99588c07c78e543588b`  
		Last Modified: Fri, 19 Dec 2025 01:33:53 GMT  
		Size: 94.9 MB (94874229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29bf5f5591736bcdd368d7ed2e1eae54f0a7b8e4cb7b135c6812e3bc65123243`  
		Last Modified: Fri, 19 Dec 2025 01:33:47 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901e21b40a5e545746fcf8869af22d4476de5a9f8b4a832526b445c3dcb7cc66`  
		Last Modified: Fri, 19 Dec 2025 01:33:50 GMT  
		Size: 13.8 MB (13806205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3ee420e7a1a40e75ebabdc453197884cd613c128f6e6afc8c4dede63c68795e`  
		Last Modified: Fri, 19 Dec 2025 01:33:47 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44bcc3cee8a3961ec966cc27223699c7af01b94a27c06b45da2626cb67e4023`  
		Last Modified: Fri, 19 Dec 2025 01:33:48 GMT  
		Size: 12.2 MB (12235797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531256b3027677048aacf60b479180b9da7e3c50c1f65cfa2e0a760329502786`  
		Last Modified: Fri, 19 Dec 2025 01:33:47 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d26372eea7b9d08c6d99c8e06637635f801edea0cd37fe5b77bccb5a992a24`  
		Last Modified: Fri, 19 Dec 2025 01:33:47 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa0dc6baf0f45f0450c366aabf9b4110fdd30f257eb208ff2940a0594585f58`  
		Last Modified: Fri, 19 Dec 2025 01:33:47 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257b72ec47a7fa862bd9164f9d1390b3d7402da85ff561cd31321c849c27ecd7`  
		Last Modified: Fri, 19 Dec 2025 01:33:47 GMT  
		Size: 9.2 KB (9196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d77aeddb2c5ca0e4f15f03c9aec6194157c77e4babc840d0ba373eaac1ce4ed`  
		Last Modified: Fri, 19 Dec 2025 02:15:23 GMT  
		Size: 174.6 KB (174632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b7e44600e6ad41964d6f01b367da4672b195f9e8df46f9a117a4ae4b706c929`  
		Last Modified: Fri, 19 Dec 2025 02:15:23 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894454d90c3d6db3d4da739b6b280a7cfda6bda96582efdffbddbcb8c17584eb`  
		Last Modified: Fri, 19 Dec 2025 02:15:24 GMT  
		Size: 6.1 MB (6073657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52aed0e7ffef56eb2c6abd76bbfed26ba8dcbb7758b47e5a4cfeae693b57bdad`  
		Last Modified: Fri, 19 Dec 2025 02:15:23 GMT  
		Size: 2.1 KB (2096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512c122636a5bbc5632d465b9451fe502d5adcc3c2fe69f125effe9b3250a8c3`  
		Last Modified: Fri, 19 Dec 2025 02:15:23 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:b9b2ad191fdcd057dc06c2786f34f082ef7f3a512ab186ebce9bcd92ec43bc71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 KB (27581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f51299e7ef8250c7f4c9a2cfa4a79ba5cd1bcbee538d6f12bb8691eb5bbb63dc`

```dockerfile
```

-	Layers:
	-	`sha256:03c3b946e9ec29ce2453ab071d89add75cbdd229ec7b750ccb908b077a1569c1`  
		Last Modified: Fri, 19 Dec 2025 05:43:37 GMT  
		Size: 27.6 KB (27581 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:fpm` - linux; arm variant v7

```console
$ docker pull yourls@sha256:375eefc61cb63b549fdf0265fe33db5f9138a17e77b0570df661fd67c01f4ebc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144075098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37f700a574c70c40dbf4b5ce17174329ca27fa7004a9e3814ede357ffc44dc71`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1765152000'
# Fri, 19 Dec 2025 01:25:54 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 19 Dec 2025 01:26:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 19 Dec 2025 01:26:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 19 Dec 2025 01:26:12 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Dec 2025 01:26:12 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Dec 2025 01:26:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 01:26:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 01:26:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Dec 2025 01:26:12 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Dec 2025 01:26:12 GMT
ENV PHP_VERSION=8.4.16
# Fri, 19 Dec 2025 01:26:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.16.tar.xz.asc
# Fri, 19 Dec 2025 01:26:12 GMT
ENV PHP_SHA256=f66f8f48db34e9e29f7bfd6901178e9cf4a1b163e6e497716dfcb8f88bcfae30
# Fri, 19 Dec 2025 01:26:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Dec 2025 01:26:23 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:29:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Dec 2025 01:29:11 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:29:11 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Dec 2025 01:29:12 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Dec 2025 01:29:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Dec 2025 01:29:12 GMT
WORKDIR /var/www/html
# Fri, 19 Dec 2025 01:29:12 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 19 Dec 2025 01:29:12 GMT
STOPSIGNAL SIGQUIT
# Fri, 19 Dec 2025 01:29:12 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 19 Dec 2025 01:29:12 GMT
CMD ["php-fpm"]
# Fri, 19 Dec 2025 02:16:59 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Fri, 19 Dec 2025 02:16:59 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 19 Dec 2025 02:17:00 GMT
ARG YOURLS_VERSION=1.10.2
# Fri, 19 Dec 2025 02:17:00 GMT
ARG YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Fri, 19 Dec 2025 02:17:00 GMT
ENV YOURLS_VERSION=1.10.2
# Fri, 19 Dec 2025 02:17:00 GMT
ENV YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Fri, 19 Dec 2025 02:17:00 GMT
# ARGS: YOURLS_VERSION=1.10.2 YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 19 Dec 2025 02:17:00 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 19 Dec 2025 02:17:00 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 02:17:00 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 19 Dec 2025 02:17:00 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:cfc411ffeb71f696e2a89e33e91be9b70084d6c3383474344babe3a4a21eb843`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 26.2 MB (26210013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cb62040b75ec45e6399eed6c5f6681e6e2bbcaa92ea1f1cf8a5803e3a6a0c5`  
		Last Modified: Fri, 19 Dec 2025 01:29:37 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2932ae65bcfbaa38950354f35713462235d7ebfbfbc4db6458a24ed461e3d595`  
		Last Modified: Fri, 19 Dec 2025 01:29:43 GMT  
		Size: 86.2 MB (86246015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02cc38dac626ba81ef442e7caf4e48e57e88eae2fa7f2a6b35f0880d94a321fc`  
		Last Modified: Fri, 19 Dec 2025 01:29:37 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2528c6d5d26b5393be9d5aff825b8bc104d0c6b721377075201474e92f99d339`  
		Last Modified: Fri, 19 Dec 2025 01:29:39 GMT  
		Size: 13.8 MB (13806283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bfaf551cf2725beba80e0d46a6b702adb4baf43597662a2db477878e682b376`  
		Last Modified: Fri, 19 Dec 2025 01:29:37 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5bd5585d962029221ca579e7a7a0748cdbaa4540ddc16eb9704f47913fa4dfe`  
		Last Modified: Fri, 19 Dec 2025 01:29:38 GMT  
		Size: 11.6 MB (11560603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d12402a096cdaa993d12166fdabbfa2401ae6890048d9bc99429d917d379684`  
		Last Modified: Fri, 19 Dec 2025 01:29:37 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebccb90233a9f03ed3a1ede13e09038780d0b7b38b552638f3522aa527d63db6`  
		Last Modified: Fri, 19 Dec 2025 01:29:37 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b46bf9fd5b20c4d7466c530f7aa8a112b432271f0688b943efe30e340c30ec`  
		Last Modified: Fri, 19 Dec 2025 01:29:37 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6318296ea18f9e9f3c6f0d4a6cb5dc52dc069a802126492abc1a4de4b7b3acc`  
		Last Modified: Fri, 19 Dec 2025 01:29:37 GMT  
		Size: 9.2 KB (9195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33be5ac7a54da8e801b2fd66f8e553eae960540a24a7e131035a8564b394f654`  
		Last Modified: Fri, 19 Dec 2025 02:17:12 GMT  
		Size: 161.3 KB (161302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4cda9ad91ef9cbaa8e631e14b9a86b731ca01be238e58909a216f63c998e18`  
		Last Modified: Fri, 19 Dec 2025 02:17:20 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32417947dd4f12614226261d20525fc01e348c2032b828e0a37611ff89428719`  
		Last Modified: Fri, 19 Dec 2025 02:17:12 GMT  
		Size: 6.1 MB (6073657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b92bcc441bbcc976c648d2223ff7100a50088ec1fb5985b8d70f446ea1311f`  
		Last Modified: Fri, 19 Dec 2025 02:17:12 GMT  
		Size: 2.1 KB (2095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de1ad6010171e316d191986a70d845b3ee2916b8e355191111855816ade662b`  
		Last Modified: Fri, 19 Dec 2025 02:17:12 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:3f2c35e493461347ed2ce9696199b16974487df3883aa8d20da9f39e6a919a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 KB (27579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8ffe8ab35e044bc0db5fd1528318cd1cd3cb71578994db7e549d220391bed1e`

```dockerfile
```

-	Layers:
	-	`sha256:21578ced1d5b581cff363ef3ca07610d9f406b94d952f1fb3eab614c238585ad`  
		Last Modified: Fri, 19 Dec 2025 05:43:40 GMT  
		Size: 27.6 KB (27579 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:fpm` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:31c34927eed95ccee69cab89ec3868b693e22585300e94ccb77e278c5a21576f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.1 MB (174129898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aef40f37567f902133ac658b477a5ad4223c4b6b580caf0d7d9fd0cf5e0d76bf`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1765152000'
# Fri, 19 Dec 2025 01:26:49 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 19 Dec 2025 01:27:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 19 Dec 2025 01:27:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 19 Dec 2025 01:27:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Dec 2025 01:27:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Dec 2025 01:27:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 01:27:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 01:27:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Dec 2025 01:27:07 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Dec 2025 01:27:07 GMT
ENV PHP_VERSION=8.4.16
# Fri, 19 Dec 2025 01:27:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.16.tar.xz.asc
# Fri, 19 Dec 2025 01:27:07 GMT
ENV PHP_SHA256=f66f8f48db34e9e29f7bfd6901178e9cf4a1b163e6e497716dfcb8f88bcfae30
# Fri, 19 Dec 2025 01:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Dec 2025 01:27:17 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:30:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Dec 2025 01:30:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:30:21 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Dec 2025 01:30:21 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Dec 2025 01:30:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Dec 2025 01:30:21 GMT
WORKDIR /var/www/html
# Fri, 19 Dec 2025 01:30:21 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 19 Dec 2025 01:30:21 GMT
STOPSIGNAL SIGQUIT
# Fri, 19 Dec 2025 01:30:21 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 19 Dec 2025 01:30:21 GMT
CMD ["php-fpm"]
# Fri, 19 Dec 2025 02:13:01 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Fri, 19 Dec 2025 02:13:02 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 19 Dec 2025 02:13:03 GMT
ARG YOURLS_VERSION=1.10.2
# Fri, 19 Dec 2025 02:13:03 GMT
ARG YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Fri, 19 Dec 2025 02:13:03 GMT
ENV YOURLS_VERSION=1.10.2
# Fri, 19 Dec 2025 02:13:03 GMT
ENV YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Fri, 19 Dec 2025 02:13:03 GMT
# ARGS: YOURLS_VERSION=1.10.2 YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 19 Dec 2025 02:13:03 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 19 Dec 2025 02:13:03 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 02:13:03 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 19 Dec 2025 02:13:03 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f626fba1463b32b20f78d29b52dcf15be927dbb5372a9ba6a5f97aad47ae220b`  
		Last Modified: Mon, 08 Dec 2025 22:17:19 GMT  
		Size: 30.1 MB (30138628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9719942f90fdaf1b60605334ff24326b9bfa17693105bf6e1f2a02b0fd74d2e`  
		Last Modified: Fri, 19 Dec 2025 01:30:52 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a849a6c95364bc7d852d457f87a6a2f549baad1d61b2c3ffc304353a44b505`  
		Last Modified: Fri, 19 Dec 2025 01:31:04 GMT  
		Size: 110.2 MB (110162840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03dbc88aba93b8d875d5a68c76abd7ad8aa6711ec441558740754fbef93525b8`  
		Last Modified: Fri, 19 Dec 2025 01:30:52 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:effe2818b0b1c1899ed2c2fc52b1e11fc704b7dbce709a35b29b619dc220b4a6`  
		Last Modified: Fri, 19 Dec 2025 01:30:55 GMT  
		Size: 13.8 MB (13808018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc23dc2dd3f7632bd71b2515a75eea0b5b190e17b28b3b60d1bf14d67caaacc`  
		Last Modified: Fri, 19 Dec 2025 01:30:30 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf248874db4de4bfcd2ce309b121a10b917a9ab97ec51e1675db3589584766e9`  
		Last Modified: Fri, 19 Dec 2025 01:30:53 GMT  
		Size: 13.3 MB (13334978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05432d2cf8c9a4568e4d13555816ab02b3d270c2be9aab6842387af24f3da213`  
		Last Modified: Fri, 19 Dec 2025 01:30:52 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9334d55b3d96a37258c4dee905e41bc722ae23fbceec6d22ac59757e02599557`  
		Last Modified: Fri, 19 Dec 2025 01:30:52 GMT  
		Size: 253.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb18af3b1a741fa62f80f7685ef1bbf1d9c75ef5f2b296c62752bd7cbb2d7b1`  
		Last Modified: Fri, 19 Dec 2025 01:30:52 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b010de06e74cd1fdb30704b5263d41ea60648fcef10bb3706d9fe6d864a9219`  
		Last Modified: Fri, 19 Dec 2025 01:30:52 GMT  
		Size: 9.2 KB (9197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0055e7e12b9c16ec2d2bc003a8cd720e7e4b4ca759b8ba95661204131f4bccd9`  
		Last Modified: Fri, 19 Dec 2025 02:13:15 GMT  
		Size: 594.5 KB (594549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21787f01e0c86908ff6f376a708bb4301b382bb95f68c37dfaf80a19cdc7b65c`  
		Last Modified: Fri, 19 Dec 2025 02:13:15 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a271b01fd9b4534c1e73683af4a8f4cfbc30813573cc0d005a9428c6fae6b560`  
		Last Modified: Fri, 19 Dec 2025 02:13:16 GMT  
		Size: 6.1 MB (6073643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d11b473f54d38f8000fb128f43c6aa9af499755b69e3e48a3584ca0a13e5bbd`  
		Last Modified: Fri, 19 Dec 2025 02:13:15 GMT  
		Size: 2.1 KB (2095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f513b46e48090afebac84c16e35be6310b7996a286421085cf864c964f3df009`  
		Last Modified: Fri, 19 Dec 2025 02:13:15 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:7662056ebaff545c4aa61dbbd91f1337c883e852e7a51af4982e2e06c5abfa68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 KB (27615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b9d83b651f32b7230aa5057ca2cb557ed90114188d400d7b873807a598fec01`

```dockerfile
```

-	Layers:
	-	`sha256:b977b4757146adfd268cf28857bf56d8c3311af100e022395a58c0cd4c0f1227`  
		Last Modified: Fri, 19 Dec 2025 05:43:43 GMT  
		Size: 27.6 KB (27615 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:fpm` - linux; 386

```console
$ docker pull yourls@sha256:64fd11100ee5a5e5ca95c8d75f1b0e45bc9559b42ce4d1c54b03c0784414e545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.0 MB (181986252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de832e51535e5ba2ecd1e12b709a528af1a13492e6dd2f5033a81059a9f5162e`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1765152000'
# Fri, 19 Dec 2025 01:26:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 19 Dec 2025 01:26:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 19 Dec 2025 01:26:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Fri, 19 Dec 2025 01:26:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 19 Dec 2025 01:26:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 19 Dec 2025 01:26:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 01:26:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 19 Dec 2025 01:26:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 19 Dec 2025 01:26:51 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Fri, 19 Dec 2025 01:26:51 GMT
ENV PHP_VERSION=8.4.16
# Fri, 19 Dec 2025 01:26:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.16.tar.xz.asc
# Fri, 19 Dec 2025 01:26:51 GMT
ENV PHP_SHA256=f66f8f48db34e9e29f7bfd6901178e9cf4a1b163e6e497716dfcb8f88bcfae30
# Fri, 19 Dec 2025 01:27:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Dec 2025 01:27:01 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:29:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Dec 2025 01:29:57 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:29:57 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Dec 2025 01:29:57 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Dec 2025 01:29:57 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Dec 2025 01:29:57 GMT
WORKDIR /var/www/html
# Fri, 19 Dec 2025 01:29:57 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 19 Dec 2025 01:29:57 GMT
STOPSIGNAL SIGQUIT
# Fri, 19 Dec 2025 01:29:57 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 19 Dec 2025 01:29:57 GMT
CMD ["php-fpm"]
# Fri, 19 Dec 2025 02:13:33 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Fri, 19 Dec 2025 02:13:33 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 19 Dec 2025 02:13:35 GMT
ARG YOURLS_VERSION=1.10.2
# Fri, 19 Dec 2025 02:13:35 GMT
ARG YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Fri, 19 Dec 2025 02:13:35 GMT
ENV YOURLS_VERSION=1.10.2
# Fri, 19 Dec 2025 02:13:35 GMT
ENV YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Fri, 19 Dec 2025 02:13:35 GMT
# ARGS: YOURLS_VERSION=1.10.2 YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 19 Dec 2025 02:13:35 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 19 Dec 2025 02:13:35 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 02:13:35 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 19 Dec 2025 02:13:35 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2648c88d9207cd6090be83f4a97e2aa4080930987d8fb62195cc994194160e67`  
		Last Modified: Mon, 08 Dec 2025 22:17:03 GMT  
		Size: 31.3 MB (31293070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf554e96695d4b8570b7d495aba4271c51ce62ea2e23374373672a1237aca53`  
		Last Modified: Fri, 19 Dec 2025 01:30:27 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ca017a3089a9eb5cb8a599595c4da3c1996779325aebb522e57d9b4ff4c7100`  
		Last Modified: Fri, 19 Dec 2025 01:30:41 GMT  
		Size: 116.1 MB (116138545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60c4f3c449259708cceef92b07753db173089a618d4f063fb566e1c2e11a6c17`  
		Last Modified: Fri, 19 Dec 2025 01:30:27 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13d820fd522dbfb30c0d00512ea619485de5f3a0e7fcc842c562e6ecc48fcf5`  
		Last Modified: Fri, 19 Dec 2025 01:30:31 GMT  
		Size: 13.8 MB (13807499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d635a9f697d25c1b098109f3bf3e7b2fecc8967d5192001dee58aa1ed40d0eca`  
		Last Modified: Fri, 19 Dec 2025 01:30:27 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f24d1f806ca56a22a8715ddd8eab9c8cbeca923ecd9805e2fd3fbad0e9eac1`  
		Last Modified: Fri, 19 Dec 2025 01:30:28 GMT  
		Size: 14.0 MB (13957838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b787cd4c66df7b341711756be3d7652dd97b0b0964007c3e4f5a3b6c47b6f9`  
		Last Modified: Fri, 19 Dec 2025 01:30:27 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7ac03d4e8eb6c0b5daa0b448486926aba2cf6fbd3c39f3ffb38db8da5cb9fe`  
		Last Modified: Fri, 19 Dec 2025 01:30:27 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51cc89830dd51d9114b637e850e8184da9d6f726a1bb4dab528d72ef00019830`  
		Last Modified: Fri, 19 Dec 2025 01:30:27 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677300a32f4f68ccc49b5ca2cd83d2ee5b7dd8a8405d8ca6d3789cffead98010`  
		Last Modified: Fri, 19 Dec 2025 01:30:27 GMT  
		Size: 9.2 KB (9198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8270179be1ac316246aba0b5a44d0f6bd9fab2a4b94fb195493cc1225cb20684`  
		Last Modified: Fri, 19 Dec 2025 02:13:48 GMT  
		Size: 698.4 KB (698403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a964903a7ddec9df5983e21484b5c2fa3e231af0f90f1ee48439f4f7e550026`  
		Last Modified: Fri, 19 Dec 2025 02:13:48 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab1c3fbdb5c758c2c3d495dfd59514bfeb3c7347c6fa2f4288e4de314e77e935`  
		Last Modified: Fri, 19 Dec 2025 02:13:48 GMT  
		Size: 6.1 MB (6073657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e453ac7f8b01445effc3bf08f14ae92b7a94c5129adc0a283896708c805cb2`  
		Last Modified: Fri, 19 Dec 2025 02:13:48 GMT  
		Size: 2.1 KB (2100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d23b6fbb1dae3a9d960178514cc2e95bb36ceb0bf92c5021dd6968987c0b9f`  
		Last Modified: Fri, 19 Dec 2025 02:13:48 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:9f8d2b83ff0de5e7a2e826bff1e3971d2ee6e969c1550057012e8c65e0994282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 KB (27444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dbe6bd6297d7845acd24237db66a0bf503df43e4960b82b775bddca43602aba`

```dockerfile
```

-	Layers:
	-	`sha256:503e08bc2c3d5530cd0dbdbab25458a65e0b734d08201b2e452cfb3e3bd5ef9f`  
		Last Modified: Fri, 19 Dec 2025 05:43:45 GMT  
		Size: 27.4 KB (27444 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:fpm` - linux; ppc64le

```console
$ docker pull yourls@sha256:d4079b76959287c0d6d82247940ee6fd1492766de7cc6670a49d536bcbf52b5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.5 MB (177528444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de5fd1576f6674e3dcebfb7dcab40ed5a212361bb6ef1bdbe57df8e10da31bb6`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 00:35:58 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 09 Dec 2025 00:36:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 09 Dec 2025 00:36:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 00:36:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 09 Dec 2025 00:36:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 09 Dec 2025 00:36:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Dec 2025 00:36:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Dec 2025 00:36:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 09 Dec 2025 00:36:49 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 09 Dec 2025 00:36:49 GMT
ENV PHP_VERSION=8.4.16
# Tue, 09 Dec 2025 00:36:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.16.tar.xz.asc
# Tue, 09 Dec 2025 00:36:49 GMT
ENV PHP_SHA256=f66f8f48db34e9e29f7bfd6901178e9cf4a1b163e6e497716dfcb8f88bcfae30
# Fri, 19 Dec 2025 01:49:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Dec 2025 01:49:06 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:58:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Dec 2025 01:58:04 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:58:05 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Dec 2025 01:58:05 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Dec 2025 01:58:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Dec 2025 01:58:05 GMT
WORKDIR /var/www/html
# Fri, 19 Dec 2025 01:58:06 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 19 Dec 2025 01:58:06 GMT
STOPSIGNAL SIGQUIT
# Fri, 19 Dec 2025 01:58:06 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 19 Dec 2025 01:58:06 GMT
CMD ["php-fpm"]
# Fri, 19 Dec 2025 02:30:33 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Fri, 19 Dec 2025 02:30:35 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 19 Dec 2025 02:30:38 GMT
ARG YOURLS_VERSION=1.10.2
# Fri, 19 Dec 2025 02:30:38 GMT
ARG YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Fri, 19 Dec 2025 02:30:38 GMT
ENV YOURLS_VERSION=1.10.2
# Fri, 19 Dec 2025 02:30:38 GMT
ENV YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Fri, 19 Dec 2025 02:30:38 GMT
# ARGS: YOURLS_VERSION=1.10.2 YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 19 Dec 2025 02:30:39 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 19 Dec 2025 02:30:39 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 02:30:39 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 19 Dec 2025 02:30:39 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:ddd908d99c8b32da8685339ba6296773100f66e08c8bf508ab82174ba5a4f600`  
		Last Modified: Tue, 09 Dec 2025 00:06:51 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e968a4c552b5d63962c849d9412a26339a7f50c4b8dee90079284c674840b8`  
		Last Modified: Tue, 09 Dec 2025 00:41:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d30124c487aeb9dddde3de1f906a208cb9bd0ae4a03d96c1622924a8622e568`  
		Last Modified: Tue, 09 Dec 2025 00:41:59 GMT  
		Size: 109.6 MB (109597911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd51466d9c6ea60e911a8b8d548a3ce159de7cc08df81891f748149917d7196`  
		Last Modified: Tue, 09 Dec 2025 00:41:49 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b39517ed7eececbe5fb5f359997fda28d338457f69d2b82a74d8afeafebee29`  
		Last Modified: Fri, 19 Dec 2025 01:54:13 GMT  
		Size: 13.8 MB (13823062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efef92fa5478d5d557dbe6c983853abd9ac4007ec3c58643fccb7ff0c7175c06`  
		Last Modified: Fri, 19 Dec 2025 01:54:12 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85f4a120a1a7b7ac9e2a1cfd37f712b8ad35565febde5e20f1736c5a78789340`  
		Last Modified: Fri, 19 Dec 2025 01:58:39 GMT  
		Size: 14.2 MB (14210443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35257630aa0c1426dc2b2f456d5aef6b6a782fc174d9eb5d5967a40d84f61874`  
		Last Modified: Fri, 19 Dec 2025 01:58:38 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:217716c3fb56d7cb420bf12feeb0020c5db048344ffbbf3cbd36364dd85f499d`  
		Last Modified: Fri, 19 Dec 2025 01:58:38 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b5e4ddcc1a549f84b8365413a91ea9b9e9ff7da621701dafad273edd7798dab`  
		Last Modified: Fri, 19 Dec 2025 01:58:38 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2487f77e22d1b8a9fff5e4a501b8a168f5ec64fc84778d93e25cedd975aefc16`  
		Last Modified: Fri, 19 Dec 2025 01:58:38 GMT  
		Size: 9.2 KB (9197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cbe23e480504e557a75be8479cafa4b00f9eec963bea3ab82ff6a09b83f9985`  
		Last Modified: Fri, 19 Dec 2025 02:31:06 GMT  
		Size: 209.3 KB (209252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a9c1def47cd6a4412e9e80316911a57f874aa98ed152bbdf8aaf423441e975`  
		Last Modified: Fri, 19 Dec 2025 02:31:06 GMT  
		Size: 324.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3851d22d53475a97da7e84545e59dab87f34e9aa609eacbd7efb08ef1935d5f`  
		Last Modified: Fri, 19 Dec 2025 02:31:06 GMT  
		Size: 6.1 MB (6073657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89d241415df9faf5882b6a842faa11ba318c6a750bc0904d3d4fa64b98d58dc`  
		Last Modified: Fri, 19 Dec 2025 02:31:06 GMT  
		Size: 2.1 KB (2099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9d5567b3c6e9956ee5d6911034fdc6bebe2ee11a5bfadc91b33aab5a3e1ce4`  
		Last Modified: Fri, 19 Dec 2025 02:31:08 GMT  
		Size: 1.7 KB (1693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:c72b8a45b88745599401f89eebcd8ffc1a4fa38e9557f89518b41d0f9bfa0f4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bcd209bda84826bcc89e02eb3277525e1034fdcef506b5128712b6018c79a62`

```dockerfile
```

-	Layers:
	-	`sha256:2e82a997b61e3a0ae837514db2d0dc6f116c45ad1c3bc43b6f2abf58de20341f`  
		Last Modified: Fri, 19 Dec 2025 05:43:55 GMT  
		Size: 27.5 KB (27528 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:fpm` - linux; riscv64

```console
$ docker pull yourls@sha256:e6ce051fe9cbb2458c32488c4d193c51761d7a88be84605bc0d64c4afb362e7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **208.1 MB (208094268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f9e4ce745921a7f1b8227cdff4aaf5a48d0cbfb2e593fd451f87d0787fc6815`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1765152000'
# Tue, 09 Dec 2025 08:01:03 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Tue, 09 Dec 2025 08:03:03 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 09 Dec 2025 08:03:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Tue, 09 Dec 2025 08:03:03 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 09 Dec 2025 08:03:04 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Tue, 09 Dec 2025 08:03:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Dec 2025 08:03:04 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 09 Dec 2025 08:03:04 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 09 Dec 2025 08:03:04 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Tue, 09 Dec 2025 08:03:04 GMT
ENV PHP_VERSION=8.4.16
# Tue, 09 Dec 2025 08:03:04 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.16.tar.xz.asc
# Tue, 09 Dec 2025 08:03:04 GMT
ENV PHP_SHA256=f66f8f48db34e9e29f7bfd6901178e9cf4a1b163e6e497716dfcb8f88bcfae30
# Sat, 20 Dec 2025 06:15:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Sat, 20 Dec 2025 06:15:47 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Sat, 20 Dec 2025 11:18:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Sat, 20 Dec 2025 11:18:46 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Sat, 20 Dec 2025 11:18:47 GMT
RUN docker-php-ext-enable opcache # buildkit
# Sat, 20 Dec 2025 11:18:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Sat, 20 Dec 2025 11:18:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 20 Dec 2025 11:18:48 GMT
WORKDIR /var/www/html
# Sat, 20 Dec 2025 11:18:48 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Sat, 20 Dec 2025 11:18:48 GMT
STOPSIGNAL SIGQUIT
# Sat, 20 Dec 2025 11:18:48 GMT
EXPOSE map[9000/tcp:{}]
# Sat, 20 Dec 2025 11:18:48 GMT
CMD ["php-fpm"]
# Mon, 22 Dec 2025 19:34:53 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Mon, 22 Dec 2025 19:34:54 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Mon, 22 Dec 2025 19:34:58 GMT
ARG YOURLS_VERSION=1.10.2
# Mon, 22 Dec 2025 19:34:58 GMT
ARG YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Mon, 22 Dec 2025 19:34:58 GMT
ENV YOURLS_VERSION=1.10.2
# Mon, 22 Dec 2025 19:34:58 GMT
ENV YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Mon, 22 Dec 2025 19:34:58 GMT
# ARGS: YOURLS_VERSION=1.10.2 YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Mon, 22 Dec 2025 19:34:58 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Mon, 22 Dec 2025 19:34:59 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 22 Dec 2025 19:34:59 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Mon, 22 Dec 2025 19:34:59 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c5d5473ebdeca51d00ece2f72c173b54f0060da7fbd8ab9486aaa33eee6a0d8c`  
		Last Modified: Tue, 09 Dec 2025 02:06:40 GMT  
		Size: 28.3 MB (28273156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a53d28a615a791c3859b4a1756ba700dc2c4f69377eb59f2058ba63d00e0869a`  
		Last Modified: Tue, 09 Dec 2025 09:06:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f8434337c0c50639ecc5b6dc774986d4e9420e3476e8e2468932a6a85632eb`  
		Last Modified: Tue, 09 Dec 2025 09:07:07 GMT  
		Size: 146.6 MB (146578870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e90ba410db15c99bcf35ee3bbf15863cbe2650207953ae1e912e0e6bf7fda0b`  
		Last Modified: Tue, 09 Dec 2025 09:06:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b5a131ea94c686cd7dded8faad5c1989c433c9b2ce64330fb940a005c25c4f`  
		Last Modified: Sat, 20 Dec 2025 07:13:42 GMT  
		Size: 13.8 MB (13822855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5740d16fb53ffe508b40e88ea100bb65bd76bbfd3b246e32fcfbd6d97e59b898`  
		Last Modified: Sat, 20 Dec 2025 07:13:40 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d250c2f4da395f52aaec059173c8751f05ee6468cdecd57582a1102022236d9e`  
		Last Modified: Sat, 20 Dec 2025 11:22:15 GMT  
		Size: 13.1 MB (13143374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab746774549ec1bae8a47cb9b5fd840a2d754ddc7f5f51229824e9c658bfadd4`  
		Last Modified: Sat, 20 Dec 2025 11:22:14 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b83ac6832c4ca94664b0b45ed8c515264f5dbc84050bf8490c1eaf6d72c107`  
		Last Modified: Sat, 20 Dec 2025 11:22:14 GMT  
		Size: 255.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04dc6f4ef01685cdefaa099e832c8dfa9a7283141e97a061de7b71e318c5df9b`  
		Last Modified: Sat, 20 Dec 2025 11:22:14 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b3005caa692eba7c9f4e25f9898fc166450b86db196622b70df9dacc6b3f909`  
		Last Modified: Sat, 20 Dec 2025 11:22:14 GMT  
		Size: 9.2 KB (9200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554cdbd8e04ec4a1dfda30427a2bf63701c86de1023fb753d875247713d0c384`  
		Last Modified: Mon, 22 Dec 2025 19:35:56 GMT  
		Size: 185.1 KB (185097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6ff5e72236ab6f65d437b7583174b9d627a65378f72b5c77030d15e8ef86d3`  
		Last Modified: Mon, 22 Dec 2025 19:35:56 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e968e41ca13707e65d07ca053918e15746340d0799df1c414fbe80e8376c79d`  
		Last Modified: Mon, 22 Dec 2025 19:35:56 GMT  
		Size: 6.1 MB (6073657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbf36151d1cba55f40490d72f7122e6925f6ec8d519021229438d68f0e83494f`  
		Last Modified: Mon, 22 Dec 2025 19:35:56 GMT  
		Size: 2.1 KB (2096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71f52064c8fb36a78397e83298210e975e782cbc9b3036eaf4c9032e6e97410a`  
		Last Modified: Mon, 22 Dec 2025 19:35:56 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:c64e94bdf0ce8b61f3c9b055a7c667749e900b8fb3de0427d348f089391f0fb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db0bb2db03d2284e48b72adcd571e8eff821b918c7014f55a1481aa35dd33e0b`

```dockerfile
```

-	Layers:
	-	`sha256:9f1061234fa567ef37e43278c3d51dcb7f5e277423a2d68771afbd814681210b`  
		Last Modified: Mon, 22 Dec 2025 20:42:38 GMT  
		Size: 27.5 KB (27528 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:fpm` - linux; s390x

```console
$ docker pull yourls@sha256:6aa4150b8b8896f5961ba1289a8ac4629122b922b2223ed8d6141c415989209a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (155972623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cdea32747b4f318eef2a3a2f9556fa954c43130246c3966580ea3cd43c9f9fb`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1765152000'
# Mon, 08 Dec 2025 22:37:09 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Mon, 08 Dec 2025 22:37:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Mon, 08 Dec 2025 22:37:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Mon, 08 Dec 2025 22:37:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Mon, 08 Dec 2025 22:37:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Mon, 08 Dec 2025 22:37:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:37:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Mon, 08 Dec 2025 22:37:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Mon, 08 Dec 2025 22:37:24 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Mon, 08 Dec 2025 22:37:24 GMT
ENV PHP_VERSION=8.4.16
# Mon, 08 Dec 2025 22:37:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.16.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.16.tar.xz.asc
# Mon, 08 Dec 2025 22:37:24 GMT
ENV PHP_SHA256=f66f8f48db34e9e29f7bfd6901178e9cf4a1b163e6e497716dfcb8f88bcfae30
# Fri, 19 Dec 2025 01:25:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 19 Dec 2025 01:25:07 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:28:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 19 Dec 2025 01:28:56 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 01:28:56 GMT
RUN docker-php-ext-enable opcache # buildkit
# Fri, 19 Dec 2025 01:28:56 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 19 Dec 2025 01:28:56 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 19 Dec 2025 01:28:56 GMT
WORKDIR /var/www/html
# Fri, 19 Dec 2025 01:28:56 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 19 Dec 2025 01:28:56 GMT
STOPSIGNAL SIGQUIT
# Fri, 19 Dec 2025 01:28:56 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 19 Dec 2025 01:28:56 GMT
CMD ["php-fpm"]
# Fri, 19 Dec 2025 02:12:25 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli # buildkit
# Fri, 19 Dec 2025 02:12:25 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Fri, 19 Dec 2025 02:12:26 GMT
ARG YOURLS_VERSION=1.10.2
# Fri, 19 Dec 2025 02:12:26 GMT
ARG YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Fri, 19 Dec 2025 02:12:26 GMT
ENV YOURLS_VERSION=1.10.2
# Fri, 19 Dec 2025 02:12:26 GMT
ENV YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
# Fri, 19 Dec 2025 02:12:26 GMT
# ARGS: YOURLS_VERSION=1.10.2 YOURLS_SHA256=c1a5c35d4f47c322d29adffb1a89642544e609808561cf340dc046af58a900e8
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Fri, 19 Dec 2025 02:12:26 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Fri, 19 Dec 2025 02:12:27 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Dec 2025 02:12:27 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Fri, 19 Dec 2025 02:12:27 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:deacec5e6af82b258c59e95e3e86abeef36fad06b1d9ff2de33e88544ffb79ff`  
		Last Modified: Mon, 08 Dec 2025 22:20:52 GMT  
		Size: 29.8 MB (29834400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06325ac7d48e9543412848e1fa70a7cb9a579c86f688b2e2e9bd944346590fce`  
		Last Modified: Mon, 08 Dec 2025 22:41:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9a4b708d85d9501bc1929ab5cadbcf5d4c4bca40490257ace724e13a60fcbe4`  
		Last Modified: Mon, 08 Dec 2025 22:41:12 GMT  
		Size: 92.6 MB (92564698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e8d9f5a2f9a70ca9e903eb070a1168477352c4a37bbecf3ddf16c7afe71c0e`  
		Last Modified: Mon, 08 Dec 2025 22:41:03 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb1e4032ea34dee7fe773b99191a56ce7d29f291575d6d1e06541fec2286fbb`  
		Last Modified: Fri, 19 Dec 2025 01:29:23 GMT  
		Size: 13.8 MB (13822253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd65da009074f8710114d5a6820c643db58239f87632f61755ed7b7c4a0379a`  
		Last Modified: Fri, 19 Dec 2025 01:29:21 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4cbb3147d9227958be6437d6d999023801722e979f05a56c6441d0e6af8f88e`  
		Last Modified: Fri, 19 Dec 2025 01:29:22 GMT  
		Size: 13.5 MB (13460150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24d3bba677a900f81b2ded1eda5cf063c8cbb5afaabc6dde08e15b8af351277d`  
		Last Modified: Fri, 19 Dec 2025 01:29:21 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70c3083b59f0b5e5f9301ffe257e45aaca917fb3366064f68d0bf04b56fe7938`  
		Last Modified: Fri, 19 Dec 2025 01:29:22 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9549d897defa196864e14261f31675b9e9049403b2c88266890a439dfc7c5b`  
		Last Modified: Fri, 19 Dec 2025 01:29:21 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548416d7a32e647b181b46dc728027b04df429aae4240c790cd1904119089ed9`  
		Last Modified: Fri, 19 Dec 2025 01:29:21 GMT  
		Size: 9.2 KB (9196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e37c99a872c93469623342496be885668c53aaef35c963925c3ebab615d89128`  
		Last Modified: Fri, 19 Dec 2025 02:12:41 GMT  
		Size: 200.2 KB (200236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f461b6076fa2c73ee44469249ba1cc3f068d7a4baf2c461a1f473ea9849cf421`  
		Last Modified: Fri, 19 Dec 2025 02:12:41 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:518395bfede3c955642eaf09c9fdf6812d90772ad868e1f9301683e494708079`  
		Last Modified: Fri, 19 Dec 2025 02:12:41 GMT  
		Size: 6.1 MB (6073656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dcb7495485c0f7ec3cc36fa537c6c00e8f63698787d215120526fa291432250`  
		Last Modified: Fri, 19 Dec 2025 02:12:41 GMT  
		Size: 2.1 KB (2095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66a91979606229e815f47d96c30bfa792cbea77a9c4de0f8c279ef77b8031217`  
		Last Modified: Fri, 19 Dec 2025 02:12:41 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:841093d0f8301aa4d2d8801136d8d862c56c25980037ac339427e89955679090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc91e7816e22daebd03529a74fb1d5a8734e0aace7ae50cef07f472801377561`

```dockerfile
```

-	Layers:
	-	`sha256:f18adbce38d084e9e23fa4ea1096a018212de02d68002abc7dbdeb49a46ae300`  
		Last Modified: Fri, 19 Dec 2025 05:44:00 GMT  
		Size: 27.5 KB (27475 bytes)  
		MIME: application/vnd.in-toto+json
