## `drupal:10-fpm-bullseye`

```console
$ docker pull drupal@sha256:50d3291794128a0b7654a0fab8dab996b01cc92f07f123a30bbc6202d36a9694
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

### `drupal:10-fpm-bullseye` - linux; amd64

```console
$ docker pull drupal@sha256:2a852a5977af6001b2a29bf61b223c36eee44818acc4c250b84259d1f1307334
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.8 MB (185758148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34b30e1cb0323cc10ae2ce5aeee99b6a804b5a87b09fba1a86f7706a47e62dc`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 08 Aug 2024 15:27:17 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Thu, 08 Aug 2024 15:27:17 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 15:27:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 08 Aug 2024 15:27:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 08 Aug 2024 15:27:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 15:27:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 08 Aug 2024 15:27:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 08 Aug 2024 15:27:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 Aug 2024 15:27:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 Aug 2024 15:27:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 08 Aug 2024 15:27:17 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 08 Aug 2024 15:27:17 GMT
ENV PHP_VERSION=8.2.22
# Thu, 08 Aug 2024 15:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.22.tar.xz.asc
# Thu, 08 Aug 2024 15:27:17 GMT
ENV PHP_SHA256=8566229bc88ad1f4aadc10700ab5fbcec81587c748999d985f11cf3b745462df
# Thu, 08 Aug 2024 15:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 08 Aug 2024 15:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 08 Aug 2024 15:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 08 Aug 2024 15:27:17 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 08 Aug 2024 15:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 08 Aug 2024 15:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 08 Aug 2024 15:27:17 GMT
WORKDIR /var/www/html
# Thu, 08 Aug 2024 15:27:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 08 Aug 2024 15:27:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 08 Aug 2024 15:27:17 GMT
EXPOSE 9000
# Thu, 08 Aug 2024 15:27:17 GMT
CMD ["php-fpm"]
# Thu, 08 Aug 2024 15:27:17 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 15:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 08 Aug 2024 15:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 15:27:17 GMT
ENV DRUPAL_VERSION=10.3.2
# Thu, 08 Aug 2024 15:27:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 08 Aug 2024 15:27:17 GMT
WORKDIR /opt/drupal
# Thu, 08 Aug 2024 15:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 08 Aug 2024 15:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:82aabceedc2fbf89030cbb4ff98215b70d9ae35c780ade6c784d9b447b1109ed`  
		Last Modified: Tue, 13 Aug 2024 00:24:25 GMT  
		Size: 31.4 MB (31428287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69850db3b70130b8aeaf7110a636bd2b8c4a3a0d12cf989aed21752bfb6122c1`  
		Last Modified: Tue, 13 Aug 2024 02:55:19 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:039fb59cd47be93b0828b3e52cafa290c824ff61c15f5377dabca280768851ab`  
		Last Modified: Tue, 13 Aug 2024 02:55:31 GMT  
		Size: 91.6 MB (91648162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ab96e11c087119245593e7395698c4b442821ef447a9384a5c0b75449a6dd9d`  
		Last Modified: Tue, 13 Aug 2024 02:55:19 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd16ca6ea1427d7bf19ce5ca574cf1ffdd8e500c74fa22eb4852c1f31e424a51`  
		Last Modified: Tue, 13 Aug 2024 03:00:41 GMT  
		Size: 12.4 MB (12419230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef2b235c7aa21aaa723c52d6d8b390c15a857fab08e49b34debdf0c993bce714`  
		Last Modified: Tue, 13 Aug 2024 03:00:40 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a4fda0a11a314322c8ebdb00cc2242e1b08a811c138fec17094c4135232dc2`  
		Last Modified: Tue, 13 Aug 2024 03:01:13 GMT  
		Size: 26.5 MB (26521230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:099ece864c09fc40e0cad9abcd844b2eb3473b4918976a3ae40ce48df2e9c651`  
		Last Modified: Tue, 13 Aug 2024 03:01:09 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:112758f4a1e411bf43727dca6c2485207702e1ce26403f5f7dbec7df7d52056f`  
		Last Modified: Tue, 13 Aug 2024 03:01:09 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3e0e3f278fdf01756879431fffa5cc130302ff4472af7b5342f012a49ed9d0`  
		Last Modified: Tue, 13 Aug 2024 03:01:09 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddff4893cbc3c598e4e309f8f6fe43e0bbb103e471c3c971d70214a279da312d`  
		Last Modified: Tue, 13 Aug 2024 04:01:40 GMT  
		Size: 1.9 MB (1902181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131b21e54918399059aab0ee0e591df20178fa17fdbdd5f74c6a9f525ab25240`  
		Last Modified: Tue, 13 Aug 2024 04:01:29 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e908d0f0177196b42b5606b458f6d9b3c3fc34924d0c6d80adc3283c113c4041`  
		Last Modified: Tue, 13 Aug 2024 04:01:40 GMT  
		Size: 726.3 KB (726344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8736e867482f362a5b3956fd22fa371b1c736047b29aa75aee72810bc73cd737`  
		Last Modified: Tue, 13 Aug 2024 04:01:40 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522085b9898d5e51fd624c9d973a16a50138e5eedb272133acbd6d48e26195e9`  
		Last Modified: Tue, 13 Aug 2024 04:01:41 GMT  
		Size: 21.1 MB (21099466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:7115fe78ba38423b190bb54c85f9f1c5538dcae5895ac50e54709553872a1a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6513636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94ef2d760cea6fd0b59026d115a4677ccaf4e5c611177445bfa5ce825cf662ad`

```dockerfile
```

-	Layers:
	-	`sha256:1762de8f16dbb0f101294f5b2cca6f42bd7f3904de1c5b2581e6c026961d2eb1`  
		Last Modified: Tue, 13 Aug 2024 04:01:40 GMT  
		Size: 6.5 MB (6480133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c91202684cc4595834d6b449ad5c91383c379ea1abdf4905fb1b03d69e0a20a3`  
		Last Modified: Tue, 13 Aug 2024 04:01:40 GMT  
		Size: 33.5 KB (33503 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-bullseye` - linux; arm variant v7

```console
$ docker pull drupal@sha256:d94fb7e12f11411747437e9f2a4fd8b39e8231b938e3002e0dc12eb1b20d15d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.7 MB (155694437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1808f8edf17411d45a1034a65a26d4792d7d5df49e30ffc5b1ae5ff4155b29dd`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 23 Jul 2024 03:03:30 GMT
ADD file:d164f59b51033ee0cb0d72ae8d9f514ca20ed5d7ba327608f8870c8bfd3d69e3 in / 
# Tue, 23 Jul 2024 03:03:30 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 04:53:13 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 23 Jul 2024 04:53:13 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 23 Jul 2024 04:53:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 04:53:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 23 Jul 2024 04:53:53 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 23 Jul 2024 04:53:53 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 Jul 2024 04:53:53 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 Jul 2024 04:53:54 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 Jul 2024 07:08:04 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 01 Aug 2024 22:05:07 GMT
ENV PHP_VERSION=8.2.22
# Thu, 01 Aug 2024 22:05:07 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.22.tar.xz.asc
# Thu, 01 Aug 2024 22:05:07 GMT
ENV PHP_SHA256=8566229bc88ad1f4aadc10700ab5fbcec81587c748999d985f11cf3b745462df
# Thu, 01 Aug 2024 22:05:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 01 Aug 2024 22:05:21 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 01 Aug 2024 22:18:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 01 Aug 2024 22:18:43 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 01 Aug 2024 22:18:44 GMT
RUN docker-php-ext-enable sodium
# Thu, 01 Aug 2024 22:18:44 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 01 Aug 2024 22:18:44 GMT
WORKDIR /var/www/html
# Thu, 01 Aug 2024 22:18:45 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 01 Aug 2024 22:18:45 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Aug 2024 22:18:45 GMT
EXPOSE 9000
# Thu, 01 Aug 2024 22:18:46 GMT
CMD ["php-fpm"]
# Thu, 08 Aug 2024 15:27:17 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 15:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 08 Aug 2024 15:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 15:27:17 GMT
ENV DRUPAL_VERSION=10.3.2
# Thu, 08 Aug 2024 15:27:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 08 Aug 2024 15:27:17 GMT
WORKDIR /opt/drupal
# Thu, 08 Aug 2024 15:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 08 Aug 2024 15:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:3bb0926631c8b9a5d54f36b0d3d892657f4f0c7a3f602ea57899de583b045143`  
		Last Modified: Tue, 23 Jul 2024 03:07:34 GMT  
		Size: 26.6 MB (26589130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d3c94b054af3824ad0d1125e76a629f6786b7bfc3ad1d0e93af25d62e248f51`  
		Last Modified: Tue, 23 Jul 2024 08:34:56 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17d0ecf8b361c4d66e3bc3dff53f4f9f62d32b065a5fdc68175481bb4a87661`  
		Last Modified: Tue, 23 Jul 2024 08:35:15 GMT  
		Size: 69.3 MB (69326095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4b6ad425e76f14bb4592a99e66018b412e5c5b24b446dc98070c425d0d8565`  
		Last Modified: Tue, 23 Jul 2024 08:34:56 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ea43314ff31b04b2573445b82bf2e6dfde5c2f09eb76df0948124ab4136f29`  
		Last Modified: Thu, 01 Aug 2024 22:46:28 GMT  
		Size: 12.4 MB (12417778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e90449b045ee745d982548fd66cf8adc5d6f47dc079089091c6a4bcf5ad506e`  
		Last Modified: Thu, 01 Aug 2024 22:46:26 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b099fbef52f1fd201995847546d79ab21ec92cfa0d949182e181f019c43d0a`  
		Last Modified: Thu, 01 Aug 2024 22:47:00 GMT  
		Size: 24.2 MB (24241250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef887b8a301879e6cf07f753ae9c8c43b02c436fc26168bb8a42dd0557f37bf9`  
		Last Modified: Thu, 01 Aug 2024 22:46:55 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd51998ee003b7807ffb8047c4cff9902f313776098117410cbf2174119c5378`  
		Last Modified: Thu, 01 Aug 2024 22:46:55 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fd5df870933cd3dfec0d6607b9cb6503bcce01ee508f61f7a461ecc51311c19`  
		Last Modified: Thu, 01 Aug 2024 22:46:55 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75385b6d9bc9feae8a61671ec60d1eff96687abda25d7416017716973dceecc7`  
		Last Modified: Fri, 02 Aug 2024 00:53:41 GMT  
		Size: 1.3 MB (1282891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205913abc3aaa38f227a49e724df4a7a8e389ab744be94da799142754e9f17fe`  
		Last Modified: Fri, 02 Aug 2024 00:53:41 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac0d1f25217924c3361688306277ba6aff65724e3d0590316ed6da47213d2268`  
		Last Modified: Fri, 02 Aug 2024 02:50:44 GMT  
		Size: 726.3 KB (726340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb284dc70387d4d24a52471f05b164dd4716e2789a5eaf05d74bfddea0df8c8`  
		Last Modified: Fri, 02 Aug 2024 02:50:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ca325886fd253db5626b3eeff6b23e75a7c022e104bdb912c17ebfea32bb74`  
		Last Modified: Thu, 08 Aug 2024 19:12:54 GMT  
		Size: 21.1 MB (21097693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:20a732e499034516d3974a0b5c96a116e148888ce31160ca98544f385712df28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6322867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f1ef27ae28bf4510cdb42d66ac45a5f13a995508f7cec14cae8d7238a9cea8f`

```dockerfile
```

-	Layers:
	-	`sha256:2d05d71ca1d0840d3f46f43fbf3ca939c2e800e9c2e6da6a859406e0eba2d453`  
		Last Modified: Thu, 08 Aug 2024 19:12:53 GMT  
		Size: 6.3 MB (6289176 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12e5fc1a9d87a069b37c4334f529c1ccf1e75a5eac147b523d2ade1da97953cf`  
		Last Modified: Thu, 08 Aug 2024 19:12:53 GMT  
		Size: 33.7 KB (33691 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-bullseye` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:021a9e32cbc7be904b658551444fe56d82c8d17e839aacd8da58b4e016994aa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.0 MB (180022208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b472b9f324d432899c1628e4113202e27f812630e977961faccee62148c7ff8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 23 Jul 2024 04:18:06 GMT
ADD file:3727dfc046704936a0b983a317eeb319ebd0fc5e9da310be06a0ca768df723ec in / 
# Tue, 23 Jul 2024 04:18:07 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 05:21:35 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 23 Jul 2024 05:21:35 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 23 Jul 2024 05:21:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 05:21:50 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 23 Jul 2024 05:21:51 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 23 Jul 2024 05:21:51 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 Jul 2024 05:21:51 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 Jul 2024 05:21:51 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 Jul 2024 06:42:06 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 01 Aug 2024 22:06:33 GMT
ENV PHP_VERSION=8.2.22
# Thu, 01 Aug 2024 22:06:33 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.22.tar.xz.asc
# Thu, 01 Aug 2024 22:06:33 GMT
ENV PHP_SHA256=8566229bc88ad1f4aadc10700ab5fbcec81587c748999d985f11cf3b745462df
# Thu, 01 Aug 2024 22:06:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 01 Aug 2024 22:06:42 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 01 Aug 2024 22:15:29 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 01 Aug 2024 22:15:29 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 01 Aug 2024 22:15:30 GMT
RUN docker-php-ext-enable sodium
# Thu, 01 Aug 2024 22:15:30 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 01 Aug 2024 22:15:30 GMT
WORKDIR /var/www/html
# Thu, 01 Aug 2024 22:15:31 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 01 Aug 2024 22:15:31 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Aug 2024 22:15:31 GMT
EXPOSE 9000
# Thu, 01 Aug 2024 22:15:31 GMT
CMD ["php-fpm"]
# Thu, 08 Aug 2024 15:27:17 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 15:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 08 Aug 2024 15:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 15:27:17 GMT
ENV DRUPAL_VERSION=10.3.2
# Thu, 08 Aug 2024 15:27:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 08 Aug 2024 15:27:17 GMT
WORKDIR /opt/drupal
# Thu, 08 Aug 2024 15:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 08 Aug 2024 15:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:bd2a3a2ed82de858b38215fac995414b3a91eea4cfe087e5f853ec1faa989ba4`  
		Last Modified: Tue, 23 Jul 2024 04:21:02 GMT  
		Size: 30.1 MB (30076083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67ea1dc36cca3c8065f64bcab06c8190d7ea87c67754f4dfa5f58787cf63576`  
		Last Modified: Tue, 23 Jul 2024 07:49:13 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b75061a10b60a63f9f01c424f5575d03426ba4335da9eb78c8fc778b1f20c0`  
		Last Modified: Tue, 23 Jul 2024 07:49:24 GMT  
		Size: 86.9 MB (86938666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53fca7938ec0579947ca273f587c83680d1e896c167aae176ac1100b0f40308`  
		Last Modified: Tue, 23 Jul 2024 07:49:13 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc083dcaa5d46ad4afc0f7d332fbe95292db3dc6d9ce668ab1682d50273cdb2`  
		Last Modified: Thu, 01 Aug 2024 22:46:49 GMT  
		Size: 12.4 MB (12418519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5230739809af920f667415e1ae035ed82506c14e63829331736cc181e281485a`  
		Last Modified: Thu, 01 Aug 2024 22:46:48 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8cbd4edbbc08e70e4545bf628dda593c5e573ace4379ab07b2bfc8539f79d8b`  
		Last Modified: Thu, 01 Aug 2024 22:47:17 GMT  
		Size: 26.6 MB (26582471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b69e524b4bc49137a671514179b4b0a48dfbe958a488b944c0b57b19c97159`  
		Last Modified: Thu, 01 Aug 2024 22:47:14 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d041425e92c978107cbf81a0a95b3a2c8868ffed3abe0e4306ea662e02b404`  
		Last Modified: Thu, 01 Aug 2024 22:47:14 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e5bdfe4170f6feaa436c5778db9c23f59e51503a5c85dca7e9b802e3b7ef23f`  
		Last Modified: Thu, 01 Aug 2024 22:47:14 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ddcc0e76195e14d71a55b22c4f8212ed8369b4b38ebd2b5c92c545a3f07f8f`  
		Last Modified: Fri, 02 Aug 2024 03:40:19 GMT  
		Size: 2.2 MB (2168854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:061e9f7a0ffab2321985313a762c4ccda7a59b201090d4ce642a5818ea080a8a`  
		Last Modified: Fri, 02 Aug 2024 03:40:19 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5c7e56f740216e06fe56e8910effb6b614147b92af0c6f7bce1e2be2dfc26f`  
		Last Modified: Fri, 02 Aug 2024 05:21:34 GMT  
		Size: 726.3 KB (726340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8b8c1840c2019de379c857c6d45e4ae5c9d26a5de711f748bd4da1bf96d958`  
		Last Modified: Fri, 02 Aug 2024 05:21:34 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b1f9c80957a9dd1b41e1889311f575c96f159d39c6a915fb37d9bbbdfcc4a4c`  
		Last Modified: Thu, 08 Aug 2024 19:08:38 GMT  
		Size: 21.1 MB (21098026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:d1bbf7e781248df51ca52f97a2e2cd00ae47b1a1e2670dd28411bbc9bc8c56b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6517254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f87c3dcb6f8c8d178faa60a7312bf69170da1378140562ff930771f85138235`

```dockerfile
```

-	Layers:
	-	`sha256:5e1ea8d940037611f23cea9a8fb456e8484c90a8cdd21d7da92babb893ce7433`  
		Last Modified: Thu, 08 Aug 2024 19:08:38 GMT  
		Size: 6.5 MB (6483042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7edac87c8a9c1d00953a09cba709d70a8394f3a2937554c79db1dcb1070276ec`  
		Last Modified: Thu, 08 Aug 2024 19:08:37 GMT  
		Size: 34.2 KB (34212 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-bullseye` - linux; 386

```console
$ docker pull drupal@sha256:474893139776bc400fc0a1e53fb7cd8f8ffdbad89c2252327da68f7dc702900b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.4 MB (188383162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99268b050d43645d80f00c3449abb7111ec737e0ec458e145d3e982663d77288`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 08 Aug 2024 15:27:17 GMT
ADD file:3c28079e98aa5b4ba96d948760be5fa7d7f99c878e193a63fab4f18eda2ee67e in / 
# Thu, 08 Aug 2024 15:27:17 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 15:27:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 08 Aug 2024 15:27:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 08 Aug 2024 15:27:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 15:27:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 08 Aug 2024 15:27:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 08 Aug 2024 15:27:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 Aug 2024 15:27:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 Aug 2024 15:27:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 08 Aug 2024 15:27:17 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 08 Aug 2024 15:27:17 GMT
ENV PHP_VERSION=8.2.22
# Thu, 08 Aug 2024 15:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.22.tar.xz.asc
# Thu, 08 Aug 2024 15:27:17 GMT
ENV PHP_SHA256=8566229bc88ad1f4aadc10700ab5fbcec81587c748999d985f11cf3b745462df
# Thu, 08 Aug 2024 15:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 08 Aug 2024 15:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 08 Aug 2024 15:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 08 Aug 2024 15:27:17 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 08 Aug 2024 15:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 08 Aug 2024 15:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 08 Aug 2024 15:27:17 GMT
WORKDIR /var/www/html
# Thu, 08 Aug 2024 15:27:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 08 Aug 2024 15:27:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 08 Aug 2024 15:27:17 GMT
EXPOSE 9000
# Thu, 08 Aug 2024 15:27:17 GMT
CMD ["php-fpm"]
# Thu, 08 Aug 2024 15:27:17 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 15:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 08 Aug 2024 15:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 15:27:17 GMT
ENV DRUPAL_VERSION=10.3.2
# Thu, 08 Aug 2024 15:27:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 08 Aug 2024 15:27:17 GMT
WORKDIR /opt/drupal
# Thu, 08 Aug 2024 15:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 08 Aug 2024 15:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:1fff23531e74037071ba9be4ee63db5ccfd9c3823dceddfee08bed3fdeb6dea1`  
		Last Modified: Tue, 13 Aug 2024 00:43:17 GMT  
		Size: 32.4 MB (32413784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae820639802ab7cf81f77371525fa7cda60f5aed373abd5904fdd20d0fdedd29`  
		Last Modified: Tue, 13 Aug 2024 07:43:39 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:967e92747aa0b67aa1888e1bb7cc9a83631ca6b559c2ec8e5df253ab7befa5cc`  
		Last Modified: Tue, 13 Aug 2024 07:43:58 GMT  
		Size: 92.7 MB (92721033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bba36adfee3a57bf955f99d92ca74a24147c507a0570dce814f42f2c7612a5e3`  
		Last Modified: Tue, 13 Aug 2024 07:43:39 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b7331352ecd317cb85fc363059428d0d526367a47715b1ec66daa9f9743273`  
		Last Modified: Tue, 13 Aug 2024 07:49:11 GMT  
		Size: 12.4 MB (12418486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc99819b4e28e0393cf23b8a1b64afa1b9b85e770b68dee216a7fd8a370dc90`  
		Last Modified: Tue, 13 Aug 2024 07:49:10 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:accf5ad0f8253be24112e1f57d30951af4ef2573dbf44393b189ca05bfd7fec9`  
		Last Modified: Tue, 13 Aug 2024 07:49:44 GMT  
		Size: 27.0 MB (27021122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a73408d1d3c193db0a12edbd4c350589b71879a29d12bc7c4bb61a968d200f`  
		Last Modified: Tue, 13 Aug 2024 07:49:39 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8d476436634e06011063eee7ec34cf3df9b6b582162452c10834c6a98346ac`  
		Last Modified: Tue, 13 Aug 2024 07:49:39 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:137077b945cecc5244c175bd13a7fbf7061cf2b97225ef652c8d583f45c44993`  
		Last Modified: Tue, 13 Aug 2024 07:49:39 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9dd05b2158273643c4a18a0be3a857c4b127415be006b2b4ac979be2b1cccd`  
		Last Modified: Tue, 13 Aug 2024 08:59:45 GMT  
		Size: 2.0 MB (1969858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660110dccfe699c2faab0431cec8d9c63cdf8e9b6cad1442ac6f85d1a9879e3b`  
		Last Modified: Tue, 13 Aug 2024 08:59:45 GMT  
		Size: 313.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4d96336021f5d5e0b978e34ee0cac3272696c2bcd416abb6f6b3a7ca2683bce`  
		Last Modified: Tue, 13 Aug 2024 08:59:45 GMT  
		Size: 726.3 KB (726340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a5806302487e623f26b5b465f607be279c4b2f3ffc51f9105a155be412f98b`  
		Last Modified: Tue, 13 Aug 2024 08:59:45 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809dee3d1174f26d531c34c6bc1e6221f18a8d8cbec2ab421f50f14f64590cde`  
		Last Modified: Tue, 13 Aug 2024 08:59:46 GMT  
		Size: 21.1 MB (21099295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:87af73fc8b57582d8f798f9011f8e7f40dd554b0ce532fe6d6096338d8f58b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6504444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:419b05beaae37bdafddb737c09c06a3d264538fa83253653566bffbe6559628e`

```dockerfile
```

-	Layers:
	-	`sha256:aeb0a2c33abf1088feac6c9a9253d3b60ea5f2f8fd4ffc474d595da3d3cc9e53`  
		Last Modified: Tue, 13 Aug 2024 08:59:45 GMT  
		Size: 6.5 MB (6470991 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35fde4bef897ca572e85b01151465a45b78cf92f7bf06a424d635ee31ea7489e`  
		Last Modified: Tue, 13 Aug 2024 08:59:45 GMT  
		Size: 33.5 KB (33453 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-bullseye` - linux; ppc64le

```console
$ docker pull drupal@sha256:7719e805937b4366456098e3f4ca03c92e7a4b25f136c5fe333a5e40ee3dedf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.6 MB (185596927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c87c905d18ddb2c01288cd5bf522ddbc32baed00462b33a139f1a14588897b1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Tue, 23 Jul 2024 01:27:23 GMT
ADD file:ea3c7c365051c72d1bebaf8f2b9d42a99d14186d8919b4371222e4f7a471fd0e in / 
# Tue, 23 Jul 2024 01:27:25 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:00:54 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Tue, 23 Jul 2024 03:00:55 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Tue, 23 Jul 2024 03:01:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 Jul 2024 03:01:30 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Tue, 23 Jul 2024 03:01:30 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Tue, 23 Jul 2024 03:01:31 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 Jul 2024 03:01:31 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Tue, 23 Jul 2024 03:01:31 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Tue, 23 Jul 2024 04:16:07 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 01 Aug 2024 21:41:27 GMT
ENV PHP_VERSION=8.2.22
# Thu, 01 Aug 2024 21:41:27 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.22.tar.xz.asc
# Thu, 01 Aug 2024 21:41:28 GMT
ENV PHP_SHA256=8566229bc88ad1f4aadc10700ab5fbcec81587c748999d985f11cf3b745462df
# Thu, 01 Aug 2024 21:41:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 01 Aug 2024 21:41:45 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 01 Aug 2024 21:50:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 01 Aug 2024 21:50:32 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 01 Aug 2024 21:50:33 GMT
RUN docker-php-ext-enable sodium
# Thu, 01 Aug 2024 21:50:33 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 01 Aug 2024 21:50:34 GMT
WORKDIR /var/www/html
# Thu, 01 Aug 2024 21:50:35 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 01 Aug 2024 21:50:35 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Aug 2024 21:50:36 GMT
EXPOSE 9000
# Thu, 01 Aug 2024 21:50:36 GMT
CMD ["php-fpm"]
# Thu, 08 Aug 2024 15:27:17 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 15:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 08 Aug 2024 15:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 15:27:17 GMT
ENV DRUPAL_VERSION=10.3.2
# Thu, 08 Aug 2024 15:27:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 08 Aug 2024 15:27:17 GMT
WORKDIR /opt/drupal
# Thu, 08 Aug 2024 15:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 08 Aug 2024 15:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:2c0db65e988f1b1fb39291776f39faf5f568126305c67c7c3ad8191e6d072781`  
		Last Modified: Tue, 23 Jul 2024 01:31:54 GMT  
		Size: 35.3 MB (35305203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bca31eac2ed8ece3ba386852bb9e717d3bcf925dea98a3ff93f0e61a8c1f9d4c`  
		Last Modified: Tue, 23 Jul 2024 05:19:27 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0cc37531317a045ead4f6cebdea9df0e36db3670bedacaf80e8221773f2aa98`  
		Last Modified: Tue, 23 Jul 2024 05:19:42 GMT  
		Size: 86.7 MB (86651319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4ba1d01ce6e77c2c36622a8a2a67c34e598bfd2f7d0447753e9ac4b7e9f051`  
		Last Modified: Tue, 23 Jul 2024 05:19:27 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21f076f894a3f72be6a9a7b05ad43435cdfd4118d3ef80a30e39bbc2cb357307`  
		Last Modified: Thu, 01 Aug 2024 22:14:13 GMT  
		Size: 12.4 MB (12419118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba7412a46ff6d3803a12099fe567d4884c52a26bcd3cd8c5c63b1277ee3ea34`  
		Last Modified: Thu, 01 Aug 2024 22:14:12 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff023481568c4d9e3b3e280862858af25f9398e5042385ccaca7a2499a3a414`  
		Last Modified: Thu, 01 Aug 2024 22:14:46 GMT  
		Size: 27.6 MB (27615778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eccfec619e99c94ef2e8ff584a31ebfce3885813cec2e77f3bfa18f9e0f54a3`  
		Last Modified: Thu, 01 Aug 2024 22:14:42 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2aed557068fe0609da399faa115d807e4387c28f4934cf42b6ec37fc148109e8`  
		Last Modified: Thu, 01 Aug 2024 22:14:42 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0ddde541d7ebdbd875bdc333d8a8bbfd30d7831c2812fb4f30911816503c2ca`  
		Last Modified: Thu, 01 Aug 2024 22:14:42 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fbf01e2c5193ba27fdcc6581b0baadd4cc9146f4803ecb5405085fd291d811`  
		Last Modified: Fri, 02 Aug 2024 00:25:38 GMT  
		Size: 1.8 MB (1768667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb8e929bd52f03d17464540cf828796a29622a596c1450e6949cbda5b8b40ab`  
		Last Modified: Fri, 02 Aug 2024 00:25:38 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c40c1a7b51a5bddaf412f3808f7f29261446f4c1cf5815dba217dc510bb2db0`  
		Last Modified: Fri, 02 Aug 2024 06:23:09 GMT  
		Size: 726.3 KB (726347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f36a3541a3c5114ab54ba9496fedb65375ba8bb248b63914fd5d89221e8fc14`  
		Last Modified: Fri, 02 Aug 2024 06:23:09 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:643f9cc208ef6f14c955c42e18296ab23562acc34351836ffb0ec56cdac0697c`  
		Last Modified: Thu, 08 Aug 2024 19:17:04 GMT  
		Size: 21.1 MB (21097241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:bcc5dcb0e4655a4d995bd9c09f7091236299372ceabe158f80874eb3735825ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6479580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:567f1108a3d4ca218c2816fdc3bc28372eab4e0c088299e046f364a659cad40f`

```dockerfile
```

-	Layers:
	-	`sha256:ae518bba21c6fa41fdde6b54ff98d2cf512d086d9646dd4a77dbc900f32a138e`  
		Last Modified: Thu, 08 Aug 2024 19:17:03 GMT  
		Size: 6.4 MB (6445959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1e0a56f73d587c87e3936a2c19e1ea2fb5ffbb0f1741c164251974b86cf3ed6`  
		Last Modified: Thu, 08 Aug 2024 19:17:03 GMT  
		Size: 33.6 KB (33621 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-bullseye` - linux; s390x

```console
$ docker pull drupal@sha256:6867a6647f127e10c1c32c59e0faab5f37223169ee2145edb9f9f585feaceda5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.8 MB (162813528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eda0feab3ab56039a236b6155a5b391468966cfcf509f3121710170cbbc1dc7`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 08 Aug 2024 15:27:17 GMT
ADD file:a473fc09ddb0d1045f7f330f3a48b9cfe65ff9ea65cfa5c8262a8a5be9d4db75 in / 
# Thu, 08 Aug 2024 15:27:17 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 15:27:17 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 08 Aug 2024 15:27:17 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 08 Aug 2024 15:27:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 15:27:17 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 08 Aug 2024 15:27:17 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 08 Aug 2024 15:27:17 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 Aug 2024 15:27:17 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 Aug 2024 15:27:17 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 08 Aug 2024 15:27:17 GMT
ENV GPG_KEYS=39B641343D8C104B2B146DC3F9C39DC0B9698544 E60913E4DF209907D8E30D96659A97C9CF2A795A 1198C0117593497A5EC5C199286AF1F9897469DC
# Thu, 08 Aug 2024 15:27:17 GMT
ENV PHP_VERSION=8.2.22
# Thu, 08 Aug 2024 15:27:17 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.2.22.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.2.22.tar.xz.asc
# Thu, 08 Aug 2024 15:27:17 GMT
ENV PHP_SHA256=8566229bc88ad1f4aadc10700ab5fbcec81587c748999d985f11cf3b745462df
# Thu, 08 Aug 2024 15:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 08 Aug 2024 15:27:17 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 08 Aug 2024 15:27:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				$(test "$gnuArch" = 'riscv64-linux-gnu' && echo '--without-pcre-jit') 		--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 08 Aug 2024 15:27:17 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 08 Aug 2024 15:27:17 GMT
RUN docker-php-ext-enable sodium
# Thu, 08 Aug 2024 15:27:17 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 08 Aug 2024 15:27:17 GMT
WORKDIR /var/www/html
# Thu, 08 Aug 2024 15:27:17 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 08 Aug 2024 15:27:17 GMT
STOPSIGNAL SIGQUIT
# Thu, 08 Aug 2024 15:27:17 GMT
EXPOSE 9000
# Thu, 08 Aug 2024 15:27:17 GMT
CMD ["php-fpm"]
# Thu, 08 Aug 2024 15:27:17 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 15:27:17 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 08 Aug 2024 15:27:17 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 15:27:17 GMT
ENV DRUPAL_VERSION=10.3.2
# Thu, 08 Aug 2024 15:27:17 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 08 Aug 2024 15:27:17 GMT
WORKDIR /opt/drupal
# Thu, 08 Aug 2024 15:27:17 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 08 Aug 2024 15:27:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:83ea1b2f9d26c88827c9a658387c782a21fca528fbf7418f1a4eaea9a9818bdf`  
		Last Modified: Tue, 13 Aug 2024 00:47:58 GMT  
		Size: 29.7 MB (29668965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6baf63313ed972f545d2ef6635043a5369c06c343aa6f9181a5750981284cc2a`  
		Last Modified: Tue, 13 Aug 2024 03:15:32 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2793133b1f1013c3ed9a9f138b2142611614d8ae8dc41e05fe81ad30a877d888`  
		Last Modified: Tue, 13 Aug 2024 03:15:42 GMT  
		Size: 71.6 MB (71640589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c12fdf4f5ddf9659dbcf26e5a15da976dbfcf3f06ae1d5c09048705d8aba4273`  
		Last Modified: Tue, 13 Aug 2024 03:15:32 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f56644d503f8d699888020e501dbc00a738dd0a29cbd648db332e5769d9d5ab`  
		Last Modified: Tue, 13 Aug 2024 03:19:48 GMT  
		Size: 12.4 MB (12418133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338b22334234c1a8d88ec46efd040f8d55c85eb689e5c26706cf38695715e0ed`  
		Last Modified: Tue, 13 Aug 2024 03:19:48 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b678bd08595f7217cd09ed5cda5b8fcc3603df19d161601455a8124504a12d`  
		Last Modified: Tue, 13 Aug 2024 03:20:11 GMT  
		Size: 25.8 MB (25750584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85afd4542b31fd0e62fe2f53efeca58df3926724efaff84db3c4246b3529f2a`  
		Last Modified: Tue, 13 Aug 2024 03:20:08 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e1ac3e598e4cfee8cb353f0aade10e8984e66ecbb9864af1c20828f51034b1e`  
		Last Modified: Tue, 13 Aug 2024 03:20:08 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4a1f661b98d1bac857e9c48c2ef6763a12ccae44e132b09859a4ed68086c5f`  
		Last Modified: Tue, 13 Aug 2024 03:20:08 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c965453031feef17aed43e48f471f8b0c9d4291c9395fb4bfaf1844c8bfad7b`  
		Last Modified: Tue, 13 Aug 2024 10:55:54 GMT  
		Size: 1.5 MB (1496164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba0d51224d7282c52d0a548f012dafa9d4dc8d55284f797ac28bca31686a7a4`  
		Last Modified: Tue, 13 Aug 2024 10:55:54 GMT  
		Size: 314.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a41cb559d849272fcb7d8ca882fb1313a27bf53a9ef17d7c2598a55c49f8eb0`  
		Last Modified: Tue, 13 Aug 2024 10:55:55 GMT  
		Size: 726.3 KB (726341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c463c3ecf2ac038d69ef449b896ffd46511ffaeb2631121e312cdc75e1bb2c5c`  
		Last Modified: Tue, 13 Aug 2024 10:55:55 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2150042403bd1df575e54bba54fa5f38696cef58b2e188d5736b2300def9ea67`  
		Last Modified: Tue, 13 Aug 2024 10:55:56 GMT  
		Size: 21.1 MB (21099507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:e4a08d2282dff8c14d005b791f0faec7bed47b8fd7f938d392f89a681c439fbd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6344204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:819185f0e70c0da12bea201120d6f7863ec60ba23fc926b81d1e8a0fd52364dd`

```dockerfile
```

-	Layers:
	-	`sha256:bec0a602c0795182450d50e7c7549f8b7cd886fe1cca9dd02a92c45dbbd5ab10`  
		Last Modified: Tue, 13 Aug 2024 10:55:53 GMT  
		Size: 6.3 MB (6310646 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bd45913954ccd80cd1123f86d41697850294a422bb8ce21d7e694e4a3892e35`  
		Last Modified: Tue, 13 Aug 2024 10:55:53 GMT  
		Size: 33.6 KB (33558 bytes)  
		MIME: application/vnd.in-toto+json
