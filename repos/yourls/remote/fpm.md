## `yourls:fpm`

```console
$ docker pull yourls@sha256:16ffbd500294d80340a0bccfed5ca5ed8d443ebc6d96c271ffe84b871183fed9
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

### `yourls:fpm` - linux; amd64

```console
$ docker pull yourls@sha256:16aa7512058740b1f3564e4ee236d0129763e9da69779746b9243a36b24d2a44
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.7 MB (165706366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b10a2698d001c6313dded98624069975d917f4ec3d14abdbf18bfad64a12f0e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 23 Jun 2022 00:20:27 GMT
ADD file:8adbbab04d6f84cd83b5f4205b89b0acb7ecbf27a1bb2dc181d0a629479039fe in / 
# Thu, 23 Jun 2022 00:20:27 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 07:22:14 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Jun 2022 07:22:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Jun 2022 07:22:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 07:22:32 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Jun 2022 07:22:33 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 23 Jun 2022 07:22:33 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Jun 2022 07:22:33 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Jun 2022 07:22:33 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Jun 2022 07:49:02 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 23 Jun 2022 07:49:02 GMT
ENV PHP_VERSION=8.1.7
# Thu, 23 Jun 2022 07:49:02 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.7.tar.xz.asc
# Thu, 23 Jun 2022 07:49:02 GMT
ENV PHP_SHA256=f042322f1b5a9f7c2decb84b7086ef676896c2f7178739b9672afafa964ed0e5
# Thu, 23 Jun 2022 07:49:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jun 2022 07:49:14 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jun 2022 07:58:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 23 Jun 2022 07:58:44 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 23 Jun 2022 07:58:44 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jun 2022 07:58:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jun 2022 07:58:45 GMT
WORKDIR /var/www/html
# Thu, 23 Jun 2022 07:58:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 23 Jun 2022 07:58:45 GMT
STOPSIGNAL SIGQUIT
# Thu, 23 Jun 2022 07:58:45 GMT
EXPOSE 9000
# Thu, 23 Jun 2022 07:58:46 GMT
CMD ["php-fpm"]
# Fri, 24 Jun 2022 02:12:46 GMT
LABEL org.opencontainers.image.title=YOURLS
# Fri, 24 Jun 2022 02:12:46 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Fri, 24 Jun 2022 02:12:46 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Fri, 24 Jun 2022 02:12:46 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Fri, 24 Jun 2022 02:12:46 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Fri, 24 Jun 2022 02:12:46 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Fri, 24 Jun 2022 02:12:47 GMT
LABEL org.opencontainers.image.licenses=MIT
# Fri, 24 Jun 2022 02:13:27 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Fri, 24 Jun 2022 02:13:28 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 24 Jun 2022 02:13:28 GMT
ARG YOURLS_VERSION=1.9
# Fri, 24 Jun 2022 02:13:28 GMT
ARG YOURLS_SHA256=212c4cd283f0b2b44e07da66a882cca4886e064f642bf4de8ecb8dbfb867e542
# Fri, 24 Jun 2022 02:13:28 GMT
LABEL org.opencontainers.image.version=1.9
# Fri, 24 Jun 2022 02:13:28 GMT
ENV YOURLS_VERSION=1.9
# Fri, 24 Jun 2022 02:13:28 GMT
ENV YOURLS_SHA256=212c4cd283f0b2b44e07da66a882cca4886e064f642bf4de8ecb8dbfb867e542
# Fri, 24 Jun 2022 02:13:30 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Fri, 24 Jun 2022 02:13:30 GMT
COPY --chown=www-data:www-datafile:f5584b9849b80034920f4de5f1297cb1be461f765f3437b87ddf6c86daa6499d in /usr/src/yourls/user/ 
# Fri, 24 Jun 2022 02:13:30 GMT
COPY file:975ababf859e7cabd8184ab0b2b317a5d8d3ccb6f4922be7f2a5d28c20d075a2 in /usr/local/bin/ 
# Fri, 24 Jun 2022 02:13:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 24 Jun 2022 02:13:30 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b85a868b505ffd0342a37e6a3b1c49f7c71878afe569a807e6238ef08252fcb7`  
		Last Modified: Thu, 23 Jun 2022 00:25:18 GMT  
		Size: 31.4 MB (31379408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fdfd2598e0ffdaa39011b909e2a79a75a60a0a87998f1072ec5d9256f19868`  
		Last Modified: Thu, 23 Jun 2022 09:03:51 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26769c8659f467675c0f34948c16e051ea7aab69ec3198c65063c299b9771a05`  
		Last Modified: Thu, 23 Jun 2022 09:04:05 GMT  
		Size: 91.6 MB (91603711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd105fadbe34a7e12eb66c424bd0de4b9c2c5c2daf01063eef044ff10e5e437`  
		Last Modified: Thu, 23 Jun 2022 09:03:50 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79256ca8bbc5c50f571d44f29cf4f3e8bb36835fcfc4086d1bf54222c0849e6e`  
		Last Modified: Thu, 23 Jun 2022 09:06:52 GMT  
		Size: 12.0 MB (12037410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec46bea2d21ff66c7633c39e20ffad13206c0fc5a42f898af5764e30d992d0c`  
		Last Modified: Thu, 23 Jun 2022 09:06:52 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c13d2051e31bb04b265301b9359d909f112d88f5035658d880bca179bd1b00e`  
		Last Modified: Thu, 23 Jun 2022 09:08:19 GMT  
		Size: 26.2 MB (26213340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cc2826173c48fc8ed6c8a5d8e671b92b5f2783a3dc504b7e8ada75722826d7c`  
		Last Modified: Thu, 23 Jun 2022 09:08:15 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44f19323300ad8aec4720fc7ec6dde5de02074c0d05fe50681d5deb916b3da61`  
		Last Modified: Thu, 23 Jun 2022 09:08:15 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7707dd22efdfdadc3f72c169bf50a307b22bb5bc380667e928df741deccb20f`  
		Last Modified: Thu, 23 Jun 2022 09:08:15 GMT  
		Size: 8.6 KB (8623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f6392541a6b88ddcb1fde28e40305c24d83e2dae8fc7c4b8b964aa1afaeed6`  
		Last Modified: Fri, 24 Jun 2022 02:14:23 GMT  
		Size: 511.9 KB (511926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40bd719fbbfce87c099faf147d4acb9ed9f1a7ede33cb6bf1eb9dbc723dae54c`  
		Last Modified: Fri, 24 Jun 2022 02:14:23 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfc79995c8c71bbe60c28b6f0b2881d9fbfc88a17c3d152312cc3fd371372a5`  
		Last Modified: Fri, 24 Jun 2022 02:14:24 GMT  
		Size: 3.9 MB (3944331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7ba27704a1a540436804efe81e15f1c78dc8bb296ed4d0854132f3db87cd519`  
		Last Modified: Fri, 24 Jun 2022 02:14:23 GMT  
		Size: 2.1 KB (2051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e4297e6dc186a3e9e78d6c97fe930034f40afd097c70724632e274b6878a9a`  
		Last Modified: Fri, 24 Jun 2022 02:14:23 GMT  
		Size: 1.6 KB (1555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm` - linux; arm variant v5

```console
$ docker pull yourls@sha256:9ec13993a1a0f3b7499dfa1f91398cb303fd10c68b0fbe79008f2a627c6dbb67
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.6 MB (143555582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ddf9f2f3d834e5f6fff14ae62f578b2dc0b0c40b6876865b7b0d93210c1922`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 28 May 2022 02:03:06 GMT
ADD file:d9560b279f64bc3973a6aaa0e0ab8f483d60a1c66647899850689eee01a729ec in / 
# Sat, 28 May 2022 02:03:07 GMT
CMD ["bash"]
# Sat, 28 May 2022 20:41:44 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 May 2022 20:41:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 May 2022 20:42:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 20:42:37 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 May 2022 20:42:38 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 May 2022 20:42:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 May 2022 20:42:39 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 May 2022 20:42:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 28 May 2022 20:42:40 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 09 Jun 2022 22:36:47 GMT
ENV PHP_VERSION=8.1.7
# Thu, 09 Jun 2022 22:36:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.7.tar.xz.asc
# Thu, 09 Jun 2022 22:36:48 GMT
ENV PHP_SHA256=f042322f1b5a9f7c2decb84b7086ef676896c2f7178739b9672afafa964ed0e5
# Thu, 09 Jun 2022 22:37:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 09 Jun 2022 22:37:15 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 09 Jun 2022 22:53:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 09 Jun 2022 22:53:06 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 09 Jun 2022 22:53:08 GMT
RUN docker-php-ext-enable sodium
# Thu, 09 Jun 2022 22:53:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Jun 2022 22:53:09 GMT
WORKDIR /var/www/html
# Thu, 09 Jun 2022 22:53:10 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 09 Jun 2022 22:53:11 GMT
STOPSIGNAL SIGQUIT
# Thu, 09 Jun 2022 22:53:11 GMT
EXPOSE 9000
# Thu, 09 Jun 2022 22:53:12 GMT
CMD ["php-fpm"]
# Fri, 10 Jun 2022 05:57:39 GMT
LABEL org.opencontainers.image.title=YOURLS
# Fri, 10 Jun 2022 05:57:39 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Fri, 10 Jun 2022 05:57:40 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Fri, 10 Jun 2022 05:57:40 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Fri, 10 Jun 2022 05:57:41 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Fri, 10 Jun 2022 05:57:41 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Fri, 10 Jun 2022 05:57:42 GMT
LABEL org.opencontainers.image.licenses=MIT
# Fri, 10 Jun 2022 05:58:44 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Fri, 10 Jun 2022 05:58:46 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 10 Jun 2022 05:58:46 GMT
ARG YOURLS_VERSION=1.9
# Fri, 10 Jun 2022 05:58:47 GMT
ARG YOURLS_SHA256=212c4cd283f0b2b44e07da66a882cca4886e064f642bf4de8ecb8dbfb867e542
# Fri, 10 Jun 2022 05:58:47 GMT
LABEL org.opencontainers.image.version=1.9
# Fri, 10 Jun 2022 05:58:47 GMT
ENV YOURLS_VERSION=1.9
# Fri, 10 Jun 2022 05:58:48 GMT
ENV YOURLS_SHA256=212c4cd283f0b2b44e07da66a882cca4886e064f642bf4de8ecb8dbfb867e542
# Fri, 10 Jun 2022 05:58:52 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Fri, 10 Jun 2022 05:58:53 GMT
COPY --chown=www-data:www-datafile:f5584b9849b80034920f4de5f1297cb1be461f765f3437b87ddf6c86daa6499d in /usr/src/yourls/user/ 
# Fri, 10 Jun 2022 05:58:53 GMT
COPY file:975ababf859e7cabd8184ab0b2b317a5d8d3ccb6f4922be7f2a5d28c20d075a2 in /usr/local/bin/ 
# Fri, 10 Jun 2022 05:58:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Jun 2022 05:58:54 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:b24540c95c3d5b61dba94dfa3665e0cc1231b3602edfb61432041c1f108be50d`  
		Last Modified: Sat, 28 May 2022 02:18:37 GMT  
		Size: 28.9 MB (28921471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12cf3513616b2ea05dba65517d17dda27a1ceee04ba9287047dd04f6979c06f9`  
		Last Modified: Sat, 28 May 2022 23:50:24 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:443372867141fb1f3fe996587efd00d75c4718138718a4515907898d5c1ad900`  
		Last Modified: Sat, 28 May 2022 23:51:14 GMT  
		Size: 73.7 MB (73685298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:728498cc6c6df3b79ec87ce8985063790e5399f12d368c50f635e46a6816ba2e`  
		Last Modified: Sat, 28 May 2022 23:50:24 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8fbdbc4424dcdaf7176771f15b805c1d28a61c3be0952083678f4d799cc6f89`  
		Last Modified: Fri, 10 Jun 2022 00:21:20 GMT  
		Size: 12.0 MB (12035847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6914877839d8afe428d1e283f517275c12844ebbfd6beae9b1607b90d89bd8f7`  
		Last Modified: Fri, 10 Jun 2022 00:21:17 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9b7384d6c2655a9c4c33258634098fa43c7d19ffbc713a88e21a9fa625fa56`  
		Last Modified: Fri, 10 Jun 2022 00:23:47 GMT  
		Size: 24.8 MB (24801734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496a3ca8421ab738bebeb3f04534037f4000846ecf9803a37dd25394410aed15`  
		Last Modified: Fri, 10 Jun 2022 00:23:31 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de80df9b6bd442bae5148183271e7317383a1f85d1a68e5cd3b487c2c5e593d`  
		Last Modified: Fri, 10 Jun 2022 00:23:31 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d81bd7403fcc542481469426af08bf4b031dbdaea0213b1fb228f8396930f3d3`  
		Last Modified: Fri, 10 Jun 2022 00:23:31 GMT  
		Size: 8.6 KB (8627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1e471e3b16965adc42bc012c444281d02aec22bfe088a90c99e3db2815dd509`  
		Last Modified: Fri, 10 Jun 2022 06:00:25 GMT  
		Size: 150.6 KB (150635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df889be00476ae41785c982414a2744bbddfbb4e9a864c02fdbbf11561914cd`  
		Last Modified: Fri, 10 Jun 2022 06:00:25 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4d85d3f3386cc947ea5f1ed91169103ccecc35de7cdc3609bea262a30a1650`  
		Last Modified: Fri, 10 Jun 2022 06:00:28 GMT  
		Size: 3.9 MB (3944337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf034ddbf7cab428dfd940790d2898abf0c32b9410436af29ee394561ac2502`  
		Last Modified: Fri, 10 Jun 2022 06:00:25 GMT  
		Size: 2.1 KB (2051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fde26ad9c7d387a4a84799b857d1238486281e4327e5cdf06ac457d986b9b58`  
		Last Modified: Fri, 10 Jun 2022 06:00:25 GMT  
		Size: 1.6 KB (1558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm` - linux; arm variant v7

```console
$ docker pull yourls@sha256:b3905adb09adb2c79005bb8dbc76aeb5c52cefd25227d2de2177e95c17edeb70
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (135997678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:294f60fad05589fa7627cd76104bfebeba4dfed47a316acb437120c22760cd24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 28 May 2022 00:59:48 GMT
ADD file:975c801b5b50aa75e07d18e69af11f21e165561abc16246e2c413c2ef96ce4c6 in / 
# Sat, 28 May 2022 00:59:49 GMT
CMD ["bash"]
# Sun, 29 May 2022 07:20:34 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sun, 29 May 2022 07:20:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sun, 29 May 2022 07:21:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 29 May 2022 07:21:19 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sun, 29 May 2022 07:21:21 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sun, 29 May 2022 07:21:21 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sun, 29 May 2022 07:21:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sun, 29 May 2022 07:21:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sun, 29 May 2022 07:21:22 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 09 Jun 2022 23:12:37 GMT
ENV PHP_VERSION=8.1.7
# Thu, 09 Jun 2022 23:12:38 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.7.tar.xz.asc
# Thu, 09 Jun 2022 23:12:38 GMT
ENV PHP_SHA256=f042322f1b5a9f7c2decb84b7086ef676896c2f7178739b9672afafa964ed0e5
# Thu, 09 Jun 2022 23:12:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 09 Jun 2022 23:13:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 09 Jun 2022 23:27:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 09 Jun 2022 23:27:42 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 09 Jun 2022 23:27:44 GMT
RUN docker-php-ext-enable sodium
# Thu, 09 Jun 2022 23:27:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Jun 2022 23:27:45 GMT
WORKDIR /var/www/html
# Thu, 09 Jun 2022 23:27:46 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 09 Jun 2022 23:27:47 GMT
STOPSIGNAL SIGQUIT
# Thu, 09 Jun 2022 23:27:47 GMT
EXPOSE 9000
# Thu, 09 Jun 2022 23:27:48 GMT
CMD ["php-fpm"]
# Fri, 10 Jun 2022 11:35:00 GMT
LABEL org.opencontainers.image.title=YOURLS
# Fri, 10 Jun 2022 11:35:00 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Fri, 10 Jun 2022 11:35:01 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Fri, 10 Jun 2022 11:35:01 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Fri, 10 Jun 2022 11:35:02 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Fri, 10 Jun 2022 11:35:02 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Fri, 10 Jun 2022 11:35:02 GMT
LABEL org.opencontainers.image.licenses=MIT
# Fri, 10 Jun 2022 11:36:05 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Fri, 10 Jun 2022 11:36:07 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 10 Jun 2022 11:36:07 GMT
ARG YOURLS_VERSION=1.9
# Fri, 10 Jun 2022 11:36:08 GMT
ARG YOURLS_SHA256=212c4cd283f0b2b44e07da66a882cca4886e064f642bf4de8ecb8dbfb867e542
# Fri, 10 Jun 2022 11:36:08 GMT
LABEL org.opencontainers.image.version=1.9
# Fri, 10 Jun 2022 11:36:08 GMT
ENV YOURLS_VERSION=1.9
# Fri, 10 Jun 2022 11:36:09 GMT
ENV YOURLS_SHA256=212c4cd283f0b2b44e07da66a882cca4886e064f642bf4de8ecb8dbfb867e542
# Fri, 10 Jun 2022 11:36:13 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Fri, 10 Jun 2022 11:36:13 GMT
COPY --chown=www-data:www-datafile:f5584b9849b80034920f4de5f1297cb1be461f765f3437b87ddf6c86daa6499d in /usr/src/yourls/user/ 
# Fri, 10 Jun 2022 11:36:14 GMT
COPY file:975ababf859e7cabd8184ab0b2b317a5d8d3ccb6f4922be7f2a5d28c20d075a2 in /usr/local/bin/ 
# Fri, 10 Jun 2022 11:36:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Jun 2022 11:36:15 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:eeb117569618df53320eb28d32b7a1d87792bda3362017123fa1025b55db44c3`  
		Last Modified: Sat, 28 May 2022 01:15:35 GMT  
		Size: 26.6 MB (26576237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d3aba112689c02d6b26a241e0065c97e4d937ec22a83ec2611313d531e8b0a`  
		Last Modified: Sun, 29 May 2022 10:31:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c1acd8b719bd38a8741d6d093c916a6a558e402efb4f9e8a9c0d8331959d0d`  
		Last Modified: Sun, 29 May 2022 10:31:44 GMT  
		Size: 69.3 MB (69318858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669dd875526c016d77dc484bfa38a4f856de0994a919ad17c67ba551ea39613a`  
		Last Modified: Sun, 29 May 2022 10:31:01 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef8c6d6e212bd3bede865cb6589ea784e8a875a71cdd08cc58263a07efff9f01`  
		Last Modified: Fri, 10 Jun 2022 02:05:08 GMT  
		Size: 12.0 MB (12035877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:025ba68a89acfaabb7970bf2a33268886256eea00fb36bb7d41ad732c9aebd33`  
		Last Modified: Fri, 10 Jun 2022 02:05:05 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df347adfd9754b3f821377e706361ce05dd223804d04206bcc39bee57b748f31`  
		Last Modified: Fri, 10 Jun 2022 02:07:30 GMT  
		Size: 24.0 MB (23967680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc6a013b87cd266d74c8d82073638d02906efe60a059a9d99d8a0eeac59aa3d1`  
		Last Modified: Fri, 10 Jun 2022 02:07:15 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92ed173dff027000600f30fb9b0399647eb38acdf543961ccef1eda9b28134f6`  
		Last Modified: Fri, 10 Jun 2022 02:07:15 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:003286a8d655b2d57f8ae7e7ece23f3953a3e68f2e2ee0fac49f26aee3de818c`  
		Last Modified: Fri, 10 Jun 2022 02:07:15 GMT  
		Size: 8.6 KB (8625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72987182e093a3f36558f3dc8211fe444b8a8ca4a189e9f7b63e0ff351cd45b`  
		Last Modified: Fri, 10 Jun 2022 11:39:34 GMT  
		Size: 138.4 KB (138444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3efd0d9326582c2b8dc2ba2831296c62659b035bbc8be6c4d0576626f0992579`  
		Last Modified: Fri, 10 Jun 2022 11:39:34 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acec9e63b857dfe03976a611f7c26f7cf531240cae1198142c822fc412441572`  
		Last Modified: Fri, 10 Jun 2022 11:39:37 GMT  
		Size: 3.9 MB (3944335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c40a0317ad738dc2400773190240610725778503b68a115e22fb555f3da342`  
		Last Modified: Fri, 10 Jun 2022 11:39:34 GMT  
		Size: 2.1 KB (2052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82bbe896284cc61b79f2403718f6ae0eff8a78bce1b318608024e827d27bf900`  
		Last Modified: Fri, 10 Jun 2022 11:39:34 GMT  
		Size: 1.6 KB (1555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:1105913b135c543fe21e4bdc25a4ccb85498681d41d0a17cc46295fc7951b1b7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.4 MB (159400347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:935eaefc906369b6698bbb7642be63b3b92600854fca561af597a6c81104aac5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 23 Jun 2022 00:40:43 GMT
ADD file:134be48af13f80f3474bf1b080ca781feb7b972148d482849862e55eb2acd61c in / 
# Thu, 23 Jun 2022 00:40:44 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 06:30:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Jun 2022 06:30:57 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Jun 2022 06:31:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 06:31:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Jun 2022 06:31:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 23 Jun 2022 06:31:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Jun 2022 06:31:16 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Jun 2022 06:31:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Jun 2022 07:04:51 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 23 Jun 2022 07:04:52 GMT
ENV PHP_VERSION=8.1.7
# Thu, 23 Jun 2022 07:04:53 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.7.tar.xz.asc
# Thu, 23 Jun 2022 07:04:54 GMT
ENV PHP_SHA256=f042322f1b5a9f7c2decb84b7086ef676896c2f7178739b9672afafa964ed0e5
# Thu, 23 Jun 2022 07:05:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jun 2022 07:05:15 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jun 2022 07:17:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 23 Jun 2022 07:17:06 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 23 Jun 2022 07:17:07 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jun 2022 07:17:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jun 2022 07:17:08 GMT
WORKDIR /var/www/html
# Thu, 23 Jun 2022 07:17:09 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 23 Jun 2022 07:17:10 GMT
STOPSIGNAL SIGQUIT
# Thu, 23 Jun 2022 07:17:11 GMT
EXPOSE 9000
# Thu, 23 Jun 2022 07:17:12 GMT
CMD ["php-fpm"]
# Thu, 23 Jun 2022 21:33:27 GMT
LABEL org.opencontainers.image.title=YOURLS
# Thu, 23 Jun 2022 21:33:28 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Thu, 23 Jun 2022 21:33:29 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Thu, 23 Jun 2022 21:33:30 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Thu, 23 Jun 2022 21:33:31 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Thu, 23 Jun 2022 21:33:32 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Thu, 23 Jun 2022 21:33:33 GMT
LABEL org.opencontainers.image.licenses=MIT
# Thu, 23 Jun 2022 21:34:42 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Thu, 23 Jun 2022 21:34:43 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 23 Jun 2022 21:34:44 GMT
ARG YOURLS_VERSION=1.9
# Thu, 23 Jun 2022 21:34:45 GMT
ARG YOURLS_SHA256=212c4cd283f0b2b44e07da66a882cca4886e064f642bf4de8ecb8dbfb867e542
# Thu, 23 Jun 2022 21:34:46 GMT
LABEL org.opencontainers.image.version=1.9
# Thu, 23 Jun 2022 21:34:47 GMT
ENV YOURLS_VERSION=1.9
# Thu, 23 Jun 2022 21:34:48 GMT
ENV YOURLS_SHA256=212c4cd283f0b2b44e07da66a882cca4886e064f642bf4de8ecb8dbfb867e542
# Thu, 23 Jun 2022 21:34:51 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 23 Jun 2022 21:34:52 GMT
COPY --chown=www-data:www-datafile:f5584b9849b80034920f4de5f1297cb1be461f765f3437b87ddf6c86daa6499d in /usr/src/yourls/user/ 
# Thu, 23 Jun 2022 21:34:53 GMT
COPY file:975ababf859e7cabd8184ab0b2b317a5d8d3ccb6f4922be7f2a5d28c20d075a2 in /usr/local/bin/ 
# Thu, 23 Jun 2022 21:34:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jun 2022 21:34:54 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3b157c852f2736e12f09046f214fe5f6a0b1652bd860269b3988c92a197026e8`  
		Last Modified: Thu, 23 Jun 2022 00:47:22 GMT  
		Size: 30.1 MB (30065720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9064b3648c6a5f2cda0032f67b6f6465e24ae3a39b2e047c4322e4108aa647a`  
		Last Modified: Thu, 23 Jun 2022 08:31:28 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cda30062909c4a13c42faa2236e16b41c16f6483668beb8238555a45c37874`  
		Last Modified: Thu, 23 Jun 2022 08:31:41 GMT  
		Size: 86.7 MB (86719420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ab96a6881fbce99f8cfaf433c36e67957f8655d9a2c83df569e1384e222b883`  
		Last Modified: Thu, 23 Jun 2022 08:31:27 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:910c80452bb127b74c5e82f6bd471f7c1c653ce0e7ec7dc2e9f387f579e1dbc8`  
		Last Modified: Thu, 23 Jun 2022 08:34:55 GMT  
		Size: 11.8 MB (11821434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb935a34224ca4111e9626cc52b80dce475619748a36147b9282a564e8219198`  
		Last Modified: Thu, 23 Jun 2022 08:34:53 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d99b45f8bc0d74bff66b374432009340a5e308fd2cadcc7bfc5e29f8a3a07d5`  
		Last Modified: Thu, 23 Jun 2022 08:36:33 GMT  
		Size: 26.0 MB (26040537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c0c84c22cd844bd179d7b3b827f073a1fcf7ded6fc1e5556b7ed22346256944`  
		Last Modified: Thu, 23 Jun 2022 08:36:29 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:821fd5bde3dc9f33c241cbf6193887b7d3183e7c09983d7b1695e9a8185acba6`  
		Last Modified: Thu, 23 Jun 2022 08:36:29 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3129e990a38f74f695fdc39c4f0ebe98d6c9e35c600c311c821b01fc7e4dd6`  
		Last Modified: Thu, 23 Jun 2022 08:36:29 GMT  
		Size: 8.6 KB (8623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4efdb02ea7be4d5399e346d2b7467b8eb71785fac542c05e22bce29b34207bc2`  
		Last Modified: Thu, 23 Jun 2022 21:36:11 GMT  
		Size: 792.8 KB (792758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a22606e17a84935ea357dca4a9f7e48426ca601fdd8cf66420b0ae910be9e0a`  
		Last Modified: Thu, 23 Jun 2022 21:36:11 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:447e136c8e6cf4bf2309dfa0e7fbd6fa9c5c8e090bfb226fa3ab9f63a9378dff`  
		Last Modified: Thu, 23 Jun 2022 21:36:12 GMT  
		Size: 3.9 MB (3944286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9392dbd8d1d6255929557ce84b25fac466494672c23a28632bfa09eb75bf83be`  
		Last Modified: Thu, 23 Jun 2022 21:36:11 GMT  
		Size: 2.1 KB (2052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7b2cda0f83937086241034afcd986ceb398e792152625895daf298391e6352`  
		Last Modified: Thu, 23 Jun 2022 21:36:11 GMT  
		Size: 1.6 KB (1554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm` - linux; 386

```console
$ docker pull yourls@sha256:94cc9576f7eedc051dc7ae003c4817742aa5a113632d20af16b6c9dc29b916ed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.7 MB (167654087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d7e45edc60c062aa7cd9ce14abd5fbd1d1729519f7587d1c385ec33cd8950d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 23 Jun 2022 00:39:33 GMT
ADD file:9d46d3f8fb63833a6dbd8dd796ad541d556046a48342d22e1fd3bffa3fb8e504 in / 
# Thu, 23 Jun 2022 00:39:33 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 11:41:40 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Jun 2022 11:41:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Jun 2022 11:42:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 11:42:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Jun 2022 11:42:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 23 Jun 2022 11:42:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Jun 2022 11:42:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Jun 2022 11:42:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Jun 2022 12:08:29 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 23 Jun 2022 12:08:30 GMT
ENV PHP_VERSION=8.1.7
# Thu, 23 Jun 2022 12:08:31 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.7.tar.xz.asc
# Thu, 23 Jun 2022 12:08:32 GMT
ENV PHP_SHA256=f042322f1b5a9f7c2decb84b7086ef676896c2f7178739b9672afafa964ed0e5
# Thu, 23 Jun 2022 12:08:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jun 2022 12:08:53 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jun 2022 12:18:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 23 Jun 2022 12:18:04 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 23 Jun 2022 12:18:04 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jun 2022 12:18:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jun 2022 12:18:06 GMT
WORKDIR /var/www/html
# Thu, 23 Jun 2022 12:18:07 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 23 Jun 2022 12:18:08 GMT
STOPSIGNAL SIGQUIT
# Thu, 23 Jun 2022 12:18:09 GMT
EXPOSE 9000
# Thu, 23 Jun 2022 12:18:10 GMT
CMD ["php-fpm"]
# Thu, 23 Jun 2022 18:51:07 GMT
LABEL org.opencontainers.image.title=YOURLS
# Thu, 23 Jun 2022 18:51:07 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Thu, 23 Jun 2022 18:51:08 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Thu, 23 Jun 2022 18:51:09 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Thu, 23 Jun 2022 18:51:10 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Thu, 23 Jun 2022 18:51:11 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Thu, 23 Jun 2022 18:51:12 GMT
LABEL org.opencontainers.image.licenses=MIT
# Thu, 23 Jun 2022 18:51:48 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Thu, 23 Jun 2022 18:51:49 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 23 Jun 2022 18:51:50 GMT
ARG YOURLS_VERSION=1.9
# Thu, 23 Jun 2022 18:51:51 GMT
ARG YOURLS_SHA256=212c4cd283f0b2b44e07da66a882cca4886e064f642bf4de8ecb8dbfb867e542
# Thu, 23 Jun 2022 18:51:52 GMT
LABEL org.opencontainers.image.version=1.9
# Thu, 23 Jun 2022 18:51:53 GMT
ENV YOURLS_VERSION=1.9
# Thu, 23 Jun 2022 18:51:54 GMT
ENV YOURLS_SHA256=212c4cd283f0b2b44e07da66a882cca4886e064f642bf4de8ecb8dbfb867e542
# Thu, 23 Jun 2022 18:51:57 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 23 Jun 2022 18:51:58 GMT
COPY --chown=www-data:www-datafile:f5584b9849b80034920f4de5f1297cb1be461f765f3437b87ddf6c86daa6499d in /usr/src/yourls/user/ 
# Thu, 23 Jun 2022 18:51:59 GMT
COPY file:975ababf859e7cabd8184ab0b2b317a5d8d3ccb6f4922be7f2a5d28c20d075a2 in /usr/local/bin/ 
# Thu, 23 Jun 2022 18:51:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jun 2022 18:52:00 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:4870b12e407743816673c11cfb39974d80c1569d876287bef61f8c585954822f`  
		Last Modified: Thu, 23 Jun 2022 00:46:40 GMT  
		Size: 32.4 MB (32390198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1090d3a60d1d6fdda24dfc39bebc748986624eb6704d50fec74f24f9d02bd359`  
		Last Modified: Thu, 23 Jun 2022 13:26:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d42ca7953461e2d2ec71f3f7b3be3185bbef10580cc04d8b2dd05333e08ae016`  
		Last Modified: Thu, 23 Jun 2022 13:26:59 GMT  
		Size: 92.5 MB (92512688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26af2ccf84cef54d7640e15316beaa5cd504fe5d633458a7c2abbc8339c8279e`  
		Last Modified: Thu, 23 Jun 2022 13:26:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a8be420c14656ff6ad4a8f092377fa6ac827d2387d220ecf73eb2777b460b4f`  
		Last Modified: Thu, 23 Jun 2022 13:30:40 GMT  
		Size: 11.8 MB (11821312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd3fdb601f71b87d39eda11f1ee989f487954a21e55d102ebe3d2c05e35857c`  
		Last Modified: Thu, 23 Jun 2022 13:30:39 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4294af245648b7c81d6fc96a534b7063fa5630608bd1949dde85200b03ca27c7`  
		Last Modified: Thu, 23 Jun 2022 13:32:27 GMT  
		Size: 26.5 MB (26476344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f70d2943e5fe513c55a4c96ad4e3248a5676af894de98ea8653a0e4daa1b87`  
		Last Modified: Thu, 23 Jun 2022 13:32:22 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:120eac48d27757db8bf83b67c438c3e2e5265e62fc094364d4fab51b1ceafdf1`  
		Last Modified: Thu, 23 Jun 2022 13:32:22 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f23de3e8c472e159b87a921a4e14b30b334f22e79a9f51ece2247f98520e093`  
		Last Modified: Thu, 23 Jun 2022 13:32:21 GMT  
		Size: 8.6 KB (8623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ffd8ae7916470f250e3a3bc0047ab6be0cb349fc1701f0f8f62c2729f78ea79`  
		Last Modified: Thu, 23 Jun 2022 18:53:15 GMT  
		Size: 493.1 KB (493061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8502f23524116558951084f7c85747ee96f786a64b04bd46468ecc68d227621a`  
		Last Modified: Thu, 23 Jun 2022 18:53:14 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb962eb49610cb689484cade13843bf57bde951ecfb3f6ec5dc954c0022764e9`  
		Last Modified: Thu, 23 Jun 2022 18:53:15 GMT  
		Size: 3.9 MB (3944285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92604c3583f8821fc5fb570ba97ae6a2a580ded516c46631f3e5e24ca2b5da16`  
		Last Modified: Thu, 23 Jun 2022 18:53:14 GMT  
		Size: 2.0 KB (2050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea11f964d2a31220e1309a2ae715b7513c86195a9a0d25828f0fcea80a8ec487`  
		Last Modified: Thu, 23 Jun 2022 18:53:14 GMT  
		Size: 1.6 KB (1556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm` - linux; mips64le

```console
$ docker pull yourls@sha256:09f056ad614736bfb2ee7c0e2b3d1bfcad54cd0da16cbb94e59ecec52741c642
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142603305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a20ad7059cee33c256f2e76124f68f5157d32141363e8b5b17a52cd023487c4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 28 May 2022 01:11:13 GMT
ADD file:f685a156b7ddafe7bafc6fad17cc36cc8a5d6d922fc1c425656ca92266d9a98e in / 
# Sat, 28 May 2022 01:11:18 GMT
CMD ["bash"]
# Sat, 28 May 2022 03:30:29 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 May 2022 03:30:32 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 May 2022 03:32:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 03:32:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 May 2022 03:32:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 May 2022 03:32:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 May 2022 03:32:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 May 2022 03:32:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 28 May 2022 03:32:27 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Fri, 10 Jun 2022 00:48:18 GMT
ENV PHP_VERSION=8.1.7
# Fri, 10 Jun 2022 00:48:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.7.tar.xz.asc
# Fri, 10 Jun 2022 00:48:25 GMT
ENV PHP_SHA256=f042322f1b5a9f7c2decb84b7086ef676896c2f7178739b9672afafa964ed0e5
# Fri, 10 Jun 2022 00:49:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 10 Jun 2022 00:49:24 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 10 Jun 2022 01:30:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 10 Jun 2022 01:30:55 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Fri, 10 Jun 2022 01:31:02 GMT
RUN docker-php-ext-enable sodium
# Fri, 10 Jun 2022 01:31:06 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 10 Jun 2022 01:31:09 GMT
WORKDIR /var/www/html
# Fri, 10 Jun 2022 01:31:16 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 10 Jun 2022 01:31:20 GMT
STOPSIGNAL SIGQUIT
# Fri, 10 Jun 2022 01:31:23 GMT
EXPOSE 9000
# Fri, 10 Jun 2022 01:31:27 GMT
CMD ["php-fpm"]
# Fri, 10 Jun 2022 12:43:28 GMT
LABEL org.opencontainers.image.title=YOURLS
# Fri, 10 Jun 2022 12:43:31 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Fri, 10 Jun 2022 12:43:34 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Fri, 10 Jun 2022 12:43:37 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Fri, 10 Jun 2022 12:43:40 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Fri, 10 Jun 2022 12:43:44 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Fri, 10 Jun 2022 12:43:47 GMT
LABEL org.opencontainers.image.licenses=MIT
# Fri, 10 Jun 2022 12:44:52 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Fri, 10 Jun 2022 12:44:58 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 10 Jun 2022 12:45:01 GMT
ARG YOURLS_VERSION=1.9
# Fri, 10 Jun 2022 12:45:04 GMT
ARG YOURLS_SHA256=212c4cd283f0b2b44e07da66a882cca4886e064f642bf4de8ecb8dbfb867e542
# Fri, 10 Jun 2022 12:45:08 GMT
LABEL org.opencontainers.image.version=1.9
# Fri, 10 Jun 2022 12:45:11 GMT
ENV YOURLS_VERSION=1.9
# Fri, 10 Jun 2022 12:45:14 GMT
ENV YOURLS_SHA256=212c4cd283f0b2b44e07da66a882cca4886e064f642bf4de8ecb8dbfb867e542
# Fri, 10 Jun 2022 12:45:24 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Fri, 10 Jun 2022 12:45:27 GMT
COPY --chown=www-data:www-datafile:f5584b9849b80034920f4de5f1297cb1be461f765f3437b87ddf6c86daa6499d in /usr/src/yourls/user/ 
# Fri, 10 Jun 2022 12:45:30 GMT
COPY file:975ababf859e7cabd8184ab0b2b317a5d8d3ccb6f4922be7f2a5d28c20d075a2 in /usr/local/bin/ 
# Fri, 10 Jun 2022 12:45:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Jun 2022 12:45:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:fdea7139ce36b557a23c4b9c4255387b175f851ed0c51e1e7d78dd301c0e4da8`  
		Last Modified: Sat, 28 May 2022 01:21:35 GMT  
		Size: 29.6 MB (29641237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f48ffa812cba4145b49cbbc61824a577807dfbea2e248d5216b5b1fa5d6d81b5`  
		Last Modified: Sat, 28 May 2022 10:42:22 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ee5523dfa904c61988aab187090bf4bdb8ce8a4c4b8fa903a0ae6bc67d00cc`  
		Last Modified: Sat, 28 May 2022 10:43:14 GMT  
		Size: 71.8 MB (71812105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85368acf1e84d74f279250b786757fc0fad630ccedb2cf42c99422aee2bd1097`  
		Last Modified: Sat, 28 May 2022 10:42:21 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f89f1f284883c1c4f24932c468b5f56125002daa6b54c8ec21ed63dc525e2ba`  
		Last Modified: Fri, 10 Jun 2022 06:04:51 GMT  
		Size: 11.8 MB (11820365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb9de978f797e6966b8f6f6379f9d784e5a24b11f7508fae578df416e178942`  
		Last Modified: Fri, 10 Jun 2022 06:04:47 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf6138975fc6102cd69f2473742e335eb274c0a6d79b11cb2f2b2aa50afab01`  
		Last Modified: Fri, 10 Jun 2022 06:06:52 GMT  
		Size: 25.2 MB (25220179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d17e8e6b939cf38af21816ae086d51e12e680db7455570228e1507a3e71cda`  
		Last Modified: Fri, 10 Jun 2022 06:06:36 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a66754b8b58e39e816a76faf740510db9240c127a572c9da8e562b0be60f5a2`  
		Last Modified: Fri, 10 Jun 2022 06:06:35 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c0b507a86dd6c68a97611ca11d8c116a44bac7337443f12b77a8e427b542613`  
		Last Modified: Fri, 10 Jun 2022 06:06:36 GMT  
		Size: 8.6 KB (8626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd260001a4799145f24d01c6b4a070de4e0a52bc8bfdb7ac75264743da48b19`  
		Last Modified: Fri, 10 Jun 2022 12:46:37 GMT  
		Size: 148.9 KB (148921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9edc833dcf3873d43566d094b054ba4c306df15f4b2386be4f68ab95a395e8`  
		Last Modified: Fri, 10 Jun 2022 12:46:37 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d658e106564b5810fedba1f16b32acfd3185c9891b0b3532e89234f341c0de70`  
		Last Modified: Fri, 10 Jun 2022 12:46:41 GMT  
		Size: 3.9 MB (3944288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30f2f359ec55840f00e304803a0fbe6b403e97f2fd0c4e7008f5307eb77cb322`  
		Last Modified: Fri, 10 Jun 2022 12:46:37 GMT  
		Size: 2.0 KB (2049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b9018a6759cf02540aaab1f3f8e37d69af5d677ecc13c9b3a206aa906236a04`  
		Last Modified: Fri, 10 Jun 2022 12:46:37 GMT  
		Size: 1.6 KB (1555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm` - linux; ppc64le

```console
$ docker pull yourls@sha256:93be8204868cbc9b66670ea45d752e6ef6f11b131928fb596baf7e75d96d0c46
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.3 MB (165339604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd9235ac5f080f48b938b6207b95a5126c50131c1fd337c74476073fceaf8fbe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Sat, 28 May 2022 01:22:54 GMT
ADD file:64e264b12eed99d87380e38f36bfecd62b9bb1e5460f0242cfbc5dc76c212ead in / 
# Sat, 28 May 2022 01:22:59 GMT
CMD ["bash"]
# Sat, 28 May 2022 07:22:10 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 28 May 2022 07:22:15 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 28 May 2022 07:24:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 07:24:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 28 May 2022 07:24:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 28 May 2022 07:24:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 May 2022 07:24:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 28 May 2022 07:24:29 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 28 May 2022 07:24:33 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 09 Jun 2022 22:50:09 GMT
ENV PHP_VERSION=8.1.7
# Thu, 09 Jun 2022 22:50:13 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.7.tar.xz.asc
# Thu, 09 Jun 2022 22:50:16 GMT
ENV PHP_SHA256=f042322f1b5a9f7c2decb84b7086ef676896c2f7178739b9672afafa964ed0e5
# Thu, 09 Jun 2022 22:52:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 09 Jun 2022 22:52:27 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 09 Jun 2022 23:09:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 09 Jun 2022 23:09:40 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 09 Jun 2022 23:09:47 GMT
RUN docker-php-ext-enable sodium
# Thu, 09 Jun 2022 23:09:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 09 Jun 2022 23:09:54 GMT
WORKDIR /var/www/html
# Thu, 09 Jun 2022 23:10:00 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 09 Jun 2022 23:10:03 GMT
STOPSIGNAL SIGQUIT
# Thu, 09 Jun 2022 23:10:07 GMT
EXPOSE 9000
# Thu, 09 Jun 2022 23:10:13 GMT
CMD ["php-fpm"]
# Fri, 10 Jun 2022 15:15:41 GMT
LABEL org.opencontainers.image.title=YOURLS
# Fri, 10 Jun 2022 15:15:43 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Fri, 10 Jun 2022 15:15:45 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Fri, 10 Jun 2022 15:15:47 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Fri, 10 Jun 2022 15:15:49 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Fri, 10 Jun 2022 15:15:52 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Fri, 10 Jun 2022 15:15:55 GMT
LABEL org.opencontainers.image.licenses=MIT
# Fri, 10 Jun 2022 15:16:29 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Fri, 10 Jun 2022 15:16:38 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 10 Jun 2022 15:16:40 GMT
ARG YOURLS_VERSION=1.9
# Fri, 10 Jun 2022 15:16:42 GMT
ARG YOURLS_SHA256=212c4cd283f0b2b44e07da66a882cca4886e064f642bf4de8ecb8dbfb867e542
# Fri, 10 Jun 2022 15:16:44 GMT
LABEL org.opencontainers.image.version=1.9
# Fri, 10 Jun 2022 15:16:46 GMT
ENV YOURLS_VERSION=1.9
# Fri, 10 Jun 2022 15:16:52 GMT
ENV YOURLS_SHA256=212c4cd283f0b2b44e07da66a882cca4886e064f642bf4de8ecb8dbfb867e542
# Fri, 10 Jun 2022 15:16:59 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Fri, 10 Jun 2022 15:17:02 GMT
COPY --chown=www-data:www-datafile:f5584b9849b80034920f4de5f1297cb1be461f765f3437b87ddf6c86daa6499d in /usr/src/yourls/user/ 
# Fri, 10 Jun 2022 15:17:02 GMT
COPY file:975ababf859e7cabd8184ab0b2b317a5d8d3ccb6f4922be7f2a5d28c20d075a2 in /usr/local/bin/ 
# Fri, 10 Jun 2022 15:17:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Jun 2022 15:17:08 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:893e245a8f6219935016f2dd4422ec4b7fdab43d98ba29c024ec0d9ce57794ba`  
		Last Modified: Sat, 28 May 2022 01:32:28 GMT  
		Size: 35.3 MB (35286698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d642c3f5450a6405bbf9bc2437851b0fead8c5637c2187c3d0138aa4c80ebf`  
		Last Modified: Sat, 28 May 2022 10:59:01 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84dd41b6c195f84ab156bcf8fb6794ba7e3f25a1e949fc8dc500f0fd4caa4d3c`  
		Last Modified: Sat, 28 May 2022 10:59:18 GMT  
		Size: 86.6 MB (86628797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f79723c6985ec0cb8d1a54a87d5714b293a1e9dbe5567d6d4997e28bdc5912ae`  
		Last Modified: Sat, 28 May 2022 10:59:01 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9e4d5ed17076ec3bbd6e93901146f1231009fd1dd42387a63223b440f18f07`  
		Last Modified: Fri, 10 Jun 2022 02:12:22 GMT  
		Size: 12.0 MB (12037627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f917e426b2e52e38d4ef640b6d6a4b95eda4369767213255c6cc00034d711816`  
		Last Modified: Fri, 10 Jun 2022 02:12:20 GMT  
		Size: 495.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42925df169f8e41040bbc0081cc0940f22f31f42e8cdadd64bbe21d57b4e91ee`  
		Last Modified: Fri, 10 Jun 2022 02:14:20 GMT  
		Size: 27.2 MB (27242137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404f88bf0dd3801371e21891b23716b2598a632e9cffe87ae0f43fae4ad87714`  
		Last Modified: Fri, 10 Jun 2022 02:14:15 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30cf8a0bc8467cd1b7e58a8c6dea26fd41652f2892ab4ff7faf951abc88c4a88`  
		Last Modified: Fri, 10 Jun 2022 02:14:15 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3ad8bab1367143b13065be1a4c51ead0a6a7d13d4ff283571e2bf1af10f093`  
		Last Modified: Fri, 10 Jun 2022 02:14:15 GMT  
		Size: 8.6 KB (8626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24b82f717509a1a2bba5d882037405d4b7dff7b761dc4a6e7630901daa5a48da`  
		Last Modified: Fri, 10 Jun 2022 15:20:27 GMT  
		Size: 183.8 KB (183759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009ecf858fc1ff70347ed7ef81443e6aceefba6cbe8f47de4092356ca584148e`  
		Last Modified: Fri, 10 Jun 2022 15:20:27 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bdacaea453cd4183cc57e4aa4c07eaf5f007db8da920777a3d7309e81a90dd`  
		Last Modified: Fri, 10 Jun 2022 15:20:27 GMT  
		Size: 3.9 MB (3944327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17868446e82cdd15e438ec7aba085adbfbd31faccf07a04f9c4fb6ad0e288586`  
		Last Modified: Fri, 10 Jun 2022 15:20:26 GMT  
		Size: 2.1 KB (2052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b7ea20fc8dfdb957ea7c082f2094d7e36533a310e03c768abed741fb07f98f`  
		Last Modified: Fri, 10 Jun 2022 15:20:26 GMT  
		Size: 1.6 KB (1557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm` - linux; s390x

```console
$ docker pull yourls@sha256:fabb7c77214119b42eb07098e30620e9ef7db8d6d19bcc39f0c434baa6dfb267
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142709454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51c5e6b347080ff17850df50592eb02e355f0d0e36fe3c4e15ee0e7961ec5b96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 23 Jun 2022 00:43:10 GMT
ADD file:0b511e3efd87267fb27161eae56c4d08f0fed733697da6ffe6ea96a4cb68e938 in / 
# Thu, 23 Jun 2022 00:43:15 GMT
CMD ["bash"]
# Thu, 23 Jun 2022 06:23:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Jun 2022 06:23:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Jun 2022 06:23:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jun 2022 06:24:01 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Jun 2022 06:24:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 23 Jun 2022 06:24:01 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Jun 2022 06:24:02 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Jun 2022 06:24:02 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Jun 2022 06:45:24 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 23 Jun 2022 06:45:24 GMT
ENV PHP_VERSION=8.1.7
# Thu, 23 Jun 2022 06:45:24 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.7.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.7.tar.xz.asc
# Thu, 23 Jun 2022 06:45:24 GMT
ENV PHP_SHA256=f042322f1b5a9f7c2decb84b7086ef676896c2f7178739b9672afafa964ed0e5
# Thu, 23 Jun 2022 06:45:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Jun 2022 06:45:33 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Jun 2022 06:52:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 23 Jun 2022 06:52:08 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 23 Jun 2022 06:52:08 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Jun 2022 06:52:08 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Jun 2022 06:52:09 GMT
WORKDIR /var/www/html
# Thu, 23 Jun 2022 06:52:09 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 23 Jun 2022 06:52:09 GMT
STOPSIGNAL SIGQUIT
# Thu, 23 Jun 2022 06:52:09 GMT
EXPOSE 9000
# Thu, 23 Jun 2022 06:52:09 GMT
CMD ["php-fpm"]
# Thu, 23 Jun 2022 20:36:21 GMT
LABEL org.opencontainers.image.title=YOURLS
# Thu, 23 Jun 2022 20:36:21 GMT
LABEL org.opencontainers.image.description=Your Own URL Shortener
# Thu, 23 Jun 2022 20:36:21 GMT
LABEL org.opencontainers.image.url=https://yourls.org/
# Thu, 23 Jun 2022 20:36:21 GMT
LABEL org.opencontainers.image.documentation=https://yourls.org/
# Thu, 23 Jun 2022 20:36:21 GMT
LABEL org.opencontainers.image.vendor=YOURLS Org
# Thu, 23 Jun 2022 20:36:22 GMT
LABEL org.opencontainers.image.authors=YOURLS
# Thu, 23 Jun 2022 20:36:22 GMT
LABEL org.opencontainers.image.licenses=MIT
# Thu, 23 Jun 2022 20:36:34 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" bcmath opcache pdo_mysql mysqli
# Thu, 23 Jun 2022 20:36:34 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=2';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 23 Jun 2022 20:36:34 GMT
ARG YOURLS_VERSION=1.9
# Thu, 23 Jun 2022 20:36:35 GMT
ARG YOURLS_SHA256=212c4cd283f0b2b44e07da66a882cca4886e064f642bf4de8ecb8dbfb867e542
# Thu, 23 Jun 2022 20:36:35 GMT
LABEL org.opencontainers.image.version=1.9
# Thu, 23 Jun 2022 20:36:35 GMT
ENV YOURLS_VERSION=1.9
# Thu, 23 Jun 2022 20:36:35 GMT
ENV YOURLS_SHA256=212c4cd283f0b2b44e07da66a882cca4886e064f642bf4de8ecb8dbfb867e542
# Thu, 23 Jun 2022 20:36:37 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 23 Jun 2022 20:36:37 GMT
COPY --chown=www-data:www-datafile:f5584b9849b80034920f4de5f1297cb1be461f765f3437b87ddf6c86daa6499d in /usr/src/yourls/user/ 
# Thu, 23 Jun 2022 20:36:37 GMT
COPY file:975ababf859e7cabd8184ab0b2b317a5d8d3ccb6f4922be7f2a5d28c20d075a2 in /usr/local/bin/ 
# Thu, 23 Jun 2022 20:36:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jun 2022 20:36:37 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c547f465e0c8708ad0c57cf09caa52f4c2b5b295bf10ab1ce71ca17ff81ea36a`  
		Last Modified: Thu, 23 Jun 2022 00:51:59 GMT  
		Size: 29.7 MB (29655262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64ac3dc014d550bf03a1729b039a5f18fc36ee17be3dd0416bb30c3b4a7535c1`  
		Last Modified: Thu, 23 Jun 2022 07:57:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4014f31e7ed528e757a0a6304c23851740d7fc224ebc60a432fe29fcfe7d22d9`  
		Last Modified: Thu, 23 Jun 2022 07:57:10 GMT  
		Size: 71.6 MB (71623880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69abfac73dadc0771e03f979a0317fbbd77e330ec2249b29ff7fe9b1847a7c6`  
		Last Modified: Thu, 23 Jun 2022 07:57:00 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3544f4d9811fc0b5bc4a42cce9f4332e5a1475107afb506dc3a3ac49854d4d0f`  
		Last Modified: Thu, 23 Jun 2022 07:59:30 GMT  
		Size: 12.0 MB (12036098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94c65436884c2f6959832cd4d25c45b0d1ccf1da4e30048d3e71de40f0597c3`  
		Last Modified: Thu, 23 Jun 2022 07:59:29 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8e14e609f0e34c192bff4279453ed9da1cc41a0c57eda96d76edb90f0be22f`  
		Last Modified: Thu, 23 Jun 2022 08:00:38 GMT  
		Size: 25.3 MB (25275485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f5c3ecdb47397474fd263ec280bfdb257fec795de9d42eb621974a06740629`  
		Last Modified: Thu, 23 Jun 2022 08:00:35 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81757210f4f360c4a5f79cc005fb981ce72969542678297866e840e75390bec2`  
		Last Modified: Thu, 23 Jun 2022 08:00:35 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b55f50d42c0c89fa049ed7879f0031b164e5e858ba1ece6e8105a552b68bc5b`  
		Last Modified: Thu, 23 Jun 2022 08:00:35 GMT  
		Size: 8.6 KB (8621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f5bd9bc7c87e892beda9ca4d9ea8cdc16d3667a2a8575fff536ee3da17695a6`  
		Last Modified: Thu, 23 Jun 2022 20:37:36 GMT  
		Size: 158.2 KB (158182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:228fbd77ff0dae546b3db52e97f015bb806d4f84054201e637e48baa34c08f61`  
		Last Modified: Thu, 23 Jun 2022 20:37:36 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a42388626b33589f69c7657132db0dab8d53ac1872b032fd95552ea58fd399`  
		Last Modified: Thu, 23 Jun 2022 20:37:36 GMT  
		Size: 3.9 MB (3944319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7deb983c21c57427459c76c9cfadf47f7d0485d9b0bbb24565ea0d1b3f11de1`  
		Last Modified: Thu, 23 Jun 2022 20:37:36 GMT  
		Size: 2.0 KB (2046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a7d598de43a34fa4daebbacd64f1065b6ea36f8432c17970d76ac02b59b073`  
		Last Modified: Thu, 23 Jun 2022 20:37:36 GMT  
		Size: 1.6 KB (1550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
