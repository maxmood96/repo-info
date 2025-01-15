## `php:8-fpm-bullseye`

```console
$ docker pull php@sha256:e0b6f12de113906013babb41a2b2adc26aebc2449de4071c9d3095d8ddb5d514
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `php:8-fpm-bullseye` - linux; amd64

```console
$ docker pull php@sha256:fba88df26210f37ab8a0ec23b9f47e7cd5bbbcff04cfe3c89e45dcccf345882b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.4 MB (164356881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38e28bba0c9f16e894a2afb7e8a6b1a65d85e9540f1e953e13b85c5c69606dfb`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 20:11:07 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1736726400'
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 20:11:07 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_VERSION=8.4.2
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 20:11:07 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
STOPSIGNAL SIGQUIT
# Thu, 19 Dec 2024 20:11:07 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 19 Dec 2024 20:11:07 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:89320e7119e225692d79aaeb4989a18d7f97daafdb2b3782f84a0a8de31a09de`  
		Last Modified: Tue, 14 Jan 2025 20:33:08 GMT  
		Size: 30.3 MB (30252665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398b12062cb78eb767d812bb3fa9a2e18740be96d18974019d8311b13be91c48`  
		Last Modified: Tue, 14 Jan 2025 23:11:30 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a263ea2e9317773dd156e31b9ed065aea13d20412247eeb9a8bbf1663d55d65f`  
		Last Modified: Tue, 14 Jan 2025 23:11:40 GMT  
		Size: 91.4 MB (91448259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9642e6e757f657297a1b3428254c8d3b1e60e3f3d2367526c74a0b9258087a93`  
		Last Modified: Tue, 14 Jan 2025 23:48:54 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e9599271b68a8f6a80a422852b3defaf6559c8a39129d0bc91873bfb5002cb5`  
		Last Modified: Tue, 14 Jan 2025 23:55:18 GMT  
		Size: 13.7 MB (13662568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b489f2f494396d3a68d18ad21a8c2a33be3531390ff02933e48fc4cc98adcc80`  
		Last Modified: Tue, 14 Jan 2025 21:57:46 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f9fcdf2e800778129c712958e42842209518fcc885267f0173bb614293f6d8`  
		Last Modified: Tue, 14 Jan 2025 02:29:16 GMT  
		Size: 29.0 MB (28980533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4569c2dd267d16fd999e3ab66406bf2a5d2b3b3407da1394adeca6c9397ba6d7`  
		Last Modified: Tue, 14 Jan 2025 23:48:56 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9fda025e7d112a2e0d80a496e480bf176f26e4003ef018d813d4e42ed77ba32`  
		Last Modified: Tue, 14 Jan 2025 02:29:17 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a28fa4fcde1c7d19d45a0a3f435056f503488d60dc596bf5171bd5ccb8704cb4`  
		Last Modified: Tue, 14 Jan 2025 02:29:17 GMT  
		Size: 9.2 KB (9195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-fpm-bullseye` - unknown; unknown

```console
$ docker pull php@sha256:52f29aa1801a3ab4c7c96b90e0ce731191946f996fd1e4ba55b5f2e095c1d7bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6433922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc62677192caa10e4e28e774418e59f77c59d2f9726684406b7e514b5012c814`

```dockerfile
```

-	Layers:
	-	`sha256:c89ace13c67be1413942207f3cea41e48bca5e13d5d813c24af15192b42eca7d`  
		Last Modified: Tue, 14 Jan 2025 02:29:15 GMT  
		Size: 6.4 MB (6383996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b779dad1e4c22c064f468aa3892e2654acbd0b6a2eeae438419c49e63ceea2f2`  
		Last Modified: Tue, 14 Jan 2025 02:29:15 GMT  
		Size: 49.9 KB (49926 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-fpm-bullseye` - linux; arm variant v7

```console
$ docker pull php@sha256:ebd5b4e30117d0394652a4890e88c1fc0c595b43eb0f27ea66709a0bbb352a4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134740751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da6d128738b12442f15bdb802bc78de07eacf511e0297b3bb1acb76f4fbdcded`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 20:11:07 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1736726400'
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 20:11:07 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_VERSION=8.4.2
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 20:11:07 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
STOPSIGNAL SIGQUIT
# Thu, 19 Dec 2024 20:11:07 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 19 Dec 2024 20:11:07 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:61fe776d618d9b70bea09742b3fce817da0393e8911c90f01094c0a407e1f7bf`  
		Last Modified: Tue, 14 Jan 2025 20:45:43 GMT  
		Size: 25.5 MB (25533960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d93b737d9d37bd60c8605bf5c054750994a7d9bf9fcc44b376fd7249244abcf`  
		Last Modified: Tue, 14 Jan 2025 03:05:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69002742768de244d879a330315c30a076fb9fcc3e1b1e78748310f0f812a011`  
		Last Modified: Tue, 14 Jan 2025 23:27:39 GMT  
		Size: 69.1 MB (69119271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b30d38aa9fbc72534a04c8660b325338232f5eb41922619c41d2da02e32be09f`  
		Last Modified: Tue, 14 Jan 2025 03:05:14 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6b2d7d7cfe7714ba59a4051743d76880dd7b678d73e0ac7d3b653163f1ba0b1`  
		Last Modified: Tue, 14 Jan 2025 03:39:40 GMT  
		Size: 13.7 MB (13660967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d75e1bd9f74565eb4eaf3623197285cc75be6eb5a1fc8ec4014e85a81e336e`  
		Last Modified: Tue, 14 Jan 2025 03:39:39 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc99ae217723382237fc5a9762f028e6e3dcfd6afb73cb17c06a018504ff503`  
		Last Modified: Tue, 14 Jan 2025 03:47:04 GMT  
		Size: 26.4 MB (26413697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a349945eb3b370a18a1297bdea1b05155d166b35687be56bf98da89f30e864`  
		Last Modified: Tue, 14 Jan 2025 03:47:03 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c595d2b3f68e6152a16c051e61af519cb3b0c0e87521a3ff85c35fe703d9e1f6`  
		Last Modified: Tue, 14 Jan 2025 03:47:03 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef96ca01685aa94b58a03aa1d26f5e2c3f5842c50325408b86671c2060b0760`  
		Last Modified: Tue, 14 Jan 2025 03:47:03 GMT  
		Size: 9.2 KB (9196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-fpm-bullseye` - unknown; unknown

```console
$ docker pull php@sha256:d88d4281affe8b72e8886244d1e70c998fdf21784b1eec256f78d5301b199386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6242891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30d3c777e335bd4c434c61949dcd1d5517f31229e081d29ad99c7930f6319036`

```dockerfile
```

-	Layers:
	-	`sha256:34444a9a39367d30ddc3ed5b5270140c55ec33adc3db0c116e27a78b41f5960a`  
		Last Modified: Tue, 14 Jan 2025 03:47:03 GMT  
		Size: 6.2 MB (6192811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de0e4eecd36c49f0ba9ee53ef985eb48e2f18324d24a819235f2f72c70b20b8c`  
		Last Modified: Tue, 14 Jan 2025 03:47:02 GMT  
		Size: 50.1 KB (50080 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-fpm-bullseye` - linux; arm64 variant v8

```console
$ docker pull php@sha256:b951e92a05e3d29d930215d135dafb8ecc8d7d0a448f82c7a42da738d73b6fd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157808569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:904020e7d8ee26b14aee1be69125fa128c135f95afc4e572bd3989b83e2f7b28`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 20:11:07 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1736726400'
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 20:11:07 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_VERSION=8.4.2
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 20:11:07 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
STOPSIGNAL SIGQUIT
# Thu, 19 Dec 2024 20:11:07 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 19 Dec 2024 20:11:07 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6a43d3167ec1fb9f3b40bf3e095c86abebf31d406e2de1d196433c26d262f72c`  
		Last Modified: Tue, 14 Jan 2025 01:36:26 GMT  
		Size: 28.7 MB (28744913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:798f4885259ede04563f6f2c30252c470e94aaf9a95576060866ba0ca177a1b8`  
		Last Modified: Tue, 14 Jan 2025 03:28:41 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f91a0cfe9d2540e4d05e8198913405c46a9a624800b104db09fb49ea98a3d13e`  
		Last Modified: Tue, 14 Jan 2025 03:28:44 GMT  
		Size: 86.7 MB (86734429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b3d3d9ba2fe6d1d3be940377c1fbbc1ab8489811531766e34900760d284128`  
		Last Modified: Tue, 14 Jan 2025 20:45:04 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740d7951f16fab4cd28552c6cc154a4e9399c1dcbc346e048a14f153cc2a2250`  
		Last Modified: Tue, 14 Jan 2025 03:55:16 GMT  
		Size: 13.7 MB (13661832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca9c22b6f89ffc6e1e7d44c8358a6c747f4e85f1e73837d7986ebf9aefb306b2`  
		Last Modified: Tue, 14 Jan 2025 21:57:13 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4383aef1b4b62bf3c8bb5b15e57e69f942c7e98ee510bca38fd90096fbb004`  
		Last Modified: Tue, 14 Jan 2025 04:01:32 GMT  
		Size: 28.7 MB (28654536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5cdb72b18d7b94f938c00aaa478e9994957a6c92f0eee4be951462e8341ce8`  
		Last Modified: Tue, 14 Jan 2025 04:01:31 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4198129f0a36193c28ad6bae5b37bfbe9654231381dd312d1eb61f71bdbc32a`  
		Last Modified: Tue, 14 Jan 2025 21:57:53 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8baeb96a76771688361d6abc175ef1ba1e004a08c443d1b91fa16bd733c9e77f`  
		Last Modified: Tue, 14 Jan 2025 21:57:54 GMT  
		Size: 9.2 KB (9198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-fpm-bullseye` - unknown; unknown

```console
$ docker pull php@sha256:c9ba03aa94a04b6c9c23b457f490e14398e84afdb5a1ce28c95454a02576a742
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6436885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c49f6c755e80b3da053b49fb5eefaef40901264379afcb48840f96143bd6803e`

```dockerfile
```

-	Layers:
	-	`sha256:59dfdb3454dfc298df2213ed301ec361f25a1387cada197e1af1d7d1cbd56a10`  
		Last Modified: Tue, 14 Jan 2025 04:01:31 GMT  
		Size: 6.4 MB (6386765 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8dbf7df571cd89cd710fa4ed32ed2b2e216274a6d3dc20d2bcf11f5ed3e61b3`  
		Last Modified: Tue, 14 Jan 2025 04:01:30 GMT  
		Size: 50.1 KB (50120 bytes)  
		MIME: application/vnd.in-toto+json

### `php:8-fpm-bullseye` - linux; 386

```console
$ docker pull php@sha256:7061d7ddfadd91bc69611693a78636baf3bc109a0e34709eb95195482c1c87d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.9 MB (166884199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982946ebaf1a50c7aa8ffe4857aef1fa1ecaf4986475c1ced0a2c19392db08b9`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 19 Dec 2024 20:11:07 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1736726400'
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 19 Dec 2024 20:11:07 GMT
ENV GPG_KEYS=AFD8691FDAEDF03BDF6E460563F15A9B715376CA 9D7F99A0CB8F05C8A6958D6256A97AF7600A39A6 0616E93D95AF471243E26761770426E17EBBB3DD
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_VERSION=8.4.2
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.4.2.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.4.2.tar.xz.asc
# Thu, 19 Dec 2024 20:11:07 GMT
ENV PHP_SHA256=92636453210f7f2174d6ee6df17a5811368f556a6c2c2cbcf019321e36456e01
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
RUN docker-php-ext-enable sodium # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 19 Dec 2024 20:11:07 GMT
WORKDIR /var/www/html
# Thu, 19 Dec 2024 20:11:07 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Thu, 19 Dec 2024 20:11:07 GMT
STOPSIGNAL SIGQUIT
# Thu, 19 Dec 2024 20:11:07 GMT
EXPOSE map[9000/tcp:{}]
# Thu, 19 Dec 2024 20:11:07 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a492ed0bb6cc66719b4111965f26bfd6269b1fc3ecb8620118584501f25cabde`  
		Last Modified: Tue, 14 Jan 2025 01:33:21 GMT  
		Size: 31.2 MB (31179029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd50d1d3e7d700c3b67d43620add0af9cf816a99faca4a473f0e235d97a375bf`  
		Last Modified: Tue, 14 Jan 2025 02:27:11 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a46af6f8ba61e83c6d7d96baa8a3e20d45af8f32f5d2b27af6ab2fc271c432`  
		Last Modified: Tue, 14 Jan 2025 02:27:15 GMT  
		Size: 92.5 MB (92521378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44d3bf1a35ca7bf71c0fb6b0133fc5caafbf526de657ec10e53b5e88e1e1f3dd`  
		Last Modified: Tue, 14 Jan 2025 02:27:11 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b04fb7f106f683a17b3e9999f12286cce7b914dd23e070900e04f7a2b5222f5`  
		Last Modified: Tue, 14 Jan 2025 02:27:12 GMT  
		Size: 13.7 MB (13661786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:258fb8c8a42ba8a6b5d29fe43d648239481dda767c3507cabf7b356ffbd87bdc`  
		Last Modified: Tue, 14 Jan 2025 02:27:12 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de213b72fb9e40fba37b6c4dbb3c1889a8478ec036f5626642537dd50f9fffb8`  
		Last Modified: Tue, 14 Jan 2025 02:27:13 GMT  
		Size: 29.5 MB (29509145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:659a16a5b43450e5f3d67774acd81ed9d13930b027006893e771b6f781c88b64`  
		Last Modified: Tue, 14 Jan 2025 02:27:13 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e4d8d776d657d51f0c5cd6cd4b4c113ae09c66f218a7d47dda87b7538a35c5`  
		Last Modified: Tue, 14 Jan 2025 02:27:13 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4b364deee843217ca44e3cd7638498d7318bbab614be59ebe7d6e2bab209df`  
		Last Modified: Tue, 14 Jan 2025 02:27:13 GMT  
		Size: 9.2 KB (9198 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `php:8-fpm-bullseye` - unknown; unknown

```console
$ docker pull php@sha256:e59589958fed11327375bcbc90d3b6f64b371acd6e35ab8723429c337b146ef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6424550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1940ba0165c786c5d656179ff71b842719ce873ec33a52ccdd9dc53355ccf784`

```dockerfile
```

-	Layers:
	-	`sha256:b5b34a7f1f80dbc9c5b3d1c65e2bf0a535bd05d8e6e3188db287e49ef16a0838`  
		Last Modified: Tue, 14 Jan 2025 02:27:11 GMT  
		Size: 6.4 MB (6374668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88e1eda6df9b9c44d723f1451e6d2d7da36960a2a694b53ed28f4eec0f298e21`  
		Last Modified: Tue, 14 Jan 2025 02:27:11 GMT  
		Size: 49.9 KB (49882 bytes)  
		MIME: application/vnd.in-toto+json
