## `backdrop:1-fpm`

```console
$ docker pull backdrop@sha256:19a5c6efb89af64bb15e6bc8da77742f5ec6e8e34109d7c4ec75e1beec663b18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `backdrop:1-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:c06ca8783fc0a63356ba7d641c4c3804697a4452a53ab81a1b6686578928e6fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.4 MB (187438284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5abacea4c56284b44617ea397463c8dc54ff1c766818ef96b6aec288e5db0cbe`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 21 Mar 2025 15:18:44 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Fri, 21 Mar 2025 15:18:44 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 21 Mar 2025 15:18:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 21 Mar 2025 15:18:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 21 Mar 2025 15:18:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 21 Mar 2025 15:18:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 21 Mar 2025 15:18:44 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 21 Mar 2025 15:18:44 GMT
ENV PHP_VERSION=8.3.20
# Fri, 21 Mar 2025 15:18:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.20.tar.xz.asc
# Fri, 21 Mar 2025 15:18:44 GMT
ENV PHP_SHA256=f15914e071b5bddaf1475b5f2ba68107e8b8846655f9e89690fb7cd410b0db6c
# Fri, 21 Mar 2025 15:18:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 21 Mar 2025 15:18:44 GMT
WORKDIR /var/www/html
# Fri, 21 Mar 2025 15:18:44 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
STOPSIGNAL SIGQUIT
# Fri, 21 Mar 2025 15:18:44 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 21 Mar 2025 15:18:44 GMT
CMD ["php-fpm"]
# Fri, 21 Mar 2025 15:18:44 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
WORKDIR /var/www/html
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_VERSION=1.30.2
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_MD5=9b85d7f71531b7eaf3e476e6666d0c0f
# Fri, 21 Mar 2025 15:18:44 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Mar 2025 15:18:44 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76c87c15113d85f4c22b0e0eeb60c0133cec0a644c93df8ea4cce3b58914bdfa`  
		Last Modified: Mon, 28 Apr 2025 21:54:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e7e72810f6381a4ac5bb94aee61b5b9fc04828ba83d6eefcfd482deabfa0666`  
		Last Modified: Mon, 28 Apr 2025 21:54:17 GMT  
		Size: 104.3 MB (104325257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e7b460a4bdc7bec868d0b694682988d6243690ad6c7b329d27be906b3e61af`  
		Last Modified: Mon, 28 Apr 2025 21:54:15 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7a2294186d6642bdd95b6404ca55391dac18a54b4d2830ba6ebf840b2a045d`  
		Last Modified: Mon, 28 Apr 2025 21:54:16 GMT  
		Size: 12.7 MB (12658348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c943d13d0aa4755204f8c40e039ec8110cf4247f8fad00ac543ae6726a413dca`  
		Last Modified: Mon, 28 Apr 2025 21:54:16 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91af39dbce2f5f4f1757db58e5a2e942af8660d05f4aa12a040d1c1cef3fb15`  
		Last Modified: Mon, 28 Apr 2025 21:54:16 GMT  
		Size: 27.8 MB (27827318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c70e19de0368362b4d1480aa3be64c8f2f39038507b3dfa6b9233fdd51266b`  
		Last Modified: Mon, 28 Apr 2025 21:54:17 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57731ba0321bd4651d6acfffc859db2480cd662ba770d8c87a7a4294806e48b4`  
		Last Modified: Mon, 28 Apr 2025 21:54:17 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa96857e26af97e6463cf9457893d3fb0b7652f2560c6eb93a65825690620ccd`  
		Last Modified: Mon, 28 Apr 2025 21:54:18 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127d00dec72b29dd24b8cac05691fdd79ac8676ab6051c26572e35c402abd610`  
		Last Modified: Mon, 28 Apr 2025 22:15:52 GMT  
		Size: 5.6 MB (5588133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de25bed4cc9d6e77f60caf377b27f3b568d5744a425c43e55844c7477f7a9f20`  
		Last Modified: Mon, 28 Apr 2025 22:15:52 GMT  
		Size: 8.8 MB (8797761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9424dde557e4029f91ff2fdb0f5a2b652f176eacf7497dab83cabc5aa029a0ca`  
		Last Modified: Mon, 28 Apr 2025 22:15:52 GMT  
		Size: 950.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:bcfa8efc7095e349523d0b4040c461286b62b487b623e33f5386c2f3f3df455f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6452748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b98a5b7e28fcf610580c2d5d3fb138052bc991b68eb2d8fa2efb1b6b60831bf`

```dockerfile
```

-	Layers:
	-	`sha256:248a6f0712707cb136c1e2bedbebfa27a20897c60da7d9c6c31cb065449f2e7a`  
		Last Modified: Mon, 28 Apr 2025 22:15:52 GMT  
		Size: 6.4 MB (6431164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b70edd854eece5c59aa6a357783328ba45865fb1674b89e663fa923b161b5a65`  
		Last Modified: Mon, 28 Apr 2025 22:15:52 GMT  
		Size: 21.6 KB (21584 bytes)  
		MIME: application/vnd.in-toto+json

### `backdrop:1-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:a3fc6c51d81f096615d657708e292c28c1f9f5cc4452fc4efa11fe307ef35cbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **181.0 MB (181044687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b00a838cf95740b5ed8426cc6a8d5a96d58fe381943d0fed8fd8b4137eb16340`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 21 Mar 2025 15:18:44 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Fri, 21 Mar 2025 15:18:44 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 21 Mar 2025 15:18:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 21 Mar 2025 15:18:44 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 21 Mar 2025 15:18:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 21 Mar 2025 15:18:44 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 21 Mar 2025 15:18:44 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Fri, 21 Mar 2025 15:18:44 GMT
ENV PHP_VERSION=8.3.20
# Fri, 21 Mar 2025 15:18:44 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.20.tar.xz.asc
# Fri, 21 Mar 2025 15:18:44 GMT
ENV PHP_SHA256=f15914e071b5bddaf1475b5f2ba68107e8b8846655f9e89690fb7cd410b0db6c
# Fri, 21 Mar 2025 15:18:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
RUN docker-php-ext-enable sodium # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 21 Mar 2025 15:18:44 GMT
WORKDIR /var/www/html
# Fri, 21 Mar 2025 15:18:44 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
STOPSIGNAL SIGQUIT
# Fri, 21 Mar 2025 15:18:44 GMT
EXPOSE map[9000/tcp:{}]
# Fri, 21 Mar 2025 15:18:44 GMT
CMD ["php-fpm"]
# Fri, 21 Mar 2025 15:18:44 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
WORKDIR /var/www/html
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_VERSION=1.30.2
# Fri, 21 Mar 2025 15:18:44 GMT
ENV BACKDROP_MD5=9b85d7f71531b7eaf3e476e6666d0c0f
# Fri, 21 Mar 2025 15:18:44 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites files # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
COPY docker-entrypoint.sh /entrypoint.sh # buildkit
# Fri, 21 Mar 2025 15:18:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Mar 2025 15:18:44 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afff2173127acd428d7c62aa9a2341113b1862a38b2320e911041f3caaef8da4`  
		Last Modified: Mon, 28 Apr 2025 22:43:21 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c7677ee413c3c4cf12dd2cf80a4a043439da4a6010129564155c572793aa96`  
		Last Modified: Mon, 28 Apr 2025 22:43:25 GMT  
		Size: 98.1 MB (98130507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96614c9ab0cf6b47b9768952cf480c72fb1a25a9f51960f66686ff34332a79f9`  
		Last Modified: Mon, 28 Apr 2025 22:43:21 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce00f2bcfda16a313557e6fd01f968d7977735cdb95454ae76effff3d400154`  
		Last Modified: Tue, 29 Apr 2025 00:02:21 GMT  
		Size: 12.7 MB (12658239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba2a5817379521540a0cb4a6b98f0c6a1518d3ed10dd120715581ca4d71d24a`  
		Last Modified: Tue, 29 Apr 2025 00:02:20 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da95bf68f38b987089cef291bad6e1bea34302b5bfd41bbffb677fe6ebe4b058`  
		Last Modified: Tue, 29 Apr 2025 00:06:19 GMT  
		Size: 27.8 MB (27774351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2721da0ce726276faf6f6b6a6aab1220dc4a76394410b6fa04a182199dc81556`  
		Last Modified: Tue, 29 Apr 2025 00:06:18 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6695f14fb3c1f32f2b8f3ac522e70064571639abe237a8d6cc8924258aa009d9`  
		Last Modified: Tue, 29 Apr 2025 00:06:18 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2003248220073050fbe2ffcacfb64d2f37a6c7988af985cd349d0721ec4f8273`  
		Last Modified: Tue, 29 Apr 2025 00:06:18 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aab105068e11661c04996e9aaa33e95690ab91475de39cddbac42612fefeede`  
		Last Modified: Tue, 29 Apr 2025 18:36:28 GMT  
		Size: 5.6 MB (5603387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7c91907898803b6ad3c05a5414b86dd890e773074ce62a9bb9588bc9c684e1`  
		Last Modified: Tue, 29 Apr 2025 18:36:29 GMT  
		Size: 8.8 MB (8797761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b10038b440c6505d6028f6b7f375ff8993002b916c44a2454c446060b8b0bb6a`  
		Last Modified: Tue, 29 Apr 2025 18:36:27 GMT  
		Size: 948.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `backdrop:1-fpm` - unknown; unknown

```console
$ docker pull backdrop@sha256:0206d93e9ee94d5e6ffedbdaaad5cf29947d83e557b23f1255fdda754eac1dc0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6481278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fe6c68b8b62b090cc8bda73f9adf164144c8109252a122b957ba82caa85362d`

```dockerfile
```

-	Layers:
	-	`sha256:513ac2f33d6de93fb81b752d1fd29978be7f258ed26388b0555164693404e317`  
		Last Modified: Tue, 29 Apr 2025 18:36:28 GMT  
		Size: 6.5 MB (6459580 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86d80781e007d0074d22b7120b001d5448cdb0efa46e6512715285ff62ef4751`  
		Last Modified: Tue, 29 Apr 2025 18:36:27 GMT  
		Size: 21.7 KB (21698 bytes)  
		MIME: application/vnd.in-toto+json
