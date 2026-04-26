## `yourls:1-fpm`

```console
$ docker pull yourls@sha256:832a22d9d62545a07c2a6ba4f87d46a80753ca3d76c40f4b3a37f62428d111c6
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
$ docker pull yourls@sha256:45f7f6ee508f91333306cdfad08af618d3e312032038ef45477848261b58c3d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.4 MB (183404310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cb9ba2af0140174ca1483e9285facf4feb327c33c2a80c0cf890886eb2c5a9b`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:22:25 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:22:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:22:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:22:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:22:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:22:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:22:42 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:22:42 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:22:42 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 22 Apr 2026 01:22:42 GMT
ENV PHP_VERSION=8.5.5
# Wed, 22 Apr 2026 01:22:42 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 22 Apr 2026 01:22:42 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 22 Apr 2026 01:22:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:22:51 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:25:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:25:42 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:25:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:25:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:25:42 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:25:42 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 22 Apr 2026 01:25:42 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 Apr 2026 01:25:42 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 22 Apr 2026 01:25:42 GMT
CMD ["php-fpm"]
# Wed, 22 Apr 2026 04:44:42 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Wed, 22 Apr 2026 04:44:42 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Wed, 22 Apr 2026 04:44:43 GMT
ARG YOURLS_VERSION=1.10.3
# Wed, 22 Apr 2026 04:44:43 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Wed, 22 Apr 2026 04:44:43 GMT
ENV YOURLS_VERSION=1.10.3
# Wed, 22 Apr 2026 04:44:43 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Wed, 22 Apr 2026 04:44:43 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Wed, 22 Apr 2026 04:44:43 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Wed, 22 Apr 2026 04:44:43 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 04:44:43 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Wed, 22 Apr 2026 04:44:43 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a923b3cdaa21f3c6e30c9662c5be29400c6b6f28e913ffb7c714816ce30bc886`  
		Last Modified: Wed, 22 Apr 2026 01:26:03 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7417fc69aeb1abfb52a71b35ffe493f50ca3ff41e13bd8ce993e487500336ff`  
		Last Modified: Wed, 22 Apr 2026 01:26:06 GMT  
		Size: 117.8 MB (117843035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f587e05427862542219f5f49fab984a5a449fb100c7eff120cc3f372f72ac2`  
		Last Modified: Wed, 22 Apr 2026 01:26:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09dc2aeabb53004d8df4328a9194d3e4f2e90c1349e3ea3d35cba5309a8e5298`  
		Last Modified: Wed, 22 Apr 2026 01:26:04 GMT  
		Size: 14.5 MB (14503475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b4dc34435e47eae94a080d2ac344960ea6388c4107ab24769dd8bc95815b2b9`  
		Last Modified: Wed, 22 Apr 2026 01:26:04 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf5d675cd5c8ee305661f697203b27c50d10adaefedee3075240fbf8427e40d`  
		Last Modified: Wed, 22 Apr 2026 01:26:05 GMT  
		Size: 15.1 MB (15103302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f6245df833d569fd48dfcc8cd547bb40dbd45804aed0028f0718abf297b8220`  
		Last Modified: Wed, 22 Apr 2026 01:26:05 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc912c9a9f8f3d39bf641f716e380521f709fa96c3b0fe74c931b1dd2eea2473`  
		Last Modified: Wed, 22 Apr 2026 01:26:06 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664fbce7d16e42a80d975db5142b3979e568170053e735e1b48736d3551cd7dd`  
		Last Modified: Wed, 22 Apr 2026 01:26:07 GMT  
		Size: 9.3 KB (9261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c2e016b8cc06d617f851c936b4151ea1ae8aa75a795b800731e446f6234985`  
		Last Modified: Wed, 22 Apr 2026 04:44:48 GMT  
		Size: 108.4 KB (108365 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df4cbc41a7e06379b24c55d2195e8541b09c1695f5ed4a299de72eb3e6e29bde`  
		Last Modified: Wed, 22 Apr 2026 04:44:48 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7238af86f82515a8f11f743525a840cec64de6e5e0ec56945c1863335af0197`  
		Last Modified: Wed, 22 Apr 2026 04:44:48 GMT  
		Size: 6.0 MB (6048924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db0c28a54986f101904703fa77abc6091d7d930715a50a32aa8def29999070b`  
		Last Modified: Wed, 22 Apr 2026 04:44:48 GMT  
		Size: 2.1 KB (2093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686b4aaefa181ccb8b5b49ed19d2a2dc625fe833c763e4351ff06faf332feb7b`  
		Last Modified: Wed, 22 Apr 2026 04:44:49 GMT  
		Size: 1.7 KB (1692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:eab0d7c7ec5645e72045f64b31499c9b4058c4c4df9d52d186e463e7343348e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19eef211cd693fae43db7976335a5150630410d183d29d19623a87d11d8d9fc2`

```dockerfile
```

-	Layers:
	-	`sha256:7bb4bc67e2fa3b9103ee30c3c2b2a28bebdd897da34eecc8128a086947bd85a5`  
		Last Modified: Wed, 22 Apr 2026 04:44:48 GMT  
		Size: 26.7 KB (26674 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm` - linux; arm variant v5

```console
$ docker pull yourls@sha256:0eb778805f72ab8415d4226d8e4b5287fb3be83303738d676742358577ae76bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.6 MB (156623245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d0f43bf2fba6c23fa431cd78963a38ff8860c8c784defe23d144d493eceda37`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:20:06 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:20:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:20:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:20:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:20:29 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:20:29 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:20:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:20:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:20:29 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 22 Apr 2026 01:20:29 GMT
ENV PHP_VERSION=8.5.5
# Wed, 22 Apr 2026 01:20:29 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 22 Apr 2026 01:20:29 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 22 Apr 2026 01:20:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:20:42 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:23:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:23:50 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:23:50 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:23:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:23:50 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:23:51 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 22 Apr 2026 01:23:51 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 Apr 2026 01:23:51 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 22 Apr 2026 01:23:51 GMT
CMD ["php-fpm"]
# Wed, 22 Apr 2026 03:36:14 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Wed, 22 Apr 2026 03:36:14 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Wed, 22 Apr 2026 03:36:15 GMT
ARG YOURLS_VERSION=1.10.3
# Wed, 22 Apr 2026 03:36:15 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Wed, 22 Apr 2026 03:36:15 GMT
ENV YOURLS_VERSION=1.10.3
# Wed, 22 Apr 2026 03:36:15 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Wed, 22 Apr 2026 03:36:15 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Wed, 22 Apr 2026 03:36:15 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Wed, 22 Apr 2026 03:36:16 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 03:36:16 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Wed, 22 Apr 2026 03:36:16 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6496d93bca0663211b9252da346044ecb734ee5b3ecaae5b1fbd230753faee2f`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 27.9 MB (27948180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cceb84c9f466573920de66d24a34f2c68c19bcf0a1b2c264f34c332471c69fb9`  
		Last Modified: Wed, 22 Apr 2026 01:24:09 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d33534dd8e573ebb0c8014512c21ee46f5bdb0a9a8bed6d2c2c4a536a5c0601`  
		Last Modified: Wed, 22 Apr 2026 01:24:12 GMT  
		Size: 94.9 MB (94884496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d956e9df4e4f3f00f9b8089a0a62668d9ac506d5116beec87459b0a803584220`  
		Last Modified: Wed, 22 Apr 2026 01:24:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b94f772dc4349c78f8501fa21c893f159e6b3aad29e96d1310e4cd9d41b15815`  
		Last Modified: Wed, 22 Apr 2026 01:24:10 GMT  
		Size: 14.5 MB (14500861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c6a0eba1f188a9fea225dfae2b3500526c78e38a56bd425375adb76895aeaf`  
		Last Modified: Wed, 22 Apr 2026 01:24:11 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d323d9e7859bfe43a4d612cc3e928178b1e3b7d3d52b3fb7bfa948b5ebb53208`  
		Last Modified: Wed, 22 Apr 2026 01:24:11 GMT  
		Size: 13.1 MB (13126779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d744c4e270cf77f6d244ff5f2bba7c8192f53201ffd97007e4d79827ce765630`  
		Last Modified: Wed, 22 Apr 2026 01:24:12 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52150e91840f25d0d67a77046fe8ef14351d3b9de1c219bfca9cec1c2ac6efac`  
		Last Modified: Wed, 22 Apr 2026 01:24:12 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e52bd01653785f373d190dc248adae553de19184b6432022e4d7628da83ec6`  
		Last Modified: Wed, 22 Apr 2026 01:24:13 GMT  
		Size: 9.3 KB (9265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270d0f83f15472bd624fb33db1c4f1a411e31b0756fb4ec091db482d81e1cf01`  
		Last Modified: Wed, 22 Apr 2026 03:36:21 GMT  
		Size: 97.0 KB (96970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8349cf3a4ba94fd677948d80aca3761d2c8b624096946310aec078ee272c5fc4`  
		Last Modified: Wed, 22 Apr 2026 03:36:21 GMT  
		Size: 325.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8bed35d532e7a032c310757259155c8d0a5fccc26be024e7f69c2f610ec6ca2`  
		Last Modified: Wed, 22 Apr 2026 03:36:21 GMT  
		Size: 6.0 MB (6048924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:218e65ee8be6fc7c551acb28cd3474346613895d220a5e81326893c4ae5ce4ae`  
		Last Modified: Wed, 22 Apr 2026 03:36:20 GMT  
		Size: 2.1 KB (2091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7052ff74b83ad787c425239b2d453718a1f51d6235faa51a9f3b75bcaafa845f`  
		Last Modified: Wed, 22 Apr 2026 03:36:22 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:309ee9e2d08dd9c95f00ae6e68aed5ae43c79748449430718a79ff4a0bd0c087
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63a0ac06796e5d7cf9956e4bb8495a30cb2ba47f06ae2df47083817b771e3f70`

```dockerfile
```

-	Layers:
	-	`sha256:30833217a9acbf1787a782977b8b5c0d27461afa790c6cb73df59c634f6f9b0a`  
		Last Modified: Wed, 22 Apr 2026 03:36:21 GMT  
		Size: 26.8 KB (26769 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm` - linux; arm variant v7

```console
$ docker pull yourls@sha256:e88b437bd57e69c47c2003554f388e2ff8455c0e8651cad7137235befb34a9f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.5 MB (145546366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:911ea3ac9a5ff0b8b16f26a05d283d13259033456a3f44b106575f1004a64755`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:23:31 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:23:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:23:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:23:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:23:49 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:23:49 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:23:49 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:23:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:23:49 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 22 Apr 2026 01:23:49 GMT
ENV PHP_VERSION=8.5.5
# Wed, 22 Apr 2026 01:23:49 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 22 Apr 2026 01:23:49 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 22 Apr 2026 01:23:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:23:58 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:26:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:26:42 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:26:42 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:26:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:26:42 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:26:42 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 22 Apr 2026 01:26:42 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 Apr 2026 01:26:42 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 22 Apr 2026 01:26:42 GMT
CMD ["php-fpm"]
# Wed, 22 Apr 2026 03:51:59 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Wed, 22 Apr 2026 03:52:00 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Wed, 22 Apr 2026 03:52:01 GMT
ARG YOURLS_VERSION=1.10.3
# Wed, 22 Apr 2026 03:52:01 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Wed, 22 Apr 2026 03:52:01 GMT
ENV YOURLS_VERSION=1.10.3
# Wed, 22 Apr 2026 03:52:01 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Wed, 22 Apr 2026 03:52:01 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Wed, 22 Apr 2026 03:52:01 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Wed, 22 Apr 2026 03:52:01 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 03:52:01 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Wed, 22 Apr 2026 03:52:01 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55902cd11f5cee73e37dd6b7274ad068d6ab77feb8165d071674df0ccf38417`  
		Last Modified: Wed, 22 Apr 2026 01:26:58 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0b5ea04af6bac36d38da15e40540ff669cfc9d5141d6bcab3317138fc62e3f`  
		Last Modified: Wed, 22 Apr 2026 01:27:02 GMT  
		Size: 86.2 MB (86248228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25364998dea0b06b29b1751f14ff8ba40896bb1fc689649eec92f9c35da15d3`  
		Last Modified: Wed, 22 Apr 2026 01:26:58 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:434302f439ed43d5079b3126f49874dd04c0f28ad3031182321f4b707f61c4fc`  
		Last Modified: Wed, 22 Apr 2026 01:26:59 GMT  
		Size: 14.5 MB (14500946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d495cda0c73d22077f8d0ede99e6bf692f8b34e9ef71e6d9f7418a3d46c780`  
		Last Modified: Wed, 22 Apr 2026 01:27:00 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9bf655072c60599df53315c5850a297edb0c19ea31a8bf099eef7103eb5265b`  
		Last Modified: Wed, 22 Apr 2026 01:27:00 GMT  
		Size: 12.4 MB (12425522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd90b85ec56d01899b69ae42c6a2d4db6588cac958fa0bc8f7eb4da93075fdeb`  
		Last Modified: Wed, 22 Apr 2026 01:27:01 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e54b1d57a2087ce5ce6d74c4dbac61a99833db378f622c700c431e40eb69a61a`  
		Last Modified: Wed, 22 Apr 2026 01:27:01 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f0a1c4db094a3be4d3abd0dab72f96131394dcdc4c086f78796a69654927c9`  
		Last Modified: Wed, 22 Apr 2026 01:27:02 GMT  
		Size: 9.3 KB (9261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b560ccf1148fd4bd3a3f391403a305f5aa28f3b7a3927803be5077398c6343b`  
		Last Modified: Wed, 22 Apr 2026 03:52:06 GMT  
		Size: 90.9 KB (90869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290a5ebd949a13a28d1289424a1f665540f1246f9abf09f27c0fed360112a35c`  
		Last Modified: Wed, 22 Apr 2026 03:52:06 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a60aa873ca3987e1f7d439bfadfc30426eac6826ee49fe977a7a105f09f459fd`  
		Last Modified: Wed, 22 Apr 2026 03:52:07 GMT  
		Size: 6.0 MB (6048927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011e43b16a60de94f8329ea2dbdbe470f379982ab3ef7584832ffec831ffbfdb`  
		Last Modified: Wed, 22 Apr 2026 03:52:06 GMT  
		Size: 2.1 KB (2093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d7d75ae5016767c7f0a2c5518792988251c7def7eb30f3dcbf877f3afb9ccf`  
		Last Modified: Wed, 22 Apr 2026 03:52:07 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:e639bacaca0bb831c3b7f0489db161dddcbbb8bceb3d791113840153d0a89ecd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfdce03639e169e082ef1339e16c7065dd6d0229b51c2bad848eeffbd059ca95`

```dockerfile
```

-	Layers:
	-	`sha256:ace2b5798ced2f852ef6c0b8223ef5652aeda734115fb38b041c169f78cc08be`  
		Last Modified: Wed, 22 Apr 2026 03:52:06 GMT  
		Size: 26.8 KB (26769 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:dbc749d57bc5a0b2565bc7a8c1c987e4cebc576eaef284f7112c3815863a9392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **175.7 MB (175661345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31305f5844c5ee3d5206310607d52bdf01f6c64b2f14c52975183b0741da97ce`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:22:51 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:23:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:23:08 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:23:09 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:23:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:23:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:23:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:23:09 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 22 Apr 2026 01:23:09 GMT
ENV PHP_VERSION=8.5.5
# Wed, 22 Apr 2026 01:23:09 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 22 Apr 2026 01:23:09 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 22 Apr 2026 01:23:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:23:18 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:26:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:26:28 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:26:28 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:26:28 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:26:28 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:26:28 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 22 Apr 2026 01:26:28 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 Apr 2026 01:26:28 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 22 Apr 2026 01:26:28 GMT
CMD ["php-fpm"]
# Wed, 22 Apr 2026 02:30:43 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Wed, 22 Apr 2026 02:30:44 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Wed, 22 Apr 2026 02:30:45 GMT
ARG YOURLS_VERSION=1.10.3
# Wed, 22 Apr 2026 02:30:45 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Wed, 22 Apr 2026 02:30:45 GMT
ENV YOURLS_VERSION=1.10.3
# Wed, 22 Apr 2026 02:30:45 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Wed, 22 Apr 2026 02:30:45 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Wed, 22 Apr 2026 02:30:45 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Wed, 22 Apr 2026 02:30:45 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:30:45 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Wed, 22 Apr 2026 02:30:45 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2fc707a20497f7b5d0b9c4ecbe2e2ca451c3010214cd57e0adfa27293237e6c`  
		Last Modified: Wed, 22 Apr 2026 01:26:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f6fad25c12040d95703eafd336ca0b921b3736fbfa031fe7bf6c925b82e381`  
		Last Modified: Wed, 22 Apr 2026 01:26:51 GMT  
		Size: 110.2 MB (110165004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089f7f311938490a3dc2e97c430055eb5d7f9ee88e8de854b49d67a60161c5d3`  
		Last Modified: Wed, 22 Apr 2026 01:25:55 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eca36d630c38f06700003df08975d3601c27a6934034aaec2ea086e639c69e74`  
		Last Modified: Wed, 22 Apr 2026 01:26:48 GMT  
		Size: 14.5 MB (14503000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87c5c5448f1f1c41b68b3dc87629ddf3e72c81d589f6990b5a93f48618b3159b`  
		Last Modified: Wed, 22 Apr 2026 01:26:49 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afec6730ac94900d578ac4ef0ff3ef41241e8bf5b0a52ddd7d0da63f3c80b3f6`  
		Last Modified: Wed, 22 Apr 2026 01:26:50 GMT  
		Size: 14.7 MB (14678015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:947609f15e0cc0da3f50160eac681ddaa90c50984714700762c237fce998c4b4`  
		Last Modified: Wed, 22 Apr 2026 01:26:50 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d7bbf546d1f7f044dd40de1a78df864a2596664295c37a2ee7f6a866a5f669`  
		Last Modified: Wed, 22 Apr 2026 01:26:50 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de728b0fa0ad62f1a677e0e3c8adf245bae2791abe493a6b8ac4f54516eb3723`  
		Last Modified: Wed, 22 Apr 2026 01:26:51 GMT  
		Size: 9.3 KB (9265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d98d524faf7bc97bdac88dc222870acce27fb751f3cf2eff9bc6953a43560a`  
		Last Modified: Wed, 22 Apr 2026 02:30:50 GMT  
		Size: 105.8 KB (105753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b031e71d1a753d0f975fb6a2399ee8289fc578d5c8da576a8f1f3b771b3106`  
		Last Modified: Wed, 22 Apr 2026 02:30:50 GMT  
		Size: 326.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2c670a2554301c14965eef53630d0edd68d76d9a904af1b9f4890c58c083e0`  
		Last Modified: Wed, 22 Apr 2026 02:30:50 GMT  
		Size: 6.0 MB (6048924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61f3f7d5c6150f8f398b0cfe80e7ea771106f61ee5a428cff136ea93931430d5`  
		Last Modified: Wed, 22 Apr 2026 02:30:50 GMT  
		Size: 2.1 KB (2093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15e78e5bcce002e2dd6cf6e73735037433f15b051544874922a4df4bbfcadc6`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:3650b3caa9d4bd957937b2f2ea07366d95d72bb0d903840dd581308919e87cb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 KB (26808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213b13b49ee012edd3e6714f03f7d8f1c2d34bf135ca82520773236e22e13338`

```dockerfile
```

-	Layers:
	-	`sha256:e9ff354e6ed82596e20ea60f37730321c5e97f18d17dd97450150cd258f89ec1`  
		Last Modified: Wed, 22 Apr 2026 02:30:50 GMT  
		Size: 26.8 KB (26808 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm` - linux; 386

```console
$ docker pull yourls@sha256:0eebf91d19356787f694d4660cfb8b787f801e74949e1d49d38ed608a4e34ec8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.5 MB (183549901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4f15c667b4677e4fb4525a37a1763a678f1838e73c90a57e8010507b468abdd`
-	Entrypoint: `["container-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:18:06 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 22 Apr 2026 01:18:24 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Apr 2026 01:18:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:18:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Apr 2026 01:18:24 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 22 Apr 2026 01:18:24 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:18:24 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Apr 2026 01:18:24 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Apr 2026 01:18:24 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 22 Apr 2026 01:18:24 GMT
ENV PHP_VERSION=8.5.5
# Wed, 22 Apr 2026 01:18:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 22 Apr 2026 01:18:24 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 22 Apr 2026 01:18:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:18:35 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:21:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:21:30 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:21:30 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:21:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:21:30 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:21:30 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 22 Apr 2026 01:21:30 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 Apr 2026 01:21:30 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 22 Apr 2026 01:21:30 GMT
CMD ["php-fpm"]
# Wed, 22 Apr 2026 05:02:08 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Wed, 22 Apr 2026 05:02:08 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Wed, 22 Apr 2026 05:02:09 GMT
ARG YOURLS_VERSION=1.10.3
# Wed, 22 Apr 2026 05:02:09 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Wed, 22 Apr 2026 05:02:09 GMT
ENV YOURLS_VERSION=1.10.3
# Wed, 22 Apr 2026 05:02:09 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Wed, 22 Apr 2026 05:02:09 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Wed, 22 Apr 2026 05:02:09 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Wed, 22 Apr 2026 05:02:09 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 05:02:09 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Wed, 22 Apr 2026 05:02:09 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38eb9b1263603a6b3b207487dbcebe389adabef709bebafce1f28417224dfc3`  
		Last Modified: Wed, 22 Apr 2026 01:21:48 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4ca906f4273fc60318b87fc644e166550636748f5cc23b3b798cc55371bee1`  
		Last Modified: Wed, 22 Apr 2026 01:21:52 GMT  
		Size: 116.1 MB (116144285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f51339c9912510dd1ae6eb156ffde81d856c6873e8006a47291133556216ebb`  
		Last Modified: Wed, 22 Apr 2026 01:21:49 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8885067c9663a7d1746411cef3f84f01e17e570fc67e31fcf8298a06017f5f7e`  
		Last Modified: Wed, 22 Apr 2026 01:21:50 GMT  
		Size: 14.5 MB (14502345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663759db9f385b7eae88aed73674089596e61cfb8885d95068b05d931aa7b57a`  
		Last Modified: Wed, 22 Apr 2026 01:21:50 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c35be6d15c66ae472a13ba9e1adafc79c9c305e3c4cad71fa15f11592adc700`  
		Last Modified: Wed, 22 Apr 2026 01:21:51 GMT  
		Size: 15.4 MB (15429158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c892460a1d3a3d6a5903e369fafd419e567f8b0cb7f63654c8450a3ca2281c1d`  
		Last Modified: Wed, 22 Apr 2026 01:21:51 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c651df2c2be2fd07a5920dca2fc0bed93638c0a7b9f0a9923815cdb55446e5`  
		Last Modified: Wed, 22 Apr 2026 01:21:51 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967ace6d58237135e627d5fa7c9e3cae2d11b49bcc0029b911094a8da43bd044`  
		Last Modified: Wed, 22 Apr 2026 01:21:52 GMT  
		Size: 9.3 KB (9263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:950eb62e51584b98585969ec822e16785350aef7c6c9e62e8afa6df153e29da8`  
		Last Modified: Wed, 22 Apr 2026 05:02:14 GMT  
		Size: 111.8 KB (111822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d19d89dd45da707a58bac1bf735dc0e4cdfc4caf0548abdb36566a2f7220103`  
		Last Modified: Wed, 22 Apr 2026 05:02:14 GMT  
		Size: 327.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cbbc6b0dfa2a35f58dace2b22081d1a300bdfe9ce61d820f6c40211df6d9605`  
		Last Modified: Wed, 22 Apr 2026 05:02:15 GMT  
		Size: 6.0 MB (6048924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7b35a899cecdb83c7d1be1f29c8bf340ffd70ee41cadca022a1ca2d9455fc2a`  
		Last Modified: Wed, 22 Apr 2026 05:02:14 GMT  
		Size: 2.1 KB (2094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20fa7e7638026b42708b9db32cb7830031e4ddc0da81181f8d38e0802b1beae4`  
		Last Modified: Wed, 22 Apr 2026 05:02:16 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:116fb902c3bb60727eda3654da81e8264f359679ae7d614fc52599561df7f5ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 KB (26637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f230740975a33515100ff7482683778e29cadd1c6dd72c21a18e7e431b428e6e`

```dockerfile
```

-	Layers:
	-	`sha256:71138548fe9058d946fc36263f1eea95822e5aa944e8a718a66c881771886274`  
		Last Modified: Wed, 22 Apr 2026 05:02:14 GMT  
		Size: 26.6 KB (26637 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm` - linux; ppc64le

```console
$ docker pull yourls@sha256:f63e6dfff2adb788786867607bad84a5b4dd6b11a45f14cee47f3d8d6fc03d21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.1 MB (179108679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c681a5db32b7971ae72081981b37901fd7b459bcd026f4f8f171ac8f9d0ffb08`
-	Entrypoint: `["container-entrypoint.sh"]`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 22 Apr 2026 01:54:51 GMT
ENV PHP_VERSION=8.5.5
# Wed, 22 Apr 2026 01:54:51 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 22 Apr 2026 01:54:51 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 22 Apr 2026 02:00:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 02:00:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:05:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 02:05:35 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 02:05:38 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 02:05:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 02:05:39 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 02:05:40 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 22 Apr 2026 02:05:40 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 Apr 2026 02:05:40 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 22 Apr 2026 02:05:40 GMT
CMD ["php-fpm"]
# Wed, 22 Apr 2026 09:36:42 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Wed, 22 Apr 2026 09:36:42 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Wed, 22 Apr 2026 09:36:44 GMT
ARG YOURLS_VERSION=1.10.3
# Wed, 22 Apr 2026 09:36:44 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Wed, 22 Apr 2026 09:36:44 GMT
ENV YOURLS_VERSION=1.10.3
# Wed, 22 Apr 2026 09:36:44 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Wed, 22 Apr 2026 09:36:44 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Wed, 22 Apr 2026 09:36:44 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Wed, 22 Apr 2026 09:36:45 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 09:36:45 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Wed, 22 Apr 2026 09:36:45 GMT
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
	-	`sha256:1b3912cbe5ded73a51d53f5055f769fa4f530154342e4896924819bef71aa798`  
		Last Modified: Wed, 22 Apr 2026 02:06:12 GMT  
		Size: 14.5 MB (14502628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51309d2fa98783151c9cd7e50bd49d7c434cfbb14519b6be16465e0c89991f8`  
		Last Modified: Wed, 22 Apr 2026 02:06:11 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe0d449d2757d070a605326d2fce883c1d4c9b7a8da020a63c2efc4d3b2a854`  
		Last Modified: Wed, 22 Apr 2026 02:06:12 GMT  
		Size: 15.2 MB (15225447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8de438cb13fbf044d290da277ff1d54b806b2b126d19b946168ff7dfe4130a`  
		Last Modified: Wed, 22 Apr 2026 02:06:11 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ca779a72e8e3f9dd95cf91b2888847b06668a7b206da7f68876385468db2dd`  
		Last Modified: Wed, 22 Apr 2026 02:06:12 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2933c56a11aa8066df5d46139cb436397e0199c958f8315cfa276a374854a1d`  
		Last Modified: Wed, 22 Apr 2026 02:06:12 GMT  
		Size: 9.3 KB (9267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc229d5f8ed2b5b235bf3da7185f035044a32a4b4e0d905ea5fe741d9f57b98`  
		Last Modified: Wed, 22 Apr 2026 09:36:52 GMT  
		Size: 117.3 KB (117315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec110d89ef9557a6a04011e69df2b272a43a398b893bee2fe0bde8b79d157f42`  
		Last Modified: Wed, 22 Apr 2026 09:36:52 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3e30d5b01516fc8e79afd9baeb10c2245fe7df44c72603d7dd6df3a798abf84`  
		Last Modified: Wed, 22 Apr 2026 09:36:53 GMT  
		Size: 6.0 MB (6048923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e78f80246e6ac9e4f60f584afeacc48deb65159c40cf4d193e27e6079b0b90`  
		Last Modified: Wed, 22 Apr 2026 09:36:52 GMT  
		Size: 2.1 KB (2093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1903e1ec87ba92240186a6d5c6f8974d3af0eb4f0eb35381dab0b5a1a43e76cd`  
		Last Modified: Wed, 22 Apr 2026 09:36:53 GMT  
		Size: 1.7 KB (1690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:ac29d92131668b1717e78239a12c1cae54ec9a530364f73fa69a2eea6226dcd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa59ad80bd14a32b653d6b1e6a4b14e0408a279ca0722392cbe2e953873ed029`

```dockerfile
```

-	Layers:
	-	`sha256:548ca2a28cdecb964435d148f8491aec9885e6c166e4fbfbe46654e1dd76c01f`  
		Last Modified: Wed, 22 Apr 2026 09:36:52 GMT  
		Size: 26.7 KB (26721 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm` - linux; riscv64

```console
$ docker pull yourls@sha256:3df14d2a3ebec9288966458b339e404e3f3a583c5677fd58b0a69e1098685cf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.6 MB (209612774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddec06f635b77f56d984029fc90cbcb33fc3ccccfc95faf9fdaf54f3f3cb8a66`
-	Entrypoint: `["container-entrypoint.sh"]`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 22 Apr 2026 14:30:22 GMT
ENV PHP_VERSION=8.5.5
# Wed, 22 Apr 2026 14:30:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 22 Apr 2026 14:30:22 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 22 Apr 2026 14:31:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 14:31:29 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 17:32:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 17:32:25 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 17:32:25 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 17:32:25 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 17:32:26 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 17:32:26 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 22 Apr 2026 17:32:26 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 Apr 2026 17:32:26 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 22 Apr 2026 17:32:26 GMT
CMD ["php-fpm"]
# Sat, 25 Apr 2026 23:02:36 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Sat, 25 Apr 2026 23:02:36 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Sat, 25 Apr 2026 23:02:40 GMT
ARG YOURLS_VERSION=1.10.3
# Sat, 25 Apr 2026 23:02:40 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Sat, 25 Apr 2026 23:02:40 GMT
ENV YOURLS_VERSION=1.10.3
# Sat, 25 Apr 2026 23:02:40 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Sat, 25 Apr 2026 23:02:40 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Sat, 25 Apr 2026 23:02:40 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Sat, 25 Apr 2026 23:02:40 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 25 Apr 2026 23:02:40 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Sat, 25 Apr 2026 23:02:40 GMT
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
	-	`sha256:85cfd26e7a1db3572ce893daf82b0588dae8f1a1373cd58fd4bff6bfea5afa49`  
		Last Modified: Wed, 22 Apr 2026 15:33:25 GMT  
		Size: 14.5 MB (14502374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec9b0529bab9265a556392973eebd9571c778b6c12735583b886973ce092638`  
		Last Modified: Wed, 22 Apr 2026 15:33:21 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78af17c22e6032d9c9d0847af931b63864a79afb1ef1eaadc075ba33bc7d9e80`  
		Last Modified: Wed, 22 Apr 2026 17:35:29 GMT  
		Size: 14.1 MB (14078676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2550d297b21fe8af6179769575b12aa3e4a267083b3325e44c2102ac4cdb33ef`  
		Last Modified: Wed, 22 Apr 2026 17:35:26 GMT  
		Size: 2.5 KB (2458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a24472c788164cceb390c1caf47cbdf48dfe213c4ebd1b12df77bd9c39bc0fa0`  
		Last Modified: Wed, 22 Apr 2026 17:35:26 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc815da74677457b86ae5a6452bb33d50cb48541c7a4c3e20e91e165da30e67b`  
		Last Modified: Wed, 22 Apr 2026 17:35:26 GMT  
		Size: 9.3 KB (9270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4494e296845e934e7efaac1a3f1f8621ac1bf62de3344c04b459b81436ad7d08`  
		Last Modified: Sat, 25 Apr 2026 23:03:29 GMT  
		Size: 106.6 KB (106577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4fe87cdc64aaf2e89d15e070b16e5c359e7113ef0de3ea22ca28d2bc181396`  
		Last Modified: Sat, 25 Apr 2026 23:03:29 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a02f1efd069ba96a7a19c12773ff24c1eef9afc0df2648a5e7dc742a25dcad`  
		Last Modified: Sat, 25 Apr 2026 23:03:30 GMT  
		Size: 6.0 MB (6048924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b62214a0e86473ec35bb808eb5bc23bcde062d36e512c4da7ee34ee22b4530c`  
		Last Modified: Sat, 25 Apr 2026 23:03:29 GMT  
		Size: 2.1 KB (2097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ff66b2095c407b81cbcdc00d5f423ef7d55df9c894dfe2ad50f17b86e498633`  
		Last Modified: Sat, 25 Apr 2026 23:03:30 GMT  
		Size: 1.7 KB (1696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:ead185042f247b857fa34b2a38dae78cf6d877684f7d7462c15b7defa9bc5822
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e086bfd73d2423ffb7b86d2e17f5fd3a4c7aad6bb01b452912e06515733914`

```dockerfile
```

-	Layers:
	-	`sha256:b661f8d347521130eba34b5a15abb791a65947e703407d3574c179e1f0852f0b`  
		Last Modified: Sat, 25 Apr 2026 23:03:28 GMT  
		Size: 26.7 KB (26722 bytes)  
		MIME: application/vnd.in-toto+json

### `yourls:1-fpm` - linux; s390x

```console
$ docker pull yourls@sha256:f7be3c2ecb97c9fbfebee30e849866a4fa642575696dd80053074417ea3507c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.5 MB (157504664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e72038e0d534e09b86f46fb9253d20a1a2a4e028531987ca33e1d20cd9d53da0`
-	Entrypoint: `["container-entrypoint.sh"]`
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
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC 49D9AF6BC72A80D6691719C8AA23F5BE9C7097D4 D95C03BC702BE9515344AE3374E44BC9067701A5
# Wed, 22 Apr 2026 01:22:21 GMT
ENV PHP_VERSION=8.5.5
# Wed, 22 Apr 2026 01:22:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.5.5.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.5.5.tar.xz.asc
# Wed, 22 Apr 2026 01:22:21 GMT
ENV PHP_SHA256=95bec382f4bd00570a8ef52a58ec04d8d9b9a90494781f1c106d1b274a3902f2
# Wed, 22 Apr 2026 01:22:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	apt-get dist-clean; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 	export GNUPGHOME="$(mktemp -d)"; 	for key in $GPG_KEYS; do 		gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 	done; 	gpg --batch --verify php.tar.xz.asc php.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME"; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 22 Apr 2026 01:22:31 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:30:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	test "$PHP_INI_DIR" != "${PHP_INI_DIR%/php}"; 	./configure 		--build="$gnuArch" 		--sysconfdir="${PHP_INI_DIR%/php}" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 22 Apr 2026 01:30:01 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 01:30:01 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 22 Apr 2026 01:30:01 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Apr 2026 01:30:01 GMT
WORKDIR /var/www/html
# Wed, 22 Apr 2026 01:30:01 GMT
RUN set -eux; 	cd "${PHP_INI_DIR%/php}"; 		cp -v php-fpm.conf.default php-fpm.conf; 	cp -v php-fpm.d/www.conf.default php-fpm.d/www.conf; 		grep -E '^listen = 127.0.0.1:9000' php-fpm.d/www.conf; 	sed -ri 's/^(listen = 127.0.0.1:9000)/;\1/' php-fpm.d/www.conf; 	grep -E '^;listen = 127.0.0.1:9000' php-fpm.d/www.conf; 		{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 		echo; 		echo '; default listen address for easy override in later php-fpm.d/*.conf files'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '; the [www] ini section below is for backwards compatibility and will be removed in 8.6+'; 		echo '[www]'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 22 Apr 2026 01:30:01 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 Apr 2026 01:30:01 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 22 Apr 2026 01:30:01 GMT
CMD ["php-fpm"]
# Wed, 22 Apr 2026 04:20:12 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)"     bcmath     pdo_mysql     mysqli # buildkit
# Wed, 22 Apr 2026 04:20:12 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > "$PHP_INI_DIR/conf.d/opcache-recommended.ini" # buildkit
# Wed, 22 Apr 2026 04:20:13 GMT
ARG YOURLS_VERSION=1.10.3
# Wed, 22 Apr 2026 04:20:13 GMT
ARG YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Wed, 22 Apr 2026 04:20:13 GMT
ENV YOURLS_VERSION=1.10.3
# Wed, 22 Apr 2026 04:20:13 GMT
ENV YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
# Wed, 22 Apr 2026 04:20:13 GMT
# ARGS: YOURLS_VERSION=1.10.3 YOURLS_SHA256=71749ae9b3950d6a7c043b1240aba8645e912c3c22eac5abfb6ae3cc576ff740
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls # buildkit
# Wed, 22 Apr 2026 04:20:13 GMT
COPY --chown=www-data:www-data config-container.php /usr/src/yourls/user/ # buildkit
# Wed, 22 Apr 2026 04:20:13 GMT
COPY container-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 04:20:13 GMT
ENTRYPOINT ["container-entrypoint.sh"]
# Wed, 22 Apr 2026 04:20:13 GMT
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
	-	`sha256:55119a11285f22fee8fc4aa5dece7566f2d3d2a63cfa8e69784d39b03264bfb0`  
		Last Modified: Wed, 22 Apr 2026 01:26:46 GMT  
		Size: 14.5 MB (14501733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094b87eb3fc7a4e85922a8df018044afb8ea34c8648f28afef15943cc5569d20`  
		Last Modified: Wed, 22 Apr 2026 01:26:47 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a185d44e74d7efdde70debdf9374a5d18183f001a55d582e58405d06975dd9`  
		Last Modified: Wed, 22 Apr 2026 01:30:19 GMT  
		Size: 14.4 MB (14412133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f77e046003796e7f174781e0cf2dbd9f96a9e2feda63d6f7a66da10b0af9048`  
		Last Modified: Wed, 22 Apr 2026 01:30:18 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a4e8f28d415d67a7146f46f9de88d11e45c209bc110fcd08e483174311b7f2`  
		Last Modified: Wed, 22 Apr 2026 01:30:19 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50258664a83a05510c8edfed9c56a685aa680cd1d84e6d14d77ee04c8e869d2d`  
		Last Modified: Wed, 22 Apr 2026 01:30:19 GMT  
		Size: 9.3 KB (9263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406f6c08327ec00f3b7df195fc0579d20c45633b0fd449738848240452084ad7`  
		Last Modified: Wed, 22 Apr 2026 04:20:22 GMT  
		Size: 111.7 KB (111691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbf9de60221532e7fe69f3cdd569d547b52e01f449d9fcf290da2e57ae8b7eb`  
		Last Modified: Wed, 22 Apr 2026 04:20:22 GMT  
		Size: 328.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6647e88ed51d4869f848e83ef6f97195d8954cc68e87470dd195226825db9cb`  
		Last Modified: Wed, 22 Apr 2026 04:20:22 GMT  
		Size: 6.0 MB (6048921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82569d22b633c20321e363875a5db926de65bd80bc3e95bfd38a44aa5b6d5f67`  
		Last Modified: Wed, 22 Apr 2026 04:20:22 GMT  
		Size: 2.1 KB (2092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42220c250ff51e4696f117c9e1f48003251de4658754ff73be6dd4521531b923`  
		Last Modified: Wed, 22 Apr 2026 04:20:23 GMT  
		Size: 1.7 KB (1691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `yourls:1-fpm` - unknown; unknown

```console
$ docker pull yourls@sha256:857654084317b281bc65052a91b255be96d68f5ea5387788f2056e79067a3e7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 KB (26668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ee1aa5ac2ea38b4866a5cd97f30101e520d100cccfab343e66c91aaea287ed7`

```dockerfile
```

-	Layers:
	-	`sha256:a7645e08214fbbf845ddcd1131c0ce41e4542bdc4a72bcc3c9ffb7cf4b185dfb`  
		Last Modified: Wed, 22 Apr 2026 04:20:22 GMT  
		Size: 26.7 KB (26668 bytes)  
		MIME: application/vnd.in-toto+json
