## `drupal:10-fpm-bullseye`

```console
$ docker pull drupal@sha256:1807b9c438970f1c7b851c1bfa6d81f46faa6fe872852109d382f2dc8cdab88a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `drupal:10-fpm-bullseye` - linux; amd64

```console
$ docker pull drupal@sha256:048fe0a26c510fc039147ef1ffed8ca9ea64439c1e01bf70703a82d5d8b55a0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **185.1 MB (185071153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a9dc35792a4d7bdb6b3c4d4e34c151325f91935abc194064645da6a1dc1db8`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
# Wed, 05 Mar 2025 22:27:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 05 Mar 2025 22:27:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Mar 2025 22:27:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Mar 2025 22:27:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Mar 2025 22:27:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Mar 2025 22:27:20 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 05 Mar 2025 22:27:20 GMT
ENV PHP_VERSION=8.3.19
# Wed, 05 Mar 2025 22:27:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Wed, 05 Mar 2025 22:27:20 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Wed, 05 Mar 2025 22:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Mar 2025 22:27:20 GMT
WORKDIR /var/www/html
# Wed, 05 Mar 2025 22:27:20 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Mar 2025 22:27:20 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 05 Mar 2025 22:27:20 GMT
CMD ["php-fpm"]
# Wed, 05 Mar 2025 22:27:20 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
ENV DRUPAL_VERSION=10.4.4
# Wed, 05 Mar 2025 22:27:20 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 05 Mar 2025 22:27:20 GMT
WORKDIR /opt/drupal
# Wed, 05 Mar 2025 22:27:20 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1702da8ffbf9e2b2009ddafcc9a65a21725b767d70224756a203e380869e23`  
		Last Modified: Fri, 14 Mar 2025 00:12:36 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b971057d9e9d5866d36b7a1a1ab07ffab62f89c8f736daaf395eea57a433e09`  
		Last Modified: Fri, 14 Mar 2025 00:12:37 GMT  
		Size: 91.4 MB (91449110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe16cd175ce6623493909ec477a1df3c3c159ace659f84849ca83530372abc95`  
		Last Modified: Fri, 14 Mar 2025 00:12:36 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a653943f74a0c894cef16b38cba0430ddaa37bc901976b8d64e204b2d4b4038`  
		Last Modified: Fri, 14 Mar 2025 00:12:36 GMT  
		Size: 12.7 MB (12664284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0f3118f69e7ab32fe4be71d8bbc07ff58dffce84fafa3c13615f0641c36f1d`  
		Last Modified: Fri, 14 Mar 2025 00:12:37 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f7f342305cce5956c1d1e1232de0384803d1099612a70bab73915466f092e87`  
		Last Modified: Fri, 14 Mar 2025 00:12:37 GMT  
		Size: 26.6 MB (26562298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbc7896b5d6862042c8527b65bef092a8158a6a195a7fce42a1d69d87a92e1e`  
		Last Modified: Fri, 14 Mar 2025 00:12:37 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56d07b78c944860af9b94c3b128dd4ad78da7fbb91b5f39d73b14c1c40bb227b`  
		Last Modified: Fri, 14 Mar 2025 00:12:38 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3cbd9d8391e56c0c2c52c0f237cd7bb46b20b2e49b4b55d18242d98bc5d705`  
		Last Modified: Fri, 14 Mar 2025 00:12:38 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:296a74fae5734b77799edf2dd6340b88fc03f43a935d0d7ec778de521c46f19f`  
		Last Modified: Fri, 14 Mar 2025 02:14:13 GMT  
		Size: 1.9 MB (1906829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6236efd7132de608e5b4c17324481029ce3614375c6c2a52989d6733c086a8d1`  
		Last Modified: Fri, 14 Mar 2025 02:14:12 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44c110c0884b3cbf2931e7f3672936fb51c95b50c381fd951fb3d2ef14ec67ac`  
		Last Modified: Fri, 14 Mar 2025 02:14:13 GMT  
		Size: 740.8 KB (740826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a4441132a69c43a0dc2c61a179581465dce2fb6ae40b9434ba60fd3e0cb5ce2`  
		Last Modified: Fri, 14 Mar 2025 02:14:12 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f93a028be83b3dacc3ea678d3a6d8b2f7f808d6e119daacf135a06664eecab4c`  
		Last Modified: Fri, 14 Mar 2025 02:14:14 GMT  
		Size: 21.5 MB (21480587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:d36e4a492c5256a53a12b564777913fd39d4d166ca0aab12e19c7190f02eb255
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6527263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7378dde6d866d1257d85ef0a17e1e057e4c852c14f1909a283dbd268e4b15f0`

```dockerfile
```

-	Layers:
	-	`sha256:95cbe5731ef16915b85be3fab96c155934c4ca4588dcf6bc6a217a8ebc746153`  
		Last Modified: Fri, 14 Mar 2025 02:14:13 GMT  
		Size: 6.5 MB (6492972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ccd825110fe1e0f8143f9b0e0108af5b866af23c324fb0a04b642d56b53438b5`  
		Last Modified: Fri, 14 Mar 2025 02:14:12 GMT  
		Size: 34.3 KB (34291 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-bullseye` - linux; arm variant v7

```console
$ docker pull drupal@sha256:f30f56dc9d77e2e949e6001b8e0a9930d9f12e128c6d70ed3f3b05aa51cbda0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.1 MB (155088756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5389db5323a90f43eb9ffffa1629b6da3846afb01b73479773c36311bfe81197`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1740355200'
# Wed, 05 Mar 2025 22:27:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 05 Mar 2025 22:27:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Mar 2025 22:27:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Mar 2025 22:27:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Mar 2025 22:27:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Mar 2025 22:27:20 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 05 Mar 2025 22:27:20 GMT
ENV PHP_VERSION=8.3.19
# Wed, 05 Mar 2025 22:27:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Wed, 05 Mar 2025 22:27:20 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Wed, 05 Mar 2025 22:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Mar 2025 22:27:20 GMT
WORKDIR /var/www/html
# Wed, 05 Mar 2025 22:27:20 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Mar 2025 22:27:20 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 05 Mar 2025 22:27:20 GMT
CMD ["php-fpm"]
# Wed, 05 Mar 2025 22:27:20 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
ENV DRUPAL_VERSION=10.4.4
# Wed, 05 Mar 2025 22:27:20 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 05 Mar 2025 22:27:20 GMT
WORKDIR /opt/drupal
# Wed, 05 Mar 2025 22:27:20 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:b0ca501b624d9dae81049df15e1024733ee21141b25f8ca123d98e0d13df5d12`  
		Last Modified: Tue, 25 Feb 2025 01:31:18 GMT  
		Size: 25.5 MB (25535432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6376edd46dda2c697c237efb83c17a91a0979b8e59e202d593f0446305d10167`  
		Last Modified: Tue, 25 Feb 2025 03:00:37 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29853446d3cd05c0eb401a13f07135f89a449ee487663701b45fb717b9b8e4e8`  
		Last Modified: Tue, 25 Feb 2025 03:00:39 GMT  
		Size: 69.1 MB (69119400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b785546b44d4e782b7e6d1ac072a5cb20d9e0432b17127beae71a8577c4cd2`  
		Last Modified: Tue, 25 Feb 2025 03:00:37 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dee2ddb0be64c4809a10b06cdbe40a625bf15e5a4929db1b9e2501c2fd98a221`  
		Last Modified: Fri, 14 Mar 2025 03:29:20 GMT  
		Size: 12.7 MB (12662901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c328eda22c1732f54567233e05fb21cccf61634b28599ffe5d06700337ce11f`  
		Last Modified: Fri, 14 Mar 2025 03:29:19 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed2619c141a60ffd80eaf2dfd18d29812e1b9b985fa933c99349b33e9033314`  
		Last Modified: Fri, 14 Mar 2025 03:35:32 GMT  
		Size: 24.3 MB (24250607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d9c9f798889b346401da72a4a8345e51af4efe0e590155fe3eaa12d9bcdf5b`  
		Last Modified: Fri, 14 Mar 2025 03:35:31 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7407ff938de28a7ffac45ee2dfe1fd39045d61b2729db285fa5a720df4b667fb`  
		Last Modified: Fri, 14 Mar 2025 03:35:31 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bce093bb3cfa91c250bfdc11d0ce432b550630432bda75f20d9c7fa1f1d9eae`  
		Last Modified: Fri, 14 Mar 2025 03:35:32 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5af153187fa4a3f233914c7259288a7c2d8d708692d1737b75f5a157f7c50b`  
		Last Modified: Fri, 14 Mar 2025 16:23:44 GMT  
		Size: 1.3 MB (1285728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab0ce7f6570867888bf3cbed509b12c259866d5067cfe15a1a2884ebf5dbc75`  
		Last Modified: Fri, 14 Mar 2025 16:23:43 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fa182730e6002cae05312f54d86a52599b9e0ca59bc9139aa732541474eff5`  
		Last Modified: Fri, 14 Mar 2025 16:23:43 GMT  
		Size: 740.8 KB (740827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47904213b019d0ec8feba027814fb1121ff94089ac9dcb52b4b78ed472bef3d3`  
		Last Modified: Fri, 14 Mar 2025 16:23:43 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859bca8434f97a3d8087a94ca6da710e2342c71f806d875f396fb10a69f939af`  
		Last Modified: Fri, 14 Mar 2025 18:30:53 GMT  
		Size: 21.5 MB (21480574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:0eb0f8d4835c11bfe00bb84324eb12ebe94ac86a9d4342b808b06b071497fb03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6336252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:240f41c9eb7ec6f732fcc261e4091635af0ffa75f10ebf696189b6f73b8e8c53`

```dockerfile
```

-	Layers:
	-	`sha256:f1564e32dca16ad64430a2f695fe61f9a1e84b2cc8af6186400c3289ac1647ca`  
		Last Modified: Fri, 14 Mar 2025 18:30:53 GMT  
		Size: 6.3 MB (6301821 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc8ee9256cdcca2a1534a685b0653828952fa1ce6e5b9e8808f13ba4bcfd47c0`  
		Last Modified: Fri, 14 Mar 2025 18:30:52 GMT  
		Size: 34.4 KB (34431 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-bullseye` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:066f94d51a28bcdaec5581da5f5a6476009cea8afda66773936955bbbf1ea867
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.2 MB (179154435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7edb9d90445b5204ea6ca26bb1f25920e9494d9417b53fbd7f1e51f8a6a946`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1740355200'
# Wed, 05 Mar 2025 22:27:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 05 Mar 2025 22:27:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Mar 2025 22:27:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Mar 2025 22:27:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Mar 2025 22:27:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Mar 2025 22:27:20 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 05 Mar 2025 22:27:20 GMT
ENV PHP_VERSION=8.3.19
# Wed, 05 Mar 2025 22:27:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Wed, 05 Mar 2025 22:27:20 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Wed, 05 Mar 2025 22:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Mar 2025 22:27:20 GMT
WORKDIR /var/www/html
# Wed, 05 Mar 2025 22:27:20 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Mar 2025 22:27:20 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 05 Mar 2025 22:27:20 GMT
CMD ["php-fpm"]
# Wed, 05 Mar 2025 22:27:20 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
ENV DRUPAL_VERSION=10.4.4
# Wed, 05 Mar 2025 22:27:20 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 05 Mar 2025 22:27:20 GMT
WORKDIR /opt/drupal
# Wed, 05 Mar 2025 22:27:20 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:c4c6d622e13259683de05019144b319d210aaf74faadf38f9ff2c9d56472ab51`  
		Last Modified: Tue, 25 Feb 2025 01:31:29 GMT  
		Size: 28.7 MB (28745987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9cac8d80438c7d8c825ba99a93071ef755fedf47f61ec6695e1a497258d4a6d`  
		Last Modified: Tue, 25 Feb 2025 03:17:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4cf5e32e0b7c2e87599c9d64521fbaff9ea36e3fbfb51f931baef0cb2e19803`  
		Last Modified: Tue, 25 Feb 2025 03:17:38 GMT  
		Size: 86.7 MB (86734530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:105bd05e74457394c989762746be7fe63b0dbcf517102c6b331508270af1b04b`  
		Last Modified: Tue, 25 Feb 2025 03:17:35 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aea3e24b30c293fbff7832206489eb675b3b2a2e22df15f573673b680afce5e`  
		Last Modified: Fri, 14 Mar 2025 02:11:23 GMT  
		Size: 12.7 MB (12663639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c626a54d995cde59c53529146b91f2a259f848757b80c18f2750fbc435ece634`  
		Last Modified: Fri, 14 Mar 2025 02:11:22 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aba74793486b992f36e66e7cc71db586c6a58ac90860dd2698b817cdacf8c87f`  
		Last Modified: Fri, 14 Mar 2025 02:15:17 GMT  
		Size: 26.6 MB (26604660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94088687e1e9153acff2aa376b61473245c4def17d7bcf7afb9e26642622fd6a`  
		Last Modified: Fri, 14 Mar 2025 02:15:16 GMT  
		Size: 2.4 KB (2448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b3f08c10a12c8cc6e96bf5e6eb01eacd1eec6e9cdffe5552f9647874a34f767`  
		Last Modified: Fri, 14 Mar 2025 02:15:16 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1afb31e358ae3ea04accc16ca7754b9c997e39c99981e2a379a11fd743dae157`  
		Last Modified: Fri, 14 Mar 2025 02:15:16 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd149b723b712d00c8efdefb4dd2648f5ae64b2071dbbc5422db6de3bc7ee208`  
		Last Modified: Fri, 14 Mar 2025 22:12:29 GMT  
		Size: 2.2 MB (2170862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3044fb9cf6847d33b1054b204bf780cfdbce2bf615ddc6a05fb5b0479fd6e66d`  
		Last Modified: Fri, 14 Mar 2025 22:12:29 GMT  
		Size: 318.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f6dab4ffbb4e2bf56e8ac88d54e86c24832cc72d60e07caaa68ba3d519c811`  
		Last Modified: Fri, 14 Mar 2025 22:12:29 GMT  
		Size: 740.8 KB (740827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eff583e370feea0e8de8d0876766342a55f2075ef6cbba67a01a83494ccbe49`  
		Last Modified: Fri, 14 Mar 2025 22:12:29 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3c6740b8997491a81501904ddf8ee6e36dc70c21ca94f4cc3e71cb571ffb79`  
		Last Modified: Fri, 14 Mar 2025 22:44:27 GMT  
		Size: 21.5 MB (21480644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:13b4a0cf5f513129457141a97da64fd76515e4c8e60e275b950cb7f58d7d8566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6530245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ba9b9a38159d0ea32ab60aee1b0ee99eed38af5cdbbea6db160cf24d9859e15`

```dockerfile
```

-	Layers:
	-	`sha256:c6ebb5ab80a71a45aa024044f6448d946d7cf143a2c4100933d8a84dad2370a8`  
		Last Modified: Fri, 14 Mar 2025 22:44:27 GMT  
		Size: 6.5 MB (6495771 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d0a5f2d5c41db63cb1336604876ceb83d96d72ade94728d1c8a41e79c33cf4d`  
		Last Modified: Fri, 14 Mar 2025 22:44:26 GMT  
		Size: 34.5 KB (34474 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:10-fpm-bullseye` - linux; 386

```console
$ docker pull drupal@sha256:4e13c962eebe08085d17da9616bfb0eaf478e2457dc9c627476225bf352a9194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187600230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9659c8f03a9c822f4111739f013195916e737929b125c11f940a5fca175cbc5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
# Wed, 05 Mar 2025 22:27:20 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 05 Mar 2025 22:27:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 05 Mar 2025 22:27:20 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Mar 2025 22:27:20 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 05 Mar 2025 22:27:20 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 05 Mar 2025 22:27:20 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 05 Mar 2025 22:27:20 GMT
ENV PHP_VERSION=8.3.19
# Wed, 05 Mar 2025 22:27:20 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.19.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.19.tar.xz.asc
# Wed, 05 Mar 2025 22:27:20 GMT
ENV PHP_SHA256=976e4077dd25bec96b5dfe8938052d243bbd838f95368a204896eff12756545f
# Wed, 05 Mar 2025 22:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 05 Mar 2025 22:27:20 GMT
WORKDIR /var/www/html
# Wed, 05 Mar 2025 22:27:20 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Mar 2025 22:27:20 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 05 Mar 2025 22:27:20 GMT
CMD ["php-fpm"]
# Wed, 05 Mar 2025 22:27:20 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
ENV DRUPAL_VERSION=10.4.4
# Wed, 05 Mar 2025 22:27:20 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 05 Mar 2025 22:27:20 GMT
WORKDIR /opt/drupal
# Wed, 05 Mar 2025 22:27:20 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 05 Mar 2025 22:27:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:bef9e4bcedd5ece70d65f7a4c14a67fd26dce78a05b7abbb6b607f6ff01887ee`  
		Last Modified: Tue, 25 Feb 2025 01:29:48 GMT  
		Size: 31.2 MB (31180427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69d0eca52591f8a554106d0880e825d49aaeda459b87795e62c202f8409376b5`  
		Last Modified: Fri, 14 Mar 2025 00:12:51 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691d5a5726c5d4f14a17ad031befe98120e71015dde08e5541e4a1d43faef2d8`  
		Last Modified: Fri, 14 Mar 2025 00:12:54 GMT  
		Size: 92.5 MB (92521282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06696045ee9c8811e25953e12fbbe10eecab2bbbf749fc48da9bad16c8b192c1`  
		Last Modified: Fri, 14 Mar 2025 00:12:51 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0231586702c337a121101de31f933f7e166a5080a0ae647c3fce91eea581f747`  
		Last Modified: Fri, 14 Mar 2025 00:12:52 GMT  
		Size: 12.7 MB (12663603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3a8ab6ca2e39bd949b0eeedc49cd75b534192c357f3941ed8d99fe1cda04c0`  
		Last Modified: Fri, 14 Mar 2025 00:12:52 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45d8bbf7a57dd3620efd19eeec91ec66da9d14a21eabc9fe0e081237797bbd4`  
		Last Modified: Fri, 14 Mar 2025 00:12:54 GMT  
		Size: 27.0 MB (27027796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a07bb3f99fc92c8ce84c04e736eda3823fa432612fb816aaccbe8062dbd123`  
		Last Modified: Fri, 14 Mar 2025 00:12:53 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50439041fc2f4cbaf98da069afa0b1f2c154a6017d56d9c359c959206687c5a`  
		Last Modified: Fri, 14 Mar 2025 00:12:54 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42297abcfbe68a49e805eabc399a66e75a21650825f9c4d6c76916f759c1ee32`  
		Last Modified: Fri, 14 Mar 2025 00:12:55 GMT  
		Size: 9.2 KB (9186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:313c093046b1eee2ab683f17d2d557316183f5b759c17eeba98a00a512e3c861`  
		Last Modified: Fri, 14 Mar 2025 02:14:12 GMT  
		Size: 2.0 MB (1972411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45814dd7834c9238f7ef71c1dd2af50dcd744d0cdc7cc5801990d663b49c6471`  
		Last Modified: Fri, 14 Mar 2025 02:14:12 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f297f03c9fcfe28c35d7710afdd49e309980d63962c698f2ef4878a5a58ab4`  
		Last Modified: Fri, 14 Mar 2025 02:14:12 GMT  
		Size: 740.8 KB (740828 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ffc2deca164f5e7ad08673fafc1c0fdb7fe40ecb898b67fe77e07bb7f8424dc`  
		Last Modified: Fri, 14 Mar 2025 02:14:12 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d769b354510c5bf7b76d6d41a788dee8f33d13f8c5639ddaa18040aa5c61795`  
		Last Modified: Fri, 14 Mar 2025 02:14:14 GMT  
		Size: 21.5 MB (21480598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:10-fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:8e2aa2d65822a324b6fa880cd94ca5987a66e67b492b101a7d7d4bfacd52e230
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6517854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:972caeca27de0df12b3bd9e94a49998b4c8ef851edca1ca43b8114d8ae47d37c`

```dockerfile
```

-	Layers:
	-	`sha256:2e69a41fea96c3627a0bcaaf7f52240f39ee1d47a5d6665ba830d8ccf23cfc5a`  
		Last Modified: Fri, 14 Mar 2025 02:14:12 GMT  
		Size: 6.5 MB (6483616 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17fd0aad44226ee2a179dda2e868187f2c9c2f0177ade5fd1bb8f795b96df624`  
		Last Modified: Fri, 14 Mar 2025 02:14:12 GMT  
		Size: 34.2 KB (34238 bytes)  
		MIME: application/vnd.in-toto+json
