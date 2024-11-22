## `drupal:php8.3-fpm-bookworm`

```console
$ docker pull drupal@sha256:b45c6c0ace8a349ca62f44ce7efdfc9c783508d1031219ad081eca329e4b3ef2
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

### `drupal:php8.3-fpm-bookworm` - linux; amd64

```console
$ docker pull drupal@sha256:0a07567b54a0ed1555d3b4110c3921dc06dba466e690012141f723a5eec5bb40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.9 MB (195927153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb30f180fefd2ac6db7b32462a2221f3be89686c21a21f645062b63727163e8e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 20 Nov 2024 22:37:48 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_VERSION=8.3.14
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.14.tar.xz.asc
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_SHA256=58b4cb9019bf70c0cbcdb814c7df79b9065059d14cf7dbf48d971f8e56ae9be7
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 20 Nov 2024 22:37:48 GMT
WORKDIR /var/www/html
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
STOPSIGNAL SIGQUIT
# Wed, 20 Nov 2024 22:37:48 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 20 Nov 2024 22:37:48 GMT
CMD ["php-fpm"]
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV DRUPAL_VERSION=11.0.8
# Wed, 20 Nov 2024 22:37:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 20 Nov 2024 22:37:48 GMT
WORKDIR /opt/drupal
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:2d429b9e73a6cf90a5bb85105c8118b30a1b2deedeae3ea9587055ffcb80eb45`  
		Last Modified: Tue, 12 Nov 2024 00:55:04 GMT  
		Size: 29.1 MB (29127995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7759049b801c269d81529f7b407b04482b5fbbe0a3c0ee52372a7115bdf696cc`  
		Last Modified: Thu, 21 Nov 2024 17:59:53 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e70a7586a08430682ae1e39afa0d7d48c8cf4b31cce7e36864613f7b3b0659f`  
		Last Modified: Thu, 21 Nov 2024 17:59:59 GMT  
		Size: 104.3 MB (104345885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc5fdb37f5266d8fd4c16c5ef526c20c0237499b8e83d1078574cdbf24a9b9c3`  
		Last Modified: Thu, 21 Nov 2024 17:59:53 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d518f36b3fbf9bd1329c2d3b6ef4391e81cbcebd8f6043064cd1799d768fdd`  
		Last Modified: Thu, 21 Nov 2024 17:59:54 GMT  
		Size: 12.6 MB (12629175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf3c21dfd7566beafe63efe651e11f04f36075676592fe1c0ffded03153d65d`  
		Last Modified: Thu, 21 Nov 2024 17:59:54 GMT  
		Size: 488.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc3127a5df190a0b433986a62cc3a93576175007de8a336149ae0389acab543`  
		Last Modified: Thu, 21 Nov 2024 17:59:56 GMT  
		Size: 27.8 MB (27818942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90ad2b29d7b3149c12be72d3d78831ebd43f173615ade176c6fbc7ecd97b53b`  
		Last Modified: Thu, 21 Nov 2024 17:59:55 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b2f9c382df984bf069eceaf5f8b1ec6a191b1681e6996d27405cd094d0b457`  
		Last Modified: Thu, 21 Nov 2024 17:59:55 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19a7cd6db971a01a7ecb27b3620c1174ae21ddbae7ab99a6c7fa07d103a34ee0`  
		Last Modified: Thu, 21 Nov 2024 17:59:55 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec44ac1ee63ef3b1ec11f8d5c54d8f7eb5103dc2939e0159a1420e40b5806f2`  
		Last Modified: Thu, 21 Nov 2024 19:28:51 GMT  
		Size: 2.0 MB (1976771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c474e2919ce49ffd3cd0e82cc9433661eef465b690fed9aa3df6498631cab60`  
		Last Modified: Thu, 21 Nov 2024 19:28:51 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a444e4d27e2bc66e92dd25b4d2e6b6dddc4dfc7fd758161ef4c1f6df4ef00afc`  
		Last Modified: Thu, 21 Nov 2024 19:28:51 GMT  
		Size: 739.9 KB (739895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f8be384351a041961dff0cbd6e9facd1e3d4c040ba3aeb1d8e62df5228df9e`  
		Last Modified: Thu, 21 Nov 2024 19:28:49 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee8a1057452c07eb3f070f7b620e6d6517404ed4a883aff554c1e971b04f486`  
		Last Modified: Thu, 21 Nov 2024 19:28:52 GMT  
		Size: 19.3 MB (19275207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:ceb8cebbc294970cb018188a8aa94dade3800292174fa35bd7b04258eec4bfb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6383819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3004b0ef3237e73d2a40aa896a3bdf4e4b7ec1cd57141ad50dad75e5288f69b`

```dockerfile
```

-	Layers:
	-	`sha256:fac2667c570a7390d56b5754bd6e443d2a7bf5106d005fb60090303d849d886e`  
		Last Modified: Thu, 21 Nov 2024 19:28:51 GMT  
		Size: 6.3 MB (6346435 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa4542ed5bb5e03cd9bd9bec4e86e0b4d61e752f6d0de7701282b0e3053911ad`  
		Last Modified: Thu, 21 Nov 2024 19:28:51 GMT  
		Size: 37.4 KB (37384 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-bookworm` - linux; arm variant v7

```console
$ docker pull drupal@sha256:5c7f1cf4bbe207f63ac55ac4bfeb9163d38c26cf5d2bef52efcfd7093d176bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160274163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2c3c0c32d53461a3902f11e6ca447c84de7d301a42487d31e8c74680dd0ac1`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 20 Nov 2024 22:37:48 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_VERSION=8.3.14
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.14.tar.xz.asc
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_SHA256=58b4cb9019bf70c0cbcdb814c7df79b9065059d14cf7dbf48d971f8e56ae9be7
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 20 Nov 2024 22:37:48 GMT
WORKDIR /var/www/html
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
STOPSIGNAL SIGQUIT
# Wed, 20 Nov 2024 22:37:48 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 20 Nov 2024 22:37:48 GMT
CMD ["php-fpm"]
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV DRUPAL_VERSION=11.0.8
# Wed, 20 Nov 2024 22:37:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 20 Nov 2024 22:37:48 GMT
WORKDIR /opt/drupal
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4297c5ae3c7e8e8915409622802213bf4512c2b4a0bf9a86ed680878ddc18a70`  
		Last Modified: Tue, 12 Nov 2024 03:10:01 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc4b50adcb7cdffa12052ba1589718b3c06d474e40507177a93fc914de46e895`  
		Last Modified: Tue, 12 Nov 2024 03:10:04 GMT  
		Size: 76.2 MB (76162385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:681174cd466f54c52977f6c159c33d12bdd6aa108d2d06470ff258ce5d3fac19`  
		Last Modified: Tue, 12 Nov 2024 03:10:01 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0570a54dac84d8bcf22b127f03cae9ee74a60b4da6ae4b91c5a103c638bf340`  
		Last Modified: Thu, 21 Nov 2024 18:56:26 GMT  
		Size: 12.6 MB (12627637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ccf670ef1827e4bb261aef16dd119d6d6b1952b817772a4c9a725d1d4ffba8`  
		Last Modified: Thu, 21 Nov 2024 18:56:25 GMT  
		Size: 486.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d2219a13bbccf3d526b01775ba7e74b768f0624853a41ac0899654d1245aef`  
		Last Modified: Thu, 21 Nov 2024 18:56:26 GMT  
		Size: 25.4 MB (25405574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586b4a4d24825dc40711e132d0a079e049fcbd7589e3af1c42a9713e8de80a54`  
		Last Modified: Thu, 21 Nov 2024 18:56:25 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba19d51656f344b0d45df85a41660cea53592240d2d5bf95061f2f87fc159d06`  
		Last Modified: Thu, 21 Nov 2024 18:56:26 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f274b9ac7f18a067551efb09730236855dd2af23c357c6e328983b46cb7fe76`  
		Last Modified: Thu, 21 Nov 2024 18:56:27 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9895ab3f37e7ce12257252a6c54eedf6c1d810c2ff04de4c198de7c4d833cea4`  
		Last Modified: Fri, 22 Nov 2024 04:02:42 GMT  
		Size: 1.3 MB (1331435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aef7fe4b0f0c6045dbbe743d317e8b6ee448d50fd3a4e840d8eeca3eef66baa`  
		Last Modified: Fri, 22 Nov 2024 04:02:41 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccc717b6998ed33fb1a45ebe1e53b06d4baca937ed1f8337c62fc0a2f579f4be`  
		Last Modified: Fri, 22 Nov 2024 04:02:42 GMT  
		Size: 739.9 KB (739899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0930433b8d1bc80107212be9b9d40870b31099b388b07fa61429cdadd7fe8c92`  
		Last Modified: Fri, 22 Nov 2024 04:02:41 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1919e4bafdeca4964122ca7380e8eb5cc0b59f9b504be99e3b3ed4c6d1b4fd06`  
		Last Modified: Fri, 22 Nov 2024 04:02:43 GMT  
		Size: 19.3 MB (19275043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:897f80cc26236d664a80424471d305cd0007d51cdd9a7bc39507d30725e0ad32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6198801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bdd957ca3bcc38735e58ef153f8d166dd55afe61070ddbf117e72607a06e8cb`

```dockerfile
```

-	Layers:
	-	`sha256:ff4e8e505dff88670875aaf224595fffaf2a80b2a30586f48dc2b2712c817191`  
		Last Modified: Fri, 22 Nov 2024 04:02:42 GMT  
		Size: 6.2 MB (6161203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74536791f9f07939df13c0792dfa1d8e0486d3a8de8e432c62e8749013e0d1f7`  
		Last Modified: Fri, 22 Nov 2024 04:02:41 GMT  
		Size: 37.6 KB (37598 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-bookworm` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:059c871c1e65173933cb02358789ddf8387e98914552fa9c58f6db088ed38eb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **189.9 MB (189940753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7ad350df1c26fa80d276fbc8b4c62e60e753b3031a029a6d8f1ed6fbd68d18e`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 20 Nov 2024 22:37:48 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_VERSION=8.3.14
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.14.tar.xz.asc
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_SHA256=58b4cb9019bf70c0cbcdb814c7df79b9065059d14cf7dbf48d971f8e56ae9be7
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 20 Nov 2024 22:37:48 GMT
WORKDIR /var/www/html
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
STOPSIGNAL SIGQUIT
# Wed, 20 Nov 2024 22:37:48 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 20 Nov 2024 22:37:48 GMT
CMD ["php-fpm"]
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV DRUPAL_VERSION=11.0.8
# Wed, 20 Nov 2024 22:37:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 20 Nov 2024 22:37:48 GMT
WORKDIR /opt/drupal
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a2c3efb5abbf8e94e4d66dc2330b25721feadd8a01a30c62c6a2d211e09fcf5`  
		Last Modified: Thu, 21 Nov 2024 17:57:35 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44629439c7e4c1ff8ecf41969075f175aeaa0d716e14846e8e273a98662ac50a`  
		Last Modified: Thu, 21 Nov 2024 17:57:38 GMT  
		Size: 98.1 MB (98130596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebc85a62df490f0424a1d74531ad9dc6c9da15950f9cff18ffc5a1ec77331483`  
		Last Modified: Thu, 21 Nov 2024 17:57:35 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e08390575c8d94825b4bb3b24f34ecc894426149a64f20e10897ad5bb8db51`  
		Last Modified: Thu, 21 Nov 2024 18:48:41 GMT  
		Size: 12.6 MB (12629069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e8526371baa38918754c31cdce9fdb3dc8419e1b103e3a94b62fed21537db6`  
		Last Modified: Thu, 21 Nov 2024 18:48:40 GMT  
		Size: 489.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9ded58418a0347a21e4468af543dbaba5a24824c68d3475ebe69642f8e7306`  
		Last Modified: Thu, 21 Nov 2024 18:56:59 GMT  
		Size: 27.8 MB (27761301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a770d5b10c2d9bc25368889554c5c310ffbb438c4a8d02517292339c89913f24`  
		Last Modified: Thu, 21 Nov 2024 18:56:58 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f403e187444fcfa6dcbd52a4880f2a478d321e53aefec99c5078049cfc9e7aa2`  
		Last Modified: Thu, 21 Nov 2024 18:56:58 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e08b4588665e8f96fb0f8b162c438c94a5cd5dc6f6e1b9c702848840174dc025`  
		Last Modified: Thu, 21 Nov 2024 18:56:58 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4156f30e5bdbf38bb4519d1eedae1a44a7442801415359086601f0644d79b23f`  
		Last Modified: Fri, 22 Nov 2024 04:17:52 GMT  
		Size: 2.2 MB (2234309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85798347163db632a30fcb8a0351ced186c26e29d44f4eccb7a030000be878a`  
		Last Modified: Fri, 22 Nov 2024 04:17:52 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfa0cff77decc777b3b96654707a26f622b193d4f66598bd7bb0fe26a9ac123f`  
		Last Modified: Fri, 22 Nov 2024 04:17:52 GMT  
		Size: 739.9 KB (739900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae550f1e8c9a7750988ff354ece5ed07bba5beb2730950c746f8a36f7dd40208`  
		Last Modified: Fri, 22 Nov 2024 04:17:52 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c81a495104d9da7b617d96a8b030b581aa875f95394a1bd5a35fe54a59bc326`  
		Last Modified: Fri, 22 Nov 2024 04:17:54 GMT  
		Size: 19.3 MB (19274937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:4aa8e2600f6fe25774c788ec22877b3999e7a76d16c535ff3352f6568ee8ba15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6412688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03909206d521e4aa8e26b104ded2612062fb1e7b87cf73e8e6c29d39fc2e5959`

```dockerfile
```

-	Layers:
	-	`sha256:67c158c8f4faed6d440df979165cc6646f97dd30d3c93fa3778655ddda856829`  
		Last Modified: Fri, 22 Nov 2024 04:17:52 GMT  
		Size: 6.4 MB (6375007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf3e25bde31c3411025b8784b416ac37764e87d1a538634186b6de8511809715`  
		Last Modified: Fri, 22 Nov 2024 04:17:52 GMT  
		Size: 37.7 KB (37681 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-bookworm` - linux; 386

```console
$ docker pull drupal@sha256:53c60799a069be3b7ca1c0a6abe460e5c4ed8c74249e4c01806ddd3dd3c95c75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.7 MB (194672362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:973c21c5b92601060105fca7017e070390b6ee780249e1867b748c883a5cb461`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 20 Nov 2024 22:37:48 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_VERSION=8.3.14
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.14.tar.xz.asc
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_SHA256=58b4cb9019bf70c0cbcdb814c7df79b9065059d14cf7dbf48d971f8e56ae9be7
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 20 Nov 2024 22:37:48 GMT
WORKDIR /var/www/html
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
STOPSIGNAL SIGQUIT
# Wed, 20 Nov 2024 22:37:48 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 20 Nov 2024 22:37:48 GMT
CMD ["php-fpm"]
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV DRUPAL_VERSION=11.0.8
# Wed, 20 Nov 2024 22:37:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 20 Nov 2024 22:37:48 GMT
WORKDIR /opt/drupal
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:7379b58056e85869f90d8f78478cafd0c7468ad3b5085482a0850cee625a847a`  
		Last Modified: Tue, 12 Nov 2024 00:54:51 GMT  
		Size: 30.1 MB (30145450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b6b21141c42b0db357a043cff5322268453b96b3a8ba6142cfb28e54509f560`  
		Last Modified: Thu, 21 Nov 2024 17:59:07 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb97b575d5cffe07ec823373b5a13f82e5330383440176af4986d97bf5f361c`  
		Last Modified: Thu, 21 Nov 2024 18:00:32 GMT  
		Size: 101.5 MB (101514332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9679d7ae00252da5c5df438af3405b4d1f08d0d10c0b4a61cbf6063523151a35`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8fc96491d60fd0981298625463ccd59608ad038c1193d9c400ae579d4c719a5`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 12.6 MB (12628544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f842f32d60da7b0029bfdf17fbda7803ecf6cdb09d2d6e75a63eb4417deb0e`  
		Last Modified: Thu, 21 Nov 2024 18:00:29 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c202d238a163cea3b81066d07d9e937a4a548d1e150f798d76684c125d512862`  
		Last Modified: Thu, 21 Nov 2024 18:00:30 GMT  
		Size: 28.3 MB (28327443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef48ccda30c54abc394af1d55b9f70df7765acf0897fc7d64b661984997569f`  
		Last Modified: Thu, 21 Nov 2024 18:00:30 GMT  
		Size: 2.4 KB (2446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:755e3ddb2bd4a49e5269710630dd93933f2c725c5a469a02e8a2d479ea91d783`  
		Last Modified: Thu, 21 Nov 2024 18:00:30 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c4ab7ce43343e2e8e53467286e6d155c83ace4159a593ce2d5bf7b3c44637a`  
		Last Modified: Thu, 21 Nov 2024 18:00:31 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcbe0b800cc208998ba0916040de0b92d1987a350e14b79beaf70eddfa5e4ef`  
		Last Modified: Thu, 21 Nov 2024 19:28:45 GMT  
		Size: 2.0 MB (2028269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c380d9541cd95afd0928fe1e419bcd66d3c71fc7558cf1613f7a3e327615a0`  
		Last Modified: Thu, 21 Nov 2024 19:28:44 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278042e2b02a43e02c06587ca0277fe4d0f2a8be5e615d885a30fc6fa9f56e28`  
		Last Modified: Thu, 21 Nov 2024 19:28:45 GMT  
		Size: 739.9 KB (739890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9def99163eca8bc8e6b66ea82825c0b712802aa3b4d4b5f588c37f8673b5ed80`  
		Last Modified: Thu, 21 Nov 2024 19:28:37 GMT  
		Size: 113.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d725acb1d7471eed50c6894dc3c095033ecc232bbf9b3e065cbf661a5968130`  
		Last Modified: Thu, 21 Nov 2024 19:28:46 GMT  
		Size: 19.3 MB (19275164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:0cc31c20f96dcef954caa768177f1ab87c033f05670de311a0913f15147f427c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6363955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82c64041cfab4c2f8cadb926bf16c5aa77bc976fe1799dfd31092a983c23175d`

```dockerfile
```

-	Layers:
	-	`sha256:d387709d9a275b996f287807a84a8d96bb262aaf010cd761028fe18e06e8e5b7`  
		Last Modified: Thu, 21 Nov 2024 19:28:45 GMT  
		Size: 6.3 MB (6326675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99252dcd8544d639279bb329272bdd80c8e590986e4deda5cecd89f56fea399b`  
		Last Modified: Thu, 21 Nov 2024 19:28:44 GMT  
		Size: 37.3 KB (37280 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-bookworm` - linux; ppc64le

```console
$ docker pull drupal@sha256:5186bce48867a01fc7447376c051c027c4f77a2f0973ee047dea26135b3ac717
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.8 MB (199817199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a326c621aece70f13033725d0a9afbbc578a6da19667ba51c27a5e581f842b37`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 20 Nov 2024 22:37:48 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_VERSION=8.3.14
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.14.tar.xz.asc
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_SHA256=58b4cb9019bf70c0cbcdb814c7df79b9065059d14cf7dbf48d971f8e56ae9be7
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 20 Nov 2024 22:37:48 GMT
WORKDIR /var/www/html
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
STOPSIGNAL SIGQUIT
# Wed, 20 Nov 2024 22:37:48 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 20 Nov 2024 22:37:48 GMT
CMD ["php-fpm"]
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV DRUPAL_VERSION=11.0.8
# Wed, 20 Nov 2024 22:37:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 20 Nov 2024 22:37:48 GMT
WORKDIR /opt/drupal
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b02cceb11c5f92ea5660ac6e0610c26c972c38dae66eeb9d41e3387390540062`  
		Last Modified: Tue, 12 Nov 2024 03:22:53 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c1d6ec9f7f7d2e7f8318e16194758fc58116d42583559cad4394fb117b2d735`  
		Last Modified: Tue, 12 Nov 2024 03:22:56 GMT  
		Size: 103.3 MB (103323960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e883340f45c1d0e36d2a728cca20410ca3254d93c803c062646dc430b8e41e7b`  
		Last Modified: Tue, 12 Nov 2024 03:22:53 GMT  
		Size: 226.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1818c53ea21f26f93892115a80b6bcd45945f906cd1f566c78de150176cf80`  
		Last Modified: Thu, 21 Nov 2024 18:36:47 GMT  
		Size: 12.6 MB (12628773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b105690e04555928450cf109d95712c50ef4db19ebb79f938a121b7993af6332`  
		Last Modified: Thu, 21 Nov 2024 18:36:45 GMT  
		Size: 490.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:decaa6b122db794244a67c543e944681bba276079c6e37b0617a1cf8c22ec09d`  
		Last Modified: Thu, 21 Nov 2024 18:44:56 GMT  
		Size: 28.9 MB (28878026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa0b972313a92327152e2080abfa93ede4a8ac672a2edde572e0ceaaafbe97a8`  
		Last Modified: Thu, 21 Nov 2024 18:44:54 GMT  
		Size: 2.4 KB (2447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754bd8803066f21dfb810ec311d59c94aa6ccc59958c47bd64d536164ec844a1`  
		Last Modified: Thu, 21 Nov 2024 18:44:54 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3784349116e4751d7763725e7140a106bdb27f118732636a99704a32c78d3`  
		Last Modified: Thu, 21 Nov 2024 18:44:54 GMT  
		Size: 9.2 KB (9187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17129eb7173f679a79fa368cf6df0d3caebe4cf6fa99ab14ff13b1941cf0db96`  
		Last Modified: Fri, 22 Nov 2024 01:12:57 GMT  
		Size: 1.8 MB (1832635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be52b8e01708b0dc021f4810cc9c2e2ec5b0e35ac13c850ebce9caf9d341b85f`  
		Last Modified: Fri, 22 Nov 2024 01:12:56 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2cd24968b52a8e530e9cb56d86880fb18131e406a252191d2c858280d8a2cc`  
		Last Modified: Fri, 22 Nov 2024 01:12:56 GMT  
		Size: 739.9 KB (739895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea7af8a888dc474aa01eb4e3a46060001e153048905f5a248742e6ddc81efc2`  
		Last Modified: Fri, 22 Nov 2024 01:12:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e9703a5051dc9325a23004a50a0600c725b89627d5e40db67477019d882d0b`  
		Last Modified: Fri, 22 Nov 2024 01:12:59 GMT  
		Size: 19.3 MB (19275272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:425ab014969468d303bc768404d309ee283b5fb84531d03518162df2175fe097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6360869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84c14cb02ed62767c6dd77a4dd7be5581ac3a28be78d9fc09eb5c8c98d19810`

```dockerfile
```

-	Layers:
	-	`sha256:6e8ba425416ec09b7e11110156b25297c029d62d5db473b30ed7503d99efd70b`  
		Last Modified: Fri, 22 Nov 2024 01:12:56 GMT  
		Size: 6.3 MB (6323355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:554c3a9437fd3eacfbe4c6003bcc62f3ebf44b0e52ec967348463d29afee2a39`  
		Last Modified: Fri, 22 Nov 2024 01:12:56 GMT  
		Size: 37.5 KB (37514 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:php8.3-fpm-bookworm` - linux; s390x

```console
$ docker pull drupal@sha256:8f76aa070fd7ef5f4a7746c52255cc59521f80a54d94f5809071fc68bf6046cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.4 MB (169414673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53433521e53a0c2225061be83ba731c0fc015b71cd78f44e2a5209bdb77ecb73`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Mon, 11 Nov 2024 00:00:00 GMT
ADD rootfs.tar.xz / # buildkit
# Mon, 11 Nov 2024 00:00:00 GMT
CMD ["bash"]
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Wed, 20 Nov 2024 22:37:48 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_VERSION=8.3.14
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.14.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.14.tar.xz.asc
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PHP_SHA256=58b4cb9019bf70c0cbcdb814c7df79b9065059d14cf7dbf48d971f8e56ae9be7
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
COPY docker-php-source /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
COPY docker-php-ext-* docker-php-entrypoint /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN docker-php-ext-enable sodium # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Wed, 20 Nov 2024 22:37:48 GMT
WORKDIR /var/www/html
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini" # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
STOPSIGNAL SIGQUIT
# Wed, 20 Nov 2024 22:37:48 GMT
EXPOSE map[9000/tcp:{}]
# Wed, 20 Nov 2024 22:37:48 GMT
CMD ["php-fpm"]
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV DRUPAL_VERSION=11.0.8
# Wed, 20 Nov 2024 22:37:48 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Wed, 20 Nov 2024 22:37:48 GMT
WORKDIR /opt/drupal
# Wed, 20 Nov 2024 22:37:48 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Wed, 20 Nov 2024 22:37:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557ec8c9288f91e0e914bc88a84e7f99c5caf8f6d9840288a739773c38a7c07a`  
		Last Modified: Tue, 12 Nov 2024 03:15:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c26af4e0d7a3fb552ad3968a1cee38ccd36f353e2162832fca3623342e7ab8a`  
		Last Modified: Tue, 12 Nov 2024 03:15:07 GMT  
		Size: 80.8 MB (80817024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36392fa6e835e08d294727ebd2c1c3a2bb6f80d6dc6273a5056d2f6ed2c1ffed`  
		Last Modified: Tue, 12 Nov 2024 03:15:05 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9208204278e8e8005fba9511ad68f3bc9e60bffc7edd430552878e49a3553157`  
		Last Modified: Thu, 21 Nov 2024 18:59:46 GMT  
		Size: 12.6 MB (12628031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d537632fa697a10a41ae1643135164d8f0c00a94fe3944cfc73673147e04d1b`  
		Last Modified: Thu, 21 Nov 2024 18:59:45 GMT  
		Size: 487.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f62b788c4f143003a5657f18badaa5a750ef316c21c62dc21dfda29e2f18a7d`  
		Last Modified: Thu, 21 Nov 2024 19:08:04 GMT  
		Size: 26.9 MB (26919293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d303fe22bcf212ba2b92089297ce2a12ecd7098b96233deef5de8fc4fb4e8d`  
		Last Modified: Thu, 21 Nov 2024 19:08:03 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f75a480ea0ecd0aceb28679a2492b506b43bd1afa549336dce16080e72b53f9`  
		Last Modified: Thu, 21 Nov 2024 19:08:03 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79b565567b28f940ec2218889c4d9dfc45774c9b08161e4d3bef54ac95cb1a98`  
		Last Modified: Thu, 21 Nov 2024 19:08:03 GMT  
		Size: 9.2 KB (9178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad041706d742bbb35151debc1bd5521ef1f80e4efc34f60bab51f191bb7da59c`  
		Last Modified: Fri, 22 Nov 2024 02:20:30 GMT  
		Size: 1.5 MB (1530368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098bb6f15887208c769798fd57347030a9849f412040bef6a86dc594bc869e65`  
		Last Modified: Fri, 22 Nov 2024 02:20:30 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86f9f561d2fee322a09c1bfe3ef34134db4e7800c9a19971b0126da46132142c`  
		Last Modified: Fri, 22 Nov 2024 02:20:30 GMT  
		Size: 739.9 KB (739894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb2037770d54b2e074dab9128ec230ce06696ce2ec378c23f2e09b7eba12dab`  
		Last Modified: Fri, 22 Nov 2024 02:20:30 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1830bafe13c2a8f86235a4fc2979b8d6312fab11b2f021703f65b4513f12bc`  
		Last Modified: Fri, 22 Nov 2024 02:20:31 GMT  
		Size: 19.3 MB (19275161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:php8.3-fpm-bookworm` - unknown; unknown

```console
$ docker pull drupal@sha256:4e19f1e411a04f3af91c68579010fc7f5a7ce5d61f91e5a53e146c6c90dea84b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6225043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44c8295f6acc66a76448916fddeeef6b2ac0dd1ac60976abc5cd464bdafab74f`

```dockerfile
```

-	Layers:
	-	`sha256:c98aa5113a2ec44c923ca386ebdb05887d55dd6fd671ccd250f96bf2d4fbb1fa`  
		Last Modified: Fri, 22 Nov 2024 02:20:30 GMT  
		Size: 6.2 MB (6187665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0f87b92cb04e86ac4797d6d8af9eec0109b4691ca0f6e67ea404bbf63a93538`  
		Last Modified: Fri, 22 Nov 2024 02:20:29 GMT  
		Size: 37.4 KB (37378 bytes)  
		MIME: application/vnd.in-toto+json
