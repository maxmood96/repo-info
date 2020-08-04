## `postfixadmin:3-fpm`

```console
$ docker pull postfixadmin@sha256:27b3a215b1c70103c07d5b4bed515eebbaa76dd2f434b2e698e057565b07416b
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

### `postfixadmin:3-fpm` - linux; amd64

```console
$ docker pull postfixadmin@sha256:33b65d90bacba7a7be03727cfbd3273c2c23d5a6bb95d0b56185588913a3025c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.9 MB (146927157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e2fa889670b14e95e2298c8c5547cd5e8958dace15172003671de059a7c0935`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:37 GMT
ADD file:6ccb3bbcc69b0d44c48a8ef1bfa08d835444ea13b8a93701bd37d86b81b13ac2 in / 
# Wed, 22 Jul 2020 02:03:37 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 08:44:09 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 22 Jul 2020 08:44:09 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Jul 2020 08:44:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 08:44:38 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Jul 2020 08:44:39 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 22 Jul 2020 09:02:11 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Wed, 22 Jul 2020 09:02:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Jul 2020 09:02:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Jul 2020 09:02:12 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Jul 2020 10:04:21 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Wed, 22 Jul 2020 10:04:21 GMT
ENV PHP_VERSION=7.3.20
# Wed, 22 Jul 2020 10:04:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.20.tar.xz.asc
# Wed, 22 Jul 2020 10:04:21 GMT
ENV PHP_SHA256=43292046f6684eb13acb637276d4aa1dd9f66b0b7045e6f1493bc90db389b888 PHP_MD5=
# Wed, 22 Jul 2020 10:04:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 22 Jul 2020 10:04:31 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 22 Jul 2020 10:13:19 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Wed, 22 Jul 2020 10:13:20 GMT
COPY multi:bd67471e0c4047be362a8a0e199558e6245207a6f70b72fdfe55aa2d2cae15e6 in /usr/local/bin/ 
# Wed, 22 Jul 2020 10:13:20 GMT
RUN docker-php-ext-enable sodium
# Wed, 22 Jul 2020 10:13:21 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Wed, 22 Jul 2020 10:13:21 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Jul 2020 10:13:22 GMT
WORKDIR /var/www/html
# Wed, 22 Jul 2020 10:13:22 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Wed, 22 Jul 2020 10:13:23 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 Jul 2020 10:13:23 GMT
EXPOSE 9000
# Wed, 22 Jul 2020 10:13:23 GMT
CMD ["php-fpm"]
# Thu, 23 Jul 2020 06:21:10 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Thu, 23 Jul 2020 06:21:43 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-install -j "$(nproc)" 		mysqli 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jul 2020 06:21:44 GMT
ARG POSTFIXADMIN_VERSION=3.2.4
# Thu, 23 Jul 2020 06:21:44 GMT
ARG POSTFIXADMIN_SHA512=2bd7ae05addbaf3c6c7eebea16ec1e21b2c67c8e6161446ed82a9553c26c04e19c1ec9ce248a9b9df504df56d309590259e6f04907b04b593548028b40e40d47
# Thu, 23 Jul 2020 06:21:44 GMT
ENV POSTFIXADMIN_VERSION=3.2.4
# Thu, 23 Jul 2020 06:21:44 GMT
ENV POSTFIXADMIN_SHA512=2bd7ae05addbaf3c6c7eebea16ec1e21b2c67c8e6161446ed82a9553c26c04e19c1ec9ce248a9b9df504df56d309590259e6f04907b04b593548028b40e40d47
# Thu, 23 Jul 2020 06:21:45 GMT
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin
# Thu, 23 Jul 2020 06:21:45 GMT
COPY file:c6e11ee7dda40f44aa31f3bcb74669e99572ad86040276440b444d5699d333f5 in /usr/local/bin/ 
# Thu, 23 Jul 2020 06:21:46 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 23 Jul 2020 06:21:46 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:6ec8c9369e08152361a01729f2c8a1e7aae898426c6e67267f41894bf9524827`  
		Last Modified: Wed, 22 Jul 2020 02:09:51 GMT  
		Size: 27.1 MB (27098544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081a822af59557fab64a7e6b1f10993a1447c4565bee919c5a63f20e5d447207`  
		Last Modified: Wed, 22 Jul 2020 11:57:02 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5bea655fca655018e10a9078d5092b4d7d491ef2a9c380a0adf1c7ed119b88`  
		Last Modified: Wed, 22 Jul 2020 11:57:28 GMT  
		Size: 76.6 MB (76648810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5d9e6a44c7084c807b3c4203ec786d5bb187a14e4344496dca2d4148030e6e`  
		Last Modified: Wed, 22 Jul 2020 11:57:02 GMT  
		Size: 222.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f318b6a94eaa111c79718260f7991fb729553bcbd1371af04b7e99d6a94706`  
		Last Modified: Wed, 22 Jul 2020 12:00:17 GMT  
		Size: 12.4 MB (12439288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a634863e022ec842f58a7a0ab680362df1eb96928ad0e194b36dad1ebbcec7e6`  
		Last Modified: Wed, 22 Jul 2020 12:00:16 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7030c133fdde1209c199a4825373b887a51fd0eb0bef4b59580dcd032c95c533`  
		Last Modified: Wed, 22 Jul 2020 12:00:20 GMT  
		Size: 28.8 MB (28765950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e454ce1b9765bf31cd7dd60ca19ef45c39bb55f063f71ed34192410a959d3bf`  
		Last Modified: Wed, 22 Jul 2020 12:00:14 GMT  
		Size: 2.3 KB (2279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220caedb76f986278effa71a36299d99901089fdd53a633d3806f8a815067411`  
		Last Modified: Wed, 22 Jul 2020 12:00:14 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed6aaf9d38bc7303828e871235ec0e9a3e78a3a8a30708605cb92114b07dabd`  
		Last Modified: Wed, 22 Jul 2020 12:00:15 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9a5246b2e3eec23e28e614970f3e3e7f767856d402f13d0ad49f0cdfeb74cf`  
		Last Modified: Wed, 22 Jul 2020 12:00:15 GMT  
		Size: 8.4 KB (8415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0abcb12f830f3b262ca07d95eec43031f45161994535808ee5a26c5646aeb67`  
		Last Modified: Thu, 23 Jul 2020 06:22:17 GMT  
		Size: 626.5 KB (626527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f187ecb4c8c72fc500fd206460810a0ffeadfaff75ecb2096c4189ef82d163`  
		Last Modified: Thu, 23 Jul 2020 06:22:17 GMT  
		Size: 1.3 MB (1334614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cbe3ab82d872660cce174a07f3cc81f99db8aba5686f92b41649f4900274769`  
		Last Modified: Thu, 23 Jul 2020 06:22:16 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postfixadmin:3-fpm` - linux; arm variant v5

```console
$ docker pull postfixadmin@sha256:2bb5c64e8c0d2110b4c7d14596c9a91432a32ba6a92b8cfd7779fcb8c349fa37
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **125.3 MB (125334669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:042e4424ce510af0316e022d19203bbb2e134d2c6607d7c55af9f77dd52caff7`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 22 Jul 2020 00:51:01 GMT
ADD file:4ea2d111c970d510f4eccf0fa08caafde1d227fc4c249d67c1b9d99998b0b906 in / 
# Wed, 22 Jul 2020 00:51:04 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 02:37:57 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 22 Jul 2020 02:38:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Jul 2020 02:39:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 02:39:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Jul 2020 02:39:52 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 22 Jul 2020 02:53:40 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Wed, 22 Jul 2020 02:53:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Jul 2020 02:53:45 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Jul 2020 02:53:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Jul 2020 03:35:20 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Wed, 22 Jul 2020 03:35:21 GMT
ENV PHP_VERSION=7.3.20
# Wed, 22 Jul 2020 03:35:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.20.tar.xz.asc
# Wed, 22 Jul 2020 03:35:23 GMT
ENV PHP_SHA256=43292046f6684eb13acb637276d4aa1dd9f66b0b7045e6f1493bc90db389b888 PHP_MD5=
# Wed, 22 Jul 2020 03:35:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 22 Jul 2020 03:35:45 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 22 Jul 2020 03:39:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Wed, 22 Jul 2020 03:39:31 GMT
COPY multi:bd67471e0c4047be362a8a0e199558e6245207a6f70b72fdfe55aa2d2cae15e6 in /usr/local/bin/ 
# Wed, 22 Jul 2020 03:39:35 GMT
RUN docker-php-ext-enable sodium
# Wed, 22 Jul 2020 03:39:38 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Wed, 22 Jul 2020 03:39:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Jul 2020 03:39:40 GMT
WORKDIR /var/www/html
# Wed, 22 Jul 2020 03:39:43 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Wed, 22 Jul 2020 03:39:44 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 Jul 2020 03:39:45 GMT
EXPOSE 9000
# Wed, 22 Jul 2020 03:39:46 GMT
CMD ["php-fpm"]
# Wed, 22 Jul 2020 18:34:03 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Wed, 22 Jul 2020 18:35:41 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-install -j "$(nproc)" 		mysqli 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 18:35:43 GMT
ARG POSTFIXADMIN_VERSION=3.2.4
# Wed, 22 Jul 2020 18:35:47 GMT
ARG POSTFIXADMIN_SHA512=2bd7ae05addbaf3c6c7eebea16ec1e21b2c67c8e6161446ed82a9553c26c04e19c1ec9ce248a9b9df504df56d309590259e6f04907b04b593548028b40e40d47
# Wed, 22 Jul 2020 18:35:52 GMT
ENV POSTFIXADMIN_VERSION=3.2.4
# Wed, 22 Jul 2020 18:35:59 GMT
ENV POSTFIXADMIN_SHA512=2bd7ae05addbaf3c6c7eebea16ec1e21b2c67c8e6161446ed82a9553c26c04e19c1ec9ce248a9b9df504df56d309590259e6f04907b04b593548028b40e40d47
# Wed, 22 Jul 2020 18:36:33 GMT
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin
# Wed, 22 Jul 2020 18:36:41 GMT
COPY file:c6e11ee7dda40f44aa31f3bcb74669e99572ad86040276440b444d5699d333f5 in /usr/local/bin/ 
# Wed, 22 Jul 2020 18:36:45 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Wed, 22 Jul 2020 18:36:48 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:7ae4223cfc253e8d54407ec654ed8fb606352daea8da124f33dacd17626259ad`  
		Last Modified: Wed, 22 Jul 2020 00:58:53 GMT  
		Size: 24.8 MB (24837461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:121b9a2d2615295452a8d377696a9c2ffb89b0176f7cc3b701db363dbb4142f0`  
		Last Modified: Wed, 22 Jul 2020 04:39:35 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae84ea44ff3bff3f0c88ef55cd974a2c80a16e636d903143859b537ce76d0fb`  
		Last Modified: Wed, 22 Jul 2020 04:39:56 GMT  
		Size: 58.8 MB (58799780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8462af0cdae0d179cc321c75b4e11be78793c1b3c7abf6032619bead6d90625f`  
		Last Modified: Wed, 22 Jul 2020 04:39:35 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f71aea908d6d9ce360fe67fa75d791501335466ef2bf86859b2bd417c1c97a88`  
		Last Modified: Wed, 22 Jul 2020 04:43:31 GMT  
		Size: 12.4 MB (12437696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2261e2dab20d8fadaed7f0bf4b691784665dc4d673fb27acf926f46f564f73f4`  
		Last Modified: Wed, 22 Jul 2020 04:43:29 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7649a0f8727d8a9be6cdd0fc2e78de9a7d4f398948eb21cc248a16be10c4ed95`  
		Last Modified: Wed, 22 Jul 2020 04:43:37 GMT  
		Size: 27.3 MB (27321821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee15c49cf16bf410a92aaa0264e45aa6e77377beabc1e6c151991267c9b83d4f`  
		Last Modified: Wed, 22 Jul 2020 04:43:28 GMT  
		Size: 2.3 KB (2276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3895a291433c521e024b59d56c3c74d5d3e889ee10cb69fe63a5bdbcde689b`  
		Last Modified: Wed, 22 Jul 2020 04:43:28 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac2c6d2ba3ea72c0c0497b6a4b1ea733277d2b8d6d5e6bdc106bca634cbb3603`  
		Last Modified: Wed, 22 Jul 2020 04:43:28 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072a539d827b8644957098601b1f6a868f60ac103b45834aa0b580cfe86e80d0`  
		Last Modified: Wed, 22 Jul 2020 04:43:28 GMT  
		Size: 8.4 KB (8413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1c4a5e72a26ef53f0f7fa69722aa0a35292673f97da4b8208acd2885096f91`  
		Last Modified: Wed, 22 Jul 2020 18:37:38 GMT  
		Size: 589.8 KB (589796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48081a9729bb257c9ca21e2078a0a42d17e03149280e16de7c4db2651a4baac`  
		Last Modified: Wed, 22 Jul 2020 18:37:39 GMT  
		Size: 1.3 MB (1334647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17f2d9af91e5b405e8360981b2fecd28890c4c63a2d11bed70e272be159ea5e0`  
		Last Modified: Wed, 22 Jul 2020 18:37:38 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postfixadmin:3-fpm` - linux; arm variant v7

```console
$ docker pull postfixadmin@sha256:c1417dff6463c5263cf7101ee3419255818e6effb00c6cf58b203c351a1e287a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **122.9 MB (122892823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc52963ad8329d4938081670410878b6995a66cefb35196b6585fde95e042ee9`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 22 Jul 2020 01:19:50 GMT
ADD file:c47f7b84c9113624f53d9c52e13f649f1e5d739665b5a5a5df6b1d5b5274d71b in / 
# Wed, 22 Jul 2020 01:19:58 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 09:31:35 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 22 Jul 2020 09:31:35 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Jul 2020 09:32:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 09:32:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Jul 2020 09:32:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 22 Jul 2020 09:40:50 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Wed, 22 Jul 2020 09:40:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Jul 2020 09:40:52 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Jul 2020 09:40:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Jul 2020 10:24:04 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Wed, 22 Jul 2020 10:24:06 GMT
ENV PHP_VERSION=7.3.20
# Wed, 22 Jul 2020 10:24:08 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.20.tar.xz.asc
# Wed, 22 Jul 2020 10:24:12 GMT
ENV PHP_SHA256=43292046f6684eb13acb637276d4aa1dd9f66b0b7045e6f1493bc90db389b888 PHP_MD5=
# Wed, 22 Jul 2020 10:24:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 22 Jul 2020 10:24:47 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 22 Jul 2020 10:28:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Wed, 22 Jul 2020 10:28:38 GMT
COPY multi:bd67471e0c4047be362a8a0e199558e6245207a6f70b72fdfe55aa2d2cae15e6 in /usr/local/bin/ 
# Wed, 22 Jul 2020 10:29:08 GMT
RUN docker-php-ext-enable sodium
# Wed, 22 Jul 2020 10:29:26 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Wed, 22 Jul 2020 10:29:29 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Jul 2020 10:29:38 GMT
WORKDIR /var/www/html
# Wed, 22 Jul 2020 10:29:58 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Wed, 22 Jul 2020 10:30:00 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 Jul 2020 10:30:02 GMT
EXPOSE 9000
# Wed, 22 Jul 2020 10:30:07 GMT
CMD ["php-fpm"]
# Thu, 23 Jul 2020 05:46:17 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Thu, 23 Jul 2020 05:47:29 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-install -j "$(nproc)" 		mysqli 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jul 2020 05:47:31 GMT
ARG POSTFIXADMIN_VERSION=3.2.4
# Thu, 23 Jul 2020 05:47:34 GMT
ARG POSTFIXADMIN_SHA512=2bd7ae05addbaf3c6c7eebea16ec1e21b2c67c8e6161446ed82a9553c26c04e19c1ec9ce248a9b9df504df56d309590259e6f04907b04b593548028b40e40d47
# Thu, 23 Jul 2020 05:47:36 GMT
ENV POSTFIXADMIN_VERSION=3.2.4
# Thu, 23 Jul 2020 05:47:38 GMT
ENV POSTFIXADMIN_SHA512=2bd7ae05addbaf3c6c7eebea16ec1e21b2c67c8e6161446ed82a9553c26c04e19c1ec9ce248a9b9df504df56d309590259e6f04907b04b593548028b40e40d47
# Thu, 23 Jul 2020 05:47:57 GMT
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin
# Thu, 23 Jul 2020 05:48:00 GMT
COPY file:c6e11ee7dda40f44aa31f3bcb74669e99572ad86040276440b444d5699d333f5 in /usr/local/bin/ 
# Thu, 23 Jul 2020 05:48:03 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 23 Jul 2020 05:48:05 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:0c4667eb56da53c2c07c288a210a70fb8d6089f57ce32a2cd88c2a75ae9ad8af`  
		Last Modified: Wed, 22 Jul 2020 01:40:34 GMT  
		Size: 22.7 MB (22705906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73a476362b835810ad6f6eaecc2a497b4302f2b8ac196c911884fe753f3be0c`  
		Last Modified: Wed, 22 Jul 2020 11:54:53 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbec70860f5643fca4a35066a02be7aab2ad53c776daa74f2b6d2bc97ad9f9f3`  
		Last Modified: Wed, 22 Jul 2020 11:55:12 GMT  
		Size: 59.5 MB (59505456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b7f7b8f25575d1efc6595391f7314710b2d0187564386d0cf3a81a74c4278d6`  
		Last Modified: Wed, 22 Jul 2020 11:54:53 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e979f3c71349149dbda24cb5ba863dec6e9a86707778853935f0616e5b0136c`  
		Last Modified: Wed, 22 Jul 2020 11:59:44 GMT  
		Size: 12.4 MB (12437696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c845fa190ab95d251b983a575c72d67b96e396b8bd788ea7bd75edd994c85899`  
		Last Modified: Wed, 22 Jul 2020 11:59:42 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753b0f962ab2f7e45937fdff70bad0497e627442e351d3163580bd0ec946b39e`  
		Last Modified: Wed, 22 Jul 2020 11:59:46 GMT  
		Size: 26.3 MB (26322092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1045277d53af97204e4cbe1ace5d34cfd196f9098110fb798cf96b1bb2ce997a`  
		Last Modified: Wed, 22 Jul 2020 11:59:38 GMT  
		Size: 2.3 KB (2276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e317f8885fae350133b7ca5f7103ef81c062d6ef03b317e45080ff45fc82b338`  
		Last Modified: Wed, 22 Jul 2020 11:59:38 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42987a470be83470406ace68cfccd9104f1e6e3f95324137a8fea1ae4fd0fb2c`  
		Last Modified: Wed, 22 Jul 2020 11:59:38 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d932bdb8c66e38d0db09c8852fb8bd1fcd5bf441379cc8aee915539bac41d6`  
		Last Modified: Wed, 22 Jul 2020 11:59:38 GMT  
		Size: 8.4 KB (8417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92434df1e8920865dd7bfe9601a241938f024ba4c5a1eb5ba9ddbd148347dce0`  
		Last Modified: Thu, 23 Jul 2020 05:48:51 GMT  
		Size: 573.6 KB (573555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d210d1e9c7025d4834726d30cb2cc4eb2b7b70fc9a7f9ff3270eb95e57c4720`  
		Last Modified: Thu, 23 Jul 2020 05:48:51 GMT  
		Size: 1.3 MB (1334644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61d3ee254ed1b06299dcc1b61a64782fa635c6095c5f982277e24d5b2745ec4`  
		Last Modified: Thu, 23 Jul 2020 05:48:51 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postfixadmin:3-fpm` - linux; arm64 variant v8

```console
$ docker pull postfixadmin@sha256:eec8d6dbccffb02bf75579421fd659777290c9498cb8d98bccc2540b05f41c53
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (139038096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c27bd73323a5ada42bcb21cb6ce50fe58369aaeba5b36c58baf0bab476cecef4`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 22 Jul 2020 00:41:09 GMT
ADD file:1efd5b51a56f36bcf79a1bcea1df36ef28299a42bc11e758f9e49066f2a1f085 in / 
# Wed, 22 Jul 2020 00:41:10 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 11:19:48 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 22 Jul 2020 11:19:49 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Jul 2020 11:20:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 11:20:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Jul 2020 11:21:01 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 22 Jul 2020 11:31:25 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Wed, 22 Jul 2020 11:31:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Jul 2020 11:31:27 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Jul 2020 11:31:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Jul 2020 12:09:54 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Wed, 22 Jul 2020 12:09:55 GMT
ENV PHP_VERSION=7.3.20
# Wed, 22 Jul 2020 12:09:56 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.20.tar.xz.asc
# Wed, 22 Jul 2020 12:09:57 GMT
ENV PHP_SHA256=43292046f6684eb13acb637276d4aa1dd9f66b0b7045e6f1493bc90db389b888 PHP_MD5=
# Wed, 22 Jul 2020 12:10:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 22 Jul 2020 12:10:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 22 Jul 2020 12:13:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Wed, 22 Jul 2020 12:13:42 GMT
COPY multi:bd67471e0c4047be362a8a0e199558e6245207a6f70b72fdfe55aa2d2cae15e6 in /usr/local/bin/ 
# Wed, 22 Jul 2020 12:13:45 GMT
RUN docker-php-ext-enable sodium
# Wed, 22 Jul 2020 12:13:47 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Wed, 22 Jul 2020 12:13:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Jul 2020 12:13:48 GMT
WORKDIR /var/www/html
# Wed, 22 Jul 2020 12:13:50 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Wed, 22 Jul 2020 12:13:51 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 Jul 2020 12:13:51 GMT
EXPOSE 9000
# Wed, 22 Jul 2020 12:13:52 GMT
CMD ["php-fpm"]
# Thu, 23 Jul 2020 03:57:51 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Thu, 23 Jul 2020 03:58:51 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-install -j "$(nproc)" 		mysqli 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Jul 2020 03:58:52 GMT
ARG POSTFIXADMIN_VERSION=3.2.4
# Thu, 23 Jul 2020 03:58:52 GMT
ARG POSTFIXADMIN_SHA512=2bd7ae05addbaf3c6c7eebea16ec1e21b2c67c8e6161446ed82a9553c26c04e19c1ec9ce248a9b9df504df56d309590259e6f04907b04b593548028b40e40d47
# Thu, 23 Jul 2020 03:58:53 GMT
ENV POSTFIXADMIN_VERSION=3.2.4
# Thu, 23 Jul 2020 03:58:54 GMT
ENV POSTFIXADMIN_SHA512=2bd7ae05addbaf3c6c7eebea16ec1e21b2c67c8e6161446ed82a9553c26c04e19c1ec9ce248a9b9df504df56d309590259e6f04907b04b593548028b40e40d47
# Thu, 23 Jul 2020 03:58:57 GMT
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin
# Thu, 23 Jul 2020 03:58:58 GMT
COPY file:c6e11ee7dda40f44aa31f3bcb74669e99572ad86040276440b444d5699d333f5 in /usr/local/bin/ 
# Thu, 23 Jul 2020 03:58:58 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Thu, 23 Jul 2020 03:58:59 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3999339def4d7591a8064bfc698302ae0e29bc5e0557ae392c122e1b3efa9305`  
		Last Modified: Wed, 22 Jul 2020 00:47:42 GMT  
		Size: 25.9 MB (25857826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4d0ba90fa18020ed9569da0e936f2c6d545f48231f27020a883d5de88d96a10`  
		Last Modified: Wed, 22 Jul 2020 13:32:50 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a37699742587260a77a7c676da89681dc8ca92dd2db86faee3dcc77109ccea`  
		Last Modified: Wed, 22 Jul 2020 13:33:12 GMT  
		Size: 70.3 MB (70337912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f6e19fa909b49d726f813175349e7ea4dcaa9589076b04108e40eda3f792b4`  
		Last Modified: Wed, 22 Jul 2020 13:32:49 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2e7b4bf131b03e818399eee0004ac7e9f98df41b102a8c992a2767d10121e3`  
		Last Modified: Wed, 22 Jul 2020 13:38:42 GMT  
		Size: 12.4 MB (12438355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7928b670eb66dd6d54df9512b5dc4f392477701b56097f9d30bce80b736e14`  
		Last Modified: Wed, 22 Jul 2020 13:38:41 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5325327235d742cf0b32a3653bfd50ae7206eb728b7c8d302febce965ce69d1`  
		Last Modified: Wed, 22 Jul 2020 13:38:47 GMT  
		Size: 28.4 MB (28437631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:467955f027ef6298f99268e5453031e8cb21f449069363fa5f92546da6dfb7cf`  
		Last Modified: Wed, 22 Jul 2020 13:38:37 GMT  
		Size: 2.3 KB (2273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aa5e7bde084dbc69adda9d142c8cb6c3b22d83e98f82f5cee3a1699d1437a63`  
		Last Modified: Wed, 22 Jul 2020 13:38:37 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:220a0fbe8409fc23b114ac7a8e5d141e0219ed50533c1e22853e7088e745b306`  
		Last Modified: Wed, 22 Jul 2020 13:38:37 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:820cad2bd4e76078edb6d45b1cfbe28485ef85c47e5bcc6e0a6e7d43ba1573a6`  
		Last Modified: Wed, 22 Jul 2020 13:38:37 GMT  
		Size: 8.4 KB (8415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d14fea6d136f8b79727d85864b5edd7610e0815e1119149bff87238eb46f24`  
		Last Modified: Thu, 23 Jul 2020 03:59:47 GMT  
		Size: 618.3 KB (618262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97eb8cef4e0298239ed189fcb33f05e08d777a54df19de162b057ba40e50cd9c`  
		Last Modified: Thu, 23 Jul 2020 03:59:47 GMT  
		Size: 1.3 MB (1334644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c879bbfefc47258ddabefc86c9fd84ac147cdb20b435d66563c84d7dad7bb8a8`  
		Last Modified: Thu, 23 Jul 2020 03:59:46 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postfixadmin:3-fpm` - linux; 386

```console
$ docker pull postfixadmin@sha256:21445f8429d3af315a795b16588fdb73f2b1a2d455590a5f035099edd4ff6962
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.7 MB (152705344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a0f8027a52b7ea4ed1244e94053491e3d06347eaa8ba285455c4e9f71a025da`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 22 Jul 2020 02:09:15 GMT
ADD file:ee51bd8fcf2e02243de32c0f0e7899acebfa23bdceb783f13feb33c484ee98b8 in / 
# Wed, 22 Jul 2020 02:09:15 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 08:42:58 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 22 Jul 2020 08:42:58 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Jul 2020 08:43:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 08:43:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Jul 2020 08:43:23 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 22 Jul 2020 09:00:17 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Wed, 22 Jul 2020 09:00:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Jul 2020 09:00:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Jul 2020 09:00:18 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Jul 2020 10:03:54 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Wed, 22 Jul 2020 10:03:54 GMT
ENV PHP_VERSION=7.3.20
# Wed, 22 Jul 2020 10:03:55 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.20.tar.xz.asc
# Wed, 22 Jul 2020 10:03:55 GMT
ENV PHP_SHA256=43292046f6684eb13acb637276d4aa1dd9f66b0b7045e6f1493bc90db389b888 PHP_MD5=
# Wed, 22 Jul 2020 10:04:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 22 Jul 2020 10:04:07 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 22 Jul 2020 10:13:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Wed, 22 Jul 2020 10:13:11 GMT
COPY multi:bd67471e0c4047be362a8a0e199558e6245207a6f70b72fdfe55aa2d2cae15e6 in /usr/local/bin/ 
# Wed, 22 Jul 2020 10:13:12 GMT
RUN docker-php-ext-enable sodium
# Wed, 22 Jul 2020 10:13:13 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Wed, 22 Jul 2020 10:13:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Jul 2020 10:13:13 GMT
WORKDIR /var/www/html
# Wed, 22 Jul 2020 10:13:14 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Wed, 22 Jul 2020 10:13:15 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 Jul 2020 10:13:15 GMT
EXPOSE 9000
# Wed, 22 Jul 2020 10:13:15 GMT
CMD ["php-fpm"]
# Wed, 22 Jul 2020 23:27:00 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Wed, 22 Jul 2020 23:27:44 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-install -j "$(nproc)" 		mysqli 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 23:27:44 GMT
ARG POSTFIXADMIN_VERSION=3.2.4
# Wed, 22 Jul 2020 23:27:44 GMT
ARG POSTFIXADMIN_SHA512=2bd7ae05addbaf3c6c7eebea16ec1e21b2c67c8e6161446ed82a9553c26c04e19c1ec9ce248a9b9df504df56d309590259e6f04907b04b593548028b40e40d47
# Wed, 22 Jul 2020 23:27:44 GMT
ENV POSTFIXADMIN_VERSION=3.2.4
# Wed, 22 Jul 2020 23:27:45 GMT
ENV POSTFIXADMIN_SHA512=2bd7ae05addbaf3c6c7eebea16ec1e21b2c67c8e6161446ed82a9553c26c04e19c1ec9ce248a9b9df504df56d309590259e6f04907b04b593548028b40e40d47
# Wed, 22 Jul 2020 23:27:46 GMT
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin
# Wed, 22 Jul 2020 23:27:47 GMT
COPY file:c6e11ee7dda40f44aa31f3bcb74669e99572ad86040276440b444d5699d333f5 in /usr/local/bin/ 
# Wed, 22 Jul 2020 23:27:47 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Wed, 22 Jul 2020 23:27:47 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:75157e9ef5a857d6b02d235e08a164737ad009bae299277f86131063e6204e0b`  
		Last Modified: Wed, 22 Jul 2020 02:15:45 GMT  
		Size: 27.8 MB (27754899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dac354b7d13e3bb52269c5c4afdb82d013431213a5c1abd2bcdbe7c8746143b`  
		Last Modified: Wed, 22 Jul 2020 12:01:42 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed3244890340b96c338e5649236ef464c2002d7f8034b40bf205bcfb8303fd8`  
		Last Modified: Wed, 22 Jul 2020 12:02:07 GMT  
		Size: 81.2 MB (81195189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c2b96264b3ad05aacda736bbf4212e47ab5aa547d7838b399eb4c1bc6237e4`  
		Last Modified: Wed, 22 Jul 2020 12:01:41 GMT  
		Size: 223.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2904a5a4f04195ee2f7582d8d6e81d3ecca9d7baafe69aae0afeaa12ffcaf32`  
		Last Modified: Wed, 22 Jul 2020 12:05:13 GMT  
		Size: 12.4 MB (12438554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73334b51f18f0f53049e39e29b613f8c272e4f2c91d7a55bfe807558a079627`  
		Last Modified: Wed, 22 Jul 2020 12:05:12 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc74bebbd415242b47ba4d05b2b6561394908ca0e1f2b5af80c1387389319844`  
		Last Modified: Wed, 22 Jul 2020 12:05:19 GMT  
		Size: 29.3 MB (29328166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0aee9d59d243f38b410393589d62ecb46efd8f1151e8457d14e2f9c602f25f`  
		Last Modified: Wed, 22 Jul 2020 12:05:11 GMT  
		Size: 2.3 KB (2275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c4f5bbef41ced88b1dd12e2b2aaae445295a2d9c6060d7db74ba77006d3182`  
		Last Modified: Wed, 22 Jul 2020 12:05:11 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e770a851240d2030a92fe9924009a7fda6adabe9efb6189cb2b8b5b0ef49e9`  
		Last Modified: Wed, 22 Jul 2020 12:05:11 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa782541f061c7c5a7915eb1b9e1f9a30b6e80529548da286b6612b61776c9ab`  
		Last Modified: Wed, 22 Jul 2020 12:05:11 GMT  
		Size: 8.4 KB (8413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a43f51e89bcdaf884135388eb699834847dc5b5a3cf7130234e2ecb683c228c3`  
		Last Modified: Wed, 22 Jul 2020 23:28:29 GMT  
		Size: 640.5 KB (640507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6b1fbf6993fbe5d0a907fba3a78457dd8d5f5eaeae00e46bd5ced31138da946`  
		Last Modified: Wed, 22 Jul 2020 23:28:30 GMT  
		Size: 1.3 MB (1334610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517e54febe95bac579c5ae941a14c59af01832612bcbd01c102970e12f2f2242`  
		Last Modified: Wed, 22 Jul 2020 23:28:29 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postfixadmin:3-fpm` - linux; mips64le

```console
$ docker pull postfixadmin@sha256:983f2d347d0f7dbce94a3abfe0400665b9ba587798955fe01db678a77a5ad1b5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.6 MB (129642876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d72e876ce08b34417170dee5ea83d0dad0c9b415e4acc658c3ea43197fcc79`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 22 Jul 2020 01:09:52 GMT
ADD file:67401cc8bdd27435a027e4051d2eb03c5012a09274aaae230008279234586dfb in / 
# Wed, 22 Jul 2020 01:09:53 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 10:58:51 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 22 Jul 2020 10:58:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Jul 2020 10:59:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 10:59:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Jul 2020 10:59:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 22 Jul 2020 11:25:35 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Wed, 22 Jul 2020 11:25:35 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Jul 2020 11:25:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Jul 2020 11:25:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Jul 2020 13:02:15 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Wed, 22 Jul 2020 13:02:15 GMT
ENV PHP_VERSION=7.3.20
# Wed, 22 Jul 2020 13:02:16 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.20.tar.xz.asc
# Wed, 22 Jul 2020 13:02:16 GMT
ENV PHP_SHA256=43292046f6684eb13acb637276d4aa1dd9f66b0b7045e6f1493bc90db389b888 PHP_MD5=
# Wed, 22 Jul 2020 13:02:38 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 22 Jul 2020 13:02:38 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 22 Jul 2020 13:15:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Wed, 22 Jul 2020 13:15:38 GMT
COPY multi:bd67471e0c4047be362a8a0e199558e6245207a6f70b72fdfe55aa2d2cae15e6 in /usr/local/bin/ 
# Wed, 22 Jul 2020 13:15:40 GMT
RUN docker-php-ext-enable sodium
# Wed, 22 Jul 2020 13:15:42 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Wed, 22 Jul 2020 13:15:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Jul 2020 13:15:43 GMT
WORKDIR /var/www/html
# Wed, 22 Jul 2020 13:15:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Wed, 22 Jul 2020 13:15:45 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 Jul 2020 13:15:45 GMT
EXPOSE 9000
# Wed, 22 Jul 2020 13:15:46 GMT
CMD ["php-fpm"]
# Wed, 22 Jul 2020 21:13:59 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Wed, 22 Jul 2020 21:15:39 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-install -j "$(nproc)" 		mysqli 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 21:15:39 GMT
ARG POSTFIXADMIN_VERSION=3.2.4
# Wed, 22 Jul 2020 21:15:40 GMT
ARG POSTFIXADMIN_SHA512=2bd7ae05addbaf3c6c7eebea16ec1e21b2c67c8e6161446ed82a9553c26c04e19c1ec9ce248a9b9df504df56d309590259e6f04907b04b593548028b40e40d47
# Wed, 22 Jul 2020 21:15:40 GMT
ENV POSTFIXADMIN_VERSION=3.2.4
# Wed, 22 Jul 2020 21:15:40 GMT
ENV POSTFIXADMIN_SHA512=2bd7ae05addbaf3c6c7eebea16ec1e21b2c67c8e6161446ed82a9553c26c04e19c1ec9ce248a9b9df504df56d309590259e6f04907b04b593548028b40e40d47
# Wed, 22 Jul 2020 21:15:43 GMT
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin
# Wed, 22 Jul 2020 21:15:44 GMT
COPY file:c6e11ee7dda40f44aa31f3bcb74669e99572ad86040276440b444d5699d333f5 in /usr/local/bin/ 
# Wed, 22 Jul 2020 21:15:44 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Wed, 22 Jul 2020 21:15:45 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:2cab09a0ed78d8465b06bc43bf504e7c4ed41f36db2ee9cb181c154d562fc9ff`  
		Last Modified: Wed, 22 Jul 2020 01:16:46 GMT  
		Size: 25.8 MB (25764196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8463e01d615b1d9517d01aa40d7ba0e6f6a788293708a58d907fa6221b7ff2`  
		Last Modified: Wed, 22 Jul 2020 14:18:42 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b823b35b4bd69b6de3643bb888921aa9369941215577b5970313929f85cd6fe`  
		Last Modified: Wed, 22 Jul 2020 14:19:32 GMT  
		Size: 61.4 MB (61386557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:514d0f889e1897eb582ad0ce9cf56634f335da1e0f69b6193ec78ac78cc68af3`  
		Last Modified: Wed, 22 Jul 2020 14:18:41 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c24b8c7118c34fb170c76163268fc82e2600b076788fa0b12a945e7f8fb172`  
		Last Modified: Wed, 22 Jul 2020 14:27:19 GMT  
		Size: 12.4 MB (12437109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3bb87ebcc7c5e80c98d3bd650ff6a3b61fd7d94f5ec58f2f290d7a1b68263de`  
		Last Modified: Wed, 22 Jul 2020 14:27:15 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0d435eb268dda49a2313bc3934a0f6b5ef30eb18df03559777a57647be39ef`  
		Last Modified: Wed, 22 Jul 2020 14:27:33 GMT  
		Size: 28.1 MB (28109977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f606889ac4430807bf514d0ec3eb4e2305cee4e5667afdc86bab982eabb1ec00`  
		Last Modified: Wed, 22 Jul 2020 14:27:13 GMT  
		Size: 2.3 KB (2276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87d7c6c92f24c34cb1824251d4efcaac6a4eb5f7bc0fefcbe76ba0a22d2c5175`  
		Last Modified: Wed, 22 Jul 2020 14:27:13 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f026302bed17093dd9b040434a75c768d626bcd51580e7935d0393101c3befc2`  
		Last Modified: Wed, 22 Jul 2020 14:27:14 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47925a0f44daba323827054345d95e2f069fc271efa6d847c2cb31541b060d31`  
		Last Modified: Wed, 22 Jul 2020 14:27:13 GMT  
		Size: 8.4 KB (8415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975f6db4a9fe7745ce5eb7bc821bb28bca34a3397691c8698dc613a923c0db1a`  
		Last Modified: Wed, 22 Jul 2020 21:16:50 GMT  
		Size: 597.0 KB (596995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aeaa0801edb66a60adaf2fa156a68aebd651e2637cddef419c846a1122c1151`  
		Last Modified: Wed, 22 Jul 2020 21:16:51 GMT  
		Size: 1.3 MB (1334610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb3333d0f24bff6e69a6c68476014e1e989bf6c0b21c525d95bef5efd814bc6`  
		Last Modified: Wed, 22 Jul 2020 21:16:50 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postfixadmin:3-fpm` - linux; ppc64le

```console
$ docker pull postfixadmin@sha256:cb2b99bf9fc3f7e9a364c3d1f328aeb12d126fb1c266baeb8801eef9696430a7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.7 MB (157713277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67d3245ee92d123a8273efbac10292ca64c0f99de1b8180b0e97831c920b867f`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Wed, 22 Jul 2020 02:16:05 GMT
ADD file:037dec996d9b742fc49f675272aa42ebd31f04226ba3d28836a6556cb61c29e7 in / 
# Wed, 22 Jul 2020 02:16:14 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 10:19:34 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 22 Jul 2020 10:19:41 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 22 Jul 2020 10:23:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 10:24:07 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 22 Jul 2020 10:24:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 22 Jul 2020 10:41:27 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Wed, 22 Jul 2020 10:41:30 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Jul 2020 10:41:36 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 22 Jul 2020 10:41:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 22 Jul 2020 11:59:55 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Wed, 22 Jul 2020 11:59:59 GMT
ENV PHP_VERSION=7.3.20
# Wed, 22 Jul 2020 12:00:05 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.20.tar.xz.asc
# Wed, 22 Jul 2020 12:00:15 GMT
ENV PHP_SHA256=43292046f6684eb13acb637276d4aa1dd9f66b0b7045e6f1493bc90db389b888 PHP_MD5=
# Wed, 22 Jul 2020 12:01:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 22 Jul 2020 12:01:39 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 22 Jul 2020 12:06:03 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Wed, 22 Jul 2020 12:06:09 GMT
COPY multi:bd67471e0c4047be362a8a0e199558e6245207a6f70b72fdfe55aa2d2cae15e6 in /usr/local/bin/ 
# Wed, 22 Jul 2020 12:06:22 GMT
RUN docker-php-ext-enable sodium
# Wed, 22 Jul 2020 12:06:34 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Wed, 22 Jul 2020 12:06:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 22 Jul 2020 12:06:43 GMT
WORKDIR /var/www/html
# Wed, 22 Jul 2020 12:06:52 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Wed, 22 Jul 2020 12:06:58 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 Jul 2020 12:07:02 GMT
EXPOSE 9000
# Wed, 22 Jul 2020 12:07:05 GMT
CMD ["php-fpm"]
# Wed, 22 Jul 2020 22:42:10 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Wed, 22 Jul 2020 22:44:04 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-install -j "$(nproc)" 		mysqli 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 22:44:09 GMT
ARG POSTFIXADMIN_VERSION=3.2.4
# Wed, 22 Jul 2020 22:44:13 GMT
ARG POSTFIXADMIN_SHA512=2bd7ae05addbaf3c6c7eebea16ec1e21b2c67c8e6161446ed82a9553c26c04e19c1ec9ce248a9b9df504df56d309590259e6f04907b04b593548028b40e40d47
# Wed, 22 Jul 2020 22:44:20 GMT
ENV POSTFIXADMIN_VERSION=3.2.4
# Wed, 22 Jul 2020 22:44:27 GMT
ENV POSTFIXADMIN_SHA512=2bd7ae05addbaf3c6c7eebea16ec1e21b2c67c8e6161446ed82a9553c26c04e19c1ec9ce248a9b9df504df56d309590259e6f04907b04b593548028b40e40d47
# Wed, 22 Jul 2020 22:44:49 GMT
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin
# Wed, 22 Jul 2020 22:44:54 GMT
COPY file:c6e11ee7dda40f44aa31f3bcb74669e99572ad86040276440b444d5699d333f5 in /usr/local/bin/ 
# Wed, 22 Jul 2020 22:45:01 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Wed, 22 Jul 2020 22:45:14 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d022338f917106731b8902d4c3d7009435a41381c11c8d210bbd6af007569f69`  
		Last Modified: Wed, 22 Jul 2020 02:26:01 GMT  
		Size: 30.5 MB (30524562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0664a61881d05cc0e8746a8342755ac9442a4f3e87073026096655cc55b0cc3`  
		Last Modified: Wed, 22 Jul 2020 13:40:57 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d65645e6fdf84bfa39a94f46a90aacec09a0d1d2d2606c365eb9a65c678fd4`  
		Last Modified: Wed, 22 Jul 2020 13:41:16 GMT  
		Size: 82.3 MB (82263064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a1f3da03577e1ffffca6abcd3a26313f2ed2f8424e1f2dfe21237345fd9b47`  
		Last Modified: Wed, 22 Jul 2020 13:40:56 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d3f74d7409b42037f5f7245e6fd1725f6e26c23cf577ed37d090b40a0e6fc2`  
		Last Modified: Wed, 22 Jul 2020 13:46:59 GMT  
		Size: 12.4 MB (12439194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:287d8de815c876ec32c2e693799451cb4be4d9f1395c4a3c1113a64aae42d620`  
		Last Modified: Wed, 22 Jul 2020 13:46:53 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f65a256778cba29ad9da64780c129fd8ef7c9712d05217bae00f78f75c2c21`  
		Last Modified: Wed, 22 Jul 2020 13:46:59 GMT  
		Size: 30.5 MB (30465689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b2b3834e1b9348c525d88f7b487a03ce3ba089403badbb9a53083eb7bb2024`  
		Last Modified: Wed, 22 Jul 2020 13:46:50 GMT  
		Size: 2.3 KB (2275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69aff80c09bff5e51cabd04757b9f79153ff8abe9f7a7dd712cbc38bff8db0ed`  
		Last Modified: Wed, 22 Jul 2020 13:46:52 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f077135edc184fc19cfb12d2f11f245c982ddabe820b8cbbd483af8494b16b66`  
		Last Modified: Wed, 22 Jul 2020 13:46:52 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56cdb839ac86d3d96c65a13324de1fd16cb96ae6b4113e412f98d34a5d0828f1`  
		Last Modified: Wed, 22 Jul 2020 13:46:52 GMT  
		Size: 8.4 KB (8417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3494574fd601de7221bb66d3a8b071bfe18c924ac2818dc41307b29cf15ed94b`  
		Last Modified: Wed, 22 Jul 2020 22:46:43 GMT  
		Size: 672.6 KB (672648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:886efd1641e869d2e7b8bf3fadb22c553e63164b34eab92c746f18c93c804a18`  
		Last Modified: Wed, 22 Jul 2020 22:46:43 GMT  
		Size: 1.3 MB (1334644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad97acc59c88c2c818065a4ba4be0b5493d413cd32d8d3668fdb1d299dca031b`  
		Last Modified: Wed, 22 Jul 2020 22:46:42 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `postfixadmin:3-fpm` - linux; s390x

```console
$ docker pull postfixadmin@sha256:2fcc61ae40f75bc6a6fdfc062b1e20bd6d5e14e36be4478aa23b635bdb3ad037
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.7 MB (132721336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:206bc7204bcef00e121a3e7205e703cbe20f10e110e30f6ed859a137267f987b`
-	Entrypoint: `["\/usr\/local\/bin\/docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 04 Aug 2020 01:17:16 GMT
ADD file:2ffa27c57800f9370adbaecca870158ec38c3d25a58b8803e2447c5e9320c5bb in / 
# Tue, 04 Aug 2020 01:17:17 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 03:17:46 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 04 Aug 2020 03:17:46 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 04 Aug 2020 03:17:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 03:18:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 04 Aug 2020 03:18:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 04 Aug 2020 03:22:38 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Tue, 04 Aug 2020 03:22:38 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Aug 2020 03:22:38 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 04 Aug 2020 03:22:39 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 04 Aug 2020 03:40:33 GMT
ENV GPG_KEYS=CBAF69F173A0FEA4B537F470D66C9593118BCCB6 F38252826ACD957EF380D39F2F7956BC5DA04B5D
# Tue, 04 Aug 2020 03:40:33 GMT
ENV PHP_VERSION=7.3.20
# Tue, 04 Aug 2020 03:40:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.3.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.3.20.tar.xz.asc
# Tue, 04 Aug 2020 03:40:33 GMT
ENV PHP_SHA256=43292046f6684eb13acb637276d4aa1dd9f66b0b7045e6f1493bc90db389b888 PHP_MD5=
# Tue, 04 Aug 2020 03:40:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 04 Aug 2020 03:40:40 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 04 Aug 2020 03:42:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 04 Aug 2020 03:42:41 GMT
COPY multi:bd67471e0c4047be362a8a0e199558e6245207a6f70b72fdfe55aa2d2cae15e6 in /usr/local/bin/ 
# Tue, 04 Aug 2020 03:42:41 GMT
RUN docker-php-ext-enable sodium
# Tue, 04 Aug 2020 03:42:42 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Tue, 04 Aug 2020 03:42:42 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 04 Aug 2020 03:42:42 GMT
WORKDIR /var/www/html
# Tue, 04 Aug 2020 03:42:43 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 04 Aug 2020 03:42:44 GMT
STOPSIGNAL SIGQUIT
# Tue, 04 Aug 2020 03:42:44 GMT
EXPOSE 9000
# Tue, 04 Aug 2020 03:42:44 GMT
CMD ["php-fpm"]
# Tue, 04 Aug 2020 09:41:20 GMT
LABEL maintainer=David Goodwin <david@codepoets.co.uk> (@DavidGoodwin)
# Tue, 04 Aug 2020 09:41:39 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 	libpq-dev 	libsqlite3-dev 	; 		docker-php-ext-install -j "$(nproc)" 		mysqli 		pdo_mysql 		pdo_pgsql 		pdo_sqlite 		pgsql 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 		ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 			apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 09:41:39 GMT
ARG POSTFIXADMIN_VERSION=3.2.4
# Tue, 04 Aug 2020 09:41:40 GMT
ARG POSTFIXADMIN_SHA512=2bd7ae05addbaf3c6c7eebea16ec1e21b2c67c8e6161446ed82a9553c26c04e19c1ec9ce248a9b9df504df56d309590259e6f04907b04b593548028b40e40d47
# Tue, 04 Aug 2020 09:41:40 GMT
ENV POSTFIXADMIN_VERSION=3.2.4
# Tue, 04 Aug 2020 09:41:40 GMT
ENV POSTFIXADMIN_SHA512=2bd7ae05addbaf3c6c7eebea16ec1e21b2c67c8e6161446ed82a9553c26c04e19c1ec9ce248a9b9df504df56d309590259e6f04907b04b593548028b40e40d47
# Tue, 04 Aug 2020 09:41:41 GMT
RUN set -eu; 	curl -fsSL -o postfixadmin.tar.gz "https://github.com/postfixadmin/postfixadmin/archive/postfixadmin-${POSTFIXADMIN_VERSION}.tar.gz"; 	echo "$POSTFIXADMIN_SHA512 *postfixadmin.tar.gz" | sha512sum -c -; 	mkdir /usr/src/postfixadmin; 	tar -xf postfixadmin.tar.gz -C /usr/src/postfixadmin --strip-components=1; 	rm postfixadmin.tar.gz; 	mkdir -p /usr/src/postfixadmin/templates_c; 	chown -R www-data:www-data /usr/src/postfixadmin
# Tue, 04 Aug 2020 09:41:42 GMT
COPY file:c6e11ee7dda40f44aa31f3bcb74669e99572ad86040276440b444d5699d333f5 in /usr/local/bin/ 
# Tue, 04 Aug 2020 09:41:42 GMT
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
# Tue, 04 Aug 2020 09:41:42 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:0c46adfa2de4a7b7eb1fe2f0cb928f9e15a4cc94b7b975f13392f397cbfb0f2c`  
		Last Modified: Tue, 04 Aug 2020 01:20:03 GMT  
		Size: 25.7 MB (25707641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0f8604b15b40b87c7c78f35c952be34d77e22c70a7a3d634af952bed77df82a`  
		Last Modified: Tue, 04 Aug 2020 03:56:06 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c79c3a25fa505e04cf025f8485f429f891ecf1609983c99d0f0b81a99aa8f54`  
		Last Modified: Tue, 04 Aug 2020 03:56:16 GMT  
		Size: 64.7 MB (64706546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007fcb88e4f44656bd1669c15b17ec295337d9d3a8ac3764848b6130f737ac05`  
		Last Modified: Tue, 04 Aug 2020 03:56:06 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73fdbf9b2774434f2f43a5e16aa2ad97a60bff092dd53c40f0032e13c368bf10`  
		Last Modified: Tue, 04 Aug 2020 03:58:51 GMT  
		Size: 12.4 MB (12437841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f26d72efa6a49fa2fd0575c45217a7b81a34452ea5f2d5ceef89b131eb63c8`  
		Last Modified: Tue, 04 Aug 2020 03:58:50 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93924c7229158071eb8d9f0f7d9e9826457f094602faaf8b3dbb6da87e3b1c7f`  
		Last Modified: Tue, 04 Aug 2020 03:58:53 GMT  
		Size: 27.9 MB (27902195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67862e3f150f07d9f8e37ea733cfdf2bee1ed3da1955a9311970134cee952311`  
		Last Modified: Tue, 04 Aug 2020 03:58:49 GMT  
		Size: 2.3 KB (2276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9caf619e105ef041b965f34b5e0966fac8f4e2a0b542ddc29e7cd91e993ca3ad`  
		Last Modified: Tue, 04 Aug 2020 03:58:49 GMT  
		Size: 246.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6517384cd7e06fc1142545456b54451ce77f79a90d928649bedbf10faf91761e`  
		Last Modified: Tue, 04 Aug 2020 03:58:49 GMT  
		Size: 214.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90f6ccd9b536b65fd30c1877542af328331560be77c78308ca321481c0263e13`  
		Last Modified: Tue, 04 Aug 2020 03:58:50 GMT  
		Size: 8.4 KB (8418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25f4d5b4068787c37f0624b6104f2aec545c39dc095849de8fec1b7feca2705`  
		Last Modified: Tue, 04 Aug 2020 09:42:11 GMT  
		Size: 619.0 KB (618989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d216eb976e5d0ed649c6a07d56648c097686cf4381b32bb617a5f1a29820656b`  
		Last Modified: Tue, 04 Aug 2020 09:42:11 GMT  
		Size: 1.3 MB (1334649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e1d7e975d353d5e40b4c25730874c601aafbebeb0a011fa55fe05dead50a225`  
		Last Modified: Tue, 04 Aug 2020 09:42:11 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
