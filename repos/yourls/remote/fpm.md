## `yourls:fpm`

```console
$ docker pull yourls@sha256:b40a93df0ec65f6f2aea47136a1f695f07342faae752da95d579f03a90569fc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `yourls:fpm` - linux; amd64

```console
$ docker pull yourls@sha256:df0a3f6a9b96e9f11e0a14fb789e42877800cadc033ad45920006cbe73a86818
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147713944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d42dcb960bbba59660d324b6dd4145d57eaf5e35f643480054a0208c6f07003`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 31 Mar 2020 01:21:01 GMT
ADD file:d1f1b387a158136fb0f8096c8a8ecf5fc146be4e85c1c3c345d44c927692723a in / 
# Tue, 31 Mar 2020 01:21:01 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 18:09:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 31 Mar 2020 18:09:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 31 Mar 2020 18:10:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 18:10:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 31 Mar 2020 18:10:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 31 Mar 2020 18:21:45 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Tue, 31 Mar 2020 18:21:46 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 31 Mar 2020 18:21:46 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 31 Mar 2020 18:21:46 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Tue, 31 Mar 2020 19:38:41 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Tue, 31 Mar 2020 19:38:41 GMT
ENV PHP_VERSION=7.2.29
# Tue, 31 Mar 2020 19:38:42 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.29.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.29.tar.xz.asc/from/this/mirror
# Tue, 31 Mar 2020 19:38:42 GMT
ENV PHP_SHA256=b117de74136bf4b439d663be9cf0c8e06a260c1f340f6b75ccadb609153a7fe8 PHP_MD5=
# Tue, 31 Mar 2020 19:38:51 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 31 Mar 2020 19:38:51 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 31 Mar 2020 19:44:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 31 Mar 2020 19:44:44 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Tue, 31 Mar 2020 19:44:46 GMT
RUN docker-php-ext-enable sodium
# Tue, 31 Mar 2020 19:44:46 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Tue, 31 Mar 2020 19:44:47 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 31 Mar 2020 19:44:47 GMT
WORKDIR /var/www/html
# Tue, 31 Mar 2020 19:44:48 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 31 Mar 2020 19:44:48 GMT
STOPSIGNAL SIGQUIT
# Tue, 31 Mar 2020 19:44:48 GMT
EXPOSE 9000
# Tue, 31 Mar 2020 19:44:48 GMT
CMD ["php-fpm"]
# Wed, 01 Apr 2020 05:30:13 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Wed, 01 Apr 2020 05:30:14 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Wed, 01 Apr 2020 05:30:14 GMT
ENV YOURLS_VERSION=1.7.6
# Wed, 01 Apr 2020 05:30:14 GMT
ENV YOURLS_SHA256=f3623af6e4cabee61a39d3deca3c941717c5e0a60bc288b6f3a668f87a20ae2e
# Wed, 01 Apr 2020 05:30:15 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Wed, 01 Apr 2020 05:30:16 GMT
COPY file:faa5e93643253a8f7b19a0098e9286cc1914eaa7154c418de43e161d69f2f157 in /usr/local/bin/ 
# Wed, 01 Apr 2020 05:30:16 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Wed, 01 Apr 2020 05:30:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Apr 2020 05:30:16 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:c499e6d256d6d4a546f1c141e04b5b4951983ba7581e39deaf5cc595289ee70f`  
		Last Modified: Tue, 31 Mar 2020 01:26:37 GMT  
		Size: 27.1 MB (27091862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a635b94b3b9b333c4d1cd96e98335cf3da4cb038b56cd018d94742ef70aa725`  
		Last Modified: Tue, 31 Mar 2020 20:16:26 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf28be682a33b9533ee39fe019dd86455927b1717cec97319ee97496a0b74521`  
		Last Modified: Tue, 31 Mar 2020 20:16:45 GMT  
		Size: 76.7 MB (76651640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7118ab6e5511a8508001b21372cd6b33c9f8a8ecc1dea2db7a7fd62585f9f5d`  
		Last Modified: Tue, 31 Mar 2020 20:16:26 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56e849a5b7510f7b17f5d3bc37e8d992deba8d75822019f8c6e9348d8ce3860`  
		Last Modified: Tue, 31 Mar 2020 20:20:14 GMT  
		Size: 12.6 MB (12630654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57369e18745e05551d2a629ade9d7cd60a483394c3527837c6545e468f31aad`  
		Last Modified: Tue, 31 Mar 2020 20:20:13 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642471d497bcacc8616e85d5f2c840e27ffd6490d07a3096be3a0727002385c`  
		Last Modified: Tue, 31 Mar 2020 20:20:18 GMT  
		Size: 28.5 MB (28548132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1541bb8d491421b769aab167970abdef5b639d6c871f9d2a037bc12c42f2ea7`  
		Last Modified: Tue, 31 Mar 2020 20:20:11 GMT  
		Size: 2.2 KB (2221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4bbcc1e202f84244c311f5a4c201740f908443e4fdc14f495df58f9b7ef45c6`  
		Last Modified: Tue, 31 Mar 2020 20:20:12 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6797562b754ea226e1eb1826d0f9401dddb2ec3d82fd4beb45c12102307cd262`  
		Last Modified: Tue, 31 Mar 2020 20:20:12 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d50cd94b1242bc574608bc843cb4fa2c1c33a2d0a0119a62d6bc1d4e77f0dbc`  
		Last Modified: Tue, 31 Mar 2020 20:20:12 GMT  
		Size: 7.8 KB (7785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a403ae23a035709ebc3be891d280bddcda1d7699e60ccf25de5743ab6ace08e`  
		Last Modified: Wed, 01 Apr 2020 05:30:43 GMT  
		Size: 291.7 KB (291673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3adbaecd955164593c1de58e286a9681127dd63726ce251d45412ac52faf8f0`  
		Last Modified: Wed, 01 Apr 2020 05:30:43 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2d7a27abe16be66b76618b249bcbcf26aac926678c46d20db81a8d195dc346c`  
		Last Modified: Wed, 01 Apr 2020 05:30:43 GMT  
		Size: 2.5 MB (2485193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b45804736d3832c3dbd216800d0eb35af349162d2c8712daacffe83a3d09902`  
		Last Modified: Wed, 01 Apr 2020 05:30:43 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ca89092fb24337bb2c2a58aa653f25b2dba887cd879f542b2b1569fd6a1d7b`  
		Last Modified: Wed, 01 Apr 2020 05:30:43 GMT  
		Size: 1.9 KB (1861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm` - linux; arm variant v5

```console
$ docker pull yourls@sha256:74890768882c039d295e30edd29ed3a1486e991b252fad6b3056437343ca6cdc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.2 MB (126202513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63dede40d95d751e87ee9fe520e299cd2bb46a1e93635bbaccd5ea33863e7be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Apr 2020 00:50:14 GMT
ADD file:761a556ec2a7d8c742c860e429c9b9ba3f7abfcd9383c6b3767499de6dcad4bc in / 
# Thu, 16 Apr 2020 00:50:15 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 01:40:24 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 16 Apr 2020 01:40:25 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 16 Apr 2020 01:41:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 01:41:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Apr 2020 01:41:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 16 Apr 2020 01:50:04 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 16 Apr 2020 01:50:05 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2020 01:50:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2020 01:50:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 16 Apr 2020 02:47:33 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 16 Apr 2020 02:47:33 GMT
ENV PHP_VERSION=7.2.29
# Thu, 16 Apr 2020 02:47:34 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.29.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.29.tar.xz.asc/from/this/mirror
# Thu, 16 Apr 2020 02:47:35 GMT
ENV PHP_SHA256=b117de74136bf4b439d663be9cf0c8e06a260c1f340f6b75ccadb609153a7fe8 PHP_MD5=
# Thu, 16 Apr 2020 02:47:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 16 Apr 2020 02:47:56 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 16 Apr 2020 02:51:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 16 Apr 2020 02:51:30 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 16 Apr 2020 02:51:33 GMT
RUN docker-php-ext-enable sodium
# Thu, 16 Apr 2020 02:51:36 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 16 Apr 2020 02:51:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 16 Apr 2020 02:51:40 GMT
WORKDIR /var/www/html
# Thu, 16 Apr 2020 02:51:42 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 16 Apr 2020 02:51:43 GMT
STOPSIGNAL SIGQUIT
# Thu, 16 Apr 2020 02:51:44 GMT
EXPOSE 9000
# Thu, 16 Apr 2020 02:51:44 GMT
CMD ["php-fpm"]
# Thu, 16 Apr 2020 10:49:10 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Thu, 16 Apr 2020 10:49:13 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 16 Apr 2020 10:49:14 GMT
ENV YOURLS_VERSION=1.7.6
# Thu, 16 Apr 2020 10:49:15 GMT
ENV YOURLS_SHA256=f3623af6e4cabee61a39d3deca3c941717c5e0a60bc288b6f3a668f87a20ae2e
# Thu, 16 Apr 2020 10:49:19 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Thu, 16 Apr 2020 10:49:20 GMT
COPY file:faa5e93643253a8f7b19a0098e9286cc1914eaa7154c418de43e161d69f2f157 in /usr/local/bin/ 
# Thu, 16 Apr 2020 10:49:21 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Thu, 16 Apr 2020 10:49:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Apr 2020 10:49:23 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:600369660a591bc9594fcf333a847fe997901785f7032d3ad2822b2812c13243`  
		Last Modified: Thu, 16 Apr 2020 00:58:26 GMT  
		Size: 24.8 MB (24836437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29865f2ca7e0e64c2dbc473422a7c9d444c1daad98f5ea1299ffdafdb253129`  
		Last Modified: Thu, 16 Apr 2020 03:14:54 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882e0065c973f6fdd11e90263bb281211d3321ceeef62f847ea256bdd6e99157`  
		Last Modified: Thu, 16 Apr 2020 03:15:14 GMT  
		Size: 58.8 MB (58799657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9576faf9c360672436dad4e93a54af59e3ceb35034f5d18a0c1a6854c672b93`  
		Last Modified: Thu, 16 Apr 2020 03:14:53 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac694c977de96429d999d9b23568c4cd49a2ef52d3e145806a387fe39a6b246`  
		Last Modified: Thu, 16 Apr 2020 03:20:02 GMT  
		Size: 12.6 MB (12628774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f0676f2a2a631587299a75b7bd0ebd3c391ebfa258691f82fc9a989ba3b69f1`  
		Last Modified: Thu, 16 Apr 2020 03:20:00 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a01c97a2893a8b0a6a7b5d4d71d5f8ce8e2b9a9d263ccbdcb6ebf762af440ca`  
		Last Modified: Thu, 16 Apr 2020 03:20:09 GMT  
		Size: 27.2 MB (27162610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76c2b0be0677dcf5428652966deb493b02a995ce21d6a77a4ac5b118a8409b32`  
		Last Modified: Thu, 16 Apr 2020 03:19:59 GMT  
		Size: 2.2 KB (2220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f55eedb2eae2e1d626a296d835409b1716abd5d5e93982b10641b3ba8e95184`  
		Last Modified: Thu, 16 Apr 2020 03:19:59 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59bbe876e0e619c9ff7e3530835e4e8aff680cd5c766330d827c28d3226faee`  
		Last Modified: Thu, 16 Apr 2020 03:19:59 GMT  
		Size: 211.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e2302b32b263a3954b014c24c536e5b7f6dc09351f12da72fff8707ca8d97e`  
		Last Modified: Thu, 16 Apr 2020 03:19:59 GMT  
		Size: 7.8 KB (7786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69617872163af62a1b33139c50056a3bc73420c10e7b342a9804b28ff579779`  
		Last Modified: Thu, 16 Apr 2020 10:49:57 GMT  
		Size: 275.0 KB (275000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:251b0ebf3fa854048eed3cf31ec0d83f5cc7fa43c605a76599a57a3b6cf0f98e`  
		Last Modified: Thu, 16 Apr 2020 10:49:57 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b5a84d254987b02493491acbbcc0bd7eb78aff7b9fe6d0aac371b14249b2fb`  
		Last Modified: Thu, 16 Apr 2020 10:49:58 GMT  
		Size: 2.5 MB (2485211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed51a8f05ab97be0ab836230f0e87375b68b05908ade7c7cc116962eed9bfc30`  
		Last Modified: Thu, 16 Apr 2020 10:49:57 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f52c223533c27ea9ee6032a845f04361fc30d8e6691c95be617c43fb63819ad`  
		Last Modified: Thu, 16 Apr 2020 10:49:57 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm` - linux; arm variant v7

```console
$ docker pull yourls@sha256:bde173e6b6ebb0c4d9738ae9612c66a4c69c5a1e1e21907ebcaf7a6dbde79113
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **123.7 MB (123725494 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffee383bf478f110d0a0b9d316ca9374e80714b93bd11232c7b7b67c841bd461`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Apr 2020 00:59:45 GMT
ADD file:e346a36a456d66d8019344b5f7d60df8b5b24aea1461c19838982135ad1f4d7d in / 
# Thu, 16 Apr 2020 00:59:47 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 09:52:28 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 16 Apr 2020 09:52:29 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 16 Apr 2020 09:53:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 09:53:11 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Apr 2020 09:53:14 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 16 Apr 2020 10:01:10 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 16 Apr 2020 10:01:11 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2020 10:01:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2020 10:01:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 16 Apr 2020 10:52:32 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 16 Apr 2020 10:52:33 GMT
ENV PHP_VERSION=7.2.29
# Thu, 16 Apr 2020 10:52:33 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.29.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.29.tar.xz.asc/from/this/mirror
# Thu, 16 Apr 2020 10:52:34 GMT
ENV PHP_SHA256=b117de74136bf4b439d663be9cf0c8e06a260c1f340f6b75ccadb609153a7fe8 PHP_MD5=
# Thu, 16 Apr 2020 10:52:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 16 Apr 2020 10:52:51 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 16 Apr 2020 10:56:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 16 Apr 2020 10:56:39 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 16 Apr 2020 10:56:42 GMT
RUN docker-php-ext-enable sodium
# Thu, 16 Apr 2020 10:56:44 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 16 Apr 2020 10:56:45 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 16 Apr 2020 10:56:46 GMT
WORKDIR /var/www/html
# Thu, 16 Apr 2020 10:56:48 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 16 Apr 2020 10:56:48 GMT
STOPSIGNAL SIGQUIT
# Thu, 16 Apr 2020 10:56:49 GMT
EXPOSE 9000
# Thu, 16 Apr 2020 10:56:50 GMT
CMD ["php-fpm"]
# Fri, 17 Apr 2020 05:22:16 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 17 Apr 2020 05:22:18 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 17 Apr 2020 05:22:18 GMT
ENV YOURLS_VERSION=1.7.6
# Fri, 17 Apr 2020 05:22:19 GMT
ENV YOURLS_SHA256=f3623af6e4cabee61a39d3deca3c941717c5e0a60bc288b6f3a668f87a20ae2e
# Fri, 17 Apr 2020 05:22:23 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Fri, 17 Apr 2020 05:22:24 GMT
COPY file:faa5e93643253a8f7b19a0098e9286cc1914eaa7154c418de43e161d69f2f157 in /usr/local/bin/ 
# Fri, 17 Apr 2020 05:22:24 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Fri, 17 Apr 2020 05:22:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2020 05:22:26 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:838dc71644c10eab485c4bdfa3879e0fb9e72426de1239cfac1d4c05c23db7be`  
		Last Modified: Thu, 16 Apr 2020 01:08:59 GMT  
		Size: 22.7 MB (22705228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51f8fdbff988ba585ce37f923bf4b49474ca9c838dfe877ca1cb91db76b4750d`  
		Last Modified: Thu, 16 Apr 2020 11:20:53 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8674d4305249be09893f40da34923200030cb3141bef3a0007a7269611c7e1c`  
		Last Modified: Thu, 16 Apr 2020 11:21:11 GMT  
		Size: 59.5 MB (59501464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d380b1b0920e653046b83a9ac2f4faf28f2aca78e9723d0a7d849bb2bb71916`  
		Last Modified: Thu, 16 Apr 2020 11:20:53 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f31b188e243e541acac5c3ffce8c4beba53d5d96c2b92ccbfa6d117c99409f5a`  
		Last Modified: Thu, 16 Apr 2020 11:25:28 GMT  
		Size: 12.6 MB (12628701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ca600015e48a6edae568c063d9a4f6f86b03e85540c4e766579aced6a45dd9`  
		Last Modified: Thu, 16 Apr 2020 11:25:27 GMT  
		Size: 493.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75b0909f9fe9c4c27db46b78de934177e3fd590c34c55d1b2b20b0ca9375175`  
		Last Modified: Thu, 16 Apr 2020 11:25:32 GMT  
		Size: 26.1 MB (26142320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb75a89b3b849dad193c3f88ef224cdc50014a35e856483764826fef78ef5da4`  
		Last Modified: Thu, 16 Apr 2020 11:25:25 GMT  
		Size: 2.2 KB (2220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f4fcb295404950d2b185da59c60ab78f95d6092039f9087cf56b9a82f9b4ce8`  
		Last Modified: Thu, 16 Apr 2020 11:25:25 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e603c929ca120bd2b9e65f9650a0c22a75b4d439fd98266c5472175a66ce190`  
		Last Modified: Thu, 16 Apr 2020 11:25:25 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b57e2e81f5729b847faee3199d255233252c23180e037aa713e1fcf0675e72e`  
		Last Modified: Thu, 16 Apr 2020 11:25:25 GMT  
		Size: 7.8 KB (7785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d7789ca4c64848bc31c3014bab02006bc3383a6f03f08df5773b1c1ebdf722`  
		Last Modified: Fri, 17 Apr 2020 05:23:16 GMT  
		Size: 247.7 KB (247735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f827b741ecc06ad2451ea43cf7e1e3e4f4f9e91279734c33155e1ec45b86c379`  
		Last Modified: Fri, 17 Apr 2020 05:23:15 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8e0181508b46f38eb018966fc655dc963ea4201a635e5358de1c4675bccf6c6`  
		Last Modified: Fri, 17 Apr 2020 05:23:16 GMT  
		Size: 2.5 MB (2485214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814309e18d535180b1a50098b78a115fe57f8898d2a6a4f14102838ee670d374`  
		Last Modified: Fri, 17 Apr 2020 05:23:16 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74dec24ce1e6d0c13aa5a981b8c56e99b66e593281f709f88a95fc0d4e6386f5`  
		Last Modified: Fri, 17 Apr 2020 05:23:15 GMT  
		Size: 1.9 KB (1861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm` - linux; arm64 variant v8

```console
$ docker pull yourls@sha256:69bc64535aeae0c002929ffe079e778b969bea457609fc94dddff40408619207
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.8 MB (139837275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b09722887cdf92b5f45de52f9075c663b7c10c13b228f787d524accc0bcaea24`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Apr 2020 02:41:52 GMT
ADD file:1aab17002a9095c31dd6928277a045cb26846ac58c3d2d63316332c99a5f90bd in / 
# Thu, 16 Apr 2020 02:41:57 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 13:31:42 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 16 Apr 2020 13:31:44 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 16 Apr 2020 13:32:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 13:32:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Apr 2020 13:32:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 16 Apr 2020 13:40:52 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 16 Apr 2020 13:40:53 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2020 13:40:54 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2020 13:40:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 16 Apr 2020 14:34:56 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 16 Apr 2020 14:34:57 GMT
ENV PHP_VERSION=7.2.29
# Thu, 16 Apr 2020 14:34:58 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.29.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.29.tar.xz.asc/from/this/mirror
# Thu, 16 Apr 2020 14:34:58 GMT
ENV PHP_SHA256=b117de74136bf4b439d663be9cf0c8e06a260c1f340f6b75ccadb609153a7fe8 PHP_MD5=
# Thu, 16 Apr 2020 14:35:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 16 Apr 2020 14:35:13 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 16 Apr 2020 14:38:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 16 Apr 2020 14:38:26 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 16 Apr 2020 14:38:28 GMT
RUN docker-php-ext-enable sodium
# Thu, 16 Apr 2020 14:38:30 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 16 Apr 2020 14:38:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 16 Apr 2020 14:38:31 GMT
WORKDIR /var/www/html
# Thu, 16 Apr 2020 14:38:33 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 16 Apr 2020 14:38:33 GMT
STOPSIGNAL SIGQUIT
# Thu, 16 Apr 2020 14:38:34 GMT
EXPOSE 9000
# Thu, 16 Apr 2020 14:38:34 GMT
CMD ["php-fpm"]
# Fri, 17 Apr 2020 07:04:29 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 17 Apr 2020 07:04:30 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 17 Apr 2020 07:04:31 GMT
ENV YOURLS_VERSION=1.7.6
# Fri, 17 Apr 2020 07:04:31 GMT
ENV YOURLS_SHA256=f3623af6e4cabee61a39d3deca3c941717c5e0a60bc288b6f3a668f87a20ae2e
# Fri, 17 Apr 2020 07:04:34 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Fri, 17 Apr 2020 07:04:35 GMT
COPY file:faa5e93643253a8f7b19a0098e9286cc1914eaa7154c418de43e161d69f2f157 in /usr/local/bin/ 
# Fri, 17 Apr 2020 07:04:35 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Fri, 17 Apr 2020 07:04:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2020 07:04:36 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:3d48095d71a365b5910cea98e5566c152a3f9aa11657560568259bf93ff2f4cb`  
		Last Modified: Thu, 16 Apr 2020 02:48:58 GMT  
		Size: 25.9 MB (25857715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90fdd0b0f5914e23b97e6b4c85e72419571f773834e9c5d730f39161697995d`  
		Last Modified: Thu, 16 Apr 2020 15:02:24 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1efc35f6808c49c804fbb7d49d5dc0cfb27df6b557216ae986e2d002c542c78b`  
		Last Modified: Thu, 16 Apr 2020 15:02:46 GMT  
		Size: 70.3 MB (70334995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d50046d41b1b2f8266660f05392abbe78af7f9798529c7b42d0860191555ea`  
		Last Modified: Thu, 16 Apr 2020 15:02:24 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d383acedae9e18c46d18909be3dad20849624da18409ed0b3eeca18f0460e2`  
		Last Modified: Thu, 16 Apr 2020 15:07:17 GMT  
		Size: 12.6 MB (12629502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e999b384691daaeb9f00411894905e5a88d0154132370428c8d0d42093574c05`  
		Last Modified: Thu, 16 Apr 2020 15:07:16 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b9f332b94dd4afee691d5c9335b99f351f89683ad9458325b5fb29818b262f`  
		Last Modified: Thu, 16 Apr 2020 15:07:23 GMT  
		Size: 28.2 MB (28230739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fd2ac34ae239b61042185261b73e92905a9d72943ec132f413d60b2ce1f5e3`  
		Last Modified: Thu, 16 Apr 2020 15:07:14 GMT  
		Size: 2.2 KB (2221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd09d9ee4d3049bfc77b91306c10db30a824591d093518be228a85152e16a00`  
		Last Modified: Thu, 16 Apr 2020 15:07:14 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:466ea2128b61fdd40f25f2a1014490aca90d3efd5bf230e22463cd88213fa012`  
		Last Modified: Thu, 16 Apr 2020 15:07:14 GMT  
		Size: 210.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85d84b94193a51a45bcaf0ad6382355868befc806efaa69c51f73c1c3acb9d6`  
		Last Modified: Thu, 16 Apr 2020 15:07:14 GMT  
		Size: 7.8 KB (7785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c21641ee3a2f27bab5d4bed54a3502138adb953749ff28110448f90386b89737`  
		Last Modified: Fri, 17 Apr 2020 07:05:18 GMT  
		Size: 284.3 KB (284284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2175bca8e3d89799631bc2dd4ddf081c557aa9eb57e10b94d7c9b341e872615`  
		Last Modified: Fri, 17 Apr 2020 07:05:18 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:261dd4082c9e0a301110b58dc1bd4ed0844b44c2b205d6770ceafcdf87defc9f`  
		Last Modified: Fri, 17 Apr 2020 07:05:19 GMT  
		Size: 2.5 MB (2485215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec4c3e526fa86ab420cfdeccf783686ffd6bc084e1ae1e78192d6aec34a03bf`  
		Last Modified: Fri, 17 Apr 2020 07:05:18 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4b843bbb2eb630a49b7a74b439d5902d3dc48b782f9ef01e333bca6f7cbace`  
		Last Modified: Fri, 17 Apr 2020 07:05:18 GMT  
		Size: 1.9 KB (1860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm` - linux; 386

```console
$ docker pull yourls@sha256:9afba2de05cdfb3d5f07a95074cce8d986859b36518e2867182ffb6ea2700f9a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.5 MB (153495070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf4c3ea80eff85b06aeec84a9ff0efc8bc35a030caf73ab3b4bc678e81e79a33`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 16 Apr 2020 01:39:55 GMT
ADD file:ab0bbfba6c4b56420ffffc6cdddcc4592fff018f0cd07578c7dc0a5faa49df2f in / 
# Thu, 16 Apr 2020 01:39:56 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 11:42:14 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 16 Apr 2020 11:42:14 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 16 Apr 2020 11:42:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 11:42:52 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 16 Apr 2020 11:42:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 16 Apr 2020 11:57:13 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Thu, 16 Apr 2020 11:57:13 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2020 11:57:13 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 16 Apr 2020 11:57:13 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Thu, 16 Apr 2020 13:36:28 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Thu, 16 Apr 2020 13:36:28 GMT
ENV PHP_VERSION=7.2.29
# Thu, 16 Apr 2020 13:36:28 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.29.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.29.tar.xz.asc/from/this/mirror
# Thu, 16 Apr 2020 13:36:29 GMT
ENV PHP_SHA256=b117de74136bf4b439d663be9cf0c8e06a260c1f340f6b75ccadb609153a7fe8 PHP_MD5=
# Thu, 16 Apr 2020 13:36:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 16 Apr 2020 13:36:38 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 16 Apr 2020 13:45:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Thu, 16 Apr 2020 13:45:22 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Thu, 16 Apr 2020 13:45:23 GMT
RUN docker-php-ext-enable sodium
# Thu, 16 Apr 2020 13:45:23 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Thu, 16 Apr 2020 13:45:24 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 16 Apr 2020 13:45:24 GMT
WORKDIR /var/www/html
# Thu, 16 Apr 2020 13:45:25 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 16 Apr 2020 13:45:25 GMT
STOPSIGNAL SIGQUIT
# Thu, 16 Apr 2020 13:45:25 GMT
EXPOSE 9000
# Thu, 16 Apr 2020 13:45:25 GMT
CMD ["php-fpm"]
# Fri, 17 Apr 2020 01:52:28 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Fri, 17 Apr 2020 01:52:30 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 17 Apr 2020 01:52:30 GMT
ENV YOURLS_VERSION=1.7.6
# Fri, 17 Apr 2020 01:52:30 GMT
ENV YOURLS_SHA256=f3623af6e4cabee61a39d3deca3c941717c5e0a60bc288b6f3a668f87a20ae2e
# Fri, 17 Apr 2020 01:52:32 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Fri, 17 Apr 2020 01:52:33 GMT
COPY file:faa5e93643253a8f7b19a0098e9286cc1914eaa7154c418de43e161d69f2f157 in /usr/local/bin/ 
# Fri, 17 Apr 2020 01:52:33 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Fri, 17 Apr 2020 01:52:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2020 01:52:33 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:75bc60a98e6523be3fadd9128c1a630cb5cbd2d2d813ee5e99dc146a3de22254`  
		Last Modified: Thu, 16 Apr 2020 01:46:20 GMT  
		Size: 27.8 MB (27753976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:580962e9450ca1b5ce83bb772724b2d0ccb693fcb5621a2a183d4c4b623bdd79`  
		Last Modified: Thu, 16 Apr 2020 14:27:13 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e05ab240d5a6be86c4185445fb618f19bc1ac549f84f9ac7e70049e8c8bd9b9`  
		Last Modified: Thu, 16 Apr 2020 14:27:53 GMT  
		Size: 81.2 MB (81198973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:328115a893c2014f3e46294f0eb8907d40cd3ffd4b14b93a13046d46e12225fb`  
		Last Modified: Thu, 16 Apr 2020 14:27:12 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:702c2a1c4a0d5756da40a69e1b68052a5a5f37ca6bef3f8ced15bb0eff43a461`  
		Last Modified: Thu, 16 Apr 2020 14:32:27 GMT  
		Size: 12.6 MB (12629928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0debe16497c7340d034751f118a41c4153f3cfbce115556644fe375497599bc8`  
		Last Modified: Thu, 16 Apr 2020 14:32:25 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84160b7adb8bc4f009fd03c0b3b57a54a5fcacee59adb3fcc21b7ea8edcd809d`  
		Last Modified: Thu, 16 Apr 2020 14:32:31 GMT  
		Size: 29.1 MB (29111883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9031961f3b34d1497a7cca4731e806860e3b795934afc4bbcf73ed6a91cf37f0`  
		Last Modified: Thu, 16 Apr 2020 14:32:24 GMT  
		Size: 2.2 KB (2221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d38c7cb657fbd994fb38fbaba214719645689dcb9a10b10d058b13a88ec69007`  
		Last Modified: Thu, 16 Apr 2020 14:32:24 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c647995e7961faf953d44b0de098a799507fbd57f56bcf69b95ba0a46acede`  
		Last Modified: Thu, 16 Apr 2020 14:32:24 GMT  
		Size: 213.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab060665dbfd97288d7d9610dfe21fea536d6341488f54ec53768724536dfc6`  
		Last Modified: Thu, 16 Apr 2020 14:32:24 GMT  
		Size: 7.8 KB (7785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9e836e4c075eb2a061f0a43c1f3cbeaeb113866eb529e3ce55a63a6f76d8546`  
		Last Modified: Fri, 17 Apr 2020 01:53:01 GMT  
		Size: 300.3 KB (300334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad59ca863c2ae8379104bc9321a3dcb9cf3cd564505092ec217c0f530edc3b4e`  
		Last Modified: Fri, 17 Apr 2020 01:53:01 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3e4d5bb3bc8d755c58ec426ae7886f25883eca66737efb5bf219897f5412e5e`  
		Last Modified: Fri, 17 Apr 2020 01:53:02 GMT  
		Size: 2.5 MB (2485192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ebdc9c6a93b50189f6b595ff7592e3431b18278a2fb59204f54c015fd9fee7`  
		Last Modified: Fri, 17 Apr 2020 01:53:01 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f09d393feff5894076da14ab373b5a7b69cbe7bacbf1e4060855654ace4f29`  
		Last Modified: Fri, 17 Apr 2020 01:53:01 GMT  
		Size: 1.9 KB (1858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `yourls:fpm` - linux; ppc64le

```console
$ docker pull yourls@sha256:8cf71ea3fba860ec8d8c44564e8d072ecb2ea2d1d8e8d99d73ba59f02cf48e9b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.5 MB (158474379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b2443d407a6ba6d4f841617881569cd7bc1679ea9aafc5e08f4b7c634c3916b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 31 Mar 2020 01:32:42 GMT
ADD file:36c02e92574faba45b64cfed78a0a0359d65ad175b17128bf554a2a5c0086ff5 in / 
# Tue, 31 Mar 2020 01:32:47 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 18:20:02 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 31 Mar 2020 18:20:06 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 31 Mar 2020 18:23:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 18:23:10 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 31 Mar 2020 18:23:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 31 Mar 2020 18:38:05 GMT
ENV PHP_EXTRA_CONFIGURE_ARGS=--enable-fpm --with-fpm-user=www-data --with-fpm-group=www-data --disable-cgi
# Tue, 31 Mar 2020 18:38:09 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 31 Mar 2020 18:38:12 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 31 Mar 2020 18:38:14 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -Wl,--hash-style=both -pie
# Tue, 31 Mar 2020 20:08:36 GMT
ENV GPG_KEYS=1729F83938DA44E27BA0F4D3DBDB397470D12172 B1B44D8F021E4E2D6021E995DC9FF8D3EE5AF27F
# Tue, 31 Mar 2020 20:08:42 GMT
ENV PHP_VERSION=7.2.29
# Tue, 31 Mar 2020 20:08:46 GMT
ENV PHP_URL=https://www.php.net/get/php-7.2.29.tar.xz/from/this/mirror PHP_ASC_URL=https://www.php.net/get/php-7.2.29.tar.xz.asc/from/this/mirror
# Tue, 31 Mar 2020 20:08:48 GMT
ENV PHP_SHA256=b117de74136bf4b439d663be9cf0c8e06a260c1f340f6b75ccadb609153a7fe8 PHP_MD5=
# Tue, 31 Mar 2020 20:09:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 	if [ -n "$PHP_MD5" ]; then 		echo "$PHP_MD5 *php.tar.xz" | md5sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 31 Mar 2020 20:09:45 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 31 Mar 2020 20:13:50 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libedit-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 		${PHP_EXTRA_BUILD_DEPS:-} 	; 	rm -rf /var/lib/apt/lists/*; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-libedit 		--with-openssl 		--with-zlib 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				${PHP_EXTRA_CONFIGURE_ARGS:-} 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find /usr/local/bin /usr/local/sbin -type f -executable -exec strip --strip-all '{}' + || true; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 	php --version
# Tue, 31 Mar 2020 20:13:53 GMT
COPY multi:5581a34bba21fbf2472e857e8cdc8db6d57694020e568954d2fd5901ee074da0 in /usr/local/bin/ 
# Tue, 31 Mar 2020 20:14:05 GMT
RUN docker-php-ext-enable sodium
# Tue, 31 Mar 2020 20:14:10 GMT
RUN { echo '#!/bin/sh'; echo 'exec pkg-config "$@" freetype2'; } > /usr/local/bin/freetype-config && chmod +x /usr/local/bin/freetype-config
# Tue, 31 Mar 2020 20:14:13 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 31 Mar 2020 20:14:17 GMT
WORKDIR /var/www/html
# Tue, 31 Mar 2020 20:14:26 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Tue, 31 Mar 2020 20:14:30 GMT
STOPSIGNAL SIGQUIT
# Tue, 31 Mar 2020 20:14:32 GMT
EXPOSE 9000
# Tue, 31 Mar 2020 20:14:36 GMT
CMD ["php-fpm"]
# Wed, 01 Apr 2020 11:33:47 GMT
RUN set -eux;     docker-php-ext-install -j "$(nproc)" opcache pdo_mysql mysqli
# Wed, 01 Apr 2020 11:33:52 GMT
RUN {         echo 'opcache.memory_consumption=128';         echo 'opcache.interned_strings_buffer=8';         echo 'opcache.max_accelerated_files=4000';         echo 'opcache.revalidate_freq=60';         echo 'opcache.fast_shutdown=1';     } > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Wed, 01 Apr 2020 11:33:54 GMT
ENV YOURLS_VERSION=1.7.6
# Wed, 01 Apr 2020 11:33:57 GMT
ENV YOURLS_SHA256=f3623af6e4cabee61a39d3deca3c941717c5e0a60bc288b6f3a668f87a20ae2e
# Wed, 01 Apr 2020 11:34:08 GMT
RUN set -eux;     curl -o yourls.tar.gz -fsSL "https://github.com/YOURLS/YOURLS/archive/${YOURLS_VERSION}.tar.gz";     echo "$YOURLS_SHA256 *yourls.tar.gz" | sha256sum -c -;     tar -xf yourls.tar.gz -C /usr/src/;     mv "/usr/src/YOURLS-${YOURLS_VERSION}" /usr/src/yourls;     rm yourls.tar.gz;     chown -R www-data:www-data /usr/src/yourls
# Wed, 01 Apr 2020 11:34:10 GMT
COPY file:faa5e93643253a8f7b19a0098e9286cc1914eaa7154c418de43e161d69f2f157 in /usr/local/bin/ 
# Wed, 01 Apr 2020 11:34:11 GMT
COPY file:3694b933d9d31fc65ed3f78f65289b778a21bf67c518d2cb89c6294ef1d41b60 in /usr/src/yourls/user/ 
# Wed, 01 Apr 2020 11:34:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Apr 2020 11:34:14 GMT
CMD ["php-fpm"]
```

-	Layers:
	-	`sha256:9df6bbae5eeb29e9aac2f39cff517c694cce60f01ee477abcdedcd8e8c01c38f`  
		Last Modified: Tue, 31 Mar 2020 01:45:59 GMT  
		Size: 30.5 MB (30518493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a5f2c37c0de46cda2befedd3876fc78801a15be2dce4b0116818a7aab35c04`  
		Last Modified: Tue, 31 Mar 2020 20:47:27 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e114e9ba1490fcf41258b1a701ea45b783428085bf612daa8bda0e94cf1504`  
		Last Modified: Tue, 31 Mar 2020 20:48:04 GMT  
		Size: 82.3 MB (82259910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65ab407be0c6f406f88af833d569c84d8ec441c22d3a940bb0db5abd2d137bf`  
		Last Modified: Tue, 31 Mar 2020 20:47:26 GMT  
		Size: 271.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9feb06d07ab28fc1ba9ca69e1a0851fa90c440750d23f643c72b561fbb4aafd3`  
		Last Modified: Tue, 31 Mar 2020 20:55:24 GMT  
		Size: 12.6 MB (12630643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eaff057e318d2e25c173b1c120d4fe1f090da077491491b88ad1cae7c9484d6`  
		Last Modified: Tue, 31 Mar 2020 20:55:22 GMT  
		Size: 492.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d30978f7152cf5b387e17a485bd857179cc6bba64a15093001603b94341f3c0`  
		Last Modified: Tue, 31 Mar 2020 20:55:24 GMT  
		Size: 30.2 MB (30242518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41261bd173871103277e83737634e80c0ed97b263735954c7a7a8564e9a7d7a9`  
		Last Modified: Tue, 31 Mar 2020 20:55:18 GMT  
		Size: 2.2 KB (2220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8067d5e184872f97cc1d8408304286ee29ceceedb9129d2857edcfab83ee93ed`  
		Last Modified: Tue, 31 Mar 2020 20:55:18 GMT  
		Size: 248.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc4b808d11c4c6fa9297582e02d6b03832880e0bed429558a51e0f31fd17056`  
		Last Modified: Tue, 31 Mar 2020 20:55:18 GMT  
		Size: 215.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29755cc00cdc6c6f81ee5f1eb7a7e40aeec0ec0415ca2f8c360d9dbbc553b2ca`  
		Last Modified: Tue, 31 Mar 2020 20:55:18 GMT  
		Size: 7.8 KB (7788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76ed01931cdca6a5d5a286fd71e13ff20e65314968ddb73115a2a34eacad536`  
		Last Modified: Wed, 01 Apr 2020 11:35:21 GMT  
		Size: 322.8 KB (322763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f667ece7700079c82ce3e903a08afcee4ed38162ef26b4b58ee26c1495ae30`  
		Last Modified: Wed, 01 Apr 2020 11:35:21 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69491c9a40803ba77de8773b0c83fb83805188070aa7ed72279d21903294ebd3`  
		Last Modified: Wed, 01 Apr 2020 11:35:22 GMT  
		Size: 2.5 MB (2485210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1e32fdfbfb21b4adc029d61dfcec55f8b076f46629fadf2184d7ca3507ab0f`  
		Last Modified: Wed, 01 Apr 2020 11:35:21 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c8a05de807139fdd23b55556077f234794d9d1dee5400081aef801fa7de8daa`  
		Last Modified: Wed, 01 Apr 2020 11:35:22 GMT  
		Size: 1.9 KB (1862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
