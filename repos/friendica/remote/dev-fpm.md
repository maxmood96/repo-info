## `friendica:dev-fpm`

```console
$ docker pull friendica@sha256:85da390c232ce0896eaec229734f17fcde0c1e44b09c64278353c5486b819dfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `friendica:dev-fpm` - linux; amd64

```console
$ docker pull friendica@sha256:458778a91705f0ab84eaf082e4acb03a797a82fe80e9c71d9989fd1e805ede23
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.4 MB (179411006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66369c1f355cfb2fca2ee168eedaf13a1d0730ee85700d0981195e4ff385110f`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 12 Mar 2021 02:20:40 GMT
ADD file:3c32f1cd03198e141dd233a7ffd13444157d4150ad917d548f3ee9bf5953ce22 in / 
# Fri, 12 Mar 2021 02:20:41 GMT
CMD ["bash"]
# Sat, 13 Mar 2021 02:15:54 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 13 Mar 2021 02:15:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 13 Mar 2021 02:16:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 13 Mar 2021 02:16:13 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 13 Mar 2021 02:16:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 13 Mar 2021 02:28:48 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 13 Mar 2021 02:28:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 13 Mar 2021 02:28:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 13 Mar 2021 02:28:49 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 13 Mar 2021 03:07:30 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Sat, 13 Mar 2021 03:07:30 GMT
ENV PHP_VERSION=7.3.27
# Sat, 13 Mar 2021 03:07:30 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.27.tar.xz.asc
# Sat, 13 Mar 2021 03:07:31 GMT
ENV PHP_SHA256=65f616e2d5b6faacedf62830fa047951b0136d5da34ae59e6744cbaf5dca148d
# Sat, 13 Mar 2021 03:07:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 13 Mar 2021 03:07:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 13 Mar 2021 03:13:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 13 Mar 2021 03:13:11 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Sat, 13 Mar 2021 03:13:12 GMT
RUN docker-php-ext-enable sodium
# Sat, 13 Mar 2021 03:13:13 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Sat, 13 Mar 2021 03:13:14 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 13 Mar 2021 03:13:14 GMT
WORKDIR /var/www/html
# Sat, 13 Mar 2021 03:13:15 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Sat, 13 Mar 2021 03:13:16 GMT
STOPSIGNAL SIGQUIT
# Sat, 13 Mar 2021 03:13:16 GMT
EXPOSE 9000
# Sat, 13 Mar 2021 03:13:16 GMT
CMD ["php-fpm"]
# Sat, 13 Mar 2021 15:58:07 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         git         msmtp         gnupg dirmngr     ;     rm -rf /var/lib/apt/lists/*;
# Sat, 13 Mar 2021 15:58:07 GMT
ENV TINI_VERSION=v0.19.0
# Sat, 13 Mar 2021 15:58:09 GMT
RUN export BUILD_ARCH=$(dpkg-architecture --query DEB_BUILD_ARCH)  && mkdir ~/.gnupg  && echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf  && curl -L -o /sbin/tini https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}  && curl -L -o /tini.asc https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}.asc  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7  && gpg --batch --verify /tini.asc /sbin/tini  && chmod +x /sbin/tini
# Sat, 13 Mar 2021 16:00:07 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.20;     pecl install memcached-3.1.5;     pecl install redis-5.3.3;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Sat, 13 Mar 2021 16:00:08 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Sat, 13 Mar 2021 16:00:08 GMT
VOLUME [/var/www/html]
# Sat, 13 Mar 2021 16:03:39 GMT
ENV FRIENDICA_VERSION=2021.03-dev
# Sat, 13 Mar 2021 16:03:39 GMT
ENV FRIENDICA_ADDONS=2021.03-dev
# Sat, 13 Mar 2021 16:03:39 GMT
COPY multi:b20e37902564ea2dd022293f7b41911842ada0268aa69dff8006238a11a5b5e0 in / 
# Sat, 13 Mar 2021 16:03:40 GMT
COPY multi:923de5042cde61ed518a7067985e18cb873d0cd10946593bfb44de6ba9e078ed in /usr/src/friendica/config/ 
# Sat, 13 Mar 2021 16:03:40 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Sat, 13 Mar 2021 16:03:40 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6f28985ad1843afd6fd4fe0b42a30bfab63c27d302362e7341e3316e8ba25ced`  
		Last Modified: Fri, 12 Mar 2021 02:26:11 GMT  
		Size: 27.1 MB (27101001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db883aae18bc008a4ef1e00647660bd700053b7a3f00c26d613533d22e4945d8`  
		Last Modified: Sat, 13 Mar 2021 03:42:06 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffae70ea03a956afbb3c504bd109810da75045c9c96c03fbb36669922ffbc161`  
		Last Modified: Sat, 13 Mar 2021 03:42:20 GMT  
		Size: 76.7 MB (76678257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8027612378a55bb01d4b8d62d26e17252295f14b45039c08331829b3c8629d`  
		Last Modified: Sat, 13 Mar 2021 03:42:06 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccac830b4f4d7362e6403cc2456eeab269807dbfece37bfdab8460cdcde11d60`  
		Last Modified: Sat, 13 Mar 2021 03:48:32 GMT  
		Size: 12.5 MB (12459914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b866577a07507af380914caea07793504cfca702fe4e1a03e0a1837ed89e65`  
		Last Modified: Sat, 13 Mar 2021 03:48:31 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ab721d965408831c4662747760eb0581007e928866ef822f627ad21406bf64`  
		Last Modified: Sat, 13 Mar 2021 03:48:34 GMT  
		Size: 28.8 MB (28768962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c8df39c216347ad77373bf3d6c892eb4e7c8bc120d9045e16f71ef8d455d10a`  
		Last Modified: Sat, 13 Mar 2021 03:48:28 GMT  
		Size: 2.3 KB (2270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf008ad2f1c1e6e162a4bcd21136f06031c35984f043b6a05fa401bf1e9c068`  
		Last Modified: Sat, 13 Mar 2021 03:48:28 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736eb2b735814b38108c05cca8507c7c8162f121b2c8e9076c591d727d0d4120`  
		Last Modified: Sat, 13 Mar 2021 03:48:28 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5ded5790b70c033b03ec2f791d0e6e10af15d5c1ba5a117756984aef661f16f`  
		Last Modified: Sat, 13 Mar 2021 03:48:28 GMT  
		Size: 8.4 KB (8418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb9603e343436e96131b2a98235e449d87030c976a6167781d16abed7c6a03b`  
		Last Modified: Sat, 13 Mar 2021 16:05:04 GMT  
		Size: 19.1 MB (19102540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cfa1edaf285a3d703cdcc80fe0e5b056985411aed08c5bd88367d6f7fa1e94b`  
		Last Modified: Sat, 13 Mar 2021 16:04:59 GMT  
		Size: 16.1 KB (16135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030a5e01c1192844fdf9b5bbba30650c22503e10048bf34b9a8c9026b89b2b35`  
		Last Modified: Sat, 13 Mar 2021 16:05:00 GMT  
		Size: 15.3 MB (15267131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75919e33d88efb24f977c01a73fb4aa7990b322e31a943866ac65f21aac5ea76`  
		Last Modified: Sat, 13 Mar 2021 16:04:57 GMT  
		Size: 579.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eab1cf79796f0e277439a4819437eb5780af118c7587034154c57f74680d030`  
		Last Modified: Sat, 13 Mar 2021 16:07:03 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d6224e0a78cfd0369aa74f0dbfe6b522cbe0c9e2ea8956b43408f679b0a0fc`  
		Last Modified: Sat, 13 Mar 2021 16:07:03 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:dev-fpm` - linux; arm variant v5

```console
$ docker pull friendica@sha256:28257bec4b6f481ecd344343c94497bd19f9c9116562ffe94397cda70ccd1b43
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155134532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8f2cf0c9e414c668edb402e7310a923ebadb2a44fcc06736e54192f313b5c42`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 26 Mar 2021 07:51:46 GMT
ADD file:3dd25698bf1578e8580b2f437a2199bfc3b1818480b874d73622357e955a091f in / 
# Fri, 26 Mar 2021 07:51:48 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 12:48:54 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 26 Mar 2021 12:48:56 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 26 Mar 2021 12:49:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 12:49:57 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 26 Mar 2021 12:50:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 26 Mar 2021 13:00:08 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 26 Mar 2021 13:00:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 26 Mar 2021 13:00:10 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 26 Mar 2021 13:00:11 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 26 Mar 2021 13:35:45 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Fri, 26 Mar 2021 13:35:48 GMT
ENV PHP_VERSION=7.3.27
# Fri, 26 Mar 2021 13:35:50 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.27.tar.xz.asc
# Fri, 26 Mar 2021 13:35:51 GMT
ENV PHP_SHA256=65f616e2d5b6faacedf62830fa047951b0136d5da34ae59e6744cbaf5dca148d
# Fri, 26 Mar 2021 13:36:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 26 Mar 2021 13:36:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 26 Mar 2021 13:39:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 26 Mar 2021 13:39:56 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 26 Mar 2021 13:39:59 GMT
RUN docker-php-ext-enable sodium
# Fri, 26 Mar 2021 13:40:02 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 26 Mar 2021 13:40:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 26 Mar 2021 13:40:04 GMT
WORKDIR /var/www/html
# Fri, 26 Mar 2021 13:40:06 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 26 Mar 2021 13:40:07 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 13:40:08 GMT
EXPOSE 9000
# Fri, 26 Mar 2021 13:40:09 GMT
CMD ["php-fpm"]
# Fri, 26 Mar 2021 22:18:11 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         git         msmtp         gnupg dirmngr     ;     rm -rf /var/lib/apt/lists/*;
# Fri, 26 Mar 2021 22:18:12 GMT
ENV TINI_VERSION=v0.19.0
# Fri, 26 Mar 2021 22:18:15 GMT
RUN export BUILD_ARCH=$(dpkg-architecture --query DEB_BUILD_ARCH)  && mkdir ~/.gnupg  && echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf  && curl -L -o /sbin/tini https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}  && curl -L -o /tini.asc https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}.asc  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7  && gpg --batch --verify /tini.asc /sbin/tini  && chmod +x /sbin/tini
# Fri, 26 Mar 2021 22:22:35 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.20;     pecl install memcached-3.1.5;     pecl install redis-5.3.3;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 22:22:38 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 26 Mar 2021 22:22:39 GMT
VOLUME [/var/www/html]
# Fri, 26 Mar 2021 22:24:39 GMT
ENV FRIENDICA_VERSION=2021.03-dev
# Fri, 26 Mar 2021 22:24:40 GMT
ENV FRIENDICA_ADDONS=2021.03-dev
# Fri, 26 Mar 2021 22:24:41 GMT
COPY multi:b20e37902564ea2dd022293f7b41911842ada0268aa69dff8006238a11a5b5e0 in / 
# Fri, 26 Mar 2021 22:24:42 GMT
COPY multi:923de5042cde61ed518a7067985e18cb873d0cd10946593bfb44de6ba9e078ed in /usr/src/friendica/config/ 
# Fri, 26 Mar 2021 22:24:43 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Fri, 26 Mar 2021 22:24:44 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:997e59852ec0e1a23e4a179db14793947d60390c392ce15abc0f811e797c49ca`  
		Last Modified: Fri, 26 Mar 2021 08:00:22 GMT  
		Size: 24.8 MB (24846159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e4f992f1746b0ab08c849afc6fcbe26e6527dba7d8ea30442d6fa1947df30a9`  
		Last Modified: Fri, 26 Mar 2021 14:06:36 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4bb1b488e61bd718851af1ed0f5528cd36d27e57974287f9de9a240a8fbe92c`  
		Last Modified: Fri, 26 Mar 2021 14:07:17 GMT  
		Size: 58.8 MB (58815829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d255b28d593bbda7f415959ea6754f02bd0faad03b926ce0a7aadb8d0f8a138c`  
		Last Modified: Fri, 26 Mar 2021 14:06:36 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1f639f53668b6fb3ab38b755d87ba18ac65089b2915d41b56bbd8c8ba4a7d8`  
		Last Modified: Fri, 26 Mar 2021 14:12:08 GMT  
		Size: 12.5 MB (12457984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727523d5f45971bacc13cba023c15d29d38921a50612b8f9f440b59d5798293c`  
		Last Modified: Fri, 26 Mar 2021 14:12:05 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b337db963182a2a88621b368ff14b8ed75d33295469b9d221c1792a84cb6dc9`  
		Last Modified: Fri, 26 Mar 2021 14:12:16 GMT  
		Size: 27.3 MB (27321629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:109a766132210f0cff1ad7de5c9fb3343d1917de8b52b7b88e8e0f38cd77056a`  
		Last Modified: Fri, 26 Mar 2021 14:12:04 GMT  
		Size: 2.3 KB (2272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f809c2c7b522152429809a07f28c2808d3d3d9a9dd34557ee56d17819591d6c`  
		Last Modified: Fri, 26 Mar 2021 14:12:04 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd30d345b7bbebd9a544ae65260cc306b379c6569b226b0e6a8f764d88efad0`  
		Last Modified: Fri, 26 Mar 2021 14:12:04 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:610cb68331529df57a473f693c9a0ad2cd1e9b7e6223fbab76ab5512f1b90f50`  
		Last Modified: Fri, 26 Mar 2021 14:12:01 GMT  
		Size: 8.4 KB (8416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b726ecd18c8fafb7c3b67da428382e64823ccef45225798605bde40286ec1438`  
		Last Modified: Fri, 26 Mar 2021 22:26:07 GMT  
		Size: 17.8 MB (17789519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a932905b29cc46fedb245a28829051d73baab3b832f2dd24e2a2f0a53aa3f683`  
		Last Modified: Fri, 26 Mar 2021 22:26:03 GMT  
		Size: 15.5 KB (15526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4eeda8e85ae0495019e5d153c8ef6b5277718a51aba8fbda1959ccd042223c4`  
		Last Modified: Fri, 26 Mar 2021 22:26:04 GMT  
		Size: 13.9 MB (13870829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96a57379d8d84d1168b2a4b44d2cce01259b16a9edb15ad94764cac47dc26488`  
		Last Modified: Fri, 26 Mar 2021 22:26:00 GMT  
		Size: 574.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e619776c1c3952702a677dcf4e0f71278aa787afc6162047666e89f5caa2bfc`  
		Last Modified: Fri, 26 Mar 2021 22:27:33 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1060e6f38fda6b49843190f3391572481d909b2587d5403f0730b61d01da29b`  
		Last Modified: Fri, 26 Mar 2021 22:27:33 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:dev-fpm` - linux; arm variant v7

```console
$ docker pull friendica@sha256:c0c8fcf7bedb7714045f7d9d8e8da79c0c7c90b33ff6938d246b76ca6e1c5df5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (149960626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:447d3bae0100df3d4378e393e4a349902bbe41e0a2a4e0e4b300873a8efb8c02`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 26 Mar 2021 11:17:38 GMT
ADD file:911acc83e6d3d4b00ecc59effce9e5ab69d62aa3e77a24db76e270db8cedce5f in / 
# Fri, 26 Mar 2021 11:17:39 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 18:19:04 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 26 Mar 2021 18:19:05 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 26 Mar 2021 18:19:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 18:19:49 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 26 Mar 2021 18:19:56 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 26 Mar 2021 18:28:11 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 26 Mar 2021 18:28:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 26 Mar 2021 18:28:14 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 26 Mar 2021 18:28:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 26 Mar 2021 18:57:10 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Fri, 26 Mar 2021 18:57:11 GMT
ENV PHP_VERSION=7.3.27
# Fri, 26 Mar 2021 18:57:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.27.tar.xz.asc
# Fri, 26 Mar 2021 18:57:15 GMT
ENV PHP_SHA256=65f616e2d5b6faacedf62830fa047951b0136d5da34ae59e6744cbaf5dca148d
# Fri, 26 Mar 2021 18:57:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 26 Mar 2021 18:57:35 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 26 Mar 2021 19:00:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 26 Mar 2021 19:00:32 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 26 Mar 2021 19:00:36 GMT
RUN docker-php-ext-enable sodium
# Fri, 26 Mar 2021 19:00:40 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 26 Mar 2021 19:00:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 26 Mar 2021 19:00:47 GMT
WORKDIR /var/www/html
# Fri, 26 Mar 2021 19:00:50 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 26 Mar 2021 19:00:51 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 19:00:52 GMT
EXPOSE 9000
# Fri, 26 Mar 2021 19:00:53 GMT
CMD ["php-fpm"]
# Sat, 27 Mar 2021 13:36:42 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         git         msmtp         gnupg dirmngr     ;     rm -rf /var/lib/apt/lists/*;
# Sat, 27 Mar 2021 13:36:43 GMT
ENV TINI_VERSION=v0.19.0
# Sat, 27 Mar 2021 13:36:49 GMT
RUN export BUILD_ARCH=$(dpkg-architecture --query DEB_BUILD_ARCH)  && mkdir ~/.gnupg  && echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf  && curl -L -o /sbin/tini https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}  && curl -L -o /tini.asc https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}.asc  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7  && gpg --batch --verify /tini.asc /sbin/tini  && chmod +x /sbin/tini
# Sat, 27 Mar 2021 13:40:40 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.20;     pecl install memcached-3.1.5;     pecl install redis-5.3.3;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 13:40:44 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Sat, 27 Mar 2021 13:40:44 GMT
VOLUME [/var/www/html]
# Sat, 27 Mar 2021 13:43:14 GMT
ENV FRIENDICA_VERSION=2021.03-dev
# Sat, 27 Mar 2021 13:43:14 GMT
ENV FRIENDICA_ADDONS=2021.03-dev
# Sat, 27 Mar 2021 13:43:17 GMT
COPY multi:b20e37902564ea2dd022293f7b41911842ada0268aa69dff8006238a11a5b5e0 in / 
# Sat, 27 Mar 2021 13:43:18 GMT
COPY multi:923de5042cde61ed518a7067985e18cb873d0cd10946593bfb44de6ba9e078ed in /usr/src/friendica/config/ 
# Sat, 27 Mar 2021 13:43:19 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Sat, 27 Mar 2021 13:43:20 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:05a8be0db5eb6dbb349e49a01211d3a11adc23881f696760a058c0c8ae8e39b7`  
		Last Modified: Fri, 26 Mar 2021 11:27:34 GMT  
		Size: 22.7 MB (22709509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d28c0b6fab1499bb2c7612e43e400e80dd01221d80304b2314e6fae3122d16`  
		Last Modified: Fri, 26 Mar 2021 19:24:07 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750c9e4cb128bf48dda1dcb9cf167ad2a67b9d8b8f561a7b1d2ad81622a67850`  
		Last Modified: Fri, 26 Mar 2021 19:24:28 GMT  
		Size: 59.5 MB (59512646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:629683649fade51a76c161487a63561cfefa29a345b8815f66673ebda404501c`  
		Last Modified: Fri, 26 Mar 2021 19:24:07 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2657658474be166f89de28895193263d02f5520b23e7362c503fbb49596080be`  
		Last Modified: Fri, 26 Mar 2021 19:29:55 GMT  
		Size: 12.5 MB (12457915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84966fe3d4f899dc8be0c34b900e6e719ba5951f2b23ff70164a9f44ae044787`  
		Last Modified: Fri, 26 Mar 2021 19:29:54 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a681b025f68d97062fd2444a88b92e484a72c6166a353be05c487c581eae74de`  
		Last Modified: Fri, 26 Mar 2021 19:30:03 GMT  
		Size: 26.3 MB (26322059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3edba973252faf44c8a113c1208e76e805bc1eba9275ac0382346bad1dd6b0cb`  
		Last Modified: Fri, 26 Mar 2021 19:29:52 GMT  
		Size: 2.3 KB (2271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d19a2852d90bd7903254de082a720a0691e9bfa8badff2b1c09a03da117be9d`  
		Last Modified: Fri, 26 Mar 2021 19:29:52 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6067d2120658669290ec71b78efd191e6f136dbea4ac2542dde11eb16264fc4`  
		Last Modified: Fri, 26 Mar 2021 19:29:52 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a648765c88bbb7499e03af2b207c2fbd6267b9aa944ae939d2963fbfe8cf497`  
		Last Modified: Fri, 26 Mar 2021 19:29:52 GMT  
		Size: 8.4 KB (8417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1ff85e9b2e7a94f079c5258cf1940e632fe0c6c0ff47c50158a4357b4b320e`  
		Last Modified: Sat, 27 Mar 2021 13:44:59 GMT  
		Size: 16.1 MB (16061433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf4a4cabb9c808669d14d44e91b0ecdd96fe9ed632f1430c12de99bc31daafd6`  
		Last Modified: Sat, 27 Mar 2021 13:44:55 GMT  
		Size: 14.8 KB (14756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b04b89c415147bb3b96be61ba13dc3e7d42b048dba54da0ed21a38f0d9cf5e7c`  
		Last Modified: Sat, 27 Mar 2021 13:44:57 GMT  
		Size: 12.9 MB (12865243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5ff14a4ec7b39e7b7a608cdd7ada3955053c46ae0a3241ac8178a2345db246`  
		Last Modified: Sat, 27 Mar 2021 13:44:53 GMT  
		Size: 577.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7455deca54ac18ada94451b103190ff48552473a849de0cf11705e158f4e196`  
		Last Modified: Sat, 27 Mar 2021 13:46:24 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7be636f4963f1a8fa732a71fc15e1ba97161a55a1a0a6389f0b01e2f3f41799`  
		Last Modified: Sat, 27 Mar 2021 13:46:24 GMT  
		Size: 1.1 KB (1090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:dev-fpm` - linux; arm64 variant v8

```console
$ docker pull friendica@sha256:6d93c0b5cb4022f8e17492b2a0feb9df2c350b0eb6fc9250e0535367b122e014
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.2 MB (170162314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e944f664f52fcc65030c53130ba2fe10b6fe53b251d50e6cec6f2ac0ad53c4a8`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 12 Mar 2021 01:53:53 GMT
ADD file:6130ddc0a939dd72c0614de4aa77de47aa16fe211274bacb31995aa1a0526164 in / 
# Fri, 12 Mar 2021 01:53:56 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 11:09:10 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 12 Mar 2021 11:09:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 12 Mar 2021 11:09:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 11:09:47 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 12 Mar 2021 11:09:50 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 12 Mar 2021 11:18:54 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 12 Mar 2021 11:18:55 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Mar 2021 11:18:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Mar 2021 11:18:57 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 12 Mar 2021 11:50:21 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Fri, 12 Mar 2021 11:50:22 GMT
ENV PHP_VERSION=7.3.27
# Fri, 12 Mar 2021 11:50:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.27.tar.xz.asc
# Fri, 12 Mar 2021 11:50:23 GMT
ENV PHP_SHA256=65f616e2d5b6faacedf62830fa047951b0136d5da34ae59e6744cbaf5dca148d
# Fri, 12 Mar 2021 11:50:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 12 Mar 2021 11:50:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 12 Mar 2021 11:53:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 12 Mar 2021 11:53:58 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 12 Mar 2021 11:54:00 GMT
RUN docker-php-ext-enable sodium
# Fri, 12 Mar 2021 11:54:03 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 12 Mar 2021 11:54:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 12 Mar 2021 11:54:06 GMT
WORKDIR /var/www/html
# Fri, 12 Mar 2021 11:54:09 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 12 Mar 2021 11:54:10 GMT
STOPSIGNAL SIGQUIT
# Fri, 12 Mar 2021 11:54:11 GMT
EXPOSE 9000
# Fri, 12 Mar 2021 11:54:12 GMT
CMD ["php-fpm"]
# Sat, 13 Mar 2021 03:11:23 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         git         msmtp         gnupg dirmngr     ;     rm -rf /var/lib/apt/lists/*;
# Sat, 13 Mar 2021 03:11:24 GMT
ENV TINI_VERSION=v0.19.0
# Sat, 13 Mar 2021 03:11:28 GMT
RUN export BUILD_ARCH=$(dpkg-architecture --query DEB_BUILD_ARCH)  && mkdir ~/.gnupg  && echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf  && curl -L -o /sbin/tini https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}  && curl -L -o /tini.asc https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}.asc  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7  && gpg --batch --verify /tini.asc /sbin/tini  && chmod +x /sbin/tini
# Sat, 13 Mar 2021 03:15:45 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.20;     pecl install memcached-3.1.5;     pecl install redis-5.3.3;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Sat, 13 Mar 2021 03:15:48 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Sat, 13 Mar 2021 03:15:48 GMT
VOLUME [/var/www/html]
# Sat, 13 Mar 2021 03:22:44 GMT
ENV FRIENDICA_VERSION=2021.03-dev
# Sat, 13 Mar 2021 03:22:45 GMT
ENV FRIENDICA_ADDONS=2021.03-dev
# Sat, 13 Mar 2021 03:22:47 GMT
COPY multi:b20e37902564ea2dd022293f7b41911842ada0268aa69dff8006238a11a5b5e0 in / 
# Sat, 13 Mar 2021 03:22:49 GMT
COPY multi:923de5042cde61ed518a7067985e18cb873d0cd10946593bfb44de6ba9e078ed in /usr/src/friendica/config/ 
# Sat, 13 Mar 2021 03:22:50 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Sat, 13 Mar 2021 03:22:51 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:706ee5d0a6b53d9257cbea22d8409fb22c867ab3a001c65f6b8bfd37dace0e58`  
		Last Modified: Fri, 12 Mar 2021 02:01:39 GMT  
		Size: 25.9 MB (25856512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:170ce16978fe5d48c07f44f3f3629b803edb31c9a5dabeb7b723d1abadf63ec0`  
		Last Modified: Fri, 12 Mar 2021 12:17:27 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5207eb43926d89dc8c3b70fcdd05040ab06c3bf87b04231bfc61ea95bbddbf79`  
		Last Modified: Fri, 12 Mar 2021 12:17:45 GMT  
		Size: 70.4 MB (70355270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65a8ea3de090ee8a21672a8b8730c898b71122c8207afdbdc1bf86ca40e9f1d`  
		Last Modified: Fri, 12 Mar 2021 12:17:25 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177e4164f2768d28134b213ba3d458396744c80dd6284d23b7d9da4d768188cf`  
		Last Modified: Fri, 12 Mar 2021 12:21:59 GMT  
		Size: 12.5 MB (12458742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4637c7de0796378ee3669134f81affcc3567f500fc773371e0427ea5fcc2ac7b`  
		Last Modified: Fri, 12 Mar 2021 12:21:58 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d49eae7f3391d047b7fc31c6a20b11c4294d6df5d4abf5d1e8ffdea0c95ee440`  
		Last Modified: Fri, 12 Mar 2021 12:22:04 GMT  
		Size: 28.4 MB (28441713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7194f42639e84066f8d2b1b021ea0e576b49c6c31c8c33547a030130a393366`  
		Last Modified: Fri, 12 Mar 2021 12:21:57 GMT  
		Size: 2.3 KB (2268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa30e65879ebe6579c07de2c97397d742be7863404a660c8507dc81fbc8cabff`  
		Last Modified: Fri, 12 Mar 2021 12:21:57 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0708b794f5c32883570e30d5ae9c2a54b930a03595225ee5dcde6e5e55a0315`  
		Last Modified: Fri, 12 Mar 2021 12:21:57 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f259ee4e4e53922bc913a15cf1df86ae2c4df717754fa4a2801cb2b8aac245d`  
		Last Modified: Fri, 12 Mar 2021 12:21:57 GMT  
		Size: 8.4 KB (8415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da1167159ea929f81ec7a1d3ed1bdc4ecf73195e5f4f854003b83a17ba80b36b`  
		Last Modified: Sat, 13 Mar 2021 03:24:56 GMT  
		Size: 19.4 MB (19406110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d3a5b0d73726b9420a22c058663d09d3f5c5d250833b393f4ef7506c8fce9c`  
		Last Modified: Sat, 13 Mar 2021 03:24:52 GMT  
		Size: 15.7 KB (15711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b36fd2abd7ae91e1138c3e794a8944f7d0640e8b9ae74feaa85c22e37b21e71e`  
		Last Modified: Sat, 13 Mar 2021 03:24:54 GMT  
		Size: 13.6 MB (13611197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83ac91ff4fb13e27e830217d643e8980f5cfcebd56d4263a866b770d7e7ecf3`  
		Last Modified: Sat, 13 Mar 2021 03:24:50 GMT  
		Size: 575.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f04344e7961ccdaa1ad2b63c78b92e1c9b23816a0453231a300e79bcc6a410bf`  
		Last Modified: Sat, 13 Mar 2021 03:26:41 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d25bf2ad3de59123ae0941952cd2de0051a2c1361997592fa5311e11676f603d`  
		Last Modified: Sat, 13 Mar 2021 03:26:41 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:dev-fpm` - linux; 386

```console
$ docker pull friendica@sha256:429398a8d0f1c490eea017ec2d2ca642aee2eed5ee69aa451546ea6c7998f0ea
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.5 MB (186482330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bfa4b48be7eafb66470a5bf12576f81424974f1cde6b2acffb561ce4e4d51cc`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 26 Mar 2021 13:53:11 GMT
ADD file:6c7524352aadfb597840d7c62001b10cf663f17dc2752a1bc5ad40b538138432 in / 
# Fri, 26 Mar 2021 13:53:12 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 00:08:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Sat, 27 Mar 2021 00:08:28 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Sat, 27 Mar 2021 00:08:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 00:08:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Sat, 27 Mar 2021 00:08:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Sat, 27 Mar 2021 00:19:56 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Sat, 27 Mar 2021 00:19:56 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Mar 2021 00:19:56 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Sat, 27 Mar 2021 00:19:56 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Sat, 27 Mar 2021 01:07:36 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Sat, 27 Mar 2021 01:07:37 GMT
ENV PHP_VERSION=7.3.27
# Sat, 27 Mar 2021 01:07:37 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.27.tar.xz.asc
# Sat, 27 Mar 2021 01:07:37 GMT
ENV PHP_SHA256=65f616e2d5b6faacedf62830fa047951b0136d5da34ae59e6744cbaf5dca148d
# Sat, 27 Mar 2021 01:09:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Sat, 27 Mar 2021 01:09:20 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Sat, 27 Mar 2021 01:16:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Sat, 27 Mar 2021 01:16:47 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Sat, 27 Mar 2021 01:16:48 GMT
RUN docker-php-ext-enable sodium
# Sat, 27 Mar 2021 01:16:49 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Sat, 27 Mar 2021 01:16:50 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Sat, 27 Mar 2021 01:16:50 GMT
WORKDIR /var/www/html
# Sat, 27 Mar 2021 01:16:52 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Sat, 27 Mar 2021 01:16:52 GMT
STOPSIGNAL SIGQUIT
# Sat, 27 Mar 2021 01:16:52 GMT
EXPOSE 9000
# Sat, 27 Mar 2021 01:16:53 GMT
CMD ["php-fpm"]
# Sat, 27 Mar 2021 12:12:58 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         git         msmtp         gnupg dirmngr     ;     rm -rf /var/lib/apt/lists/*;
# Sat, 27 Mar 2021 12:12:58 GMT
ENV TINI_VERSION=v0.19.0
# Sat, 27 Mar 2021 12:13:00 GMT
RUN export BUILD_ARCH=$(dpkg-architecture --query DEB_BUILD_ARCH)  && mkdir ~/.gnupg  && echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf  && curl -L -o /sbin/tini https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}  && curl -L -o /tini.asc https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}.asc  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7  && gpg --batch --verify /tini.asc /sbin/tini  && chmod +x /sbin/tini
# Sat, 27 Mar 2021 12:15:22 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.20;     pecl install memcached-3.1.5;     pecl install redis-5.3.3;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 12:15:24 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Sat, 27 Mar 2021 12:15:24 GMT
VOLUME [/var/www/html]
# Sat, 27 Mar 2021 12:16:55 GMT
ENV FRIENDICA_VERSION=2021.03-dev
# Sat, 27 Mar 2021 12:16:55 GMT
ENV FRIENDICA_ADDONS=2021.03-dev
# Sat, 27 Mar 2021 12:16:56 GMT
COPY multi:b20e37902564ea2dd022293f7b41911842ada0268aa69dff8006238a11a5b5e0 in / 
# Sat, 27 Mar 2021 12:16:56 GMT
COPY multi:923de5042cde61ed518a7067985e18cb873d0cd10946593bfb44de6ba9e078ed in /usr/src/friendica/config/ 
# Sat, 27 Mar 2021 12:16:56 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Sat, 27 Mar 2021 12:16:57 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:8cd20c3ac698e839ccd9bbdb86bc90efa00779d975e4064809852f86f56d8f3e`  
		Last Modified: Fri, 26 Mar 2021 14:01:40 GMT  
		Size: 27.8 MB (27760999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4eaf8c1a6dd01fc50d06db11b4b9396e69cfeb99ee89c2032e1a835ea65be972`  
		Last Modified: Sat, 27 Mar 2021 02:05:19 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:611a98c08be9befb8bf55728977114f649136f26c4f515d91bac2c5bc13578db`  
		Last Modified: Sat, 27 Mar 2021 02:05:47 GMT  
		Size: 81.2 MB (81229794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4dff8967bdfda4a517f1f8ae58ff46c35c493a360c9dda4637f74967fa6bf8a`  
		Last Modified: Sat, 27 Mar 2021 02:05:19 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7dd90fa2f208611108be9fda177854b64863575b5d3851ea4ed6907ec5d548b`  
		Last Modified: Sat, 27 Mar 2021 02:15:18 GMT  
		Size: 12.5 MB (12459231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ef74477c66be3d3416927064fff9f5bde217a1e88abb754dc97723f7c7f322`  
		Last Modified: Sat, 27 Mar 2021 02:15:16 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54eedcc62491da14a9ccfbd04b7403f486af8ebc408ae340f695be3f6f69c805`  
		Last Modified: Sat, 27 Mar 2021 02:15:22 GMT  
		Size: 29.3 MB (29319032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9c1afb2d4ccf400d49267692b9c3bc52400ee652bcb72412121f8cd238f20b`  
		Last Modified: Sat, 27 Mar 2021 02:15:13 GMT  
		Size: 2.3 KB (2273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b665f11588f3ca4a2877ab160a1f00f6c18674221797fc45512d35e626150f89`  
		Last Modified: Sat, 27 Mar 2021 02:15:14 GMT  
		Size: 244.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecbdc76b77e9dbb56a5c82c9440b63edc2b3fa1872eba3d821db4f11ae84d229`  
		Last Modified: Sat, 27 Mar 2021 02:15:14 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a246f1f730e68468d6ba04e405b02cd01ec43918b84cb5d64a4ae2d5c8f55a6d`  
		Last Modified: Sat, 27 Mar 2021 02:15:13 GMT  
		Size: 8.4 KB (8417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0087b496531f51b34c11cd14c1cf4f9545157f947a22bb0eb81df961868a60b6`  
		Last Modified: Sat, 27 Mar 2021 12:19:22 GMT  
		Size: 21.1 MB (21090997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d9a8dbc909bd38bf65b3554f0e42f1b235300dfe9dc9de5a5270e8b35837ff`  
		Last Modified: Sat, 27 Mar 2021 12:19:17 GMT  
		Size: 16.2 KB (16155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb400bb67bdfc65140d52f1be6445e39772bfe8869c0019dd354ee15009eb2ce`  
		Last Modified: Sat, 27 Mar 2021 12:19:23 GMT  
		Size: 14.6 MB (14589063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:069be24e975241f546f47961a39c45e4f94d5d4a841b848ad6bd824a3be8211a`  
		Last Modified: Sat, 27 Mar 2021 12:19:14 GMT  
		Size: 576.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5c8f35ff70e2d8c42ef31018d39f917e1cc68384a210a3ea5f66e8748f6b64`  
		Last Modified: Sat, 27 Mar 2021 12:21:13 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef50549655c5b095ba0e36ee81197ff13a425acb0c914c1fb432106c471f37e2`  
		Last Modified: Sat, 27 Mar 2021 12:21:13 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:dev-fpm` - linux; mips64le

```console
$ docker pull friendica@sha256:73f258aa2f5395a957b679e2923ca30288219f198a1e01159929e23439485afe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160923352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92a2b6062098699ad838ffad55fcd660b4c4ef324756777c54421287624f6fa4`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 26 Mar 2021 08:09:56 GMT
ADD file:74d504a9a34f47729165ef4ceedc9f0eaa2e91bfb6a24ebfc3ceed0248267a27 in / 
# Fri, 26 Mar 2021 08:09:57 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 08:46:08 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 26 Mar 2021 08:46:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 26 Mar 2021 08:46:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 08:46:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 26 Mar 2021 08:47:00 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 26 Mar 2021 09:12:53 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 26 Mar 2021 09:12:54 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 26 Mar 2021 09:12:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 26 Mar 2021 09:12:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 26 Mar 2021 10:31:40 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Fri, 26 Mar 2021 10:31:40 GMT
ENV PHP_VERSION=7.3.27
# Fri, 26 Mar 2021 10:31:40 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.27.tar.xz.asc
# Fri, 26 Mar 2021 10:31:41 GMT
ENV PHP_SHA256=65f616e2d5b6faacedf62830fa047951b0136d5da34ae59e6744cbaf5dca148d
# Fri, 26 Mar 2021 10:32:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 26 Mar 2021 10:32:04 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 26 Mar 2021 10:44:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 26 Mar 2021 10:45:00 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 26 Mar 2021 10:45:02 GMT
RUN docker-php-ext-enable sodium
# Fri, 26 Mar 2021 10:45:04 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 26 Mar 2021 10:45:04 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 26 Mar 2021 10:45:04 GMT
WORKDIR /var/www/html
# Fri, 26 Mar 2021 10:45:06 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 26 Mar 2021 10:45:06 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 10:45:07 GMT
EXPOSE 9000
# Fri, 26 Mar 2021 10:45:07 GMT
CMD ["php-fpm"]
# Fri, 26 Mar 2021 19:08:22 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         git         msmtp         gnupg dirmngr     ;     rm -rf /var/lib/apt/lists/*;
# Fri, 26 Mar 2021 19:08:22 GMT
ENV TINI_VERSION=v0.19.0
# Fri, 26 Mar 2021 19:08:26 GMT
RUN export BUILD_ARCH=$(dpkg-architecture --query DEB_BUILD_ARCH)  && mkdir ~/.gnupg  && echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf  && curl -L -o /sbin/tini https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}  && curl -L -o /tini.asc https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}.asc  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7  && gpg --batch --verify /tini.asc /sbin/tini  && chmod +x /sbin/tini
# Fri, 26 Mar 2021 19:14:56 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.20;     pecl install memcached-3.1.5;     pecl install redis-5.3.3;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 19:14:58 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Fri, 26 Mar 2021 19:14:59 GMT
VOLUME [/var/www/html]
# Fri, 26 Mar 2021 19:17:03 GMT
ENV FRIENDICA_VERSION=2021.03-dev
# Fri, 26 Mar 2021 19:17:04 GMT
ENV FRIENDICA_ADDONS=2021.03-dev
# Fri, 26 Mar 2021 19:17:05 GMT
COPY multi:b20e37902564ea2dd022293f7b41911842ada0268aa69dff8006238a11a5b5e0 in / 
# Fri, 26 Mar 2021 19:17:06 GMT
COPY multi:923de5042cde61ed518a7067985e18cb873d0cd10946593bfb44de6ba9e078ed in /usr/src/friendica/config/ 
# Fri, 26 Mar 2021 19:17:06 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Fri, 26 Mar 2021 19:17:06 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5f863e006c40853ec8c23aa5b7a0e95918001f96878fb45770410ac4df51cf88`  
		Last Modified: Fri, 26 Mar 2021 08:16:29 GMT  
		Size: 25.8 MB (25772487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9917ef2e3fa9a9a75c1035ce8562e1089983ed624743c4708c4d2018071f53b6`  
		Last Modified: Fri, 26 Mar 2021 11:00:12 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04c039fb3abecd33217b5c88dc3534e112402036ef8e200a3123e52cf68a041b`  
		Last Modified: Fri, 26 Mar 2021 11:01:02 GMT  
		Size: 61.4 MB (61403203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4d6086af3e9bd8107de474e634822da995e1488ff71a5b3a04e92b3822df21b`  
		Last Modified: Fri, 26 Mar 2021 11:00:12 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e229bf2671e2fe4525370d9a9be65bfc68622db69e3dc496c128ba5bc05cb6`  
		Last Modified: Fri, 26 Mar 2021 11:08:19 GMT  
		Size: 12.5 MB (12457242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fa191fc1dc0a26bb32dbda3e60c29296bbe73b96d2027f0d57a357fadb18a1a`  
		Last Modified: Fri, 26 Mar 2021 11:08:16 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e298f4b294d0d460909c087534c8278fad21be9fd27f9684019bd098f710a775`  
		Last Modified: Fri, 26 Mar 2021 11:08:33 GMT  
		Size: 28.1 MB (28118867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b130d03eea8a14fec8908fa6985e3791e999403ab08ba782f8f3e9943eacd23a`  
		Last Modified: Fri, 26 Mar 2021 11:08:13 GMT  
		Size: 2.3 KB (2270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f908f8bb28182420a89357190478534e2180b32ef8eb2878ed6858f15e77143`  
		Last Modified: Fri, 26 Mar 2021 11:08:13 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f31a1dfc792481efafe8c0d582a73e6c6d4a9f6e829e4d65f3f9545b67e23eb2`  
		Last Modified: Fri, 26 Mar 2021 11:08:13 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abda649412de7f1ec2822ecc828a8309643213ea1eb055916d0c108bcff21f3`  
		Last Modified: Fri, 26 Mar 2021 11:08:13 GMT  
		Size: 8.4 KB (8417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad14462732ea54ded84398a78411a67b0d4af8d53476138794baa89e2b29943`  
		Last Modified: Fri, 26 Mar 2021 19:18:44 GMT  
		Size: 19.4 MB (19449998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec3ddd3ca30752fe5ef226a36e08c017f712337daf48b76d4909a418ca5a54c`  
		Last Modified: Fri, 26 Mar 2021 19:18:30 GMT  
		Size: 15.9 KB (15909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e495bfea0e2b9036b86aca5e911804fe2ba4a079c27f000833a28cd96779143`  
		Last Modified: Fri, 26 Mar 2021 19:18:38 GMT  
		Size: 13.7 MB (13688680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd6e1db867f96306c3063b4b3b846ec1411933ea40830c55747ea9e9042e76c4`  
		Last Modified: Fri, 26 Mar 2021 19:18:26 GMT  
		Size: 550.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc43511e5007ed95ef630f931daee461338cc747c6612e9d691f3c16283e6a0b`  
		Last Modified: Fri, 26 Mar 2021 19:21:16 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3acb31d57c8f2aa8c41b4f4bea08b9c15689f33e7e0671d71fa803aaa97a5b4`  
		Last Modified: Fri, 26 Mar 2021 19:21:16 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:dev-fpm` - linux; ppc64le

```console
$ docker pull friendica@sha256:3aafa7587c3db68fe1086ee8e2f1b47b53812b5f42c8af4613908888379e1668
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.1 MB (195083600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071fdb05f37b43c4c4c046cfe9d0bca88841719a938e4d615cda97795879ba72`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 12 Mar 2021 02:32:43 GMT
ADD file:6a0c0cfa71979cf6fdd859dce1e32582f0e55ed382b9e17b77a2001defc2c9db in / 
# Fri, 12 Mar 2021 02:32:50 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 17:34:56 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 12 Mar 2021 17:34:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 12 Mar 2021 17:37:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 17:37:28 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 12 Mar 2021 17:37:46 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 12 Mar 2021 17:56:09 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 12 Mar 2021 17:56:12 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Mar 2021 17:56:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 12 Mar 2021 17:56:21 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 12 Mar 2021 19:03:47 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Fri, 12 Mar 2021 19:04:05 GMT
ENV PHP_VERSION=7.3.27
# Fri, 12 Mar 2021 19:04:12 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.27.tar.xz.asc
# Fri, 12 Mar 2021 19:04:29 GMT
ENV PHP_SHA256=65f616e2d5b6faacedf62830fa047951b0136d5da34ae59e6744cbaf5dca148d
# Fri, 12 Mar 2021 19:06:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 12 Mar 2021 19:07:01 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 12 Mar 2021 19:12:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 12 Mar 2021 19:12:38 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 12 Mar 2021 19:12:48 GMT
RUN docker-php-ext-enable sodium
# Fri, 12 Mar 2021 19:13:07 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 12 Mar 2021 19:13:12 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 12 Mar 2021 19:13:25 GMT
WORKDIR /var/www/html
# Fri, 12 Mar 2021 19:13:41 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 12 Mar 2021 19:13:49 GMT
STOPSIGNAL SIGQUIT
# Fri, 12 Mar 2021 19:13:55 GMT
EXPOSE 9000
# Fri, 12 Mar 2021 19:14:02 GMT
CMD ["php-fpm"]
# Sat, 13 Mar 2021 07:09:17 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         git         msmtp         gnupg dirmngr     ;     rm -rf /var/lib/apt/lists/*;
# Sat, 13 Mar 2021 07:09:21 GMT
ENV TINI_VERSION=v0.19.0
# Sat, 13 Mar 2021 07:09:31 GMT
RUN export BUILD_ARCH=$(dpkg-architecture --query DEB_BUILD_ARCH)  && mkdir ~/.gnupg  && echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf  && curl -L -o /sbin/tini https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}  && curl -L -o /tini.asc https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}.asc  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7  && gpg --batch --verify /tini.asc /sbin/tini  && chmod +x /sbin/tini
# Sat, 13 Mar 2021 07:25:09 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.20;     pecl install memcached-3.1.5;     pecl install redis-5.3.3;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Sat, 13 Mar 2021 07:25:19 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Sat, 13 Mar 2021 07:25:24 GMT
VOLUME [/var/www/html]
# Sat, 13 Mar 2021 07:41:04 GMT
ENV FRIENDICA_VERSION=2021.03-dev
# Sat, 13 Mar 2021 07:41:10 GMT
ENV FRIENDICA_ADDONS=2021.03-dev
# Sat, 13 Mar 2021 07:41:14 GMT
COPY multi:b20e37902564ea2dd022293f7b41911842ada0268aa69dff8006238a11a5b5e0 in / 
# Sat, 13 Mar 2021 07:41:19 GMT
COPY multi:923de5042cde61ed518a7067985e18cb873d0cd10946593bfb44de6ba9e078ed in /usr/src/friendica/config/ 
# Sat, 13 Mar 2021 07:41:30 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Sat, 13 Mar 2021 07:41:40 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:1d686056fdac1848f4fd78ba2b335502055ffe98c79619e21d0c2fb7db95257e`  
		Last Modified: Fri, 12 Mar 2021 02:45:35 GMT  
		Size: 30.5 MB (30525728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994f1c929cf4cdf280602a39a5424c2a98bd1ce0fbb2880c809bb43caa96bee2`  
		Last Modified: Fri, 12 Mar 2021 19:28:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f67d778602ea1f65e87b664100468b01997ab3269ca189acff1347986108636`  
		Last Modified: Fri, 12 Mar 2021 19:29:41 GMT  
		Size: 82.3 MB (82289990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f7763e63ddfa88dbf082b4847b929463333096d46fce614f628fd8fd64bf702`  
		Last Modified: Fri, 12 Mar 2021 19:28:26 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61a82244fc5297fab50beca02e8abf6a85dae3fe8cdafb6bb1d5aaf34a96aac2`  
		Last Modified: Fri, 12 Mar 2021 19:36:22 GMT  
		Size: 12.5 MB (12459794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dea85462120ffe1678ec2b1efff2129578ea2f5254436e85a29bddab1b24ce8`  
		Last Modified: Fri, 12 Mar 2021 19:36:20 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d9389e4c78319bc34d7134ab00c2d97c68b9ffe5aa0de4453e8027aee04d09c`  
		Last Modified: Fri, 12 Mar 2021 19:36:23 GMT  
		Size: 30.5 MB (30470651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3695110b90d59c23c22d3f580979212fbcc1c99306824eef0aee7d9d12c58c42`  
		Last Modified: Fri, 12 Mar 2021 19:36:16 GMT  
		Size: 2.3 KB (2271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f111f330e5c72f9f92496caa008fc2471185c779bece85b9493ffa7e88670540`  
		Last Modified: Fri, 12 Mar 2021 19:36:16 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb73a9c5d26813d60ed4a745c09fc9e423a6f36a7babc3f9d234aef377a3965b`  
		Last Modified: Fri, 12 Mar 2021 19:36:16 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c52c4bf0a1bb482ab67bd421e2ceeb42643b0e5ec76f300a4ac830db80f12b7`  
		Last Modified: Fri, 12 Mar 2021 19:36:17 GMT  
		Size: 8.4 KB (8415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e0422bea87b3b9db98fffe723dc1e402d97b0c7482f374890a2823e0605e4d`  
		Last Modified: Sat, 13 Mar 2021 07:47:13 GMT  
		Size: 23.9 MB (23888492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516a13074fd2adb4d13b9e4d597dcc74ffb4d8b7ebc10411353990277b2edf4c`  
		Last Modified: Sat, 13 Mar 2021 07:46:51 GMT  
		Size: 16.3 KB (16320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40af2d01bc61cd055aded4a50bf87772bc2d9668bad5e84b36ebc4dfbf31fa24`  
		Last Modified: Sat, 13 Mar 2021 07:47:26 GMT  
		Size: 15.4 MB (15415564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f97f53626af55192c1f214a154a8200838750655d1c986c957df02e82ac41ad8`  
		Last Modified: Sat, 13 Mar 2021 07:46:46 GMT  
		Size: 576.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a13ca4dc6366b29fcf25ee03bc93779486f7d420d9b2c35bfd277bfa4b73ab8`  
		Last Modified: Sat, 13 Mar 2021 07:54:14 GMT  
		Size: 3.3 KB (3261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98f092491315f3820a405eedb974c04191c2e1952bfd52cef11f4ebf04ccfec9`  
		Last Modified: Sat, 13 Mar 2021 07:54:14 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `friendica:dev-fpm` - linux; s390x

```console
$ docker pull friendica@sha256:59a22ff9f02e42ed024f76096cb089b529c3698dbed626aae58f1ff558e54736
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.9 MB (162934639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84e784b70da5e3c6edd576aa109734106226059e981a786c4d10fb57f06bfb51`
-	Entrypoint: `["\/entrypoint-dev.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Fri, 26 Mar 2021 10:53:48 GMT
ADD file:3a3cf2e796c665cae881fb0b8a23a071206531af98c03548ab5a8721b3c67353 in / 
# Fri, 26 Mar 2021 10:53:49 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 17:33:35 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 26 Mar 2021 17:33:35 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 26 Mar 2021 17:34:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 17:34:29 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 26 Mar 2021 17:34:31 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 26 Mar 2021 17:45:22 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 26 Mar 2021 17:45:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 26 Mar 2021 17:45:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 26 Mar 2021 17:45:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 26 Mar 2021 18:24:22 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Fri, 26 Mar 2021 18:24:22 GMT
ENV PHP_VERSION=7.3.27
# Fri, 26 Mar 2021 18:24:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.27.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.27.tar.xz.asc
# Fri, 26 Mar 2021 18:24:23 GMT
ENV PHP_SHA256=65f616e2d5b6faacedf62830fa047951b0136d5da34ae59e6744cbaf5dca148d
# Fri, 26 Mar 2021 18:24:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Fri, 26 Mar 2021 18:24:41 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 26 Mar 2021 18:29:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 26 Mar 2021 18:29:28 GMT
COPY multi:6dfba8f7e64bd54e4d9aa0855ff6ce7a53059e0a733752b4537fd3fdfd32d837 in /usr/local/bin/ 
# Fri, 26 Mar 2021 18:29:29 GMT
RUN docker-php-ext-enable sodium
# Fri, 26 Mar 2021 18:29:31 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Fri, 26 Mar 2021 18:29:31 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 26 Mar 2021 18:29:32 GMT
WORKDIR /var/www/html
# Fri, 26 Mar 2021 18:29:34 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 26 Mar 2021 18:29:34 GMT
STOPSIGNAL SIGQUIT
# Fri, 26 Mar 2021 18:29:35 GMT
EXPOSE 9000
# Fri, 26 Mar 2021 18:29:35 GMT
CMD ["php-fpm"]
# Sat, 27 Mar 2021 02:08:37 GMT
RUN set -ex;         apt-get update;     apt-get install -y --no-install-recommends         rsync         bzip2         git         msmtp         gnupg dirmngr     ;     rm -rf /var/lib/apt/lists/*;
# Sat, 27 Mar 2021 02:08:38 GMT
ENV TINI_VERSION=v0.19.0
# Sat, 27 Mar 2021 02:08:40 GMT
RUN export BUILD_ARCH=$(dpkg-architecture --query DEB_BUILD_ARCH)  && mkdir ~/.gnupg  && echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf  && curl -L -o /sbin/tini https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}  && curl -L -o /tini.asc https://github.com/krallin/tini/releases/download/${TINI_VERSION}/tini-${BUILD_ARCH}.asc  && gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 595E85A6B1B4779EA4DAAEC70B588DFF0527A9B7  && gpg --batch --verify /tini.asc /sbin/tini  && chmod +x /sbin/tini
# Sat, 27 Mar 2021 02:10:55 GMT
RUN set -ex;         savedAptMark="$(apt-mark showmanual)";         apt-get update;     apt-get install -y --no-install-recommends         mariadb-client         bash         libpng-dev         libjpeg62-turbo-dev         libtool         libmagick++-dev         libmemcached-dev         libgraphicsmagick1-dev         libfreetype6-dev         librsvg2-2         libzip-dev         libldap2-dev     ;             debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)";         docker-php-ext-configure gd         --with-gd         --with-freetype-dir=/usr/include/         --with-png-dir=/usr/include/         --with-jpeg-dir=/usr/include/     ;     docker-php-ext-configure ldap         --with-libdir=lib/$debMultiarch/     ;    docker-php-ext-install -j "$(nproc)"         pdo_mysql         gd         zip         opcache         ctype         pcntl         ldap     ;         pecl install apcu-5.1.20;     pecl install memcached-3.1.5;     pecl install redis-5.3.3;     pecl install imagick-3.4.4;         docker-php-ext-enable         apcu         memcached         redis         imagick     ;         apt-mark auto '.*' > /dev/null;     apt-mark manual $savedAptMark;     ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so         | awk '/=>/ { print $3 }'         | sort -u         | xargs -r dpkg-query -S         | cut -d: -f1         | sort -u         | xargs -rt apt-mark manual;         apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false;     rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 02:10:57 GMT
RUN set -ex;     {         echo 'opcache.enable=1' ;         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=10000';         echo 'opcache.memory_consumption=128';         echo 'opcache.save_comments=1';         echo 'opcache.revalidte_freq=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini;         {         echo sendmail_path = "/usr/bin/msmtp -t";     } > /usr/local/etc/php/conf.d/sendmail.ini;         echo 'apc.enable_cli=1' >> /usr/local/etc/php/conf.d/docker-php-ext-apcu.ini;         echo 'memory_limit=512M' > /usr/local/etc/php/conf.d/memory-limit.ini;         mkdir /var/www/data;     chown -R www-data:root /var/www;     chmod -R g=u /var/www
# Sat, 27 Mar 2021 02:10:57 GMT
VOLUME [/var/www/html]
# Sat, 27 Mar 2021 02:12:25 GMT
ENV FRIENDICA_VERSION=2021.03-dev
# Sat, 27 Mar 2021 02:12:25 GMT
ENV FRIENDICA_ADDONS=2021.03-dev
# Sat, 27 Mar 2021 02:12:26 GMT
COPY multi:b20e37902564ea2dd022293f7b41911842ada0268aa69dff8006238a11a5b5e0 in / 
# Sat, 27 Mar 2021 02:12:26 GMT
COPY multi:923de5042cde61ed518a7067985e18cb873d0cd10946593bfb44de6ba9e078ed in /usr/src/friendica/config/ 
# Sat, 27 Mar 2021 02:12:26 GMT
ENTRYPOINT ["/entrypoint-dev.sh"]
# Sat, 27 Mar 2021 02:12:26 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a37ca8d63090f0f22441ceecc0af7881a2668336202cf586e841e3d9e06f2f4b`  
		Last Modified: Fri, 26 Mar 2021 10:57:46 GMT  
		Size: 25.7 MB (25716264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be1b3cedc30dabafd64e605f67b4625e9e68cc48c12ef6ca51cdd91230d8748a`  
		Last Modified: Fri, 26 Mar 2021 18:38:15 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85446454c2c447c62d489f8068ebcdb98578cea2207a7e1f1e5b5e6698d63675`  
		Last Modified: Fri, 26 Mar 2021 18:38:26 GMT  
		Size: 64.7 MB (64709831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6e30a5aeb7c9fec839b4fdc8d4d6fc4fa7e8d24c0e78eea3a5e6cec59a2662`  
		Last Modified: Fri, 26 Mar 2021 18:38:14 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a9898f9844087472e326812a4110a3f2943c864de5472df44ffc81df23f4e2`  
		Last Modified: Fri, 26 Mar 2021 18:43:18 GMT  
		Size: 12.5 MB (12458290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efacd5f33b10595e9a17d52b46289754648827a05667c80924953bfdaf9d64ab`  
		Last Modified: Fri, 26 Mar 2021 18:43:17 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a0a4a001fda3e0240c37bae7f426ff50e135c0993b9246bdd25ef1a4ed638d`  
		Last Modified: Fri, 26 Mar 2021 18:43:20 GMT  
		Size: 27.9 MB (27906085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a9fbfa0980b4ef6a57756a30d92dccb43eefcaedf4034e8c38d9125a70d1fc`  
		Last Modified: Fri, 26 Mar 2021 18:43:16 GMT  
		Size: 2.3 KB (2274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0caddcff19f2f3b9d2b9c96dc4f820914869841a973e2dd3ec0be13f3059071`  
		Last Modified: Fri, 26 Mar 2021 18:43:16 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e52ff73c56a9f9938d3aa0e1afa2b99a3197b42aaded8849068a6c2f84698d`  
		Last Modified: Fri, 26 Mar 2021 18:43:17 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d88dc7df1669869f6aa2f62b70613d62ce7bdc0e700903cc7bb7703ad2ef390`  
		Last Modified: Fri, 26 Mar 2021 18:43:15 GMT  
		Size: 8.4 KB (8419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb234a1275d30bbe6b400b932f68a2b59240ca88c298e66357da4a66dbc5902d`  
		Last Modified: Sat, 27 Mar 2021 02:13:42 GMT  
		Size: 18.4 MB (18374919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8a97c8efc525d84d03cf00ec9931141647727c9a9da1296246e30095fdb19e`  
		Last Modified: Sat, 27 Mar 2021 02:13:40 GMT  
		Size: 16.4 KB (16416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e0706f553327a57759525c84393e8edcc195954c7d3e09971f28264cda1d5b`  
		Last Modified: Sat, 27 Mar 2021 02:13:40 GMT  
		Size: 13.7 MB (13735766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef84169cb35836d1612fa82541d2e0590837244847247fda745cca36689f6f1`  
		Last Modified: Sat, 27 Mar 2021 02:13:38 GMT  
		Size: 577.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dadc39ac6fef5d3dafb241c430ecd86a259abf106f9a49764c7d787162cdb02`  
		Last Modified: Sat, 27 Mar 2021 02:14:29 GMT  
		Size: 3.3 KB (3260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d1d2854adc35ba1e8cc28163ecfa75945c2e616779c0f9f919663ec39360fae`  
		Last Modified: Sat, 27 Mar 2021 02:14:29 GMT  
		Size: 1.1 KB (1090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
