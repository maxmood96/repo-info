## `drupal:php8.2-fpm-bullseye`

```console
$ docker pull drupal@sha256:010b648e44d3978d33c6d6b39bad498f12a1af4e98090b7bb7d9525cce28884b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 12
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `drupal:php8.2-fpm-bullseye` - linux; amd64

```console
$ docker pull drupal@sha256:80b28d35bbe5ebcd2a12901d587557da1d381ac2a10f56680fcea8b698251259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.7 MB (185743369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d9b959e5486bf7f9c5a420c69928a8fcbb001d10e246ac8021b8765fd7b2a6`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:24 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Tue, 02 Jul 2024 01:25:24 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 02:25:08 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 02 Jul 2024 02:25:08 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 02 Jul 2024 02:25:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 02:25:26 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jul 2024 02:25:26 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 02 Jul 2024 02:25:26 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 02:25:26 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 02:25:27 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jul 2024 03:23:32 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_VERSION=8.2.21
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.21.tar.xz.asc
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_SHA256=8cc44d51bb2506399ec176f70fe110f0c9e1f7d852a5303a2cd1403402199707
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 04 Jul 2024 15:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 04 Jul 2024 15:27:17 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 04 Jul 2024 15:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 04 Jul 2024 15:27:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Jul 2024 15:27:17 GMT
EXPOSE 9000
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["php-fpm"]
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV DRUPAL_VERSION=10.3.1
# Thu, 04 Jul 2024 15:27:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /opt/drupal
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35dbe43e30a1ec070f064e78ba481c34bcddadbad30a2204b3674f7551121b4e`  
		Last Modified: Tue, 02 Jul 2024 04:37:51 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759ee6bd3706c33b42cb784d34dec8a4eabbea15cfca2530b93bb24821b7adc1`  
		Last Modified: Tue, 02 Jul 2024 04:38:06 GMT  
		Size: 91.7 MB (91650270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3df42241e90d0821c6beaae0b632772ca7c45471efc1fd020bb51049f741038`  
		Last Modified: Tue, 02 Jul 2024 04:37:51 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c251148b228b819d10ee71f98b42158200bb5d4be366dff634ea62bb78604bb`  
		Last Modified: Sat, 06 Jul 2024 02:30:48 GMT  
		Size: 12.4 MB (12425800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84e382c214cadc4b15d79300925d7c3af04eab414d843bb55ed06513cf2bace`  
		Last Modified: Sat, 06 Jul 2024 02:30:47 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac246b52d8150921bce68f45697fdebe9a79825269fc081ee2861f7d2fa0087`  
		Last Modified: Sat, 06 Jul 2024 02:31:21 GMT  
		Size: 26.5 MB (26520305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361f7ffe2cd2eb46e44253a55241d14a4291100dff7abdc22ba5cfc1e3eef02c`  
		Last Modified: Sat, 06 Jul 2024 02:31:18 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fee4229474776ed718358276db1c8d0122e75cd67ce94eb5cecb5757e429a531`  
		Last Modified: Sat, 06 Jul 2024 02:31:18 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908cadf1d89c4997e1ae529a74d50d2b08ffa279d2990a3b44bfbc2a1d1c4715`  
		Last Modified: Sat, 06 Jul 2024 02:31:18 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30fca60dbe3755284e0873992a769be285ae3d31bba58a493089e3f996b83354`  
		Last Modified: Sat, 06 Jul 2024 05:55:20 GMT  
		Size: 1.9 MB (1902220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7d4d674d0c52a42777e6be2a6bec6b89f1bf77c25250dd2c71aa861a1f2ec6c`  
		Last Modified: Sat, 06 Jul 2024 05:55:20 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b936255303ad92c1080cd13ef498992afaf059077dd617b296c65411ab4107`  
		Last Modified: Sat, 06 Jul 2024 05:55:20 GMT  
		Size: 726.3 KB (726344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab307329c4b6f0cae34aea016efa620729d96abe98eceafd71eb05bfd2fd0556`  
		Last Modified: Sat, 06 Jul 2024 05:55:20 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97b6bac49bbe447a29f4b09e0ce91c53aec298aa469f4f53c17bce20081c2b92`  
		Last Modified: Sat, 06 Jul 2024 05:55:21 GMT  
		Size: 21.1 MB (21082895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.2-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:117af2ffa238b6459b2ca04040a03e61b93147616c3fbc41a43f0d52c5075686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6471276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d78afda3c92e35cb608358fc3874a4dd2f91ae64aa41e23f5fbfa4e8404883`

```dockerfile
```

-	Layers:
	-	`sha256:3d9a21c8c40f69cb634d014beb635bf77901d3ed928ca47cd64944892383f146`  
		Last Modified: Sat, 06 Jul 2024 05:55:20 GMT  
		Size: 6.4 MB (6437399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45ad679f75c1b47a43a97c2f0d9e04f0e0b421ad57cfef5cb24f63ea3e2e3c9c`  
		Last Modified: Sat, 06 Jul 2024 05:55:20 GMT  
		Size: 33.9 KB (33877 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.2-fpm-bullseye` - linux; arm variant v7

```console
$ docker pull drupal@sha256:60da39f1f423c63623c82edbc02d4c8876e314f6261e9d0ae6ba22184566a6e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.7 MB (155680431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ad99d1d84af6170c46d9e4f137c8ef85a1ceb60f53c369180ea0b00ba6dc12c`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 02 Jul 2024 01:00:21 GMT
ADD file:563299626f09e20ec4b37394c5283e43db5efc7b5e37a08ddd5c45ffb7abfec2 in / 
# Tue, 02 Jul 2024 01:00:22 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 02:02:04 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 02 Jul 2024 02:02:04 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 02 Jul 2024 02:02:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 02:02:25 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jul 2024 02:02:25 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 02 Jul 2024 02:02:25 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 02:02:25 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 02:02:26 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jul 2024 02:52:05 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_VERSION=8.2.21
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.21.tar.xz.asc
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_SHA256=8cc44d51bb2506399ec176f70fe110f0c9e1f7d852a5303a2cd1403402199707
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 04 Jul 2024 15:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 04 Jul 2024 15:27:17 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 04 Jul 2024 15:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 04 Jul 2024 15:27:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Jul 2024 15:27:17 GMT
EXPOSE 9000
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["php-fpm"]
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV DRUPAL_VERSION=10.3.1
# Thu, 04 Jul 2024 15:27:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /opt/drupal
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:bdce93002696ef4b66001b32686cd3da5bf3a88d3cd2d2b3b65fb9755b1f1f83`  
		Last Modified: Tue, 02 Jul 2024 01:04:00 GMT  
		Size: 26.6 MB (26582706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7169340bbc9b11466dc02ad185ab4ec5be5ae3f2d1bfadf025062aee784d7cf8`  
		Last Modified: Tue, 02 Jul 2024 03:58:29 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33cc5c115210ef3a85f7c10ea07381ce083592b603b1061dc201bea60ecafbd`  
		Last Modified: Tue, 02 Jul 2024 03:58:41 GMT  
		Size: 69.3 MB (69327786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4fcbcd04aaf63c6b9ff83a247cf90682f60d62cabedfca5e92463f2e670db42`  
		Last Modified: Tue, 02 Jul 2024 03:58:29 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd9c43180353464b7b2e185c22e0ca174d2949cee1c98e5dcf9ab3d36bded16`  
		Last Modified: Sat, 06 Jul 2024 02:50:35 GMT  
		Size: 12.4 MB (12424077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7a99f75bbee3d4db25a10578b25f6e43a5bd383c139efdb2a9efe048d9aee8`  
		Last Modified: Sat, 06 Jul 2024 02:50:33 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11bb58e3a48c35b93c95ae9181e979eaece3565f35573b43850bdfa692a62e2`  
		Last Modified: Sat, 06 Jul 2024 02:51:06 GMT  
		Size: 24.2 MB (24240706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e13d6624bce625ef2799c171d8640b9c622c99f0778dbc64727e87597a5c943`  
		Last Modified: Sat, 06 Jul 2024 02:51:02 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:121bcc6c973517afd1df7def31a60f10bd9666c3bd3f0861ca80d40599a5f48a`  
		Last Modified: Sat, 06 Jul 2024 02:51:02 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe41ee2aed8dfeee3aa4b7dd7696b822d0dc311a28abb4a58515d98290ffef8`  
		Last Modified: Sat, 06 Jul 2024 02:51:02 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1942eead08177dc9c37c976890ad7a0afb0562c526784b4f85ad0c5fd42687a`  
		Last Modified: Sat, 06 Jul 2024 05:27:58 GMT  
		Size: 1.3 MB (1282864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0e3bb120f18eb9531e370d3dbd820c26c42a0fb30829f35edb217bd9f56600`  
		Last Modified: Sat, 06 Jul 2024 05:27:58 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a898f8f4d872287053146cdbaf9d2347a40a4561615ebaefab75cb24edde80a0`  
		Last Modified: Sat, 06 Jul 2024 06:05:32 GMT  
		Size: 726.3 KB (726340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026b18c12066b360211344f2bce3aa2939f2937dc25635040ae33be37be8b222`  
		Last Modified: Sat, 06 Jul 2024 06:05:31 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c81f630f60e3ae4821e8fd6379c2125ba86347d55506083663a6848e13deea`  
		Last Modified: Sat, 06 Jul 2024 06:15:25 GMT  
		Size: 21.1 MB (21082701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.2-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:f1b121d4508dd7ffd3ebb913c8abcfa6e6ae083ff33d69f8e4c9d49a323b9a7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6281111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5be1b84ea8fb2a4f142d7e99822e43f071d595a964143f2bfe65ad314e888f4`

```dockerfile
```

-	Layers:
	-	`sha256:96a8d276d90896960310c852daa0f33872e9a1aba1b14a91e27a820bf9162da5`  
		Last Modified: Sat, 06 Jul 2024 06:15:24 GMT  
		Size: 6.2 MB (6247030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c821b3c43b7b378f2f3f1252b4a3ef0bacb4a7e4a9be5ac116b73fed3692363b`  
		Last Modified: Sat, 06 Jul 2024 06:15:24 GMT  
		Size: 34.1 KB (34081 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.2-fpm-bullseye` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:dc043d47ea9a9148609d9f10fc2fc9d4232b60316a316a2cd2f26c3091efdd97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.0 MB (180007089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:988fdec23b8565be28b55e3e64f68cc3f472000c3e4cc8dd79afa9f7a3c062d1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:52 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Tue, 02 Jul 2024 00:39:52 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:33:55 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 02 Jul 2024 01:33:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 02 Jul 2024 01:34:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:34:14 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jul 2024 01:34:15 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 02 Jul 2024 01:34:15 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:34:15 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:34:15 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jul 2024 02:29:53 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_VERSION=8.2.21
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.21.tar.xz.asc
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_SHA256=8cc44d51bb2506399ec176f70fe110f0c9e1f7d852a5303a2cd1403402199707
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 04 Jul 2024 15:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 04 Jul 2024 15:27:17 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 04 Jul 2024 15:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 04 Jul 2024 15:27:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Jul 2024 15:27:17 GMT
EXPOSE 9000
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["php-fpm"]
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV DRUPAL_VERSION=10.3.1
# Thu, 04 Jul 2024 15:27:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /opt/drupal
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c335aec71aeb153fbea1427f7ea534c8097ca1898940f18317d638023574b8ee`  
		Last Modified: Tue, 02 Jul 2024 03:37:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68bc195ca28e4f92808a4f6fd9b73331db6859db9e2ec74c189e231c415818e0`  
		Last Modified: Tue, 02 Jul 2024 03:38:01 GMT  
		Size: 86.9 MB (86939700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451e19963414458f43c8264137cea0d3aaaf9648417827bdcd7a2db62f7e0f89`  
		Last Modified: Tue, 02 Jul 2024 03:37:52 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a57958683b0eea533993f93e768a17d10f6a79d4e0fff29d97971d936dba0c`  
		Last Modified: Sat, 06 Jul 2024 02:35:00 GMT  
		Size: 12.4 MB (12424963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd57851ea7f26b0bcc936c83d53364dab036728447da69d58a570c5b637e12af`  
		Last Modified: Sat, 06 Jul 2024 02:34:59 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64aa2f92083b4b4c1cc89511e0c7d0805bf847cc1b74e295ba834e1fcf06d78c`  
		Last Modified: Sat, 06 Jul 2024 02:35:29 GMT  
		Size: 26.6 MB (26581720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac7d88b9ef5baac418397719f0c0a07fbbac56011b44acfa1aaf164b3d35ba2b`  
		Last Modified: Sat, 06 Jul 2024 02:35:26 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81aed00084e40c3af5e83d0e68eb3d6879c105f084f24fd11e49e4a263139123`  
		Last Modified: Sat, 06 Jul 2024 02:35:26 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86fef0b01bae60d97305d3c08697fcffb71388dff787ff438ebc5127d0fdaca8`  
		Last Modified: Sat, 06 Jul 2024 02:35:26 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7313704fb4203a4e3aa38e972e60eb116bd20b2047adc4866c7270f2f4d41dcd`  
		Last Modified: Sat, 06 Jul 2024 05:13:30 GMT  
		Size: 2.2 MB (2168781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03b11906b162582b0a05af60b6895e75a8cdc0bb78e6766a7daf6fa3c68fe596`  
		Last Modified: Sat, 06 Jul 2024 05:13:30 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aade24b81c8c9223858658bda7aa38021d352d6481a9691a44e48751d39306c`  
		Last Modified: Sat, 06 Jul 2024 06:08:11 GMT  
		Size: 726.3 KB (726340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16215ce322c46eeb64d9e92b651d31e9dc7da5dc900ed28699dd60fcb79aa94d`  
		Last Modified: Sat, 06 Jul 2024 06:08:11 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69048ec444e2d1daa68a327a533998344c4133dbeaccc1f0c138a92561acdee0`  
		Last Modified: Sat, 06 Jul 2024 06:15:48 GMT  
		Size: 21.1 MB (21082724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.2-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:92e7149d7e67761eb813097f568e3c716df0eae4d8cfe0aa5857ceba8ab90e96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6475085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82d69d179e5074c5aad0643480a720165ac122ef7e56fa8fbbdcc63c3b7c7b4`

```dockerfile
```

-	Layers:
	-	`sha256:6efe4c26305c1cbf81efc1cee9e9f1898df02f1e9fc39a656edb06d6432bd3db`  
		Last Modified: Sat, 06 Jul 2024 06:15:48 GMT  
		Size: 6.4 MB (6440475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3482fee5dbb081c4fb00c162a99a430a5c5460328844d143b3b8fdec31629c22`  
		Last Modified: Sat, 06 Jul 2024 06:15:47 GMT  
		Size: 34.6 KB (34610 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.2-fpm-bullseye` - linux; 386

```console
$ docker pull drupal@sha256:2d3c52c7e1ed10ed034a5856e13b390b5f62149fad14fc89006f9e9242d67eef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.4 MB (188356214 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4da378c2689508204c6c3d09a370e320eb7527747a873bca758b7ce4a3650679`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:16 GMT
ADD file:82c5579b81dad9a5dff7724fd8e74d225f919e378995a95c9a0a9c17ca55a77a in / 
# Tue, 02 Jul 2024 00:39:17 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 02:08:16 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 02 Jul 2024 02:08:16 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 02 Jul 2024 02:08:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 02:08:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jul 2024 02:08:43 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 02 Jul 2024 02:08:43 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 02:08:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 02:08:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jul 2024 03:42:33 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Tue, 02 Jul 2024 04:29:20 GMT
ENV PHP_VERSION=8.2.20
# Tue, 02 Jul 2024 04:29:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.20.tar.xz.asc
# Tue, 02 Jul 2024 04:29:20 GMT
ENV PHP_SHA256=4474cc430febef6de7be958f2c37253e5524d5c5331a7e1765cd2d2234881e50
# Tue, 02 Jul 2024 04:29:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Tue, 02 Jul 2024 04:29:32 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:45:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Tue, 02 Jul 2024 04:45:05 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Tue, 02 Jul 2024 04:45:05 GMT
RUN docker-php-ext-enable sodium
# Tue, 02 Jul 2024 04:45:05 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Tue, 02 Jul 2024 04:45:05 GMT
WORKDIR /var/www/html
# Tue, 02 Jul 2024 04:45:06 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Tue, 02 Jul 2024 04:45:06 GMT
STOPSIGNAL SIGQUIT
# Tue, 02 Jul 2024 04:45:06 GMT
EXPOSE 9000
# Tue, 02 Jul 2024 04:45:06 GMT
CMD ["php-fpm"]
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV DRUPAL_VERSION=10.3.1
# Thu, 04 Jul 2024 15:27:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /opt/drupal
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:1084208571fd0651d255a493f4e05ba8b2b837b52064c5f2f317a2d979e679bc`  
		Last Modified: Tue, 02 Jul 2024 00:43:26 GMT  
		Size: 32.4 MB (32408452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:850ab6efef12df0de52bf9e83bb54eeb04b25e4bddee111bb8de64345305496a`  
		Last Modified: Tue, 02 Jul 2024 05:40:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90549434c6bff14f52cbc9958e76ddae4f172308e4aba9cdcc10c126accc3b94`  
		Last Modified: Tue, 02 Jul 2024 05:41:16 GMT  
		Size: 92.7 MB (92720434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e55f446fcc5301935ef2eed4717ce1921ca07f5b60bea264e88372cd08c54e8`  
		Last Modified: Tue, 02 Jul 2024 05:40:56 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fdd1c57eb8ac7d6bc0b261089aba13026fcf91778a87bbdb0607bc530c669a0`  
		Last Modified: Tue, 02 Jul 2024 05:49:24 GMT  
		Size: 12.4 MB (12416709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec5e2b9ac200ec13425233c33b2c1a93b60880632e4727a04f80b7ea55d0739`  
		Last Modified: Tue, 02 Jul 2024 05:49:23 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:361d6ce4d36899743aa88388f9438c5360cd953384a59bbae3aea72a62850ba5`  
		Last Modified: Tue, 02 Jul 2024 05:49:58 GMT  
		Size: 27.0 MB (27018460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907f02b018a5a1c8630964183c294bec80beb95b9cc2fcb936805c689c64dc74`  
		Last Modified: Tue, 02 Jul 2024 05:49:52 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae396cd9cb1bc56adbf863a3c9d5bee40d46e141898f73b1746bc38b6275173`  
		Last Modified: Tue, 02 Jul 2024 05:49:52 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c992ead2a6fcfb09b2433a6c01c55996a98f5e8aa1f244f60aa1546e7844c4`  
		Last Modified: Tue, 02 Jul 2024 05:49:52 GMT  
		Size: 9.2 KB (9177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e01f11d8c2f4bc7d2965b5350ed729d35aaf5674b575c329f8c31ea3f9a26dc`  
		Last Modified: Sat, 06 Jul 2024 00:57:15 GMT  
		Size: 2.0 MB (1969955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32accb5c2a31d9c63853c79aaea45c9f04f0b103720a471eb42e7da0cf08af2d`  
		Last Modified: Sat, 06 Jul 2024 00:57:15 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37758b9d0c16a63ab9c5eabd059b881f229d5690fc2d80436c3add326237bc8`  
		Last Modified: Sat, 06 Jul 2024 00:57:16 GMT  
		Size: 726.3 KB (726339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fde7b1dc5c3e276de34e48841da644568e5a8ac04a1893b74420dcf87a75becf`  
		Last Modified: Sat, 06 Jul 2024 00:57:16 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71637911350b3b39bb68d820fb348ce64dd82954e34d562e6976e4d2a590e711`  
		Last Modified: Sat, 06 Jul 2024 00:57:17 GMT  
		Size: 21.1 MB (21082626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.2-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:3cd71b67c9e15b2372f181c8587e51f4955075ed0d43fcddd70b1ecfa33f338b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6462350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c5d8a975aa8dd325ba51ea4b8e8b381bde2c693b8fbd3e4d828585a9639bbc3`

```dockerfile
```

-	Layers:
	-	`sha256:50f25905e2860cf96c945ba5640d3bd2771241865c0254041f2d420c7a10cdbc`  
		Last Modified: Sat, 06 Jul 2024 00:57:16 GMT  
		Size: 6.4 MB (6428533 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:100b16c7b93e5d4d8f8a8e601eae8ebaf2edbd64e2eeb20c0ceeacbf7672b373`  
		Last Modified: Sat, 06 Jul 2024 00:57:15 GMT  
		Size: 33.8 KB (33817 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.2-fpm-bullseye` - linux; ppc64le

```console
$ docker pull drupal@sha256:593b95eef92d4584df52f2a828c4852bdcca087ef7a0b17518253cc36f8a69ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185567275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d48cbd04b9e6dbedda59d2679f33ab7db0375b278637f6760adbf12d9c078476`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 20 Jun 2024 21:27:23 GMT
ADD file:8fcbfde241e9377ada40ad73089516c86d20e018c99a8192ba63a50f0168b8b9 in / 
# Thu, 20 Jun 2024 21:27:23 GMT
CMD ["bash"]
# Thu, 20 Jun 2024 21:27:23 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 20 Jun 2024 21:27:23 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 20 Jun 2024 21:27:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 20 Jun 2024 21:27:23 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 20 Jun 2024 21:27:23 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 20 Jun 2024 21:27:23 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 21:27:23 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 20 Jun 2024 21:27:23 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 20 Jun 2024 21:27:23 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 20 Jun 2024 21:27:23 GMT
ENV PHP_VERSION=8.2.20
# Thu, 20 Jun 2024 21:27:23 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.20.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.20.tar.xz.asc
# Thu, 20 Jun 2024 21:27:23 GMT
ENV PHP_SHA256=4474cc430febef6de7be958f2c37253e5524d5c5331a7e1765cd2d2234881e50
# Thu, 20 Jun 2024 21:27:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 20 Jun 2024 21:27:23 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 20 Jun 2024 21:27:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 20 Jun 2024 21:27:23 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 20 Jun 2024 21:27:23 GMT
RUN docker-php-ext-enable sodium
# Thu, 20 Jun 2024 21:27:23 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 20 Jun 2024 21:27:23 GMT
WORKDIR /var/www/html
# Thu, 20 Jun 2024 21:27:23 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 20 Jun 2024 21:27:23 GMT
STOPSIGNAL SIGQUIT
# Thu, 20 Jun 2024 21:27:23 GMT
EXPOSE 9000
# Thu, 20 Jun 2024 21:27:23 GMT
CMD ["php-fpm"]
# Thu, 20 Jun 2024 21:27:23 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 20 Jun 2024 21:27:23 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 20 Jun 2024 21:27:23 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 20 Jun 2024 21:27:23 GMT
ENV DRUPAL_VERSION=10.3.0
# Thu, 20 Jun 2024 21:27:23 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 20 Jun 2024 21:27:23 GMT
WORKDIR /opt/drupal
# Thu, 20 Jun 2024 21:27:23 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 20 Jun 2024 21:27:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:687d52b24394339ceb9470debd0e5f0d6b612ceb063cc228cbef23d23fb7f6a2`  
		Last Modified: Tue, 02 Jul 2024 01:22:46 GMT  
		Size: 35.3 MB (35299189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:339f489d1e564c9c7d91a1bafdbd753bea976cf7d4e49aac09781b3a7179dffa`  
		Last Modified: Tue, 02 Jul 2024 04:16:16 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f44c23a5c69cce13d9ff3aa0ee9590ebb9a7850465f19d2721100e288312e7b9`  
		Last Modified: Tue, 02 Jul 2024 04:16:31 GMT  
		Size: 86.6 MB (86647997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4efbc073f0d2c267667e6f9fa4d3a5d430b0c9e921cd8823dc6cd7b4d22002d`  
		Last Modified: Tue, 02 Jul 2024 04:16:16 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83689ccace8a0b7e4265cc0b76c9f5c27f4205deb1c6dc3524ac4716559101db`  
		Last Modified: Tue, 02 Jul 2024 04:24:14 GMT  
		Size: 12.4 MB (12417290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d2a65a8c2e310e4a320a97165d3ae5234ae6a06488eaf10132594001694560`  
		Last Modified: Tue, 02 Jul 2024 04:24:13 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd09e870e60816dab57597b568ceef70615adb68a1754fa0975ec47caf84eb0f`  
		Last Modified: Tue, 02 Jul 2024 04:24:47 GMT  
		Size: 27.6 MB (27614432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5de0ea02f2ea847f5c18ca146aa1cc9e970e601d8e4548d598918546efb7e55`  
		Last Modified: Tue, 02 Jul 2024 04:24:42 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002b87e749833b7be75221913ff64f54102135a5f661f7629225381a3775020c`  
		Last Modified: Tue, 02 Jul 2024 04:24:43 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ddfa6d402c08435c9d9ac9fecc1c4e92b36452b24f6e98de4d8e5aa258aae0`  
		Last Modified: Tue, 02 Jul 2024 04:24:42 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7a6737dd963501e58dcbcde835c00a64063acc7a7c686cd1103dc2df62c76d`  
		Last Modified: Wed, 03 Jul 2024 01:12:31 GMT  
		Size: 1.8 MB (1768658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4254824dfaf01487f6d8eb37b3d69fc088b83693d33e981bf9d5f09dd297cf00`  
		Last Modified: Wed, 03 Jul 2024 01:12:30 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c88cdee4868b78750774323acd2d8a478fc875d9a060529d3752c4ed2e80dcb`  
		Last Modified: Wed, 03 Jul 2024 01:12:31 GMT  
		Size: 726.3 KB (726341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ff839f49fd31c73d192e668d6d891a39b68e298fb297f583f7701547289d03`  
		Last Modified: Wed, 03 Jul 2024 01:12:30 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82fdef0d6e332fc11d2c50d49afa2f901824aa0b603488bbf611f147fa8d97eb`  
		Last Modified: Wed, 03 Jul 2024 01:22:22 GMT  
		Size: 21.1 MB (21080108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.2-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:363f0fb37d65930f144d287fba294ce3c177451788ad1455c64fe0df76bee1b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6437196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9f99036551b7ef94e89bab9a9283ebffddb6993de3cd72c337e7b096671903`

```dockerfile
```

-	Layers:
	-	`sha256:b2fef00ae8eef4f3327d2a4b73d020efde379f747a80356d3fe45d3bb95d20ae`  
		Last Modified: Wed, 03 Jul 2024 01:22:20 GMT  
		Size: 6.4 MB (6403237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4b6080c1507fc7862084de2c042ce5214f0257db6ca4264809c10c2ead56d47`  
		Last Modified: Wed, 03 Jul 2024 01:22:20 GMT  
		Size: 34.0 KB (33959 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.2-fpm-bullseye` - linux; s390x

```console
$ docker pull drupal@sha256:35d895531e90464b19ae7d82ca40cc44f98c7cd675ad20f5b4a321d1af725958
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.8 MB (162796341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4192c35bd5937ba547b6a2b235b72ec0ec71e01c8e9fae6f7188e0c40213420`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 02 Jul 2024 00:44:15 GMT
ADD file:31ece4c92b8738b187a4c8ac4ec5558c9127823e7a57214b84a551afab6e97a0 in / 
# Tue, 02 Jul 2024 00:44:16 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:26:27 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 02 Jul 2024 01:26:27 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 02 Jul 2024 01:26:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:26:42 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 02 Jul 2024 01:26:42 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 02 Jul 2024 01:26:42 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:26:43 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 02 Jul 2024 01:26:43 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 02 Jul 2024 02:09:54 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_VERSION=8.2.21
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.21.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.21.tar.xz.asc
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PHP_SHA256=8cc44d51bb2506399ec176f70fe110f0c9e1f7d852a5303a2cd1403402199707
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 04 Jul 2024 15:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 04 Jul 2024 15:27:17 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 04 Jul 2024 15:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 04 Jul 2024 15:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /var/www/html
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 04 Jul 2024 15:27:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 04 Jul 2024 15:27:17 GMT
EXPOSE 9000
# Thu, 04 Jul 2024 15:27:17 GMT
CMD ["php-fpm"]
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV DRUPAL_VERSION=10.3.1
# Thu, 04 Jul 2024 15:27:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 04 Jul 2024 15:27:17 GMT
WORKDIR /opt/drupal
# Thu, 04 Jul 2024 15:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 04 Jul 2024 15:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:a3136cefab0552c07b47b507af992477c2b33aff541d74a1bdb0f0c475f008fe`  
		Last Modified: Tue, 02 Jul 2024 00:49:04 GMT  
		Size: 29.7 MB (29662353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17d7bf4982e21c3386b6bdf8634c3d59503cac65f62f788141a1b7410b7dae4`  
		Last Modified: Tue, 02 Jul 2024 03:06:09 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c47f9558ba7962aecc1f4c8fdf9a69dc59140624ff107a83d97ca9b2f2ea5f64`  
		Last Modified: Tue, 02 Jul 2024 03:06:19 GMT  
		Size: 71.6 MB (71641635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740b856ce936618b60f15e78d2808c90765f0df4fce2766a82eea320ba3d832f`  
		Last Modified: Tue, 02 Jul 2024 03:06:09 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc30c76d9a179a09cb27b9f6412c8f2f46a2c5e369ae3d1e1bdc62a6875c3d33`  
		Last Modified: Sat, 06 Jul 2024 02:11:34 GMT  
		Size: 12.4 MB (12424443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e6d632b05453587b904728d9b4c3532b85aeb040aa6881a7720eec5e81e7995`  
		Last Modified: Sat, 06 Jul 2024 02:11:33 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c339694d7f1d530e6cf6c4fc192fa401d2954487a6d42ec3f50c9d37c9fe5f9`  
		Last Modified: Sat, 06 Jul 2024 02:11:58 GMT  
		Size: 25.7 MB (25749748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa192f944d5e992dfb6cfd313e557518d6365cb83c5f93c1f46f4c241ecf05cb`  
		Last Modified: Sat, 06 Jul 2024 02:11:54 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:819e6ba175360e1b192c29a12fc8b9436c6ced85f5e948eb1639d620b46087f1`  
		Last Modified: Sat, 06 Jul 2024 02:11:54 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff186a1b878d7e650e9450a25ec580ef37cfc0f6a2c85343561ae0d2e52f84e1`  
		Last Modified: Sat, 06 Jul 2024 02:11:54 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6f24d880c49500b1283d53fafd9a6e577064642304f1efc0afb65e029c6eee0`  
		Last Modified: Sat, 06 Jul 2024 04:16:58 GMT  
		Size: 1.5 MB (1496108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bc05771d5403a98d28c659ef494b767ecee1426175db4327a4dcea35cd015ad`  
		Last Modified: Sat, 06 Jul 2024 04:16:59 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d5f75f62de33121b8f0d3bfde7bda1d1aef136aa530382ae932cd586edb5b0`  
		Last Modified: Sat, 06 Jul 2024 06:04:21 GMT  
		Size: 726.3 KB (726344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a1a8e1989ed499f605e9f60946f8a52097c50362bedd54652be8fa48be71e3`  
		Last Modified: Sat, 06 Jul 2024 06:04:21 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bbcb5a866f506f2733ef9a48503a129de8ab79b89e0d5035fc2ec2ae83768f6`  
		Last Modified: Sat, 06 Jul 2024 06:14:32 GMT  
		Size: 21.1 MB (21082466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.2-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:45a32f621abf880173b7a08981e26b35f28ec37bbac91edb5c218a1e24d254e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6302272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbaeccde0e10a94edd1ba274056fda5aa0595821e64f6a5b8cbc244f5911ba63`

```dockerfile
```

-	Layers:
	-	`sha256:105ca0fa801028d4b46954d0b863693f954d8c8957f48ed783230ff104a360c2`  
		Last Modified: Sat, 06 Jul 2024 06:14:31 GMT  
		Size: 6.3 MB (6268341 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1efd29c9f7e00c75909e32dd9d1f244739884cb2ee8c755bf3b66c883bac8468`  
		Last Modified: Sat, 06 Jul 2024 06:14:31 GMT  
		Size: 33.9 KB (33931 bytes)  
		MIME: application/vnd.in-toto+json
