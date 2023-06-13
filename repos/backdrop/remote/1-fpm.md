## `backdrop:1-fpm`

```console
$ docker pull backdrop@sha256:5f20befd411991f5c9dcc7126237a7f2910cb9a11624f2c5ca282513a9aaa782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `backdrop:1-fpm` - linux; amd64

```console
$ docker pull backdrop@sha256:0478cf3d2c9aa3a7c57f73bfae12c609cd01fa2d57f66f491746e320d2e4b5a5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.5 MB (174512768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1b4d130d7ab8d4ec15847515e3e355d52270de8e46dc6912351e8deb3ec50f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 09:36:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 23 May 2023 09:36:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 23 May 2023 09:36:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 09:36:39 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 23 May 2023 09:36:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 23 May 2023 09:36:39 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 09:36:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 May 2023 09:36:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 May 2023 10:03:35 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 09 Jun 2023 00:59:43 GMT
ENV PHP_VERSION=8.1.20
# Fri, 09 Jun 2023 00:59:43 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.20.tar.xz.asc
# Fri, 09 Jun 2023 00:59:43 GMT
ENV PHP_SHA256=4c9973f599e93ed5e8ce2b45ce1d41bb8fb54ce642824fd23e56b52fd75029a6
# Fri, 09 Jun 2023 00:59:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 09 Jun 2023 00:59:58 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:09:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 09 Jun 2023 01:09:25 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 09 Jun 2023 01:09:26 GMT
RUN docker-php-ext-enable sodium
# Fri, 09 Jun 2023 01:09:26 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 09 Jun 2023 01:09:26 GMT
WORKDIR /var/www/html
# Fri, 09 Jun 2023 01:09:26 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Fri, 09 Jun 2023 01:09:26 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Jun 2023 01:09:27 GMT
EXPOSE 9000
# Fri, 09 Jun 2023 01:09:27 GMT
CMD ["php-fpm"]
# Fri, 09 Jun 2023 04:01:25 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Fri, 09 Jun 2023 04:01:25 GMT
WORKDIR /var/www/html
# Fri, 09 Jun 2023 04:01:25 GMT
ENV BACKDROP_VERSION=1.25.1
# Fri, 09 Jun 2023 04:01:25 GMT
ENV BACKDROP_MD5=9c2bbcb4ddd52cbd85e1e31ee4fc8a17
# Fri, 09 Jun 2023 04:01:28 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites
# Fri, 09 Jun 2023 04:01:28 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Fri, 09 Jun 2023 04:01:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 09 Jun 2023 04:01:28 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662d8f2fcdb9ff5b9497538bdbb929df1cc5f1d371a15f5ea427ade8ed4dc08f`  
		Last Modified: Tue, 23 May 2023 10:55:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fe0ef5ed7711aab5b14ba79dee1d8f750f1cb661645280d76336db6017764c`  
		Last Modified: Tue, 23 May 2023 10:55:59 GMT  
		Size: 91.6 MB (91635720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e258eed73a3b01f73bf29d2258f63746f27920625d424190f90f708a26e84ee`  
		Last Modified: Tue, 23 May 2023 10:55:46 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f94fcedaefe080e3ed1e2e8ff76be549d4d7be1b0596bc0e335b9d33d90bcd4e`  
		Last Modified: Fri, 09 Jun 2023 02:48:42 GMT  
		Size: 12.1 MB (12111656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb3c7d20542ec78b2e2b74f29914cc2963e57a22ddf3d4a5ac0843812ce2d5d`  
		Last Modified: Fri, 09 Jun 2023 02:48:41 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc87360a828e1367c389850baf810f08991cac8a0aae7cefee87920d2a56120`  
		Last Modified: Fri, 09 Jun 2023 02:49:28 GMT  
		Size: 28.2 MB (28159707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9636b80dd5c47b9a90ebf426e2584205d3f5f8640f4ed18ed88822fafc7dd1cd`  
		Last Modified: Fri, 09 Jun 2023 02:49:24 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a556a07c48dd9765dbd516a557012b8da81b71cfa97649840e3e8bd394b6092f`  
		Last Modified: Fri, 09 Jun 2023 02:49:24 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d09e0f4ff9411d92b72cb7193867ab206d7adbaa91c85fc463535d1faf54cd77`  
		Last Modified: Fri, 09 Jun 2023 02:49:24 GMT  
		Size: 8.9 KB (8882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3ad6265ffb81f0acc292ce8905ee10a19647bc9f0fdb99976ffe16e656a534`  
		Last Modified: Fri, 09 Jun 2023 04:02:13 GMT  
		Size: 2.4 MB (2422856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35525a5c29bbd7a3d75b931913cbb20c3ea55bfb396d9ab51e0b44cd1c175eab`  
		Last Modified: Fri, 09 Jun 2023 04:02:15 GMT  
		Size: 8.8 MB (8765723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc5ed8d332ebd499de1cc5ca6d17678dcc6379a3f621d4bf2422abf6c1b9594`  
		Last Modified: Fri, 09 Jun 2023 04:02:13 GMT  
		Size: 948.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `backdrop:1-fpm` - linux; arm64 variant v8

```console
$ docker pull backdrop@sha256:34417d7868f201e40d518cebd2fbf8cd8249e0a3ae675094a765ce9127a6fb56
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **166.6 MB (166556146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f51af6351a70a4162931d5d520945770da696cf754054f393a09e19b1052f7e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 12 Jun 2023 23:40:33 GMT
ADD file:10af42ddb9f028c5418d370fe2b841aa61e81f37de1ffe76900a783ba3926646 in / 
# Mon, 12 Jun 2023 23:40:33 GMT
CMD ["bash"]
# Tue, 13 Jun 2023 08:27:14 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 13 Jun 2023 08:27:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 13 Jun 2023 08:27:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Jun 2023 08:27:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 13 Jun 2023 08:27:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 13 Jun 2023 08:27:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jun 2023 08:27:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 13 Jun 2023 08:27:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 13 Jun 2023 09:18:05 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 13 Jun 2023 09:18:05 GMT
ENV PHP_VERSION=8.1.20
# Tue, 13 Jun 2023 09:18:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.20.tar.xz.asc
# Tue, 13 Jun 2023 09:18:05 GMT
ENV PHP_SHA256=4c9973f599e93ed5e8ce2b45ce1d41bb8fb54ce642824fd23e56b52fd75029a6
# Tue, 13 Jun 2023 09:18:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 13 Jun 2023 09:18:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:27:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 13 Jun 2023 09:27:03 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 13 Jun 2023 09:27:04 GMT
RUN docker-php-ext-enable sodium
# Tue, 13 Jun 2023 09:27:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 13 Jun 2023 09:27:04 GMT
WORKDIR /var/www/html
# Tue, 13 Jun 2023 09:27:05 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Tue, 13 Jun 2023 09:27:05 GMT
STOPSIGNAL SIGQUIT
# Tue, 13 Jun 2023 09:27:05 GMT
EXPOSE 9000
# Tue, 13 Jun 2023 09:27:05 GMT
CMD ["php-fpm"]
# Tue, 13 Jun 2023 19:09:30 GMT
RUN apt-get update && apt-get install -y libzip-dev libonig-dev libpng-dev libjpeg-dev libpq-dev 	&& rm -rf /var/lib/apt/lists/* 	&& docker-php-ext-configure gd --with-jpeg=/usr 	&& docker-php-ext-install gd mbstring pdo pdo_mysql pdo_pgsql zip
# Tue, 13 Jun 2023 19:09:30 GMT
WORKDIR /var/www/html
# Tue, 13 Jun 2023 19:09:30 GMT
ENV BACKDROP_VERSION=1.25.1
# Tue, 13 Jun 2023 19:09:30 GMT
ENV BACKDROP_MD5=9c2bbcb4ddd52cbd85e1e31ee4fc8a17
# Tue, 13 Jun 2023 19:09:33 GMT
RUN curl -fSL "https://github.com/backdrop/backdrop/archive/${BACKDROP_VERSION}.tar.gz" -o backdrop.tar.gz 	&& echo "${BACKDROP_MD5} *backdrop.tar.gz" | md5sum -c - 	&& tar -xz --strip-components=1 -f backdrop.tar.gz 	&& rm backdrop.tar.gz 	&& chown -R www-data:www-data sites
# Tue, 13 Jun 2023 19:09:33 GMT
COPY file:dc282a331b642ab4cd043a874f505e04001cc1bdcf4f846fb117f413030d2835 in /entrypoint.sh 
# Tue, 13 Jun 2023 19:09:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 13 Jun 2023 19:09:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:92ad4775570054c645678402c8b75eb489b8e05313c9ccd7867bb591266db4d8`  
		Last Modified: Mon, 12 Jun 2023 23:44:45 GMT  
		Size: 30.1 MB (30062834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130acfd80cbcc92bb088194a5f70107163cf2c64ec03afbb8cef48a8d5cb64b9`  
		Last Modified: Tue, 13 Jun 2023 10:01:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c452fc3771f0e24d7a4608cb7fa0a3fef8338f180867edddc951516ee483df5f`  
		Last Modified: Tue, 13 Jun 2023 10:01:56 GMT  
		Size: 86.9 MB (86928318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67e73365700a60b46358bf991bb3261b2892f868de457a8248e947d38b0e2ec7`  
		Last Modified: Tue, 13 Jun 2023 10:01:46 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057240c114d62c093225ecb2f25e1fb120d14d85d1ae5ffebcbf3235a060f639`  
		Last Modified: Tue, 13 Jun 2023 10:07:22 GMT  
		Size: 12.1 MB (12110892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261cdaf3dea02295e9b652f0a6e24217fa30b46c56137b29556d72355ccf37bb`  
		Last Modified: Tue, 13 Jun 2023 10:07:21 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9667c550c5b773eae15d1d8286dbf153b0970f8e3faaf5989e8cb8af60fa1e7e`  
		Last Modified: Tue, 13 Jun 2023 10:08:03 GMT  
		Size: 26.3 MB (26289957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4bd8b43a56a5ba574db217ae164bf8d0c5b1f1807909f6d020f760389cf4da3`  
		Last Modified: Tue, 13 Jun 2023 10:08:00 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8edcfd607aa0599182b1c27bb0b11ae99f227fd3c81fdf8ce3e1e42a0de84f`  
		Last Modified: Tue, 13 Jun 2023 10:08:00 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389016bdc7b75157113a00b89a23ac21dfa9197d65ecb6fa81f1742ff1e27d45`  
		Last Modified: Tue, 13 Jun 2023 10:08:00 GMT  
		Size: 8.9 KB (8880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66003234794732c9b9029059a3551949ff32f8cb6c267937828ea98cc4efa76`  
		Last Modified: Tue, 13 Jun 2023 19:10:20 GMT  
		Size: 2.4 MB (2384896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d523a2b4c34cd9649c633e56f3ef2ae01b39f151d302d4c5e6f82e068615ab`  
		Last Modified: Tue, 13 Jun 2023 19:10:21 GMT  
		Size: 8.8 MB (8765744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a398e269f3cab8cbb1c467d7120dc7f89a45405717a22d559ec83e6c8e5a50fa`  
		Last Modified: Tue, 13 Jun 2023 19:10:20 GMT  
		Size: 949.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
