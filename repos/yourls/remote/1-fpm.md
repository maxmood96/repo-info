## `yourls:1-fpm`

```console
$ docker pull yourls@sha256:58c36d5b23b3201efebeb50169da611296f7a3990726b50754aa6c6778706a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `yourls:1-fpm` - linux; amd64

```console
$ docker pull yourls@sha256:fe352d4a378ba6bb8acda19f3faf33c6d2a8cdecdb4e3eb8820d760185b5d154
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.1 MB (167058603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b06846e177a522b20c5eb110719dc0d40b05169659fe21c3c1b79cbdfc14a1fd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 21 Dec 2021 01:22:43 GMT
ADD file:09675d11695f65c55efdc393ff0cd32f30194cd7d0fbef4631eebfed4414ac97 in / 
# Tue, 21 Dec 2021 01:22:43 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 19:30:08 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 21 Dec 2021 19:30:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 21 Dec 2021 19:30:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 19:30:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 21 Dec 2021 19:30:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 21 Dec 2021 19:30:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Dec 2021 19:30:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Dec 2021 19:30:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 21 Dec 2021 20:28:48 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Thu, 20 Jan 2022 20:02:36 GMT
ENV PHP_VERSION=8.0.15
# Thu, 20 Jan 2022 20:02:36 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.15.tar.xz.asc
# Thu, 20 Jan 2022 20:02:37 GMT
ENV PHP_SHA256=5f33544061d37d805a2a9ce791f081ef08a7155bd7ba2362e69bba2d06b0f8b2
# Thu, 20 Jan 2022 20:03:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 20 Jan 2022 20:03:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jan 2022 20:25:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jan 2022 20:25:11 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Thu, 20 Jan 2022 20:25:12 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jan 2022 20:25:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jan 2022 20:25:13 GMT
WORKDIR /var/www/html
# Thu, 20 Jan 2022 20:25:14 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 20 Jan 2022 20:25:14 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Jan 2022 20:25:14 GMT
EXPOSE 9000
# Thu, 20 Jan 2022 20:25:14 GMT
CMD ["php-fpm"]
# Thu, 20 Jan 2022 23:43:31 GMT
LABEL org.opencontainers.image.title=YOURLS
# Thu, 20 Jan 2022 23:43:31 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Thu, 20 Jan 2022 23:43:32 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Thu, 20 Jan 2022 23:43:32 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Thu, 20 Jan 2022 23:43:32 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Thu, 20 Jan 2022 23:43:32 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Thu, 20 Jan 2022 23:43:32 GMT
LABEL org.opencontainers.image.version=1.8.2
# Thu, 20 Jan 2022 23:44:21 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Thu, 20 Jan 2022 23:44:21 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 20 Jan 2022 23:44:23 GMT
RUN set -eux;     version="1.8.2";     sha256="6d818622e3ba1d5785c2dbcc088be6890f5675fd4f24a2e3111eda4523bbd7ae";     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${version}.tar.gz";     echo "$sha256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${version}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 20 Jan 2022 23:44:23 GMT
COPY --chown=www-data:www-datafile:0bcfdfe0566007e7477c55552a1341b82b958e95879a5314f411d2188da2429e in /usr/src/yourls/user/ 
# Thu, 20 Jan 2022 23:44:24 GMT
COPY file:a47a395071c52d8d08402c95253924b09809713039b46033d6f6f75603938896 in /usr/local/bin/ 
# Thu, 20 Jan 2022 23:44:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jan 2022 23:44:24 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a2abf6c4d29d43a4bf9fbb769f524d0fb36a2edab49819c1bf3e76f409f953ea`  
		Last Modified: Tue, 21 Dec 2021 01:27:48 GMT  
		Size: 31.4 MB (31357624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5608244554dec85339ec1c4946f2ed8998a1d9e8592283a13dd7a6169919656`  
		Last Modified: Tue, 21 Dec 2021 22:41:48 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d07066487a0cbf4adc6fef4372421dfd28c101b62eb404118e440133b65d422`  
		Last Modified: Tue, 21 Dec 2021 22:42:04 GMT  
		Size: 91.6 MB (91604190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6dfaf1958c6d3e5fad6e48d4e8a6df231e94d65bde1c3df6a971203da8a1d5`  
		Last Modified: Tue, 21 Dec 2021 22:41:47 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3ca67bd70cd7a1d7afdeb77dc377ea76e983f9d89349cd6f92563febc36fa6`  
		Last Modified: Thu, 20 Jan 2022 21:50:08 GMT  
		Size: 11.1 MB (11083201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ccbfca43df3c06148740aae07353794993643c4fc4d496e9caf0e5f241f341`  
		Last Modified: Thu, 20 Jan 2022 21:50:07 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c873cc29e69b45aedda38fb34dd53ae0796c4649c35e6b7360c2bc5f774ae8e4`  
		Last Modified: Thu, 20 Jan 2022 21:51:09 GMT  
		Size: 29.8 MB (29756872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6831494fad0758717825af2da53633b8c00229bf443ec9e3582b5b18d8d92210`  
		Last Modified: Thu, 20 Jan 2022 21:51:04 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f8e332b5a7dec1613b13c4ed15394b9336ec233270625dea4a5d8affb67d4f9`  
		Last Modified: Thu, 20 Jan 2022 21:51:04 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06b32129aa8f11bd71bc9236127f73b4ee9d288ecb43fe9eae627093e48bda7`  
		Last Modified: Thu, 20 Jan 2022 21:51:04 GMT  
		Size: 8.6 KB (8574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f0365f89b7b64efa31f5107077ef535ad044ad576f489d49354fd12032ea9cf`  
		Last Modified: Thu, 20 Jan 2022 23:46:46 GMT  
		Size: 666.2 KB (666230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d409268725211e8ef8467e3ad75c27450bba0918cb4a0f1bd1c6698804b6f6`  
		Last Modified: Thu, 20 Jan 2022 23:46:47 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325569955e73e4d955771c0461c48589a1739c16c4d4f1d1264bb16300e102bf`  
		Last Modified: Thu, 20 Jan 2022 23:46:47 GMT  
		Size: 2.6 MB (2574446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:199ba035e93886f094a0a11b5099ca8b5ac30be4e2ec5f14866013c13c8967c5`  
		Last Modified: Thu, 20 Jan 2022 23:46:46 GMT  
		Size: 2.0 KB (2039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c98b5de2e4a68d3d10bbb8ffdb95de3db75640db83ad3a667ee166fee3d1cd4`  
		Last Modified: Thu, 20 Jan 2022 23:46:46 GMT  
		Size: 1.5 KB (1549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-fpm` - linux; arm variant v5

```console
$ docker pull yourls@sha256:4be71be24552d1a4e450c9e631337c34a97026d5ff844140b788239ca8d03d2d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144598062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c903f37fc212fb8094acf8d461904b96a6d6a04474097178324cc26725328bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 21 Dec 2021 01:50:31 GMT
ADD file:a3023f71bd93966e7db1419adda3ccde4fcc5e2e8cf58e7b13c51036ed5ff796 in / 
# Tue, 21 Dec 2021 01:50:32 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 03:59:53 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 21 Dec 2021 03:59:53 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 21 Dec 2021 04:00:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 04:00:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 21 Dec 2021 04:00:55 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 21 Dec 2021 04:00:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Dec 2021 04:00:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Dec 2021 04:00:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 21 Dec 2021 04:48:21 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Thu, 20 Jan 2022 19:51:45 GMT
ENV PHP_VERSION=8.0.15
# Thu, 20 Jan 2022 19:51:46 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.15.tar.xz.asc
# Thu, 20 Jan 2022 19:51:46 GMT
ENV PHP_SHA256=5f33544061d37d805a2a9ce791f081ef08a7155bd7ba2362e69bba2d06b0f8b2
# Thu, 20 Jan 2022 19:52:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 20 Jan 2022 19:52:16 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jan 2022 20:08:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jan 2022 20:08:12 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Thu, 20 Jan 2022 20:08:14 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jan 2022 20:08:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jan 2022 20:08:14 GMT
WORKDIR /var/www/html
# Thu, 20 Jan 2022 20:08:16 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 20 Jan 2022 20:08:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Jan 2022 20:08:17 GMT
EXPOSE 9000
# Thu, 20 Jan 2022 20:08:18 GMT
CMD ["php-fpm"]
# Fri, 21 Jan 2022 01:32:45 GMT
LABEL org.opencontainers.image.title=YOURLS
# Fri, 21 Jan 2022 01:32:45 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Fri, 21 Jan 2022 01:32:46 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Fri, 21 Jan 2022 01:32:46 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Fri, 21 Jan 2022 01:32:47 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Fri, 21 Jan 2022 01:32:47 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Fri, 21 Jan 2022 01:32:48 GMT
LABEL org.opencontainers.image.version=1.8.2
# Fri, 21 Jan 2022 01:34:01 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Fri, 21 Jan 2022 01:34:03 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 21 Jan 2022 01:34:06 GMT
RUN set -eux;     version="1.8.2";     sha256="6d818622e3ba1d5785c2dbcc088be6890f5675fd4f24a2e3111eda4523bbd7ae";     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${version}.tar.gz";     echo "$sha256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${version}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Fri, 21 Jan 2022 01:34:07 GMT
COPY --chown=www-data:www-datafile:0bcfdfe0566007e7477c55552a1341b82b958e95879a5314f411d2188da2429e in /usr/src/yourls/user/ 
# Fri, 21 Jan 2022 01:34:07 GMT
COPY file:a47a395071c52d8d08402c95253924b09809713039b46033d6f6f75603938896 in /usr/local/bin/ 
# Fri, 21 Jan 2022 01:34:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Jan 2022 01:34:08 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:054429d0cf4038fef39a3b5eb6ce52f600f9a2cbb71a4fb3e95ecf9b2da62581`  
		Last Modified: Tue, 21 Dec 2021 02:05:52 GMT  
		Size: 28.9 MB (28900253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4baf12a4235b144f3de87f3ca79e810afaf05728d988c6d002b17d5427d896f2`  
		Last Modified: Tue, 21 Dec 2021 07:06:41 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e2575fdbc3ac400a3f665d5895774c0e6b232dfbae749cd1e4bc49f8d60fe91`  
		Last Modified: Tue, 21 Dec 2021 07:07:31 GMT  
		Size: 73.7 MB (73683870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea7c814d6012464d1a56ac1010664916804cf016706f239ed03fed04e26eafb`  
		Last Modified: Tue, 21 Dec 2021 07:06:38 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187a20f4ef70fdf76cf7033f9a6f4eb1e32cbe22f920e4142f32f7d34859f795`  
		Last Modified: Thu, 20 Jan 2022 20:52:52 GMT  
		Size: 11.1 MB (11082021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d0289f26592ba3c1dde090c871b3c2f1c58878e5bca9422c6c5eaf4e1f11c46`  
		Last Modified: Thu, 20 Jan 2022 20:52:48 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6919da117fa69306655de7a11cb6c05e29cf9ccae38ceec22232a0e8ded827e8`  
		Last Modified: Thu, 20 Jan 2022 20:54:39 GMT  
		Size: 28.0 MB (28022899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e84cd80017a83dff3967c80f6b629926eb9d8e92f721693dd18107274604010`  
		Last Modified: Thu, 20 Jan 2022 20:54:20 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a1fdcdb2c1743092b535d25b4df12d4e360ca913573fde2ca80c9907b055b1`  
		Last Modified: Thu, 20 Jan 2022 20:54:21 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710f30466b64f0dd53566f16629e4771caec642157e8ccd4eb9c40d41cb25645`  
		Last Modified: Thu, 20 Jan 2022 20:54:20 GMT  
		Size: 8.6 KB (8577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93c16414c14201fc264d003ce455a8578d67dc486a7533248aafb7bc2089e6ca`  
		Last Modified: Fri, 21 Jan 2022 01:35:59 GMT  
		Size: 318.5 KB (318521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e68c30115f8c289d44fe212c4c118ada5b8024db8e3b2f99ca475d6c97eff25`  
		Last Modified: Fri, 21 Jan 2022 01:35:59 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23bc0ecf5c4719880c83c746be773bcd4df55c5fc3f87c095780b946d3d4d4da`  
		Last Modified: Fri, 21 Jan 2022 01:36:01 GMT  
		Size: 2.6 MB (2574447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aecad833660e7da9a38d15dbcea1c89520f3fde0e94d88f6419846af392ffe9`  
		Last Modified: Fri, 21 Jan 2022 01:35:59 GMT  
		Size: 2.0 KB (2043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2e3de1f116ea3b92515abe753db6827bd5ccab0522c92aea1fa5b9ee73619a`  
		Last Modified: Fri, 21 Jan 2022 01:35:59 GMT  
		Size: 1.6 KB (1551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-fpm` - linux; arm variant v7

```console
$ docker pull yourls@sha256:76af563d7446a8aa4bd8ec5cfdda8ce20dfbfd1a40738c5aa6488309874d829f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.9 MB (136850098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9918047a365ec0f10842dfebd9f68d7d860a2052e48d0ced311af4bb4e31a1a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 21 Dec 2021 01:59:48 GMT
ADD file:6a5555c3e40db91fae5bb112464a4c405a976de17ff64c98f25d3033a6a608d8 in / 
# Tue, 21 Dec 2021 01:59:48 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 10:05:19 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 21 Dec 2021 10:05:19 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 21 Dec 2021 10:06:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 10:06:06 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 21 Dec 2021 10:06:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 21 Dec 2021 10:06:08 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Dec 2021 10:06:08 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Dec 2021 10:06:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 21 Dec 2021 10:50:25 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Thu, 20 Jan 2022 20:28:05 GMT
ENV PHP_VERSION=8.0.15
# Thu, 20 Jan 2022 20:28:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.15.tar.xz.asc
# Thu, 20 Jan 2022 20:28:06 GMT
ENV PHP_SHA256=5f33544061d37d805a2a9ce791f081ef08a7155bd7ba2362e69bba2d06b0f8b2
# Thu, 20 Jan 2022 20:28:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 20 Jan 2022 20:28:38 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jan 2022 20:42:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jan 2022 20:42:50 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Thu, 20 Jan 2022 20:42:52 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jan 2022 20:42:52 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jan 2022 20:42:52 GMT
WORKDIR /var/www/html
# Thu, 20 Jan 2022 20:42:54 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 20 Jan 2022 20:42:55 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Jan 2022 20:42:55 GMT
EXPOSE 9000
# Thu, 20 Jan 2022 20:42:55 GMT
CMD ["php-fpm"]
# Fri, 21 Jan 2022 01:46:33 GMT
LABEL org.opencontainers.image.title=YOURLS
# Fri, 21 Jan 2022 01:46:34 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Fri, 21 Jan 2022 01:46:34 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Fri, 21 Jan 2022 01:46:35 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Fri, 21 Jan 2022 01:46:35 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Fri, 21 Jan 2022 01:46:36 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Fri, 21 Jan 2022 01:46:36 GMT
LABEL org.opencontainers.image.version=1.8.2
# Fri, 21 Jan 2022 01:47:46 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Fri, 21 Jan 2022 01:47:48 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 21 Jan 2022 01:47:51 GMT
RUN set -eux;     version="1.8.2";     sha256="6d818622e3ba1d5785c2dbcc088be6890f5675fd4f24a2e3111eda4523bbd7ae";     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${version}.tar.gz";     echo "$sha256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${version}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Fri, 21 Jan 2022 01:47:52 GMT
COPY --chown=www-data:www-datafile:0bcfdfe0566007e7477c55552a1341b82b958e95879a5314f411d2188da2429e in /usr/src/yourls/user/ 
# Fri, 21 Jan 2022 01:47:52 GMT
COPY file:a47a395071c52d8d08402c95253924b09809713039b46033d6f6f75603938896 in /usr/local/bin/ 
# Fri, 21 Jan 2022 01:47:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Jan 2022 01:47:53 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d0061d6703dc4975804c3419e00c85efbe3f1b79c86d87e048fa14a683e88e31`  
		Last Modified: Tue, 21 Dec 2021 02:15:26 GMT  
		Size: 26.6 MB (26560815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:762f25a36ce89a4171ec47f9f2c67d1681291f9f5944248ee7d93c1a7e3b0a4a`  
		Last Modified: Tue, 21 Dec 2021 13:09:14 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df607e3d79a26f2cb4fe08aa876a5732ebfedfef639fb1afc2fa95c784234826`  
		Last Modified: Tue, 21 Dec 2021 13:09:52 GMT  
		Size: 69.3 MB (69315261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e1598ec97c23b6bc2531b0153249fd96e021a195c84e096c876a00686244aa8`  
		Last Modified: Tue, 21 Dec 2021 13:09:14 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b6c85feba3d2cbcc472a1b303e9f1439c907b6023f4e90fab31e6adf48fc3a7`  
		Last Modified: Thu, 20 Jan 2022 21:55:08 GMT  
		Size: 11.1 MB (11081947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc17827dd5fd8f81884d76c7414ec2b19553a3963d06cd3dc5790822f319cf3`  
		Last Modified: Thu, 20 Jan 2022 21:55:05 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce5b0b5e7c2daa4926d4a18ac906fcbbf6bdf9ae2eaa7ce1a8779da29d5fece`  
		Last Modified: Thu, 20 Jan 2022 21:56:50 GMT  
		Size: 27.0 MB (27014545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3002584dbc993159f4f10f2760c8bc9a90e40049d910c0345db82288faf0152`  
		Last Modified: Thu, 20 Jan 2022 21:56:33 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:615c4ebdd92f2fbf1d21c2226af063e7ffaa1efe9778299f9418e85fe67c4c60`  
		Last Modified: Thu, 20 Jan 2022 21:56:33 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f4703fda4f8ebf31a94dcf7b86e76ab1d98b887b6ca307db7a908f22287f67`  
		Last Modified: Thu, 20 Jan 2022 21:56:33 GMT  
		Size: 8.6 KB (8575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d4e9bc9f28770ba754beb9af1930b48d5714cad04a5406475ad27c6f58e3218`  
		Last Modified: Fri, 21 Jan 2022 01:51:40 GMT  
		Size: 287.0 KB (287039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8104a375cc78cf497dde546d07e506d28b6fc1c4979ff7328d192945a694fe`  
		Last Modified: Fri, 21 Jan 2022 01:51:41 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:992e27f47455d56bf2b0c7dc5b9ebfe0cc73dee8856b30c4ede24094ea590fe4`  
		Last Modified: Fri, 21 Jan 2022 01:51:42 GMT  
		Size: 2.6 MB (2574447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b11c6a5619aedf36db3ff2f5bdf005192d9d21dca76df026186da16a9a62c6`  
		Last Modified: Fri, 21 Jan 2022 01:51:40 GMT  
		Size: 2.0 KB (2040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17ab0a366b25d77cb681da244f1373167dad4df9906559bb4281d7c2b2d5e2d`  
		Last Modified: Fri, 21 Jan 2022 01:51:40 GMT  
		Size: 1.6 KB (1550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-fpm` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:136eadd26445c5a6ff301b783b5435bd5c85e6ae3c0657b25db3b8db121bff5c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.6 MB (159645395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7eb49771f92d2c79ac737fe514d9160b09888e952389614d6c74a2c57100971`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 21 Dec 2021 01:42:23 GMT
ADD file:986f91febed4aa8e2072081ff8419d52ba2060510822e717086d3b3d9469e4d7 in / 
# Tue, 21 Dec 2021 01:42:24 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 03:35:10 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 21 Dec 2021 03:35:10 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 21 Dec 2021 03:35:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 03:35:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 21 Dec 2021 03:35:28 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 21 Dec 2021 03:35:28 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Dec 2021 03:35:29 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Dec 2021 03:35:30 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 21 Dec 2021 04:10:27 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Thu, 20 Jan 2022 19:46:06 GMT
ENV PHP_VERSION=8.0.15
# Thu, 20 Jan 2022 19:46:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.15.tar.xz.asc
# Thu, 20 Jan 2022 19:46:08 GMT
ENV PHP_SHA256=5f33544061d37d805a2a9ce791f081ef08a7155bd7ba2362e69bba2d06b0f8b2
# Thu, 20 Jan 2022 19:46:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 20 Jan 2022 19:46:40 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jan 2022 19:54:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jan 2022 19:54:52 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Thu, 20 Jan 2022 19:54:53 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jan 2022 19:54:53 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jan 2022 19:54:54 GMT
WORKDIR /var/www/html
# Thu, 20 Jan 2022 19:54:55 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 20 Jan 2022 19:54:56 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Jan 2022 19:54:57 GMT
EXPOSE 9000
# Thu, 20 Jan 2022 19:54:58 GMT
CMD ["php-fpm"]
# Thu, 20 Jan 2022 21:51:55 GMT
LABEL org.opencontainers.image.title=YOURLS
# Thu, 20 Jan 2022 21:51:56 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Thu, 20 Jan 2022 21:51:57 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Thu, 20 Jan 2022 21:51:58 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Thu, 20 Jan 2022 21:51:59 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Thu, 20 Jan 2022 21:52:00 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Thu, 20 Jan 2022 21:52:01 GMT
LABEL org.opencontainers.image.version=1.8.2
# Thu, 20 Jan 2022 21:52:23 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Thu, 20 Jan 2022 21:52:24 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 20 Jan 2022 21:52:27 GMT
RUN set -eux;     version="1.8.2";     sha256="6d818622e3ba1d5785c2dbcc088be6890f5675fd4f24a2e3111eda4523bbd7ae";     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${version}.tar.gz";     echo "$sha256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${version}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 20 Jan 2022 21:52:28 GMT
COPY --chown=www-data:www-datafile:0bcfdfe0566007e7477c55552a1341b82b958e95879a5314f411d2188da2429e in /usr/src/yourls/user/ 
# Thu, 20 Jan 2022 21:52:29 GMT
COPY file:a47a395071c52d8d08402c95253924b09809713039b46033d6f6f75603938896 in /usr/local/bin/ 
# Thu, 20 Jan 2022 21:52:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jan 2022 21:52:30 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:927a35006d93ea08499b57046904046d7926cd76fb17be193e3e74f56d634a08`  
		Last Modified: Tue, 21 Dec 2021 01:48:54 GMT  
		Size: 30.0 MB (30043793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3fabbcc6f532a6a8b531637691358450f915c31905ac07c8bafef41a6529224`  
		Last Modified: Tue, 21 Dec 2021 05:22:06 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e737003186221828fccfeddc973f0e3dc6c217db56d064ad52aff59977d933`  
		Last Modified: Tue, 21 Dec 2021 05:22:19 GMT  
		Size: 86.9 MB (86920347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7adcc66be5bd6c34225cc77d6a19284e8c323df6241875eb616acb8cddd9011`  
		Last Modified: Tue, 21 Dec 2021 05:22:06 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3cec847b6c817d0f1755826115e484cf5bb8b0a4373a9197220f0b37a6b29b`  
		Last Modified: Thu, 20 Jan 2022 20:35:45 GMT  
		Size: 10.9 MB (10867303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf544677f21e7fdd7d7ceab619d24cee57481a67a1707a114e970b7284764d9`  
		Last Modified: Thu, 20 Jan 2022 20:35:44 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ef007a1e428cc8ffa082b09cec42e11ad51d6033a9fe5828fd5309d49ed043`  
		Last Modified: Thu, 20 Jan 2022 20:36:45 GMT  
		Size: 28.9 MB (28892635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab8e753d5d118982557a73bf5954917e394c161fdbabe347f4d49ec955da8ac`  
		Last Modified: Thu, 20 Jan 2022 20:36:41 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e89afa503ba78ecf41cbf08959f80cecf3696c8968efe92e65668d514a2c2aa`  
		Last Modified: Thu, 20 Jan 2022 20:36:41 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba7d6218f056487235879e98e81a1802f1cf064a9ca42314467e006249ef722`  
		Last Modified: Thu, 20 Jan 2022 20:36:41 GMT  
		Size: 8.6 KB (8579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18add7f25654dbf842656ecf96283c328bedd6e7809412f979839dd08fe5974`  
		Last Modified: Thu, 20 Jan 2022 21:54:40 GMT  
		Size: 329.8 KB (329805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0599f6fe5a7532f9a8d2fd8ebdc7e2284491082a77ecd91bb804f93d24d463b7`  
		Last Modified: Thu, 20 Jan 2022 21:54:40 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e375517d7fd21dd478aca29ce34ddbc8f83232536da0a1db16bdbe2f5309b9da`  
		Last Modified: Thu, 20 Jan 2022 21:54:40 GMT  
		Size: 2.6 MB (2575512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9658730b8907685f6412e1e40f369eae7d5f6ac0aa50716f47b404d74bd558b3`  
		Last Modified: Thu, 20 Jan 2022 21:54:40 GMT  
		Size: 2.0 KB (2043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0024f38a85b20858bcff794507a6b3c0f2edb365fdc7317bb947d5d0628b82d`  
		Last Modified: Thu, 20 Jan 2022 21:54:40 GMT  
		Size: 1.6 KB (1551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-fpm` - linux; 386

```console
$ docker pull yourls@sha256:322a8632a475830783d190f234620148b069fc4b50bc9ea66489cd1d0151c3c1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.7 MB (169686343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90416c07dbe906d4a28e31a983e5fa1d0e44c6f8ff03a9d28fac7a819047e843`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 21 Dec 2021 01:40:06 GMT
ADD file:6b67a0d4d176747cc8cefbd105facde82f1795467bf02eb45e8385c91cdc9c41 in / 
# Tue, 21 Dec 2021 01:40:09 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 12:55:21 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 21 Dec 2021 12:55:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 21 Dec 2021 12:55:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 12:55:45 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 21 Dec 2021 12:55:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 21 Dec 2021 12:55:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Dec 2021 12:55:47 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Dec 2021 12:55:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 21 Dec 2021 13:51:43 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Thu, 20 Jan 2022 19:48:34 GMT
ENV PHP_VERSION=8.0.15
# Thu, 20 Jan 2022 19:48:34 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.15.tar.xz.asc
# Thu, 20 Jan 2022 19:48:34 GMT
ENV PHP_SHA256=5f33544061d37d805a2a9ce791f081ef08a7155bd7ba2362e69bba2d06b0f8b2
# Thu, 20 Jan 2022 19:48:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 20 Jan 2022 19:48:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jan 2022 20:07:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jan 2022 20:07:03 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Thu, 20 Jan 2022 20:07:04 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jan 2022 20:07:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jan 2022 20:07:05 GMT
WORKDIR /var/www/html
# Thu, 20 Jan 2022 20:07:07 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 20 Jan 2022 20:07:07 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Jan 2022 20:07:08 GMT
EXPOSE 9000
# Thu, 20 Jan 2022 20:07:08 GMT
CMD ["php-fpm"]
# Thu, 20 Jan 2022 23:49:01 GMT
LABEL org.opencontainers.image.title=YOURLS
# Thu, 20 Jan 2022 23:49:01 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Thu, 20 Jan 2022 23:49:01 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Thu, 20 Jan 2022 23:49:02 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Thu, 20 Jan 2022 23:49:02 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Thu, 20 Jan 2022 23:49:02 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Thu, 20 Jan 2022 23:49:03 GMT
LABEL org.opencontainers.image.version=1.8.2
# Thu, 20 Jan 2022 23:49:54 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Thu, 20 Jan 2022 23:49:55 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 20 Jan 2022 23:49:57 GMT
RUN set -eux;     version="1.8.2";     sha256="6d818622e3ba1d5785c2dbcc088be6890f5675fd4f24a2e3111eda4523bbd7ae";     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${version}.tar.gz";     echo "$sha256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${version}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 20 Jan 2022 23:49:58 GMT
COPY --chown=www-data:www-datafile:0bcfdfe0566007e7477c55552a1341b82b958e95879a5314f411d2188da2429e in /usr/src/yourls/user/ 
# Thu, 20 Jan 2022 23:49:58 GMT
COPY file:a47a395071c52d8d08402c95253924b09809713039b46033d6f6f75603938896 in /usr/local/bin/ 
# Thu, 20 Jan 2022 23:49:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jan 2022 23:49:59 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9b9a100d632569e96aeb2d7b0bc45bc436609bb61335815f207994f3b557f0f7`  
		Last Modified: Tue, 21 Dec 2021 01:48:45 GMT  
		Size: 32.4 MB (32370850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3024a970d01a7ef049e3539cd86216f2b9ba836cc7349134a8daac2cd7967a3`  
		Last Modified: Tue, 21 Dec 2021 17:08:50 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c53ffbaa8e42e904ade656bec770a649d2440f23381661e50812c484003c32`  
		Last Modified: Tue, 21 Dec 2021 17:09:29 GMT  
		Size: 92.7 MB (92715879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0401ee648bb0837c49fd04dd8d305a1106b6d151227c0f56981dbb1efba74aa4`  
		Last Modified: Tue, 21 Dec 2021 17:08:50 GMT  
		Size: 272.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33c06cb2612124153f9366a39b48dde90411ad900096c8220cc1fb111f0352f`  
		Last Modified: Thu, 20 Jan 2022 21:49:04 GMT  
		Size: 11.1 MB (11082540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba2e8766abbdd4f353b233a8b9df7794a388e639da6c459df316de42514791c`  
		Last Modified: Thu, 20 Jan 2022 21:49:02 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade1147bed966609d8828b63d735970f018a6755ca6c1bcce47729ee2eabbef6`  
		Last Modified: Thu, 20 Jan 2022 21:50:17 GMT  
		Size: 30.3 MB (30281772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2181ade898ec112c8137c070d9da65e8bf27015cf64137db7eb22c407ced527`  
		Last Modified: Thu, 20 Jan 2022 21:50:10 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f7e1f8ad49b30ebb9d0fe2b381d84461107d66842afad170924ee804726ef70`  
		Last Modified: Thu, 20 Jan 2022 21:50:10 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf3817e74ed57f082890652db547178fbd415b2a03c71032cc2093cdf693c740`  
		Last Modified: Thu, 20 Jan 2022 21:50:10 GMT  
		Size: 8.6 KB (8577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b587b630bd2ef1688a8f6f0129147090dd85bfe9a7f1152084ece1c6a4bbaa6f`  
		Last Modified: Thu, 20 Jan 2022 23:53:25 GMT  
		Size: 644.8 KB (644811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91611a4303b1c9329adf0a46e84b08da7d819512933c0e4806a73cff486b5390`  
		Last Modified: Thu, 20 Jan 2022 23:53:25 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3be1e7ea45fdda1584b60669ca243973e839a750f635e1fd7caf8dc8fdb19c`  
		Last Modified: Thu, 20 Jan 2022 23:53:26 GMT  
		Size: 2.6 MB (2574444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1209af195f1764256fdcd5afffd18926264b298e89d989b5c1ea0a2916ca8b1a`  
		Last Modified: Thu, 20 Jan 2022 23:53:25 GMT  
		Size: 2.0 KB (2040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9981fb06c3960f9e2e9497702ea2619466b4a140131c8b9297f1d0044015373`  
		Last Modified: Thu, 20 Jan 2022 23:53:25 GMT  
		Size: 1.6 KB (1550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-fpm` - linux; mips64le

```console
$ docker pull yourls@sha256:2885da78bf7a46f8b68ba205e03b288e198cc1ed4a99023491ad80f8841e9c6d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.4 MB (144384037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a16dff79220f1e209f533e352a1c2a04027f4c6c2247fc12e57fdce2852f5cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 21 Dec 2021 02:09:07 GMT
ADD file:9e5931d5ed32a23b2e93bd8846258c647613637c581b6813bbc7d7e6b86bbdf5 in / 
# Tue, 21 Dec 2021 02:09:08 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 05:04:59 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 21 Dec 2021 05:04:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 21 Dec 2021 05:05:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 05:05:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 21 Dec 2021 05:05:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 21 Dec 2021 05:05:53 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Dec 2021 05:05:53 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Dec 2021 05:05:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 21 Dec 2021 07:01:04 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Thu, 20 Jan 2022 19:13:30 GMT
ENV PHP_VERSION=8.0.15
# Thu, 20 Jan 2022 19:13:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.15.tar.xz.asc
# Thu, 20 Jan 2022 19:13:31 GMT
ENV PHP_SHA256=5f33544061d37d805a2a9ce791f081ef08a7155bd7ba2362e69bba2d06b0f8b2
# Thu, 20 Jan 2022 19:13:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 20 Jan 2022 19:13:57 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jan 2022 19:52:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jan 2022 19:52:19 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Thu, 20 Jan 2022 19:52:21 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jan 2022 19:52:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jan 2022 19:52:22 GMT
WORKDIR /var/www/html
# Thu, 20 Jan 2022 19:52:24 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 20 Jan 2022 19:52:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Jan 2022 19:52:24 GMT
EXPOSE 9000
# Thu, 20 Jan 2022 19:52:25 GMT
CMD ["php-fpm"]
# Thu, 20 Jan 2022 22:31:49 GMT
LABEL org.opencontainers.image.title=YOURLS
# Thu, 20 Jan 2022 22:31:49 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Thu, 20 Jan 2022 22:31:50 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Thu, 20 Jan 2022 22:31:50 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Thu, 20 Jan 2022 22:31:50 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Thu, 20 Jan 2022 22:31:51 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Thu, 20 Jan 2022 22:31:51 GMT
LABEL org.opencontainers.image.version=1.8.2
# Thu, 20 Jan 2022 22:33:21 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Thu, 20 Jan 2022 22:33:23 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 20 Jan 2022 22:33:27 GMT
RUN set -eux;     version="1.8.2";     sha256="6d818622e3ba1d5785c2dbcc088be6890f5675fd4f24a2e3111eda4523bbd7ae";     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${version}.tar.gz";     echo "$sha256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${version}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 20 Jan 2022 22:33:28 GMT
COPY --chown=www-data:www-datafile:0bcfdfe0566007e7477c55552a1341b82b958e95879a5314f411d2188da2429e in /usr/src/yourls/user/ 
# Thu, 20 Jan 2022 22:33:28 GMT
COPY file:a47a395071c52d8d08402c95253924b09809713039b46033d6f6f75603938896 in /usr/local/bin/ 
# Thu, 20 Jan 2022 22:33:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 20 Jan 2022 22:33:29 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6a6edb95e2485a5b9b3c44b27b7ebad16384c0e08a3d61b7e48c65d7278763cf`  
		Last Modified: Tue, 21 Dec 2021 02:18:14 GMT  
		Size: 29.6 MB (29619177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3f12ab46e103f65b4518c01930c0ed787c5335525baefca57ffdd2aea3579e`  
		Last Modified: Tue, 21 Dec 2021 11:21:58 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:200ae147e93b06631d6d4c909ae45d76f0a3cf3f95a75593fe2cf8788ea5d8c0`  
		Last Modified: Tue, 21 Dec 2021 11:22:54 GMT  
		Size: 72.0 MB (72014111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0211171d833bd2fd5c2f5efc3ab0ca5aa65b20e9b833abadb50575c7dfaafd35`  
		Last Modified: Tue, 21 Dec 2021 11:21:58 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a8e5a08bba951ddc08492fa4cb3accb42cfaeabe0cc690ddc9bd7115f033e3d`  
		Last Modified: Thu, 20 Jan 2022 20:59:34 GMT  
		Size: 11.1 MB (11081333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28b5ebd3f4e291cd05e82cf4996f03ced52a1b02b14942fc5929fbce87e549d1`  
		Last Modified: Thu, 20 Jan 2022 20:59:30 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3abbbf74b70fc3e2dffd55a315fbe585de4aa7b927c452172753eb52a51a0732`  
		Last Modified: Thu, 20 Jan 2022 21:01:21 GMT  
		Size: 28.8 MB (28750824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71da6be97cc69a2c4c08f160c72d03b6c2b745acd3a6a70afc3c98c39b92aa54`  
		Last Modified: Thu, 20 Jan 2022 21:00:59 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b0673e0ac7f79562617e70925a457264a294b2e6beb13fb1490786f27ed6c0`  
		Last Modified: Thu, 20 Jan 2022 21:00:59 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921885ae8eb8a6fb67d7bfcef88868947332016aac9686c5313c7a3583d81a38`  
		Last Modified: Thu, 20 Jan 2022 21:00:59 GMT  
		Size: 8.6 KB (8577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8aced27b9a8b843297f3ccc104ebce53487bc59862cb0e863836c576284c2c`  
		Last Modified: Thu, 20 Jan 2022 22:34:23 GMT  
		Size: 328.2 KB (328173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3842a3279ee9deb1e69f0728f79071aae88f8a5e8c6c096f6b568723ebab632`  
		Last Modified: Thu, 20 Jan 2022 22:34:23 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d55bdfe43b3c9777b2a66aac583996596d6b2480c889d4180faa4a19dc63be`  
		Last Modified: Thu, 20 Jan 2022 22:34:26 GMT  
		Size: 2.6 MB (2574418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8602eb07c64236b7c1732dfd6eab525e1afeabd2c046d0f18e84aaefec7881a4`  
		Last Modified: Thu, 20 Jan 2022 22:34:23 GMT  
		Size: 2.0 KB (2043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99eabcea60db0898535e02fabfd214b229fe8f5f486ff2e0538b29d45a626c5c`  
		Last Modified: Thu, 20 Jan 2022 22:34:23 GMT  
		Size: 1.6 KB (1550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-fpm` - linux; ppc64le

```console
$ docker pull yourls@sha256:5c866b4a0dfa5baf701e0165ae0098f7f1aa551ea7786d3e9c9b24f46d9a4fd6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.0 MB (167008003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccae252ccb248673709d7670067d18d5921e6c1c26a33f26596b02ef89dccc70`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 21 Dec 2021 02:20:24 GMT
ADD file:078a17bf7e519cb7a60fbbf743ba7e5897554201cb44957154ab518d6991a033 in / 
# Tue, 21 Dec 2021 02:20:28 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 06:34:06 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 21 Dec 2021 06:34:07 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 21 Dec 2021 06:35:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 06:35:53 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 21 Dec 2021 06:35:58 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 21 Dec 2021 06:36:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Dec 2021 06:36:06 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 21 Dec 2021 06:36:08 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 21 Dec 2021 07:24:54 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Thu, 20 Jan 2022 21:06:27 GMT
ENV PHP_VERSION=8.0.15
# Thu, 20 Jan 2022 21:06:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.15.tar.xz.asc
# Thu, 20 Jan 2022 21:06:33 GMT
ENV PHP_SHA256=5f33544061d37d805a2a9ce791f081ef08a7155bd7ba2362e69bba2d06b0f8b2
# Thu, 20 Jan 2022 21:07:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 20 Jan 2022 21:07:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jan 2022 21:28:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jan 2022 21:28:34 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Thu, 20 Jan 2022 21:28:40 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jan 2022 21:28:43 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jan 2022 21:28:46 GMT
WORKDIR /var/www/html
# Thu, 20 Jan 2022 21:28:57 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 20 Jan 2022 21:29:00 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Jan 2022 21:29:04 GMT
EXPOSE 9000
# Thu, 20 Jan 2022 21:29:06 GMT
CMD ["php-fpm"]
# Fri, 21 Jan 2022 03:16:15 GMT
LABEL org.opencontainers.image.title=YOURLS
# Fri, 21 Jan 2022 03:16:18 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Fri, 21 Jan 2022 03:16:24 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Fri, 21 Jan 2022 03:16:28 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Fri, 21 Jan 2022 03:16:32 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Fri, 21 Jan 2022 03:16:38 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Fri, 21 Jan 2022 03:16:44 GMT
LABEL org.opencontainers.image.version=1.8.2
# Fri, 21 Jan 2022 03:17:27 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Fri, 21 Jan 2022 03:17:40 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 21 Jan 2022 03:17:53 GMT
RUN set -eux;     version="1.8.2";     sha256="6d818622e3ba1d5785c2dbcc088be6890f5675fd4f24a2e3111eda4523bbd7ae";     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${version}.tar.gz";     echo "$sha256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${version}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Fri, 21 Jan 2022 03:17:56 GMT
COPY --chown=www-data:www-datafile:0bcfdfe0566007e7477c55552a1341b82b958e95879a5314f411d2188da2429e in /usr/src/yourls/user/ 
# Fri, 21 Jan 2022 03:17:57 GMT
COPY file:a47a395071c52d8d08402c95253924b09809713039b46033d6f6f75603938896 in /usr/local/bin/ 
# Fri, 21 Jan 2022 03:17:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Jan 2022 03:18:01 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3345479fea0cdce1382b927b0908af4f239b288b30efa203c50edf7ac0cb055e`  
		Last Modified: Tue, 21 Dec 2021 02:29:20 GMT  
		Size: 35.3 MB (35258992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2031a2d9a9486eb693888310bd7c404b858eab6e58b93f9a67b0fa0ba0a076d`  
		Last Modified: Tue, 21 Dec 2021 09:23:11 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfef6776fce19b49c4cf70c3d6d31adf3afee6e19352646f3bc27655b8af9072`  
		Last Modified: Tue, 21 Dec 2021 09:23:43 GMT  
		Size: 86.6 MB (86624501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368374be7cc559a071ecd39ce723f773680ae0523d3213e72fef1d724547a300`  
		Last Modified: Tue, 21 Dec 2021 09:23:11 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7912d254b36d445add766eb0b39a8ef4667a20a93e57c8ba57897361bfde6e5b`  
		Last Modified: Thu, 20 Jan 2022 22:36:59 GMT  
		Size: 11.1 MB (11083519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541bb91f129dc78e78c0ce5494e5c62e9b744c567cd3610451178534a811243c`  
		Last Modified: Thu, 20 Jan 2022 22:36:58 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bed3defebbcc75206d29d87f8965bfd8275e84ffe53a8377f98f45001f78924`  
		Last Modified: Thu, 20 Jan 2022 22:38:09 GMT  
		Size: 31.1 MB (31071496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd877095451bdcf486644ecbc218d413a9dee75a1f043632f8b7d76a9d89e3c1`  
		Last Modified: Thu, 20 Jan 2022 22:38:03 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a9da90db01d812568818329e2ca3754c175de096d9fa5ed0da3c332118601eb`  
		Last Modified: Thu, 20 Jan 2022 22:38:03 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726ba5da627bc3ffbb47b1b0728aa55bb1e96b000aa0ecccd5017a5fb3a129fc`  
		Last Modified: Thu, 20 Jan 2022 22:38:03 GMT  
		Size: 8.6 KB (8579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb9ae3149e34876baf2dbc00f61e6cf2bd82fde8cea547f9d85feabe5d8b465`  
		Last Modified: Fri, 21 Jan 2022 03:21:20 GMT  
		Size: 379.0 KB (379000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:178e79cb84881bf7364b3d1e4898d0577906725c4fc0c78060caad14bcb6b2d8`  
		Last Modified: Fri, 21 Jan 2022 03:21:20 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc6fc6b3cfaa38a071705d79f7e0c62a2974d7c5d3a2d0bd956471d9a0d198d`  
		Last Modified: Fri, 21 Jan 2022 03:21:20 GMT  
		Size: 2.6 MB (2574444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e4a7570aef5c4ebd0d0f0f13e90223835b841c5110b749f676a5cbe6f42c8c5`  
		Last Modified: Fri, 21 Jan 2022 03:21:20 GMT  
		Size: 2.0 KB (2045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0692d7dc2365e79f3cc41e2a82de89b3d8f632b3c7c9939541bfcee8530bc29`  
		Last Modified: Fri, 21 Jan 2022 03:21:20 GMT  
		Size: 1.5 KB (1549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:1-fpm` - linux; s390x

```console
$ docker pull yourls@sha256:c8977b7a920832daea1ac6634f34d207351eb6b06f876ed8ccaa218726533e3d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143837931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c74431c7308e0c803efb753032fc8bb895e6e04cf89d7c606c34671cc7c02e1c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 26 Jan 2022 01:41:13 GMT
ADD file:03b224b82f458b08d3b5071e42b67915a3db309332c0fc9229db7cf1148bc1b5 in / 
# Wed, 26 Jan 2022 01:41:15 GMT
CMD ["bash"]
# Wed, 26 Jan 2022 03:50:15 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 26 Jan 2022 03:50:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 26 Jan 2022 03:50:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Jan 2022 03:50:33 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 26 Jan 2022 03:50:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 26 Jan 2022 03:50:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 26 Jan 2022 03:50:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 26 Jan 2022 03:50:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 26 Jan 2022 04:13:41 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 BFDDD28642824F8118EF77909B67A5C12229118F
# Wed, 26 Jan 2022 04:13:41 GMT
ENV PHP_VERSION=8.0.15
# Wed, 26 Jan 2022 04:13:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.0.15.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.0.15.tar.xz.asc
# Wed, 26 Jan 2022 04:13:42 GMT
ENV PHP_SHA256=5f33544061d37d805a2a9ce791f081ef08a7155bd7ba2362e69bba2d06b0f8b2
# Wed, 26 Jan 2022 04:14:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 26 Jan 2022 04:14:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 26 Jan 2022 04:21:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-openssl 		--with-readline 		--with-zlib 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Wed, 26 Jan 2022 04:21:24 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Wed, 26 Jan 2022 04:21:24 GMT
RUN docker-php-ext-enable sodium
# Wed, 26 Jan 2022 04:21:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 26 Jan 2022 04:21:25 GMT
WORKDIR /var/www/html
# Wed, 26 Jan 2022 04:21:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Wed, 26 Jan 2022 04:21:25 GMT
STOPSIGNAL SIGQUIT
# Wed, 26 Jan 2022 04:21:26 GMT
EXPOSE 9000
# Wed, 26 Jan 2022 04:21:26 GMT
CMD ["php-fpm"]
# Wed, 26 Jan 2022 21:56:45 GMT
LABEL org.opencontainers.image.title=YOURLS
# Wed, 26 Jan 2022 21:56:45 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Wed, 26 Jan 2022 21:56:45 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Wed, 26 Jan 2022 21:56:45 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Wed, 26 Jan 2022 21:56:45 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Wed, 26 Jan 2022 21:56:45 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Wed, 26 Jan 2022 21:56:45 GMT
LABEL org.opencontainers.image.version=1.8.2
# Wed, 26 Jan 2022 21:57:01 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Wed, 26 Jan 2022 21:57:02 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Wed, 26 Jan 2022 21:57:03 GMT
RUN set -eux;     version="1.8.2";     sha256="6d818622e3ba1d5785c2dbcc088be6890f5675fd4f24a2e3111eda4523bbd7ae";     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${version}.tar.gz";     echo "$sha256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${version}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Wed, 26 Jan 2022 21:57:03 GMT
COPY --chown=www-data:www-datafile:0bcfdfe0566007e7477c55552a1341b82b958e95879a5314f411d2188da2429e in /usr/src/yourls/user/ 
# Wed, 26 Jan 2022 21:57:03 GMT
COPY file:a47a395071c52d8d08402c95253924b09809713039b46033d6f6f75603938896 in /usr/local/bin/ 
# Wed, 26 Jan 2022 21:57:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 26 Jan 2022 21:57:04 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:70bed29526f8483937e4d2540d19256d30786007c7c321e717e00d2e74700380`  
		Last Modified: Wed, 26 Jan 2022 01:46:57 GMT  
		Size: 29.6 MB (29647071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d388c00adf9d70c76ee6e62579fb6aaaf5de79c35dfdec2f01bac554e92b217f`  
		Last Modified: Wed, 26 Jan 2022 05:19:03 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e7fd053151e2d3345606bec45dc234d4da439d0212c54fea8710ca8886a597`  
		Last Modified: Wed, 26 Jan 2022 05:19:12 GMT  
		Size: 71.6 MB (71617962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180f356f15b9f7b050e52b2895a61c852b462ee0e88317b4be1cb7f38cecaf64`  
		Last Modified: Wed, 26 Jan 2022 05:19:02 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea63b6af0825c5cb3e618372d9c1c4c9b164c50388c4ef1a038eb6bf7d78a21`  
		Last Modified: Wed, 26 Jan 2022 05:22:48 GMT  
		Size: 11.1 MB (11082228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02db0098adee21a6f6093c727dd92f8271d09c1d1a565f451aa5f2b8627ed9a5`  
		Last Modified: Wed, 26 Jan 2022 05:22:47 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd5140c117aea386d0a9c594b465a2784286e7be526e46e087eb8a9eee0ab65`  
		Last Modified: Wed, 26 Jan 2022 05:23:27 GMT  
		Size: 28.6 MB (28566906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0da9941b7d0395c4de280ffe176f280c2f8b9a9a854d0c302fc1a6801d28a5b3`  
		Last Modified: Wed, 26 Jan 2022 05:23:23 GMT  
		Size: 2.3 KB (2307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb666352e2cbda9b6ad9e9b564adbd2ad39580340218b65a37e3408121d57e8`  
		Last Modified: Wed, 26 Jan 2022 05:23:23 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564e6a42e82489230fe273a7f45cd2a924f4e32099a4eb53678c9306676397cd`  
		Last Modified: Wed, 26 Jan 2022 05:23:23 GMT  
		Size: 8.6 KB (8570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657630a88d4c795844d7e58d18b3fba151d67d419a59317e4ad870de42a1213a`  
		Last Modified: Wed, 26 Jan 2022 21:58:12 GMT  
		Size: 333.3 KB (333296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329a3a602ce656252fe133c36aac9ccbc05f4dcebb54b1a07f22afa30b16551e`  
		Last Modified: Wed, 26 Jan 2022 21:58:12 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ef1fdc2860d78a9901e91c1d566d2bdd0ec19c94bbf48bd0098eda7929934c5`  
		Last Modified: Wed, 26 Jan 2022 21:58:12 GMT  
		Size: 2.6 MB (2574444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a60710e247da835e251fb7bad03bc5318e9a040a6c5fd7a4d2f946f2333b943`  
		Last Modified: Wed, 26 Jan 2022 21:58:12 GMT  
		Size: 2.0 KB (2038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff2cbc66203a54c1be0ede722bac8a4688acbc49ee6c34eea6f57e58997deef`  
		Last Modified: Wed, 26 Jan 2022 21:58:12 GMT  
		Size: 1.5 KB (1546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
