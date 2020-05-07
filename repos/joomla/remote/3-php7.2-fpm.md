## `joomla:3-php7.2-fpm`

```console
$ docker pull joomla@sha256:bd0c133c0603ec64f4994e4a77683bff0a69b0bb3606743f39be406df78bcf74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `joomla:3-php7.2-fpm` - linux; amd64

```console
$ docker pull joomla@sha256:20700f0665600533b9ee004adfb97b60d73b33470778f02113ab3e1eea106f2b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.9 MB (157896124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec6efcc3cd622e020caca4df23a29f7df05a3f8e859534e023dc2ca5b3d4137a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 23 Apr 2020 00:20:32 GMT
ADD file:9b8be2b52ee0fa31da1b6256099030b73546253a57e94cccb24605cd888bb74d in / 
# Thu, 23 Apr 2020 00:20:32 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 16:34:10 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Apr 2020 16:34:11 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Apr 2020 16:34:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 16:34:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Apr 2020 16:34:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 23 Apr 2020 16:45:18 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 23 Apr 2020 16:45:18 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Apr 2020 16:45:18 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Apr 2020 16:45:19 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Apr 2020 18:07:06 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 23 Apr 2020 18:07:06 GMT
ENV PHP_VERSION=7.2.30
# Thu, 23 Apr 2020 18:07:06 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.30.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.30.tar.xz.asc/from/this/mirror
# Thu, 23 Apr 2020 18:07:06 GMT
ENV PHP_SHA256=aa93df27b58a45d6c9800ac813245dfdca03490a918ebe515b3a70189b1bf8c3 PHP_MD5=
# Thu, 23 Apr 2020 18:07:15 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Apr 2020 18:07:15 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Apr 2020 18:13:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Apr 2020 18:13:43 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 23 Apr 2020 18:13:44 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Apr 2020 18:13:44 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 23 Apr 2020 18:13:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Apr 2020 18:13:45 GMT
WORKDIR /var/www/html
# Thu, 23 Apr 2020 18:13:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 23 Apr 2020 18:13:46 GMT
STOPSIGNAL SIGQUIT
# Thu, 23 Apr 2020 18:13:46 GMT
EXPOSE 9000
# Thu, 23 Apr 2020 18:13:46 GMT
CMD ["php-fpm"]
# Fri, 24 Apr 2020 11:42:01 GMT
LABEL maintainer=Michael Babker <michael.babker@joomla.org> (@mbabker)
# Fri, 24 Apr 2020 11:42:01 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Fri, 24 Apr 2020 11:43:31 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 	; 		docker-php-ext-configure gd --with-jpeg-dir=/usr --with-png-dir=/usr; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.18; 	pecl install memcached-3.1.5; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 11:43:31 GMT
VOLUME [/var/www/html]
# Fri, 24 Apr 2020 11:43:31 GMT
ENV JOOMLA_VERSION=3.9.16
# Fri, 24 Apr 2020 11:43:31 GMT
ENV JOOMLA_SHA512=3266ff375631fd0c4c45c66368f3d07cdc1b41010ffad907a957e6c1acb511847bf2c112e0991792f84455b48bea95c84eca9a7325baa3cab61078fda697ed0f
# Fri, 24 Apr 2020 11:43:35 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Fri, 24 Apr 2020 11:43:36 GMT
COPY file:fcc18c5b9c2d514cfb965bab84e10b4f924a39a5f202055df75d7990da099d8f in /entrypoint.sh 
# Fri, 24 Apr 2020 11:43:36 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Fri, 24 Apr 2020 11:43:36 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Apr 2020 11:43:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:54fec2fa59d0a0de9cd2dec9850b36c43de451f1fd1c0a5bf8f1cf26a61a5da4`  
		Last Modified: Thu, 23 Apr 2020 00:25:10 GMT  
		Size: 27.1 MB (27098254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4504446071184d4707bc1b754311b73a078008c3d1c64b7c3603e062f9e826`  
		Last Modified: Thu, 23 Apr 2020 18:46:20 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d55b89827dff29b49f86cebc978eddb06ffdf89e9675cc9e43e76939a1a3cd`  
		Last Modified: Thu, 23 Apr 2020 18:46:38 GMT  
		Size: 76.7 MB (76651558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf7f8bea876f55a2bbbf9e69e2190755e54d4dfc340c16418a66593e8f0cc61`  
		Last Modified: Thu, 23 Apr 2020 18:46:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c8a2134daff4c37501d0198f2cc4709f185b6525e508d41e81c0aabcb16af9`  
		Last Modified: Thu, 23 Apr 2020 18:50:22 GMT  
		Size: 12.6 MB (12605492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203812a551de0b8f398617cdd41d95e28e1c2ecc9ac735c48dbaa61baf3be191`  
		Last Modified: Thu, 23 Apr 2020 18:50:21 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c6aa1564dc4ea61e37ca036ffa8fb1570440595fb816bc012d9c8c8c555b518`  
		Last Modified: Thu, 23 Apr 2020 18:50:26 GMT  
		Size: 28.5 MB (28529520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c2af4cbdc952f58b40c9ba1e533957d4ee9a989c91557ebe6c057b1f9a05e09`  
		Last Modified: Thu, 23 Apr 2020 18:50:20 GMT  
		Size: 2.2 KB (2223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5882f07a58b775f818946c171511d5cee9726cc0c76b1517ddd2559a6e87c90d`  
		Last Modified: Thu, 23 Apr 2020 18:50:20 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be369d8f6b61627b3553498a39f30c06ec77c57b00e80a61a8a0b1f3fd8f430c`  
		Last Modified: Thu, 23 Apr 2020 18:50:20 GMT  
		Size: 215.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07aa6855a1c99661cc0f2785e6c5135303ab74fdd70213646198adff72c17178`  
		Last Modified: Thu, 23 Apr 2020 18:50:21 GMT  
		Size: 7.8 KB (7788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7773f22506704aaecbeed30575b17b622fabbd657f180ba21139ae52a219511`  
		Last Modified: Fri, 24 Apr 2020 11:51:38 GMT  
		Size: 3.3 MB (3344601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e43608977dd0c4072d2050855c97349c8860052cb64d21b2d1c80e489fb6469`  
		Last Modified: Fri, 24 Apr 2020 11:51:40 GMT  
		Size: 9.7 MB (9653495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1d32588d99339a93292561f237e7184472cbdbc4312ae38abae454b80fc8e1`  
		Last Modified: Fri, 24 Apr 2020 11:51:37 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d21bdaeb7cf70e1907a212ba234dbb21c279e35226743e2e41f5eb63b69f7911`  
		Last Modified: Fri, 24 Apr 2020 11:51:37 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:3-php7.2-fpm` - linux; arm variant v5

```console
$ docker pull joomla@sha256:a28ad56fb252229c8f4654c882c190a5fe248c2df11bdd4238607dd9bd4ef24d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.4 MB (136372869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca428038fb19b72992265dc176378de509d24c0edca5726c6eda751ce3333dac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 23 Apr 2020 00:52:22 GMT
ADD file:62a9732be4e3237ccc896f724a34606e01f351c4877e52c9a9cd85029c06b956 in / 
# Thu, 23 Apr 2020 00:52:23 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 05:05:35 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Apr 2020 05:05:36 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Apr 2020 05:06:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 05:06:24 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Apr 2020 05:06:26 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 23 Apr 2020 05:14:48 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 23 Apr 2020 05:14:50 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Apr 2020 05:14:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Apr 2020 05:14:53 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Apr 2020 06:06:22 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 23 Apr 2020 06:06:23 GMT
ENV PHP_VERSION=7.2.30
# Wed, 06 May 2020 22:56:41 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.30.tar.xz.asc
# Wed, 06 May 2020 22:56:42 GMT
ENV PHP_SHA256=aa93df27b58a45d6c9800ac813245dfdca03490a918ebe515b3a70189b1bf8c3 PHP_MD5=
# Wed, 06 May 2020 22:57:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 06 May 2020 22:57:08 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 06 May 2020 23:01:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Wed, 06 May 2020 23:01:27 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Wed, 06 May 2020 23:01:29 GMT
RUN docker-php-ext-enable sodium
# Wed, 06 May 2020 23:01:31 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Wed, 06 May 2020 23:01:32 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 May 2020 23:01:33 GMT
WORKDIR /var/www/html
# Wed, 06 May 2020 23:01:35 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Wed, 06 May 2020 23:01:36 GMT
STOPSIGNAL SIGQUIT
# Wed, 06 May 2020 23:01:37 GMT
EXPOSE 9000
# Wed, 06 May 2020 23:01:38 GMT
CMD ["php-fpm"]
# Thu, 07 May 2020 00:12:27 GMT
LABEL maintainer=Michael Babker <michael.babker@joomla.org> (@mbabker)
# Thu, 07 May 2020 00:12:28 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Thu, 07 May 2020 00:16:09 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 	; 		docker-php-ext-configure gd --with-jpeg-dir=/usr --with-png-dir=/usr; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.18; 	pecl install memcached-3.1.5; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 May 2020 00:16:12 GMT
VOLUME [/var/www/html]
# Thu, 07 May 2020 00:16:14 GMT
ENV JOOMLA_VERSION=3.9.16
# Thu, 07 May 2020 00:16:15 GMT
ENV JOOMLA_SHA512=3266ff375631fd0c4c45c66368f3d07cdc1b41010ffad907a957e6c1acb511847bf2c112e0991792f84455b48bea95c84eca9a7325baa3cab61078fda697ed0f
# Thu, 07 May 2020 00:16:33 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Thu, 07 May 2020 00:16:35 GMT
COPY file:fcc18c5b9c2d514cfb965bab84e10b4f924a39a5f202055df75d7990da099d8f in /entrypoint.sh 
# Thu, 07 May 2020 00:16:36 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Thu, 07 May 2020 00:16:38 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 May 2020 00:16:39 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:a8c46e5952878f9f324df86c5a2b45b2e0020f6721e820981e74461d77a100dd`  
		Last Modified: Thu, 23 Apr 2020 00:59:50 GMT  
		Size: 24.8 MB (24836319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a265de7879713459cf6e6045e802665b84c49dcb7194d42e80f713168a926d4`  
		Last Modified: Thu, 23 Apr 2020 06:32:43 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710cdb8f85f5abf4fda742431a0310421e7bd540337a4d831a04c9da4f000b2e`  
		Last Modified: Thu, 23 Apr 2020 06:33:06 GMT  
		Size: 58.8 MB (58799213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36a8c43726552051e04d6641b87a0c8dd7104c18f21f0b0a2f06ed6d5e03377`  
		Last Modified: Thu, 23 Apr 2020 06:32:43 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12d14a0162caa59dbd6d69a86a548714988b155da11f9ce7942fc9475479125`  
		Last Modified: Wed, 06 May 2020 23:30:39 GMT  
		Size: 12.6 MB (12603500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d70d5db5212e5535bdd2b412177fa664b89d7032986f388c4e33874db5169a0`  
		Last Modified: Wed, 06 May 2020 23:30:37 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c67ac265af53d9c220b8586a8fe6de4eb1dac19f8c8a507349afeb84cb64050`  
		Last Modified: Wed, 06 May 2020 23:30:45 GMT  
		Size: 27.1 MB (27139873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cfb988112a3d7287df39152e9b4268a897be2559d5211abbbb62a9ae7db2882`  
		Last Modified: Wed, 06 May 2020 23:30:37 GMT  
		Size: 2.2 KB (2222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54045822a4a3e14e2fe30d160b040dd71160e7cf8f71c555bdb650000b0cfa16`  
		Last Modified: Wed, 06 May 2020 23:30:36 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c5d009fbf28ed61925dcbb06e4f915f78409f8994f28e677f4e0eeff9e1aba`  
		Last Modified: Wed, 06 May 2020 23:30:36 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c373737b5f4dcab3bd9f815c05968db4a1f50acd0a929d4e134830fd41338322`  
		Last Modified: Wed, 06 May 2020 23:30:36 GMT  
		Size: 7.8 KB (7787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04eadf7c8048c8a5e5550d1352b674bb309a10528aa43398bdd6fe6e6d72ea67`  
		Last Modified: Thu, 07 May 2020 00:32:56 GMT  
		Size: 3.3 MB (3327044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdee91c6bcf6dd421b2a089b04079783e8a617845974ddbd7dc400fcaef8fee1`  
		Last Modified: Thu, 07 May 2020 00:32:59 GMT  
		Size: 9.7 MB (9653671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a0906b42d85850901d4ca3da70b05c44b4e3af7f8162d205e411264f6806cb`  
		Last Modified: Thu, 07 May 2020 00:32:54 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:299cebcea7c1a00e7bdd48dded2226b7a28de8af012c1ec265bd32a06b5b6c94`  
		Last Modified: Thu, 07 May 2020 00:32:54 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:3-php7.2-fpm` - linux; arm variant v7

```console
$ docker pull joomla@sha256:a61383badc2585733254b895f70fc7d8784c68fd384e03769c970d2e83a816ea
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133822995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0af6bb2bf95c75654fb0e87d6641aed5f9afa99032826dafa629186692344f9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 23 Apr 2020 01:03:26 GMT
ADD file:db6122b36f3e70c5f490b50afba99d49fa345f11d0f5c77bb3c6749f8e2a4f81 in / 
# Thu, 23 Apr 2020 01:03:28 GMT
CMD ["bash"]
# Fri, 24 Apr 2020 08:57:05 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Fri, 24 Apr 2020 08:57:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Fri, 24 Apr 2020 08:57:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 08:57:51 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Fri, 24 Apr 2020 08:57:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Fri, 24 Apr 2020 09:05:33 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Fri, 24 Apr 2020 09:05:34 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Apr 2020 09:05:35 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Fri, 24 Apr 2020 09:05:35 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Fri, 24 Apr 2020 10:28:55 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Fri, 24 Apr 2020 10:28:55 GMT
ENV PHP_VERSION=7.2.30
# Wed, 06 May 2020 23:39:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-7.2.30.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-7.2.30.tar.xz.asc
# Wed, 06 May 2020 23:39:08 GMT
ENV PHP_SHA256=aa93df27b58a45d6c9800ac813245dfdca03490a918ebe515b3a70189b1bf8c3 PHP_MD5=
# Wed, 06 May 2020 23:39:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 06 May 2020 23:39:26 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Wed, 06 May 2020 23:42:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Wed, 06 May 2020 23:42:40 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Wed, 06 May 2020 23:42:42 GMT
RUN docker-php-ext-enable sodium
# Wed, 06 May 2020 23:42:45 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Wed, 06 May 2020 23:42:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 06 May 2020 23:42:46 GMT
WORKDIR /var/www/html
# Wed, 06 May 2020 23:42:49 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Wed, 06 May 2020 23:42:50 GMT
STOPSIGNAL SIGQUIT
# Wed, 06 May 2020 23:42:52 GMT
EXPOSE 9000
# Wed, 06 May 2020 23:42:53 GMT
CMD ["php-fpm"]
# Thu, 07 May 2020 01:09:11 GMT
LABEL maintainer=Michael Babker <michael.babker@joomla.org> (@mbabker)
# Thu, 07 May 2020 01:09:12 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Thu, 07 May 2020 01:12:05 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 	; 		docker-php-ext-configure gd --with-jpeg-dir=/usr --with-png-dir=/usr; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.18; 	pecl install memcached-3.1.5; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Thu, 07 May 2020 01:12:07 GMT
VOLUME [/var/www/html]
# Thu, 07 May 2020 01:12:08 GMT
ENV JOOMLA_VERSION=3.9.16
# Thu, 07 May 2020 01:12:09 GMT
ENV JOOMLA_SHA512=3266ff375631fd0c4c45c66368f3d07cdc1b41010ffad907a957e6c1acb511847bf2c112e0991792f84455b48bea95c84eca9a7325baa3cab61078fda697ed0f
# Thu, 07 May 2020 01:12:21 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Thu, 07 May 2020 01:12:24 GMT
COPY file:fcc18c5b9c2d514cfb965bab84e10b4f924a39a5f202055df75d7990da099d8f in /entrypoint.sh 
# Thu, 07 May 2020 01:12:25 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Thu, 07 May 2020 01:12:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 07 May 2020 01:12:28 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:50fb0052086928803f00724ca465c89c45dde5b082b1e59dadb8101286dd5ab6`  
		Last Modified: Thu, 23 Apr 2020 01:11:08 GMT  
		Size: 22.7 MB (22705377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f226b25862554006e56e97824faf9ba02bccdf2ecc2fdd30bb5b7f4619213354`  
		Last Modified: Fri, 24 Apr 2020 11:13:40 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0536d00b13e2f95b0ce7abb5b67c563d0ff2829359ecfa094f0fda731c40da1e`  
		Last Modified: Fri, 24 Apr 2020 11:13:57 GMT  
		Size: 59.5 MB (59501349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe33b7ba1f364ebeff5d799606435019145f125dd9f627718c2526f5c08726b0`  
		Last Modified: Fri, 24 Apr 2020 11:13:39 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76258f6fd90141f5fb1571afa09d1b4435b698ad5279b20d7be8dffdd611a6e`  
		Last Modified: Thu, 07 May 2020 00:35:50 GMT  
		Size: 12.6 MB (12603542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75097d9ef7be002ca06f311f9ec0f43a731fb984feadbaf36889200ed0acb4d6`  
		Last Modified: Thu, 07 May 2020 00:35:48 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac2fac71a4af14c671b6408d09d949742d4edf11ca4a99b222e334d33c95c6c`  
		Last Modified: Thu, 07 May 2020 00:35:55 GMT  
		Size: 26.1 MB (26117395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fff6e06b7f5003b731cd9f1cb6a54b87eefef316a8533bde54829f0ad4fc7fa`  
		Last Modified: Thu, 07 May 2020 00:35:46 GMT  
		Size: 2.2 KB (2223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baaa1b50232b8ef9626c74fd3f410018adc8507346beff883a599e0d784ad1fd`  
		Last Modified: Thu, 07 May 2020 00:35:46 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:825f5aca6bd4f70c1ad94e46ec81afa6bb1312887195da5463c0e18daf8310a5`  
		Last Modified: Thu, 07 May 2020 00:35:46 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b1a9765c82ec5087bf4b73fcc65b7995f17d6ce84ec4e535ad5d17949bb2c5`  
		Last Modified: Thu, 07 May 2020 00:35:46 GMT  
		Size: 7.8 KB (7787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:618c448e84b8227760d45ccea99b2f533bb47c546ef5a8fb5b26e774cedd0b71`  
		Last Modified: Thu, 07 May 2020 01:35:58 GMT  
		Size: 3.2 MB (3228412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7392a870804e91bad9b042a84e3c5cfb69d325d23b10eea00e7cbb3b6575fcef`  
		Last Modified: Thu, 07 May 2020 01:36:01 GMT  
		Size: 9.7 MB (9653669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7bbd3b94b7036133ab536c917ef57d46e4b48faf91d377408c850ab9bb0d5e0`  
		Last Modified: Thu, 07 May 2020 01:35:56 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7342f042a43768eb09c7de060aa8759d7441b7523804739bfbc6cdbb7cebc74b`  
		Last Modified: Thu, 07 May 2020 01:35:56 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:3-php7.2-fpm` - linux; arm64 variant v8

```console
$ docker pull joomla@sha256:a6475109d43b7630d8a4b08f2d469b24a6c5c5c04f91dfe1db6ab11fd72042ab
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (149960163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f792e6db128740f004cd936bbf66ec52d682dcf146b86f5e34fa4da792c11522`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 23 Apr 2020 00:54:55 GMT
ADD file:581ee9c3c19f0d971aeda008fd399f59171cae75e8936b967dbf3888db4fc0d0 in / 
# Thu, 23 Apr 2020 00:54:58 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 16:09:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Apr 2020 16:09:21 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Apr 2020 16:10:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 16:10:05 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Apr 2020 16:10:08 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 23 Apr 2020 16:22:42 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 23 Apr 2020 16:22:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Apr 2020 16:22:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Apr 2020 16:22:45 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Apr 2020 17:23:41 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 23 Apr 2020 17:23:42 GMT
ENV PHP_VERSION=7.2.30
# Thu, 23 Apr 2020 17:23:44 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.30.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.30.tar.xz.asc/from/this/mirror
# Thu, 23 Apr 2020 17:23:44 GMT
ENV PHP_SHA256=aa93df27b58a45d6c9800ac813245dfdca03490a918ebe515b3a70189b1bf8c3 PHP_MD5=
# Thu, 23 Apr 2020 17:23:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Apr 2020 17:24:00 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Apr 2020 17:27:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Apr 2020 17:27:35 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 23 Apr 2020 17:27:38 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Apr 2020 17:27:40 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 23 Apr 2020 17:27:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Apr 2020 17:27:42 GMT
WORKDIR /var/www/html
# Thu, 23 Apr 2020 17:27:44 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 23 Apr 2020 17:27:45 GMT
STOPSIGNAL SIGQUIT
# Thu, 23 Apr 2020 17:27:46 GMT
EXPOSE 9000
# Thu, 23 Apr 2020 17:27:47 GMT
CMD ["php-fpm"]
# Fri, 24 Apr 2020 01:39:11 GMT
LABEL maintainer=Michael Babker <michael.babker@joomla.org> (@mbabker)
# Fri, 24 Apr 2020 01:39:12 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Fri, 24 Apr 2020 01:41:44 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 	; 		docker-php-ext-configure gd --with-jpeg-dir=/usr --with-png-dir=/usr; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.18; 	pecl install memcached-3.1.5; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 24 Apr 2020 01:41:44 GMT
VOLUME [/var/www/html]
# Fri, 24 Apr 2020 01:41:46 GMT
ENV JOOMLA_VERSION=3.9.16
# Fri, 24 Apr 2020 01:41:47 GMT
ENV JOOMLA_SHA512=3266ff375631fd0c4c45c66368f3d07cdc1b41010ffad907a957e6c1acb511847bf2c112e0991792f84455b48bea95c84eca9a7325baa3cab61078fda697ed0f
# Fri, 24 Apr 2020 01:41:57 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Fri, 24 Apr 2020 01:41:59 GMT
COPY file:fcc18c5b9c2d514cfb965bab84e10b4f924a39a5f202055df75d7990da099d8f in /entrypoint.sh 
# Fri, 24 Apr 2020 01:42:00 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Fri, 24 Apr 2020 01:42:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 24 Apr 2020 01:42:02 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:bdc84a41f2513e28e99efeff9fcbb196b7df9883fb30532184bd67ca415b4673`  
		Last Modified: Thu, 23 Apr 2020 01:03:27 GMT  
		Size: 25.9 MB (25857800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f00aeccd126509e0b42d6cba92126cce7c342206083cc40a285bd447cf1f2d46`  
		Last Modified: Thu, 23 Apr 2020 17:51:33 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103463f158e3c7f91314c099c5524db53fd97efd35b7502a2991750063630384`  
		Last Modified: Thu, 23 Apr 2020 17:51:55 GMT  
		Size: 70.3 MB (70334752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12c968fd52774e9a63a8ca1cd66b708fb02df8fdc207dc98e23a8682010b0047`  
		Last Modified: Thu, 23 Apr 2020 17:51:33 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0eff54424bf898ddb089339048c6460d28bbb12d478d9b94a82d8a69fa7418e`  
		Last Modified: Thu, 23 Apr 2020 17:57:43 GMT  
		Size: 12.6 MB (12604318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76ef67f6b44195ecc92f4068ace21ae4a39bf7043c0ba76076846840eab5ef5`  
		Last Modified: Thu, 23 Apr 2020 17:57:41 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe3652c042b995e216d5fe83e8b5d4f69b6ca47f2ef1cb75cc5c6ef0b6276f5`  
		Last Modified: Thu, 23 Apr 2020 17:57:47 GMT  
		Size: 28.2 MB (28205719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af04da97e715665b35fef22093fa1e649052a7063e7f4317d17d4a00c4baab96`  
		Last Modified: Thu, 23 Apr 2020 17:57:39 GMT  
		Size: 2.2 KB (2226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0ccf76331567bf56c7aa8081cefcf49b7ebc82414b2a3a337ac66486567312`  
		Last Modified: Thu, 23 Apr 2020 17:57:39 GMT  
		Size: 251.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b3e56dbddd194a5813f9db899663ca383fabd96332787f3ae1e2ec3b5c76a1`  
		Last Modified: Thu, 23 Apr 2020 17:57:40 GMT  
		Size: 215.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff373ba870252f8ea0a275ae338a41dda3b8f186945af5aafd953e3b2f252a3`  
		Last Modified: Thu, 23 Apr 2020 17:57:39 GMT  
		Size: 7.8 KB (7790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee5958a396f5e8e4adff0302c511637a7adfa3ed78ba660a6975d45c6e7b67e`  
		Last Modified: Fri, 24 Apr 2020 01:56:48 GMT  
		Size: 3.3 MB (3290636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec985be8a90f49d007ebf34fd9215f54bcc5320b52f0c4123e26ab1462958f22`  
		Last Modified: Fri, 24 Apr 2020 01:56:52 GMT  
		Size: 9.7 MB (9653677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d28e178261f9665e112b026eb62905476ea27e914368ff8f2ffcba7e9c220aa`  
		Last Modified: Fri, 24 Apr 2020 01:56:46 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eba31bc02fceb7efc1c4ef11643aa969d120718565901ef4081bc8c5fe2fc56`  
		Last Modified: Fri, 24 Apr 2020 01:56:46 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:3-php7.2-fpm` - linux; 386

```console
$ docker pull joomla@sha256:dcea03b3fd198771d66d6f2d20fdf17eefda1bc78ecc51a04feff7adbdb48164
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.6 MB (163621137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c95178db52b9c26af47c6a9f66cc1b9dfc2ac8b16792ad72be8f4c07783bf05`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 23 Apr 2020 00:39:36 GMT
ADD file:ca6a74f6b738c738c033152fab2a9aacf22bec5f19a994e6a02b5f919ee33ee9 in / 
# Thu, 23 Apr 2020 00:39:36 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 11:58:12 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Apr 2020 11:58:12 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Apr 2020 11:58:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 11:58:40 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Apr 2020 11:58:41 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 23 Apr 2020 12:12:09 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 23 Apr 2020 12:12:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Apr 2020 12:12:09 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Apr 2020 12:12:09 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Apr 2020 13:33:47 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 23 Apr 2020 13:33:47 GMT
ENV PHP_VERSION=7.2.30
# Thu, 23 Apr 2020 13:33:47 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.30.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.30.tar.xz.asc/from/this/mirror
# Thu, 23 Apr 2020 13:33:47 GMT
ENV PHP_SHA256=aa93df27b58a45d6c9800ac813245dfdca03490a918ebe515b3a70189b1bf8c3 PHP_MD5=
# Thu, 23 Apr 2020 13:33:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Apr 2020 13:33:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Apr 2020 13:40:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Apr 2020 13:40:01 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 23 Apr 2020 13:40:02 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Apr 2020 13:40:03 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 23 Apr 2020 13:40:03 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Apr 2020 13:40:03 GMT
WORKDIR /var/www/html
# Thu, 23 Apr 2020 13:40:04 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 23 Apr 2020 13:40:04 GMT
STOPSIGNAL SIGQUIT
# Thu, 23 Apr 2020 13:40:05 GMT
EXPOSE 9000
# Thu, 23 Apr 2020 13:40:05 GMT
CMD ["php-fpm"]
# Thu, 23 Apr 2020 19:17:36 GMT
LABEL maintainer=Michael Babker <michael.babker@joomla.org> (@mbabker)
# Thu, 23 Apr 2020 19:17:36 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Thu, 23 Apr 2020 19:19:41 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 	; 		docker-php-ext-configure gd --with-jpeg-dir=/usr --with-png-dir=/usr; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.18; 	pecl install memcached-3.1.5; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 19:19:41 GMT
VOLUME [/var/www/html]
# Thu, 23 Apr 2020 19:19:42 GMT
ENV JOOMLA_VERSION=3.9.16
# Thu, 23 Apr 2020 19:19:42 GMT
ENV JOOMLA_SHA512=3266ff375631fd0c4c45c66368f3d07cdc1b41010ffad907a957e6c1acb511847bf2c112e0991792f84455b48bea95c84eca9a7325baa3cab61078fda697ed0f
# Thu, 23 Apr 2020 19:19:53 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Thu, 23 Apr 2020 19:19:54 GMT
COPY file:fcc18c5b9c2d514cfb965bab84e10b4f924a39a5f202055df75d7990da099d8f in /entrypoint.sh 
# Thu, 23 Apr 2020 19:19:55 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Thu, 23 Apr 2020 19:19:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 19:19:55 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:5d3da8f33b97fc107a05b3255a55836b76df9f817de632b1fb63c6e9c024f0df`  
		Last Modified: Thu, 23 Apr 2020 00:44:35 GMT  
		Size: 27.8 MB (27753972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b6f6109ad6afc6066a9a9b19c9903065b90dc4ecb232ad312a50d2a3af7c20`  
		Last Modified: Thu, 23 Apr 2020 14:14:03 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79b8d4220a9dc78cfb17d7518deddaa4957545b12088485de215374ec8cd5fcd`  
		Last Modified: Thu, 23 Apr 2020 14:14:26 GMT  
		Size: 81.2 MB (81198126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd893e354bac0fa6072eb200ef4c28c499dce07f2bf148816b9b04550dc27082`  
		Last Modified: Thu, 23 Apr 2020 14:14:02 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a460c63d2bb99d3f2eef1df9f7660e38305a72451c0eae4d8d5c5bbda71f0c`  
		Last Modified: Thu, 23 Apr 2020 14:18:56 GMT  
		Size: 12.6 MB (12604717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f700683cfd30aa7d19204ab13c8f568ca16cbbc130b83f09776014479aded0`  
		Last Modified: Thu, 23 Apr 2020 14:18:54 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae010b6bae54a8d6dc3da0eea74eba96f64783a72bb0e12c3133b19f8c7e6c24`  
		Last Modified: Thu, 23 Apr 2020 14:19:02 GMT  
		Size: 29.1 MB (29083439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:043de43ec3132fe388e3e04e60784ef454166fc360cdd5b38c6c43c7a55a5f2c`  
		Last Modified: Thu, 23 Apr 2020 14:18:53 GMT  
		Size: 2.2 KB (2222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0d03c82a8e915ab470fa1083214848d5c57547da6203d9a79e759e90c8e18e`  
		Last Modified: Thu, 23 Apr 2020 14:18:54 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58989ae2cd9d59e8b3a9c71551874e2a58811d2cdee42fdc25e900e38487b4d5`  
		Last Modified: Thu, 23 Apr 2020 14:18:53 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66779da8379e9ca7a50f2a82030224f0818a0fba2406c86b615a852b9d8c58c3`  
		Last Modified: Thu, 23 Apr 2020 14:18:53 GMT  
		Size: 7.8 KB (7785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55a851d1580ffe6604dc8a974b1a8e2c3d4f2940cdf833d802d0c5a44d81bb9`  
		Last Modified: Thu, 23 Apr 2020 19:31:42 GMT  
		Size: 3.3 MB (3314191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:932682fe66d60ebb381718f300c9eef18a953f6f405a57d1610ea0357b8adeef`  
		Last Modified: Thu, 23 Apr 2020 19:31:46 GMT  
		Size: 9.7 MB (9653487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d960123c8a349cb67545853cfc02a95e580b09b5684d55cdd29c97f365160076`  
		Last Modified: Thu, 23 Apr 2020 19:31:40 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3689605590b92f161ab550558f631e3eda92c9fb010482b72e1178ab75e2dc93`  
		Last Modified: Thu, 23 Apr 2020 19:31:40 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:3-php7.2-fpm` - linux; ppc64le

```console
$ docker pull joomla@sha256:d7c0641ec794174852bef6d7de6ae72800f1779e487b7ffd1b98b7af753bc354
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.8 MB (168786385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e12fe87cf72b433979603f6f7048933c5b1c2d92275828fc5cc1654a8d6c0a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 23 Apr 2020 00:36:00 GMT
ADD file:5b3c3d2945800e1743dc02a4f68bd830fe2f67ca437223692eb460147c158c2b in / 
# Thu, 23 Apr 2020 00:36:04 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 14:58:48 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Apr 2020 14:58:51 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Apr 2020 15:00:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 15:01:04 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Apr 2020 15:01:13 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 23 Apr 2020 15:15:05 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 23 Apr 2020 15:15:08 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Apr 2020 15:15:11 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Apr 2020 15:15:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Apr 2020 16:37:42 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 23 Apr 2020 16:37:45 GMT
ENV PHP_VERSION=7.2.30
# Thu, 23 Apr 2020 16:37:48 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.30.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.30.tar.xz.asc/from/this/mirror
# Thu, 23 Apr 2020 16:37:53 GMT
ENV PHP_SHA256=aa93df27b58a45d6c9800ac813245dfdca03490a918ebe515b3a70189b1bf8c3 PHP_MD5=
# Thu, 23 Apr 2020 16:38:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Apr 2020 16:38:51 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Apr 2020 16:42:54 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Apr 2020 16:42:57 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 23 Apr 2020 16:43:02 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Apr 2020 16:43:08 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 23 Apr 2020 16:43:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Apr 2020 16:43:14 GMT
WORKDIR /var/www/html
# Thu, 23 Apr 2020 16:43:22 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 23 Apr 2020 16:43:24 GMT
STOPSIGNAL SIGQUIT
# Thu, 23 Apr 2020 16:43:27 GMT
EXPOSE 9000
# Thu, 23 Apr 2020 16:43:29 GMT
CMD ["php-fpm"]
# Thu, 23 Apr 2020 23:18:10 GMT
LABEL maintainer=Michael Babker <michael.babker@joomla.org> (@mbabker)
# Thu, 23 Apr 2020 23:18:12 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Thu, 23 Apr 2020 23:20:34 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 	; 		docker-php-ext-configure gd --with-jpeg-dir=/usr --with-png-dir=/usr; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.18; 	pecl install memcached-3.1.5; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 23:20:38 GMT
VOLUME [/var/www/html]
# Thu, 23 Apr 2020 23:20:42 GMT
ENV JOOMLA_VERSION=3.9.16
# Thu, 23 Apr 2020 23:20:47 GMT
ENV JOOMLA_SHA512=3266ff375631fd0c4c45c66368f3d07cdc1b41010ffad907a957e6c1acb511847bf2c112e0991792f84455b48bea95c84eca9a7325baa3cab61078fda697ed0f
# Thu, 23 Apr 2020 23:21:03 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Thu, 23 Apr 2020 23:21:05 GMT
COPY file:fcc18c5b9c2d514cfb965bab84e10b4f924a39a5f202055df75d7990da099d8f in /entrypoint.sh 
# Thu, 23 Apr 2020 23:21:06 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Thu, 23 Apr 2020 23:21:09 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 23:21:12 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:012c6cdbd1af202bbfbea5945fafbb9aca9097f1fa3cb493a29155fdc02cc43c`  
		Last Modified: Thu, 23 Apr 2020 00:50:14 GMT  
		Size: 30.5 MB (30524638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b755a3bf05f4bf7425e586a874481ea765f886765d68e5e3973f9ac727187c6c`  
		Last Modified: Thu, 23 Apr 2020 17:16:22 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81edbd0a9383cf9bc58dcb07cb9b0cc6454030497e3a606ae400db6a3b6a1962`  
		Last Modified: Thu, 23 Apr 2020 17:17:15 GMT  
		Size: 82.3 MB (82259619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947531f183613e1f7fca563adeccbc3242cda14370ed376901fbf634af0264c3`  
		Last Modified: Thu, 23 Apr 2020 17:16:20 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4307ae64bd660f149c34bf83e934255657df59ecb9290be0ec8ecb557653e974`  
		Last Modified: Thu, 23 Apr 2020 17:26:22 GMT  
		Size: 12.6 MB (12605218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd920be099fc052931e0d070b6e5959bf55447f681445ce4ff5e991fdd89ffc`  
		Last Modified: Thu, 23 Apr 2020 17:26:19 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2687b49311625bf05b6c62000505f078fa7f0f136fd14453cd5a178329ded67a`  
		Last Modified: Thu, 23 Apr 2020 17:26:28 GMT  
		Size: 30.2 MB (30215860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40b224b584f0f2daec7c4f77e96eabfc5c523e5b5f8a284e6e5587a70abd417b`  
		Last Modified: Thu, 23 Apr 2020 17:26:15 GMT  
		Size: 2.2 KB (2224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc5dbce85c4be0f14dca684aff6d1fb07833cec9eb435c91064d376016b6f8f7`  
		Last Modified: Thu, 23 Apr 2020 17:26:15 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001066ab777dd273b61f18efdbe823a355f7c05871e00de42925bb851e70c8d5`  
		Last Modified: Thu, 23 Apr 2020 17:26:15 GMT  
		Size: 215.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451e2736214066f91beb2ecbd9f743c26e096c06332939985c5d8e751716b131`  
		Last Modified: Thu, 23 Apr 2020 17:26:16 GMT  
		Size: 7.8 KB (7787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae8b8583b65a0a2664fd123fedd96346a7602c714ce86f11edb7ad2675424532`  
		Last Modified: Thu, 23 Apr 2020 23:36:29 GMT  
		Size: 3.5 MB (3514125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e04dca0d58d4401d5be3c2328a094ccbaa151b28a9da8cb794774e084f85ea62`  
		Last Modified: Thu, 23 Apr 2020 23:36:45 GMT  
		Size: 9.7 MB (9653670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cab0c90a0757260e2bb3f2290684b7292e25a3fe892f6dc8e184d93fb825cbb`  
		Last Modified: Thu, 23 Apr 2020 23:36:26 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85b4fe73bd59a8aea4faab4a98938ca7c12110970cabd96cb147d74e2dd7aa3`  
		Last Modified: Thu, 23 Apr 2020 23:36:26 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `joomla:3-php7.2-fpm` - linux; s390x

```console
$ docker pull joomla@sha256:9a4215ecfcc50f97423faa066268841d46a266bd6d44bb14c4c479a90ea78a05
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.7 MB (143686029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f1c77928af1d79adc06a2b826928f7b4a92cba315fa1862da9d2411d82ff1b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 23 Apr 2020 00:51:48 GMT
ADD file:f6c2560f9185c1bcaff95e576e57449f606d51b85fad02646c1b0962bc9353c9 in / 
# Thu, 23 Apr 2020 00:51:50 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 07:06:58 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 23 Apr 2020 07:06:59 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 23 Apr 2020 07:07:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 07:07:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 23 Apr 2020 07:07:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 23 Apr 2020 07:12:25 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 23 Apr 2020 07:12:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Apr 2020 07:12:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 23 Apr 2020 07:12:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 23 Apr 2020 07:47:09 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 23 Apr 2020 07:47:09 GMT
ENV PHP_VERSION=7.2.30
# Thu, 23 Apr 2020 07:47:10 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.30.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.30.tar.xz.asc/from/this/mirror
# Thu, 23 Apr 2020 07:47:10 GMT
ENV PHP_SHA256=aa93df27b58a45d6c9800ac813245dfdca03490a918ebe515b3a70189b1bf8c3 PHP_MD5=
# Thu, 23 Apr 2020 07:47:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 23 Apr 2020 07:47:18 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 23 Apr 2020 07:50:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 23 Apr 2020 07:50:37 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 23 Apr 2020 07:50:38 GMT
RUN docker-php-ext-enable sodium
# Thu, 23 Apr 2020 07:50:39 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 23 Apr 2020 07:50:39 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 23 Apr 2020 07:50:39 GMT
WORKDIR /var/www/html
# Thu, 23 Apr 2020 07:50:40 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 23 Apr 2020 07:50:40 GMT
STOPSIGNAL SIGQUIT
# Thu, 23 Apr 2020 07:50:40 GMT
EXPOSE 9000
# Thu, 23 Apr 2020 07:50:41 GMT
CMD ["php-fpm"]
# Thu, 23 Apr 2020 15:29:55 GMT
LABEL maintainer=Michael Babker <michael.babker@joomla.org> (@mbabker)
# Thu, 23 Apr 2020 15:29:56 GMT
ENV JOOMLA_INSTALLATION_DISABLE_LOCALHOST_CHECK=1
# Thu, 23 Apr 2020 15:32:08 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libbz2-dev 		libjpeg-dev 		libldap2-dev 		libmemcached-dev 		libpng-dev 		libpq-dev 	; 		docker-php-ext-configure gd --with-jpeg-dir=/usr --with-png-dir=/usr; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	docker-php-ext-configure ldap --with-libdir="lib/$debMultiarch"; 	docker-php-ext-install -j "$(nproc)" 		bz2 		gd 		ldap 		mysqli 		pdo_mysql 		pdo_pgsql 		pgsql 		zip 	; 		pecl install APCu-5.1.18; 	pecl install memcached-3.1.5; 	pecl install redis-4.3.0; 		docker-php-ext-enable 		apcu 		memcached 		redis 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 15:32:08 GMT
VOLUME [/var/www/html]
# Thu, 23 Apr 2020 15:32:08 GMT
ENV JOOMLA_VERSION=3.9.16
# Thu, 23 Apr 2020 15:32:09 GMT
ENV JOOMLA_SHA512=3266ff375631fd0c4c45c66368f3d07cdc1b41010ffad907a957e6c1acb511847bf2c112e0991792f84455b48bea95c84eca9a7325baa3cab61078fda697ed0f
# Thu, 23 Apr 2020 15:32:23 GMT
RUN set -ex; 	curl -o joomla.tar.bz2 -SL https://github.com/joomla/joomla-cms/releases/download/${JOOMLA_VERSION}/Joomla_${JOOMLA_VERSION}-Stable-Full_Package.tar.bz2; 	echo "$JOOMLA_SHA512 *joomla.tar.bz2" | sha512sum -c -; 	mkdir /usr/src/joomla; 	tar -xf joomla.tar.bz2 -C /usr/src/joomla; 	rm joomla.tar.bz2; 	chown -R www-data:www-data /usr/src/joomla
# Thu, 23 Apr 2020 15:32:27 GMT
COPY file:fcc18c5b9c2d514cfb965bab84e10b4f924a39a5f202055df75d7990da099d8f in /entrypoint.sh 
# Thu, 23 Apr 2020 15:32:28 GMT
COPY file:5a85d779aaae74cfa3ab6228df0f24236d4d5ad9097e2a1b277e3daea0d6d3dc in /makedb.php 
# Thu, 23 Apr 2020 15:32:28 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Apr 2020 15:32:29 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:d89dc3741ad42b79c3d8545495c429f3100d3f22234ff993bd04017b0675e868`  
		Last Modified: Thu, 23 Apr 2020 00:56:00 GMT  
		Size: 25.7 MB (25712105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea08bde6b0b1d4817b549715812249f566ebbdb1c81c26581d3a34e9f0646ac7`  
		Last Modified: Thu, 23 Apr 2020 08:06:47 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb184ae545a538a5e99fa27bf76f21aeb7324f061ae0e6ed7ab6003f8ec8d861`  
		Last Modified: Thu, 23 Apr 2020 08:06:57 GMT  
		Size: 64.7 MB (64698982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3bff96336b89f3c42d3c1ca154c9bee84597dd2e1776952a82e47e94dac6e5c`  
		Last Modified: Thu, 23 Apr 2020 08:06:45 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32d691ea859928fa750d34a76c5176d8b867db8381bdb5472ca7643607c5b96`  
		Last Modified: Thu, 23 Apr 2020 08:12:20 GMT  
		Size: 12.6 MB (12603735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea0a87351b2de7c8fa52ab7806ff14276de7e833d6814dda918a65731d78691`  
		Last Modified: Thu, 23 Apr 2020 08:12:16 GMT  
		Size: 494.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afbc05337fb310c51db393fb0837d2c9d31df35b8a7b6653086c1bf5f2500c9`  
		Last Modified: Thu, 23 Apr 2020 08:12:18 GMT  
		Size: 27.7 MB (27702866 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ffacc33e78a27bbf04009082236c403dec3cad3a77bca98a027da0e8e56fee4`  
		Last Modified: Thu, 23 Apr 2020 08:12:19 GMT  
		Size: 2.2 KB (2220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413fd48591d2a0205a9781b89fb395febcb7bd8a0b0c28adb8de75fac3d338a0`  
		Last Modified: Thu, 23 Apr 2020 08:12:19 GMT  
		Size: 250.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33cd5987650805e029ef0b8e0aa1085105bd654975023be5e7499342bb0400f7`  
		Last Modified: Thu, 23 Apr 2020 08:12:14 GMT  
		Size: 212.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7774bfa9e69eb19e5a6040bc474f6e59dc0eb28688b730b5afb0f2cae4879385`  
		Last Modified: Thu, 23 Apr 2020 08:12:19 GMT  
		Size: 7.8 KB (7788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8917c436a902a5d5b94a69d260e92e9c475ba0696e04eca3137ac65dfcd72a`  
		Last Modified: Thu, 23 Apr 2020 15:41:29 GMT  
		Size: 3.3 MB (3301429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9db6a4d93404296ad2213b94a75d3e0bbd561854178cf288255943090ab9fd`  
		Last Modified: Thu, 23 Apr 2020 15:41:31 GMT  
		Size: 9.7 MB (9653670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3830ed70172acd9086600aebc39afef1f11f61231073e94f32c4b052c0c840f`  
		Last Modified: Thu, 23 Apr 2020 15:41:35 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f7e9d282de0127531cce68e76a1b2e6bf1789a37db32808e1b98e7af0852aee`  
		Last Modified: Thu, 23 Apr 2020 15:41:29 GMT  
		Size: 613.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
