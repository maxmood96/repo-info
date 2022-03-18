## `drupal:rc-php8.1-fpm-buster`

```console
$ docker pull drupal@sha256:089a84b6d19894ee01915c3f3a9141c7bf2a745b24f390092d92e262ada881ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `drupal:rc-php8.1-fpm-buster` - linux; amd64

```console
$ docker pull drupal@sha256:b86243671b2df311c556bdd36f9bc92790becb08a861e549d73ea4680fdd766e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163392113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:135ccfd410acf0898caff1c4650daac86950669014802449e4a7855c6f7341e0`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:56 GMT
ADD file:702017714ad3e1567b4f60b688750f8b631d91088e4dcf41351c4bb07749c579 in / 
# Tue, 01 Mar 2022 02:13:56 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 19:37:41 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 01 Mar 2022 19:37:42 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 01 Mar 2022 19:37:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 19:37:59 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 01 Mar 2022 19:37:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 01 Mar 2022 19:37:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 01 Mar 2022 19:37:59 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 01 Mar 2022 19:37:59 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 01 Mar 2022 19:38:00 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 01 Mar 2022 19:38:00 GMT
ENV PHP_VERSION=8.1.3
# Tue, 01 Mar 2022 19:38:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Tue, 01 Mar 2022 19:38:00 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Tue, 01 Mar 2022 19:39:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 01 Mar 2022 19:39:11 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:48:44 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 03:48:45 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:48:46 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 03:48:46 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 03:48:46 GMT
WORKDIR /var/www/html
# Fri, 11 Mar 2022 03:48:47 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 11 Mar 2022 03:48:47 GMT
STOPSIGNAL SIGQUIT
# Fri, 11 Mar 2022 03:48:47 GMT
EXPOSE 9000
# Fri, 11 Mar 2022 03:48:47 GMT
CMD ["php-fpm"]
# Fri, 11 Mar 2022 12:02:56 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Mar 2022 12:02:57 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Wed, 16 Mar 2022 19:36:13 GMT
COPY file:608f7625682057a8f327a57b0a8d1d350465d3209e7a8c9e119158b6dc4b876a in /usr/local/bin/ 
# Wed, 16 Mar 2022 19:36:14 GMT
ENV DRUPAL_VERSION=10.0.0-alpha2
# Wed, 16 Mar 2022 19:36:14 GMT
WORKDIR /opt/drupal
# Wed, 16 Mar 2022 19:36:25 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Wed, 16 Mar 2022 19:36:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:15115158dd02a1bf2fd28724e3c1024394033fb0e9a5d3e451ed2715b6ae312d`  
		Last Modified: Tue, 01 Mar 2022 02:20:08 GMT  
		Size: 27.2 MB (27153737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601b5119b01195e0ab4cc813c56610c296b5a446c950b2df23f1045cbe5d5f81`  
		Last Modified: Tue, 01 Mar 2022 22:07:50 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e126f6ddd1fc272906f55b52bbb2dc87f83ca764af5bfd36bbe45398ec7e20b4`  
		Last Modified: Tue, 01 Mar 2022 22:08:04 GMT  
		Size: 76.7 MB (76680865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d3be01dcb2ff53840047b141a554ef76c77c0cc682e97165f4b71d439eecd2`  
		Last Modified: Tue, 01 Mar 2022 22:07:50 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8c73d796be29e0813d0e36f43d4a38eec13d9afcf9c32df4cf0b321bd91f492`  
		Last Modified: Tue, 01 Mar 2022 22:07:49 GMT  
		Size: 12.1 MB (12073963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fbe4ad1661009b2229a001d694167d20990454e2d4db5d2707d98c0bfb72ff`  
		Last Modified: Tue, 01 Mar 2022 22:07:48 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913ee23e15b62ca0f726577130b3428cee3ca91d9631da52c6cde2951cf1837f`  
		Last Modified: Fri, 11 Mar 2022 11:16:05 GMT  
		Size: 25.7 MB (25702115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5005bd0f6e634275b436f5de409b41a98004e82bcd6535cf73987dd39727af9e`  
		Last Modified: Fri, 11 Mar 2022 11:16:00 GMT  
		Size: 2.3 KB (2309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534b9af63b3f95c449e71c6de43998fda2d7db73663a3420cf5149299e01456a`  
		Last Modified: Fri, 11 Mar 2022 11:16:00 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f015d2c6255611770441f99e11b453c908cf04d54041fb00d237793c62c01ed`  
		Last Modified: Fri, 11 Mar 2022 11:16:00 GMT  
		Size: 8.6 KB (8625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4316bb05ba03246093e390a86f795d2c4f7118dffd25635467d6015da5de459`  
		Last Modified: Fri, 11 Mar 2022 12:29:00 GMT  
		Size: 2.1 MB (2056749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81387ee6fdae326df1f3e36c5f05ddb9eef2edab26113ca489b794394db671d1`  
		Last Modified: Fri, 11 Mar 2022 12:28:59 GMT  
		Size: 329.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1fa139ce628cfe48ef53ced45245bb19643f707ae92799c6c2e3a15904b9cb`  
		Last Modified: Wed, 16 Mar 2022 19:48:18 GMT  
		Size: 575.7 KB (575720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:700029f5d7bd5c95f5cea8f8d12c56dfddc85eb515159002022e27c2ae764dba`  
		Last Modified: Wed, 16 Mar 2022 19:48:18 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3daf22b84b5be9c8aa8855b20ce0887b781b360eab5d3a796cb519c6afc33285`  
		Last Modified: Wed, 16 Mar 2022 19:48:23 GMT  
		Size: 19.1 MB (19136321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:rc-php8.1-fpm-buster` - linux; arm variant v7

```console
$ docker pull drupal@sha256:17e504a3d3608c5643aec100cfbf165d6d3d908bc9d89dc1ae1f96bdc61a36a4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (138957911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b6057818dc42dd8ced03ab1bf50e65d1efb045c209b91ff89da21b44e43d0c9`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 01 Mar 2022 02:04:06 GMT
ADD file:d73a3eaf767825b31d0c0189624b35193e5ad7c5907f839edf6f7917036c2d0b in / 
# Tue, 01 Mar 2022 02:04:07 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 23:11:33 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 01 Mar 2022 23:11:34 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 01 Mar 2022 23:12:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 23:12:18 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 01 Mar 2022 23:12:19 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 01 Mar 2022 23:12:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 01 Mar 2022 23:12:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 01 Mar 2022 23:12:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 01 Mar 2022 23:12:21 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 01 Mar 2022 23:12:21 GMT
ENV PHP_VERSION=8.1.3
# Tue, 01 Mar 2022 23:12:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Tue, 01 Mar 2022 23:12:22 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Tue, 01 Mar 2022 23:12:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 01 Mar 2022 23:12:59 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 02:33:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 02:33:13 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Fri, 11 Mar 2022 02:33:15 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 02:33:15 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 02:33:15 GMT
WORKDIR /var/www/html
# Fri, 11 Mar 2022 02:33:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 11 Mar 2022 02:33:17 GMT
STOPSIGNAL SIGQUIT
# Fri, 11 Mar 2022 02:33:18 GMT
EXPOSE 9000
# Fri, 11 Mar 2022 02:33:18 GMT
CMD ["php-fpm"]
# Fri, 11 Mar 2022 12:34:19 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Mar 2022 12:34:21 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Wed, 16 Mar 2022 18:57:50 GMT
COPY file:608f7625682057a8f327a57b0a8d1d350465d3209e7a8c9e119158b6dc4b876a in /usr/local/bin/ 
# Wed, 16 Mar 2022 18:57:50 GMT
ENV DRUPAL_VERSION=10.0.0-alpha2
# Wed, 16 Mar 2022 18:57:50 GMT
WORKDIR /opt/drupal
# Wed, 16 Mar 2022 18:58:21 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Wed, 16 Mar 2022 18:58:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:1acfd43b1a25aefe6117ba65bf2b46a19e3cf8e72b76f522a9fe299412e1c5f2`  
		Last Modified: Tue, 01 Mar 2022 02:20:32 GMT  
		Size: 22.8 MB (22754370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8091c140a16be6c865ac0a0f4d85b970d0674adea568954f54e1f5c880114a09`  
		Last Modified: Wed, 02 Mar 2022 01:57:47 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3c2837a47e874246ad0d49971bc781b8b80cd87a070d3a35a4fcd3d68dbbd7`  
		Last Modified: Wed, 02 Mar 2022 01:58:25 GMT  
		Size: 59.5 MB (59515719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a799d53e4b5b1d80e81a6c90fa52c161d0c333a7bcdbfdcebda8791a8c95511`  
		Last Modified: Wed, 02 Mar 2022 01:57:47 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948531d2c8e87471a446280174e4c1d6c2411f21871028a55f6c203e16292108`  
		Last Modified: Wed, 02 Mar 2022 01:57:48 GMT  
		Size: 12.1 MB (12071984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8059b44863b7af5da0e14d2a48692d0198a7dbdf549cdfefc7e625c92eb07216`  
		Last Modified: Wed, 02 Mar 2022 01:57:45 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da0725dff18d2e85bd8b6fdd76ad71f538169f6228addcbd322f4a8ec45f94d`  
		Last Modified: Fri, 11 Mar 2022 07:37:49 GMT  
		Size: 23.4 MB (23435872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9fe1f87fd6506398955e973be60370faf3c14fffd92c6e752da372f21d3afee`  
		Last Modified: Fri, 11 Mar 2022 07:37:34 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223597699fe4d5ae6c09fcabb0f0c435dd999f0dd719b5125190ff5c04293958`  
		Last Modified: Fri, 11 Mar 2022 07:37:34 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80760adb60923217d66dc220ec34bf340463174c1363d2fcf937edfc60fd2c39`  
		Last Modified: Fri, 11 Mar 2022 07:37:35 GMT  
		Size: 8.6 KB (8626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d34959f3b316da6c47bb0b5ed920c6889feab66f131e9aa692d5145eba4941b`  
		Last Modified: Fri, 11 Mar 2022 15:21:51 GMT  
		Size: 1.5 MB (1454971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f760f923e736f0d990e0a790e44a3aca4629a7e04787564288c049e0942425a`  
		Last Modified: Fri, 11 Mar 2022 15:21:50 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19711d1531dc66f88c1b5f6a453062bde0cdc02bced21ee56337aa0adaf2b1dc`  
		Last Modified: Wed, 16 Mar 2022 19:41:30 GMT  
		Size: 575.7 KB (575714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9830e87ed72770b44ac764dd895f888135e13516b04cb7af1a77fcd1ec32c5`  
		Last Modified: Wed, 16 Mar 2022 19:41:29 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d512e559216ca985fae48e077cedfef5ff886e4183d09ab75fae5042976ee078`  
		Last Modified: Wed, 16 Mar 2022 19:41:57 GMT  
		Size: 19.1 MB (19136629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:rc-php8.1-fpm-buster` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:c37f6cde54fd272505d8a3f5069d365d040cd47963105d5e82b5d783c9f02805
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155509903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4dde2eddc1eb55512f3704c5a56aae98cf3ec41ac34a81607913b22c2b7822a`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 17 Mar 2022 03:22:22 GMT
ADD file:1c7d8cedf5dc79c676acebde5252ecd3005088a9f29e5e6be547f659f41efb1f in / 
# Thu, 17 Mar 2022 03:22:22 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 14:23:44 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 17 Mar 2022 14:23:45 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 17 Mar 2022 14:24:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 14:24:02 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Mar 2022 14:24:03 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 17 Mar 2022 14:24:04 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Mar 2022 14:24:05 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Mar 2022 14:24:06 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Mar 2022 14:24:07 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 17 Mar 2022 15:15:21 GMT
ENV PHP_VERSION=8.1.3
# Thu, 17 Mar 2022 15:15:21 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Thu, 17 Mar 2022 15:15:22 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Thu, 17 Mar 2022 15:16:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 17 Mar 2022 15:16:54 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 17 Mar 2022 15:29:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 17 Mar 2022 15:29:48 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Thu, 17 Mar 2022 15:29:48 GMT
RUN docker-php-ext-enable sodium
# Thu, 17 Mar 2022 15:29:49 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 17 Mar 2022 15:29:50 GMT
WORKDIR /var/www/html
# Thu, 17 Mar 2022 15:29:51 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 17 Mar 2022 15:29:52 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Mar 2022 15:29:53 GMT
EXPOSE 9000
# Thu, 17 Mar 2022 15:29:54 GMT
CMD ["php-fpm"]
# Fri, 18 Mar 2022 10:37:36 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 10:37:37 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Fri, 18 Mar 2022 10:37:39 GMT
COPY file:608f7625682057a8f327a57b0a8d1d350465d3209e7a8c9e119158b6dc4b876a in /usr/local/bin/ 
# Fri, 18 Mar 2022 10:37:39 GMT
ENV DRUPAL_VERSION=10.0.0-alpha2
# Fri, 18 Mar 2022 10:37:40 GMT
WORKDIR /opt/drupal
# Fri, 18 Mar 2022 10:38:08 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Fri, 18 Mar 2022 10:38:10 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c9277cac12165646c33f028489f2a5be3f70745382f4385cd9ed12fcc8cec183`  
		Last Modified: Thu, 17 Mar 2022 03:29:27 GMT  
		Size: 25.9 MB (25923233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b6c2b1e25add7315508df3aedb73d3d05b44920510c571e9746aecc9212808`  
		Last Modified: Thu, 17 Mar 2022 18:15:35 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e868294ede19eddb4934c00c242c3b7fb276b81ef1b28e07cacbda2706c1ad`  
		Last Modified: Thu, 17 Mar 2022 18:15:45 GMT  
		Size: 70.4 MB (70359368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c21cecb898c34df71bbb62a78234d013af6c31c04b6d6bf2bcf0c9cf1069d2fc`  
		Last Modified: Thu, 17 Mar 2022 18:15:35 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5255b0c878a53cd2c1e772de4e2ef98e2fcb8934b1a735a7d79300bfdd51b7fc`  
		Last Modified: Thu, 17 Mar 2022 18:21:19 GMT  
		Size: 11.9 MB (11859754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f943acfd41ef964f7ad16de2e5a5251587af3c4b34836de0bf3c028f7746759`  
		Last Modified: Thu, 17 Mar 2022 18:21:18 GMT  
		Size: 491.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a39676d7f77c52317af6bf6ce2ceafe7ee1fd915212a90eb420ab9fa6bc3b4f`  
		Last Modified: Thu, 17 Mar 2022 18:22:22 GMT  
		Size: 25.5 MB (25532088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bbef2d93f7f090528426c23aa10446fe4b730ecb7654a64d689ee7e59fc9dad`  
		Last Modified: Thu, 17 Mar 2022 18:22:18 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab46dfab62dad7c83964f27b26c9d625a2caa6fa8c0fd8e9a2a4e9ac308b26eb`  
		Last Modified: Thu, 17 Mar 2022 18:22:18 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2db58cd150f030f0953ad232b19cd20b453771f492194194dda876e5e125cf63`  
		Last Modified: Thu, 17 Mar 2022 18:22:18 GMT  
		Size: 8.6 KB (8619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7843774688135285d3fd67b181820788165474a4324973651c1692551120e86`  
		Last Modified: Fri, 18 Mar 2022 11:08:00 GMT  
		Size: 2.1 MB (2111273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ea1265669439e0d5b85c3ea496095909d67f9e1982fe40d55e61d0b41c1360`  
		Last Modified: Fri, 18 Mar 2022 11:07:59 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4606774478a18aacc4d10dff7c2d9683fb2bef0e494556f594039b387c5a9d`  
		Last Modified: Fri, 18 Mar 2022 11:08:00 GMT  
		Size: 575.7 KB (575714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb07651568ef0d5cd17eb73647d3e2f0ee8277ff48140ca21c66c6b57bb1393`  
		Last Modified: Fri, 18 Mar 2022 11:08:00 GMT  
		Size: 115.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbc0d2613bc8b433903e3356f2a882741127c5e43f1a5a0a0a9871fb24ffbfff`  
		Last Modified: Fri, 18 Mar 2022 11:08:05 GMT  
		Size: 19.1 MB (19135923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:rc-php8.1-fpm-buster` - linux; 386

```console
$ docker pull drupal@sha256:e0ffb77bad94ff9c524e76744b4563e64352d98fe102f85f474202c3eea69531
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.1 MB (169123142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89620115645b5e2600abfdb6fc8203d6130e1a1f0b70c4f5bfcca263cd49b17c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 01 Mar 2022 02:08:04 GMT
ADD file:d9d384f0402bc696e46e7529f52d64859a66aa7a60bca9c7beee7433a5f7af6e in / 
# Tue, 01 Mar 2022 02:08:04 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 15:47:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 01 Mar 2022 15:47:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 01 Mar 2022 15:47:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 15:47:58 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 01 Mar 2022 15:47:59 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Tue, 01 Mar 2022 15:47:59 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 01 Mar 2022 15:48:00 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 01 Mar 2022 15:48:00 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 01 Mar 2022 15:48:00 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Tue, 01 Mar 2022 15:48:00 GMT
ENV PHP_VERSION=8.1.3
# Tue, 01 Mar 2022 15:48:00 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Tue, 01 Mar 2022 15:48:01 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Tue, 01 Mar 2022 15:49:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 01 Mar 2022 15:49:04 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 04:24:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 04:24:06 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Fri, 11 Mar 2022 04:24:07 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 04:24:07 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 04:24:07 GMT
WORKDIR /var/www/html
# Fri, 11 Mar 2022 04:24:07 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 11 Mar 2022 04:24:08 GMT
STOPSIGNAL SIGQUIT
# Fri, 11 Mar 2022 04:24:08 GMT
EXPOSE 9000
# Fri, 11 Mar 2022 04:24:08 GMT
CMD ["php-fpm"]
# Fri, 11 Mar 2022 14:37:45 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Mar 2022 14:37:46 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Wed, 16 Mar 2022 18:23:08 GMT
COPY file:608f7625682057a8f327a57b0a8d1d350465d3209e7a8c9e119158b6dc4b876a in /usr/local/bin/ 
# Wed, 16 Mar 2022 18:23:08 GMT
ENV DRUPAL_VERSION=10.0.0-alpha2
# Wed, 16 Mar 2022 18:23:08 GMT
WORKDIR /opt/drupal
# Wed, 16 Mar 2022 18:23:30 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Wed, 16 Mar 2022 18:23:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c761ce6f2bf0aed07e1198c6f827444969d6e76dda0e55dbb45900920e551d27`  
		Last Modified: Tue, 01 Mar 2022 02:16:51 GMT  
		Size: 27.8 MB (27804590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a29b427e71eb7e1ff745c98433694074bfc9827e4a6deae78c5a8f9c35afbaca`  
		Last Modified: Tue, 01 Mar 2022 19:23:57 GMT  
		Size: 227.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c858978934e4ad1cb5c3a373aae3e9709353e928e1347b48c2c60ac035f8ee5`  
		Last Modified: Tue, 01 Mar 2022 19:24:30 GMT  
		Size: 81.2 MB (81229698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15397aa73308994ae5416b0dda851652beacba723bc6a402ba001bca543da166`  
		Last Modified: Tue, 01 Mar 2022 19:23:57 GMT  
		Size: 268.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd120e72b7af256b8af006bb96d81f35cfdbdeac8738b421444380923e254652`  
		Last Modified: Tue, 01 Mar 2022 19:23:57 GMT  
		Size: 12.1 MB (12073311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f51362772871ecb2dcfacee6617971a818d32afe3d5fb5b747c51154d57a4b44`  
		Last Modified: Tue, 01 Mar 2022 19:23:54 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9ea281b54332233eaee48b5de1b49ca42b7375453bcdc961c947ef7d939ee5`  
		Last Modified: Fri, 11 Mar 2022 11:58:13 GMT  
		Size: 26.2 MB (26161858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06cccbeffeba80c5f7ecb9601ed5b8c190c1cab7ea44a20a0811e5edc5624e6d`  
		Last Modified: Fri, 11 Mar 2022 11:58:06 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c3a3a83fbf435f4d2406e580ea9b887619b738bc6284f4f1342d5561393e9ee`  
		Last Modified: Fri, 11 Mar 2022 11:58:06 GMT  
		Size: 249.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fca633dd0e83d7b8efaa0d04c1680b0b5102f9652887519f6d9a80d01263d4a`  
		Last Modified: Fri, 11 Mar 2022 11:58:06 GMT  
		Size: 8.6 KB (8627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc54b8f158c76d34e38d0c775f45fd5ea1d90081f9b39de195edc2292a9440f`  
		Last Modified: Fri, 11 Mar 2022 15:15:09 GMT  
		Size: 2.1 MB (2128890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5ab251f615bb12a25f27266a16134786dc7ff3296f34801e1f2903c314190a`  
		Last Modified: Fri, 11 Mar 2022 15:15:08 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f0ca3a12e3326c01f0b284a4e8583e0ec647b43b88a81dc57125dc1d15139d`  
		Last Modified: Wed, 16 Mar 2022 18:52:23 GMT  
		Size: 575.7 KB (575715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24dc8610d15544ebe3e92211c2c8e985d1a7dccf8779670bad491007ddb82967`  
		Last Modified: Wed, 16 Mar 2022 18:52:22 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9040dcd7ee4e2984704d683d6a8d49f436d30593d3ec7b03b1936a1512187ccd`  
		Last Modified: Wed, 16 Mar 2022 18:52:40 GMT  
		Size: 19.1 MB (19136430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:rc-php8.1-fpm-buster` - linux; ppc64le

```console
$ docker pull drupal@sha256:cb72978b5836225eeb7230345eeee04c2cba6022f56c950af891e97e99dd2866
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.3 MB (173311364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da204f35e125c25287046fa33ea6deb99ec64f52f0660a9d4c487177760028a1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 01 Mar 2022 02:06:09 GMT
ADD file:005ec6e437fc9cf8458edb6369462ce53feb585501ea6b5e5f4a6264557b3a01 in / 
# Tue, 01 Mar 2022 02:06:14 GMT
CMD ["bash"]
# Wed, 02 Mar 2022 20:22:52 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Wed, 02 Mar 2022 20:22:54 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 02 Mar 2022 20:25:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 20:25:27 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 02 Mar 2022 20:25:37 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Wed, 02 Mar 2022 20:25:41 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Mar 2022 20:25:44 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 02 Mar 2022 20:25:47 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 02 Mar 2022 20:25:51 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Wed, 02 Mar 2022 20:25:54 GMT
ENV PHP_VERSION=8.1.3
# Wed, 02 Mar 2022 20:25:57 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Wed, 02 Mar 2022 20:25:59 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Wed, 02 Mar 2022 20:28:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Wed, 02 Mar 2022 20:28:43 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:30:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Fri, 11 Mar 2022 03:30:31 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Fri, 11 Mar 2022 03:30:39 GMT
RUN docker-php-ext-enable sodium
# Fri, 11 Mar 2022 03:30:41 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Fri, 11 Mar 2022 03:30:45 GMT
WORKDIR /var/www/html
# Fri, 11 Mar 2022 03:30:51 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Fri, 11 Mar 2022 03:30:53 GMT
STOPSIGNAL SIGQUIT
# Fri, 11 Mar 2022 03:30:55 GMT
EXPOSE 9000
# Fri, 11 Mar 2022 03:30:57 GMT
CMD ["php-fpm"]
# Fri, 11 Mar 2022 11:15:57 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Mar 2022 11:16:08 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Wed, 16 Mar 2022 20:25:51 GMT
COPY file:608f7625682057a8f327a57b0a8d1d350465d3209e7a8c9e119158b6dc4b876a in /usr/local/bin/ 
# Wed, 16 Mar 2022 20:25:55 GMT
ENV DRUPAL_VERSION=10.0.0-alpha2
# Wed, 16 Mar 2022 20:25:59 GMT
WORKDIR /opt/drupal
# Wed, 16 Mar 2022 20:26:38 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Wed, 16 Mar 2022 20:26:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:3cee81bb9485c9d0b620c87842e566d7a1f93086ef88c00a4d7175fc776b7f3f`  
		Last Modified: Tue, 01 Mar 2022 02:16:22 GMT  
		Size: 30.6 MB (30562288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f989091e71df355cb7529f6c58e9eb907346356079848598c517d3f81d5b995`  
		Last Modified: Thu, 03 Mar 2022 02:09:41 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b433eb8ed01760479b9fe8c020598e6f51b2bfa766b60ef5b70c04c79b1505`  
		Last Modified: Thu, 03 Mar 2022 02:10:45 GMT  
		Size: 82.3 MB (82291771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8a110a95bdc94e2027f47a128712d8a24e8709cac0adb3e1b27e3ff5d3c3b8`  
		Last Modified: Thu, 03 Mar 2022 02:09:39 GMT  
		Size: 270.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fa14fed4ea584b3782086c2e744bc27e58036a6f1b29b7b8ecd9e094014c146`  
		Last Modified: Thu, 03 Mar 2022 02:09:38 GMT  
		Size: 12.1 MB (12073703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b04024973af9325614c1fdb9eb024288d37e43bf7cff88d196c3ade08e1ff3`  
		Last Modified: Thu, 03 Mar 2022 02:09:36 GMT  
		Size: 488.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4478e1d3d7195cb5c376086e7ef5f8222b629eab37c2315fd025bcf7ef82b6c`  
		Last Modified: Fri, 11 Mar 2022 09:51:22 GMT  
		Size: 26.7 MB (26730999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b20b81f68776dcc01c44a2384183e6195bbbb3c571608df04004757744eeae5`  
		Last Modified: Fri, 11 Mar 2022 09:51:15 GMT  
		Size: 2.3 KB (2308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:145584ce85808a403ec7e1a53085a4d7c01214f74f4e3b3cb6286c20b557cba6`  
		Last Modified: Fri, 11 Mar 2022 09:51:15 GMT  
		Size: 247.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64de3fc301898d0aa518a30b6a4db58cf943a767c8d0592d370d7899c6e7b6d`  
		Last Modified: Fri, 11 Mar 2022 09:51:16 GMT  
		Size: 8.6 KB (8624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0d600887173bde1de8bc611242c91b64236dcc1bc5595a0862ed8d2e9e70c5e`  
		Last Modified: Fri, 11 Mar 2022 12:43:55 GMT  
		Size: 1.9 MB (1927615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9be351cbe315208e4fd52617417a35285c2a87ce07ffb80bca0d5c373d1e82e3`  
		Last Modified: Fri, 11 Mar 2022 12:43:51 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fdff14151e3d0ac2d7aa0a60f014de81dd62fc0d7fde7fa512ebaf02e08e1e`  
		Last Modified: Wed, 16 Mar 2022 21:31:22 GMT  
		Size: 575.7 KB (575717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e9a04190c7623d062e424cbe3cc9b56ae711ed689e459eb159474ad2b0d35c`  
		Last Modified: Wed, 16 Mar 2022 21:31:21 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15407d98e17b8d978281703060ed61b205521715069990aa2d6d3e6123528bb`  
		Last Modified: Wed, 16 Mar 2022 21:34:00 GMT  
		Size: 19.1 MB (19136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `drupal:rc-php8.1-fpm-buster` - linux; s390x

```console
$ docker pull drupal@sha256:001175e266737a274ab8bbdcc3af94cf94a7f7f82a421ee509bbfeb748db35ef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148657263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62367300a0c89c6f03ae2a88d6cda96b2420637afc3aeef93b0106cdb8c220e3`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 17 Mar 2022 03:07:30 GMT
ADD file:4342e1d9db757e91953273ac7120c9d6004d38281f9cea830898b4f35ca43517 in / 
# Thu, 17 Mar 2022 03:07:32 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 09:08:13 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 17 Mar 2022 09:08:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 17 Mar 2022 09:08:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 09:08:31 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 17 Mar 2022 09:08:32 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 777 /var/www/html
# Thu, 17 Mar 2022 09:08:32 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Mar 2022 09:08:32 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 17 Mar 2022 09:08:32 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 17 Mar 2022 09:08:32 GMT
ENV GPG_KEYS=528995BFEDFBA7191D46839EF9BA0ADA31CBD89E 39B641343D8C104B2B146DC3F9C39DC0B9698544 F1F692238FBC1666E5A5CCD4199F9DFEF6FFBAFD
# Thu, 17 Mar 2022 09:38:18 GMT
ENV PHP_VERSION=8.1.3
# Thu, 17 Mar 2022 09:38:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.1.3.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.1.3.tar.xz.asc
# Thu, 17 Mar 2022 09:38:18 GMT
ENV PHP_SHA256=5d65a11071b47669c17452fb336c290b67c101efb745c1dbe7525b5caf546ec6
# Thu, 17 Mar 2022 09:39:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg dirmngr; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 17 Mar 2022 09:39:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 17 Mar 2022 09:46:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-ftp 		--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 's390x-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 17 Mar 2022 09:46:10 GMT
COPY multi:7d7d4b016ee2e2e18720a1a58004eb4d59de798c619f217398cc1066a656bfd0 in /usr/local/bin/ 
# Thu, 17 Mar 2022 09:46:10 GMT
RUN docker-php-ext-enable sodium
# Thu, 17 Mar 2022 09:46:11 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 17 Mar 2022 09:46:11 GMT
WORKDIR /var/www/html
# Thu, 17 Mar 2022 09:46:11 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; if we send this to /proc/self/fd/1, it never appears'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf
# Thu, 17 Mar 2022 09:46:11 GMT
STOPSIGNAL SIGQUIT
# Thu, 17 Mar 2022 09:46:11 GMT
EXPOSE 9000
# Thu, 17 Mar 2022 09:46:12 GMT
CMD ["php-fpm"]
# Thu, 17 Mar 2022 21:10:46 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { print $3 }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 21:10:46 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 		echo 'opcache.fast_shutdown=1'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini
# Thu, 17 Mar 2022 21:10:46 GMT
COPY file:608f7625682057a8f327a57b0a8d1d350465d3209e7a8c9e119158b6dc4b876a in /usr/local/bin/ 
# Thu, 17 Mar 2022 21:10:46 GMT
ENV DRUPAL_VERSION=10.0.0-alpha2
# Thu, 17 Mar 2022 21:10:47 GMT
WORKDIR /opt/drupal
# Thu, 17 Mar 2022 21:11:08 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME"
# Thu, 17 Mar 2022 21:11:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:6f8a08956872b0f67802da3a67e007322eb963a60e0dadd736077f3ece414e1f`  
		Last Modified: Thu, 17 Mar 2022 03:13:18 GMT  
		Size: 25.8 MB (25769076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc72acd2dc6ea4ea7e921a154c127beeb2bbe65bb77a3770e49e4f7a5d38d51`  
		Last Modified: Thu, 17 Mar 2022 11:56:03 GMT  
		Size: 225.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c130d936c6d923444315825d6c86136e0f51e13f08d9159fad3d8c3fbddef678`  
		Last Modified: Thu, 17 Mar 2022 11:56:12 GMT  
		Size: 64.7 MB (64712322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de0c874059d92bfeaa8d5758b9fc43758f30edfea4543ad5c67b4230f2fea34c`  
		Last Modified: Thu, 17 Mar 2022 11:56:03 GMT  
		Size: 269.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ffda9ca39929283cf6dbe699359ba556bffa9243aafbac787c6227b02b47c42`  
		Last Modified: Thu, 17 Mar 2022 11:59:40 GMT  
		Size: 12.1 MB (12072227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e2dff66e2920fa7d197c8568ee6e7e8bc95558479724db0055a0e5f6ec8cc1`  
		Last Modified: Thu, 17 Mar 2022 11:59:39 GMT  
		Size: 490.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e9dc0a2edd86b61ed8ee5a820ac0b3c2cd7bf87b2417098ded518623352a03`  
		Last Modified: Thu, 17 Mar 2022 12:00:18 GMT  
		Size: 24.7 MB (24721401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01622999a27a99bd5c5a2627d859aeaf96c8a4fb8d4e3913310db2b858d33f5e`  
		Last Modified: Thu, 17 Mar 2022 12:00:15 GMT  
		Size: 2.3 KB (2305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d3fee69e75f84e8def1cf070ca8250bcc65f960575b323c1fa0262bac40143`  
		Last Modified: Thu, 17 Mar 2022 12:00:15 GMT  
		Size: 245.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e752eccfd081262a579946032f73737656e75f1d9357b07cea9a71412abc27b8`  
		Last Modified: Thu, 17 Mar 2022 12:00:15 GMT  
		Size: 8.6 KB (8624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc9fe80519af4391f369e436098be8d26867790f46a4fa923e7471b0366c2fe1`  
		Last Modified: Thu, 17 Mar 2022 21:36:06 GMT  
		Size: 1.7 MB (1657303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb73265871261a89a6fde50a3b15ec5247ca030482a833f9e3482678ba3c6a60`  
		Last Modified: Thu, 17 Mar 2022 21:36:05 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c616cb7d350de5acfbbcb8c0976e6700e74f51dc48765faacc2e2a8fe0cf71`  
		Last Modified: Thu, 17 Mar 2022 21:36:06 GMT  
		Size: 575.7 KB (575710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beea9c78fb1ebc7e54eddc386cc30832140e025e8655700e27488b67f4638891`  
		Last Modified: Thu, 17 Mar 2022 21:36:05 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b3c1fe2f626ec4ebd7ba085d514b7cc4b837888c7f8c33a68f21656566628fd`  
		Last Modified: Thu, 17 Mar 2022 21:36:09 GMT  
		Size: 19.1 MB (19136589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
