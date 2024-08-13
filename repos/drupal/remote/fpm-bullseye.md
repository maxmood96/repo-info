## `drupal:fpm-bullseye`

```console
$ docker pull drupal@sha256:320a0725bdbe1b0ceb9e42444d19a3f9e1818da298ca52f4749c0a76222880f7
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

### `drupal:fpm-bullseye` - linux; amd64

```console
$ docker pull drupal@sha256:1dca9795a49e1d35d9376e20dff88b51f22bd7580b1893f93626d0eb050c8c9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.5 MB (184506476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16939f9b0b91582d51d7b8e03493ab7c1f7bd854ae28fbdf2b0930959be89e4b`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 08 Aug 2024 09:27:22 GMT
ADD file:8b272f437a81ca538a72714301aab84c945a2ff3829fd205d401f488514d36a9 in / 
# Thu, 08 Aug 2024 09:27:22 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 09:27:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 08 Aug 2024 09:27:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 08 Aug 2024 09:27:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 09:27:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 08 Aug 2024 09:27:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 08 Aug 2024 09:27:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 Aug 2024 09:27:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 Aug 2024 09:27:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 08 Aug 2024 09:27:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 08 Aug 2024 09:27:22 GMT
ENV PHP_VERSION=8.3.10
# Thu, 08 Aug 2024 09:27:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.10.tar.xz.asc
# Thu, 08 Aug 2024 09:27:22 GMT
ENV PHP_SHA256=a0f2179d00931fe7631a12cbc3428f898ca3d99fe564260c115af381d2a1978d
# Thu, 08 Aug 2024 09:27:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 08 Aug 2024 09:27:22 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 08 Aug 2024 09:27:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 08 Aug 2024 09:27:22 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 08 Aug 2024 09:27:22 GMT
RUN docker-php-ext-enable sodium
# Thu, 08 Aug 2024 09:27:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 08 Aug 2024 09:27:22 GMT
WORKDIR /var/www/html
# Thu, 08 Aug 2024 09:27:22 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 08 Aug 2024 09:27:22 GMT
STOPSIGNAL SIGQUIT
# Thu, 08 Aug 2024 09:27:22 GMT
EXPOSE 9000
# Thu, 08 Aug 2024 09:27:22 GMT
CMD ["php-fpm"]
# Thu, 08 Aug 2024 09:27:22 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 09:27:22 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 08 Aug 2024 09:27:22 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 09:27:22 GMT
ENV DRUPAL_VERSION=11.0.1
# Thu, 08 Aug 2024 09:27:22 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 08 Aug 2024 09:27:22 GMT
WORKDIR /opt/drupal
# Thu, 08 Aug 2024 09:27:22 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 08 Aug 2024 09:27:22 GMT
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
	-	`sha256:78beb65ea45356eeec3d9b8195e00b0cc7aafc9f8a0262b06b131105a2cb3cef`  
		Last Modified: Tue, 13 Aug 2024 02:58:11 GMT  
		Size: 12.8 MB (12803672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f21f500f0ee388f8121b4ae4a70ffc2310e28aef82e70ab21326a48bed88ea40`  
		Last Modified: Tue, 13 Aug 2024 02:58:10 GMT  
		Size: 491.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1254680fee09d627250e845465a06c89d2e7e5c9ce7df679be9140eab538fb`  
		Last Modified: Tue, 13 Aug 2024 02:58:52 GMT  
		Size: 26.8 MB (26758610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6b59b8f2ccdd8112b96305fd9e608be3314461bc74c45daa692d79f3001e157`  
		Last Modified: Tue, 13 Aug 2024 02:58:48 GMT  
		Size: 2.5 KB (2452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4da30b35eeeb9d7ec0280c5f464fd4c3ff5eacd168deba51d59ab388c6c34464`  
		Last Modified: Tue, 13 Aug 2024 02:58:48 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f46a5d191a54cc002d55337ba08b4fd6ca499ba7926278abc88d74661e62fb9d`  
		Last Modified: Tue, 13 Aug 2024 02:58:48 GMT  
		Size: 9.2 KB (9180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1a26a4e333c4d28a81a24e70d23e90e6487102cfacc777f487096b93b78969`  
		Last Modified: Tue, 13 Aug 2024 04:01:48 GMT  
		Size: 1.9 MB (1904631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f58f53b0dcd2771d7ee39175c97dab5ffbcddfb7892bc7c59b5916f808ac9d7`  
		Last Modified: Tue, 13 Aug 2024 04:01:47 GMT  
		Size: 312.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3734d6c4c203156cf44a691de4a0a7c00e93e4aadfbc42ebe51b33e12fd7cef6`  
		Last Modified: Tue, 13 Aug 2024 04:01:47 GMT  
		Size: 726.3 KB (726340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6af9e54c61f704edfb2dc975f4fa36eb230d8e4c92f90f090295e2bab1aa0a0a`  
		Last Modified: Tue, 13 Aug 2024 04:01:45 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c00b8367d881a241246be9d4387828c592f8ffa7cb3e2b61bbab43d4cdcb3b83`  
		Last Modified: Tue, 13 Aug 2024 04:01:48 GMT  
		Size: 19.2 MB (19223528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:c12702c76e6598f98bfe4232ab09aeb8a4a66d7426023e405e6d7c0147074cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6514877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8031084f0dd0e1e45765f5cd0457aa6a194c1a40da4c48ca25f940c18adc687`

```dockerfile
```

-	Layers:
	-	`sha256:0991577698fb1b073a8f9372db4091010c4459bcbe93aaf1a4d9e03895608b0c`  
		Last Modified: Tue, 13 Aug 2024 04:01:47 GMT  
		Size: 6.5 MB (6480741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee54c1de85dba54972a94f2e45182661066d16d167e71e04b912ab5a6361103d`  
		Last Modified: Tue, 13 Aug 2024 04:01:47 GMT  
		Size: 34.1 KB (34136 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-bullseye` - linux; arm variant v7

```console
$ docker pull drupal@sha256:3d40fb33a3f7ffdc4c00e3f1a883b77d70cabcf15fc0e8b92146a1cf45cc2fbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154408558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e1c9fdfeb61227b2b2d5749c09f1c84ebded22baba57c9dd8f57b1eca1eb09b`
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
# Tue, 23 Jul 2024 05:39:35 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 01 Aug 2024 19:27:18 GMT
ENV PHP_VERSION=8.3.10
# Thu, 01 Aug 2024 19:27:18 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.10.tar.xz.asc
# Thu, 01 Aug 2024 19:27:18 GMT
ENV PHP_SHA256=a0f2179d00931fe7631a12cbc3428f898ca3d99fe564260c115af381d2a1978d
# Thu, 01 Aug 2024 19:27:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 01 Aug 2024 19:27:30 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 01 Aug 2024 19:36:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 01 Aug 2024 19:36:49 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 01 Aug 2024 19:36:51 GMT
RUN docker-php-ext-enable sodium
# Thu, 01 Aug 2024 19:36:51 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 01 Aug 2024 19:36:51 GMT
WORKDIR /var/www/html
# Thu, 01 Aug 2024 19:36:53 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 01 Aug 2024 19:36:53 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Aug 2024 19:36:53 GMT
EXPOSE 9000
# Thu, 01 Aug 2024 19:36:54 GMT
CMD ["php-fpm"]
# Thu, 08 Aug 2024 09:27:22 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 09:27:22 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 08 Aug 2024 09:27:22 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 09:27:22 GMT
ENV DRUPAL_VERSION=11.0.1
# Thu, 08 Aug 2024 09:27:22 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 08 Aug 2024 09:27:22 GMT
WORKDIR /opt/drupal
# Thu, 08 Aug 2024 09:27:22 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 08 Aug 2024 09:27:22 GMT
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
	-	`sha256:0a9c22e13ffb0e8c5b7fd2c2a3694c4605edbb4c2fb8108f595bd0d210537727`  
		Last Modified: Thu, 01 Aug 2024 20:07:22 GMT  
		Size: 12.8 MB (12802179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b39bf8a2e54d31cb919e14e55405b8f4c1122e29b9e0049a1175f44c7565491`  
		Last Modified: Thu, 01 Aug 2024 20:07:21 GMT  
		Size: 494.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73aa28fb762454918849f503cc499e0cd11082eace0e2a8bd49adcc9ade1437c`  
		Last Modified: Thu, 01 Aug 2024 20:08:12 GMT  
		Size: 24.4 MB (24444218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9576578359cc06d0a87aa8aaf2f100c7250e512382380ebbc41814db95819b0`  
		Last Modified: Thu, 01 Aug 2024 20:08:08 GMT  
		Size: 2.5 KB (2454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dad1421d8da6aaefff66c6cf48e2eac8cf478c4824c7ea5b675e571ff3f5983`  
		Last Modified: Thu, 01 Aug 2024 20:08:08 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:560857dfc9aa5996b894576526eb4f37b3970af7f29966dd9941bd1f29eb20b2`  
		Last Modified: Thu, 01 Aug 2024 20:08:08 GMT  
		Size: 9.2 KB (9186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550c9b0306ab3092fd12f5a42889820a4363c724d0f5e5427da3fd27fbef7723`  
		Last Modified: Fri, 02 Aug 2024 02:44:45 GMT  
		Size: 1.3 MB (1284674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58bfdc9c8b2b01c30d6f962d38d5ff123198fc84a621ec1e0091b35bd3432b0f`  
		Last Modified: Fri, 02 Aug 2024 02:44:45 GMT  
		Size: 317.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7820076db68e6c18c71facfc98fd379c48906333944ad0a3d5c1f59aa90c553c`  
		Last Modified: Fri, 02 Aug 2024 02:44:45 GMT  
		Size: 726.3 KB (726342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7992d54c9e9090d7e9dddcc10d3ec841b7dd193a36b11ddd32c6771abd6e42c`  
		Last Modified: Fri, 02 Aug 2024 02:44:45 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f44b4a08152db8e4b4345958c59e174400bc49e5c2d124d6b5a07d582d98507`  
		Last Modified: Thu, 08 Aug 2024 19:02:01 GMT  
		Size: 19.2 MB (19222655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:0d10750b3b67ce5ec0d22a8b6537b2b08a6c1d173063692bc64bb2641c80af9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6324141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0aef038c894e0534b69f95be678aeeccd6e5f416a50b1b004dcccbcab134cd5`

```dockerfile
```

-	Layers:
	-	`sha256:cc08e30114f544a764b3db73c625b8b4b82c25c08f22fd608877d500fe5ba24f`  
		Last Modified: Thu, 08 Aug 2024 19:02:00 GMT  
		Size: 6.3 MB (6289800 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79767269777f3362fcd5d94405a99fe0be54a35505f269b3a78713c24684f7ac`  
		Last Modified: Thu, 08 Aug 2024 19:02:00 GMT  
		Size: 34.3 KB (34341 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-bullseye` - linux; arm64 variant v8

```console
$ docker pull drupal@sha256:6050fb7ffb29d0357b6b229f1390c0c73e31c2444245f4893dadd62fa593a023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.7 MB (178745852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74134d94b88948d1cd1720506285a7994491525f9ec5f02af616270a908a322f`
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
# Tue, 23 Jul 2024 05:47:35 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 01 Aug 2024 19:04:14 GMT
ENV PHP_VERSION=8.3.10
# Thu, 01 Aug 2024 19:04:14 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.10.tar.xz.asc
# Thu, 01 Aug 2024 19:04:14 GMT
ENV PHP_SHA256=a0f2179d00931fe7631a12cbc3428f898ca3d99fe564260c115af381d2a1978d
# Thu, 01 Aug 2024 19:04:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 01 Aug 2024 19:04:24 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 01 Aug 2024 19:13:37 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 01 Aug 2024 19:13:37 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 01 Aug 2024 19:13:38 GMT
RUN docker-php-ext-enable sodium
# Thu, 01 Aug 2024 19:13:38 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 01 Aug 2024 19:13:38 GMT
WORKDIR /var/www/html
# Thu, 01 Aug 2024 19:13:39 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 01 Aug 2024 19:13:39 GMT
STOPSIGNAL SIGQUIT
# Thu, 01 Aug 2024 19:13:39 GMT
EXPOSE 9000
# Thu, 01 Aug 2024 19:13:39 GMT
CMD ["php-fpm"]
# Thu, 08 Aug 2024 09:27:22 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 09:27:22 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 08 Aug 2024 09:27:22 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 09:27:22 GMT
ENV DRUPAL_VERSION=11.0.1
# Thu, 08 Aug 2024 09:27:22 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 08 Aug 2024 09:27:22 GMT
WORKDIR /opt/drupal
# Thu, 08 Aug 2024 09:27:22 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 08 Aug 2024 09:27:22 GMT
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
	-	`sha256:0326e80fb48b88e073627501183ce76c434b83885f0258f98eaeec394e909b86`  
		Last Modified: Thu, 01 Aug 2024 19:48:29 GMT  
		Size: 12.8 MB (12803028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24c2de294fc655b25302a1c3fe4cc4b2d73ee72c96f70b28d965b2359fb71655`  
		Last Modified: Thu, 01 Aug 2024 19:48:28 GMT  
		Size: 493.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e373694afd39dfe359df8b8b487a9fb1fc09631a4847e37e4f9c67fe1fff169`  
		Last Modified: Thu, 01 Aug 2024 19:49:11 GMT  
		Size: 26.8 MB (26796710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e25a1d0697491d41be13f0e708d8c03ab8a1da9ddf2a48409ee7cc42aef27a59`  
		Last Modified: Thu, 01 Aug 2024 19:49:08 GMT  
		Size: 2.5 KB (2453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36331a2356a7da9a30a4e0febf38c062afb5966aa909cf8eed3b14325878907a`  
		Last Modified: Thu, 01 Aug 2024 19:49:08 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93d8dd9c54b26f982f31d2de064514590b1f5497397d736edae1a17feaf3ac35`  
		Last Modified: Thu, 01 Aug 2024 19:49:08 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be35cfdb5624fdc12450dedb4210ca896e9b9f727fc4de2ffae6f13fc8ad9803`  
		Last Modified: Fri, 02 Aug 2024 05:14:34 GMT  
		Size: 2.2 MB (2168591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18d3b6ce0dba406412f08c2291786bc117f08737cb1f00c21937cd3f3f01b232`  
		Last Modified: Fri, 02 Aug 2024 05:14:33 GMT  
		Size: 318.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa24c9a4c47961b146269f133236b58c39de55b24055aa74fc0f91328ebc193c`  
		Last Modified: Fri, 02 Aug 2024 05:14:34 GMT  
		Size: 726.3 KB (726341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c4f2e5e6d41c9fbad2245a18d0e00517ea83a36d8c402012cd8563a89a4b09`  
		Last Modified: Fri, 02 Aug 2024 05:14:34 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:319e5c808a4fc164d8d20e0b89ee203a98475b345d96bc02c781f74bfb2cfbbc`  
		Last Modified: Thu, 08 Aug 2024 19:01:03 GMT  
		Size: 19.2 MB (19223178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:2df1a73b5949f93ee13a508abffaae3ec81434a566b54c0e6dfeb6be367b564a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6518544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0177c6e30cd1747d8db3670133d216a71fe26fb37ea0f099c5a8885f3d781285`

```dockerfile
```

-	Layers:
	-	`sha256:6d51da580bdb59157ad1a5fe378dc44ac677b9f65a354cba1e40f8ed70840f1b`  
		Last Modified: Thu, 08 Aug 2024 19:01:02 GMT  
		Size: 6.5 MB (6483674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b875c9abbaf7923442fc01dc0abfd37111f6c62c1db3aaee134ce8d6f18510d`  
		Last Modified: Thu, 08 Aug 2024 19:01:02 GMT  
		Size: 34.9 KB (34870 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-bullseye` - linux; 386

```console
$ docker pull drupal@sha256:f58e30ad7b1e0870294ec48e60ac75a851aa5b305808d941e3895f95920fd423
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.1 MB (187097201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e322f01fe339f5af8a59b27d1267cef4fe9d83fcc584809a9fec29d421d78690`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 08 Aug 2024 09:27:22 GMT
ADD file:3c28079e98aa5b4ba96d948760be5fa7d7f99c878e193a63fab4f18eda2ee67e in / 
# Thu, 08 Aug 2024 09:27:22 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 09:27:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 08 Aug 2024 09:27:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 08 Aug 2024 09:27:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 09:27:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 08 Aug 2024 09:27:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 08 Aug 2024 09:27:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 Aug 2024 09:27:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 Aug 2024 09:27:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 08 Aug 2024 09:27:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 08 Aug 2024 09:27:22 GMT
ENV PHP_VERSION=8.3.10
# Thu, 08 Aug 2024 09:27:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.10.tar.xz.asc
# Thu, 08 Aug 2024 09:27:22 GMT
ENV PHP_SHA256=a0f2179d00931fe7631a12cbc3428f898ca3d99fe564260c115af381d2a1978d
# Thu, 08 Aug 2024 09:27:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 08 Aug 2024 09:27:22 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 08 Aug 2024 09:27:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 08 Aug 2024 09:27:22 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 08 Aug 2024 09:27:22 GMT
RUN docker-php-ext-enable sodium
# Thu, 08 Aug 2024 09:27:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 08 Aug 2024 09:27:22 GMT
WORKDIR /var/www/html
# Thu, 08 Aug 2024 09:27:22 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 08 Aug 2024 09:27:22 GMT
STOPSIGNAL SIGQUIT
# Thu, 08 Aug 2024 09:27:22 GMT
EXPOSE 9000
# Thu, 08 Aug 2024 09:27:22 GMT
CMD ["php-fpm"]
# Thu, 08 Aug 2024 09:27:22 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 09:27:22 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 08 Aug 2024 09:27:22 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 09:27:22 GMT
ENV DRUPAL_VERSION=11.0.1
# Thu, 08 Aug 2024 09:27:22 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 08 Aug 2024 09:27:22 GMT
WORKDIR /opt/drupal
# Thu, 08 Aug 2024 09:27:22 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 08 Aug 2024 09:27:22 GMT
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
	-	`sha256:8cc3f207dd05ab11a6ad70d437c1306652eb91fc9d6261e0007947b2764e1c19`  
		Last Modified: Tue, 13 Aug 2024 07:46:54 GMT  
		Size: 12.8 MB (12802953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d17b3eff80aaecea3a7f2e60cad188777db6ecb46f7236a57557a8043332700`  
		Last Modified: Tue, 13 Aug 2024 07:46:52 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47bd0a70747ef75f0b34623638058b67ecb138c171e8cd1bdd38739b24f3a233`  
		Last Modified: Tue, 13 Aug 2024 07:47:40 GMT  
		Size: 27.2 MB (27224925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082b6e9ed9f7bd3a61ec74a9dd7948edb85fcbfe52af4a38d71a59fa41aa5855`  
		Last Modified: Tue, 13 Aug 2024 07:47:35 GMT  
		Size: 2.5 KB (2451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4bca1ccdee749103dabb2bd70868bbec69601fbaf6063810cc163148eeabdc1`  
		Last Modified: Tue, 13 Aug 2024 07:47:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de7c91754629b3e0c59bb2fc61115f6a0be2a2976ac6936f7ab2dd27d1e5365d`  
		Last Modified: Tue, 13 Aug 2024 07:47:35 GMT  
		Size: 9.2 KB (9181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e396cca4db6719752e2a155bf8736f5258790264e0b955369c793b68fb58d3`  
		Last Modified: Tue, 13 Aug 2024 08:59:51 GMT  
		Size: 2.0 MB (1971282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9674607a09ef14b6f03d9b5180586c8987c80cae433198bba9a2960829372f6f`  
		Last Modified: Tue, 13 Aug 2024 08:59:51 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:199cd30d90343c146b9e586c5e3d998cb45a0358cfdf91b55cf3fd95c45a1b7f`  
		Last Modified: Tue, 13 Aug 2024 08:59:51 GMT  
		Size: 726.3 KB (726347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f3949c79d1da6925b94d32fda1c49a71a09a60c43c6484e136641309fc6eaec`  
		Last Modified: Tue, 13 Aug 2024 08:59:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3ec23fd9e04da7d1dc07697df30b77925e367ce62fd3e5c206ab2fe6f82161`  
		Last Modified: Tue, 13 Aug 2024 08:59:53 GMT  
		Size: 19.2 MB (19223630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:c4157e9158b6372e49d2d388b674e2397918c151dd540c2d850fe1562d29050f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6505666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b21f0c8111ac6ac1bcb8d864e512b1587099f6ead0be482d2afdc275fcacbb0`

```dockerfile
```

-	Layers:
	-	`sha256:6ea0d3ec669464b169f2735049e17fce8230751e58bcec5e9f2ef525d32d7a8a`  
		Last Modified: Tue, 13 Aug 2024 08:59:51 GMT  
		Size: 6.5 MB (6471589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c284503b6ac24bb7f070b29e035059238d87f7e7d4d827144743e9dd4fe53513`  
		Last Modified: Tue, 13 Aug 2024 08:59:51 GMT  
		Size: 34.1 KB (34077 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-bullseye` - linux; ppc64le

```console
$ docker pull drupal@sha256:f463e9b8e604dace76ee938a76dd16df539e9fb98859455504f8d88d0e9cf35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.3 MB (184324759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46cc034e09971ab21e9dbee7b3320a1ea59112f364c6e3ef9fb8cfb24c66e3ca`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 08 Aug 2024 09:27:22 GMT
ADD file:715c22b2255eb123bfbede0885c3f36e9320dbf42add04a4424aa8b7c213146e in / 
# Thu, 08 Aug 2024 09:27:22 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 09:27:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 08 Aug 2024 09:27:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 08 Aug 2024 09:27:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 09:27:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 08 Aug 2024 09:27:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 08 Aug 2024 09:27:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 Aug 2024 09:27:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 Aug 2024 09:27:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 08 Aug 2024 09:27:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 08 Aug 2024 09:27:22 GMT
ENV PHP_VERSION=8.3.10
# Thu, 08 Aug 2024 09:27:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.10.tar.xz.asc
# Thu, 08 Aug 2024 09:27:22 GMT
ENV PHP_SHA256=a0f2179d00931fe7631a12cbc3428f898ca3d99fe564260c115af381d2a1978d
# Thu, 08 Aug 2024 09:27:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 08 Aug 2024 09:27:22 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 08 Aug 2024 09:27:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 08 Aug 2024 09:27:22 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 08 Aug 2024 09:27:22 GMT
RUN docker-php-ext-enable sodium
# Thu, 08 Aug 2024 09:27:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 08 Aug 2024 09:27:22 GMT
WORKDIR /var/www/html
# Thu, 08 Aug 2024 09:27:22 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 08 Aug 2024 09:27:22 GMT
STOPSIGNAL SIGQUIT
# Thu, 08 Aug 2024 09:27:22 GMT
EXPOSE 9000
# Thu, 08 Aug 2024 09:27:22 GMT
CMD ["php-fpm"]
# Thu, 08 Aug 2024 09:27:22 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 09:27:22 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 08 Aug 2024 09:27:22 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 09:27:22 GMT
ENV DRUPAL_VERSION=11.0.1
# Thu, 08 Aug 2024 09:27:22 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 08 Aug 2024 09:27:22 GMT
WORKDIR /opt/drupal
# Thu, 08 Aug 2024 09:27:22 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 08 Aug 2024 09:27:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/drupal/vendor/bin
```

-	Layers:
	-	`sha256:b900d36478638456315492fd30b0de0aeac56205b9198ff240ac61a39d17ba97`  
		Last Modified: Tue, 13 Aug 2024 00:27:11 GMT  
		Size: 35.3 MB (35305133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acccc6cd204dfdd1d7a4546e484b312ba783126fc54fc14547d272642342d2c2`  
		Last Modified: Tue, 13 Aug 2024 03:24:58 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6905d94fdf281fc926213ed4a8898dee15c28b9c067f741d973779a7299b78d`  
		Last Modified: Tue, 13 Aug 2024 03:25:13 GMT  
		Size: 86.7 MB (86650811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f25e18c2f6556a0096abd2faed23b5a7239c8c0c64bd7005786e087f1915b8e8`  
		Last Modified: Tue, 13 Aug 2024 03:24:58 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d371276b87289dd14a77407c60dd7b77c7a0349a1a89850504cf6eee533da3aa`  
		Last Modified: Tue, 13 Aug 2024 03:28:09 GMT  
		Size: 12.8 MB (12803579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baaf76f5a53e519cf3e559f28bc57a9a5f73e52ade241c457119a67dba45746e`  
		Last Modified: Tue, 13 Aug 2024 03:28:08 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b9d9e410d7154bea63d6f273aac941624e04843a9f2743fb554d013758c26b`  
		Last Modified: Tue, 13 Aug 2024 03:28:54 GMT  
		Size: 27.8 MB (27832890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c9cc2f746ac5050d4f67d8c4d5fcb4579b1a8aea1462fb89f09ffa98dea88c`  
		Last Modified: Tue, 13 Aug 2024 03:28:49 GMT  
		Size: 2.4 KB (2449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aadaa8c65f5671123675d076a7467fbec30a9935cc18d7f78cacb0a4497bc50`  
		Last Modified: Tue, 13 Aug 2024 03:28:49 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c08ed6e34fe051f2e45a020bda3c6c4dd1f5090802fe18902d1f6524fc8caa49`  
		Last Modified: Tue, 13 Aug 2024 03:28:49 GMT  
		Size: 9.2 KB (9182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e52302e8f2d4b87afcae0c3138d1633f182bc88997169a89fabc0180c19408d`  
		Last Modified: Tue, 13 Aug 2024 13:15:11 GMT  
		Size: 1.8 MB (1769017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2d239a5fab370a176f3a57bd378ceb83fd206928a1bde702cd683510af71981`  
		Last Modified: Tue, 13 Aug 2024 13:15:12 GMT  
		Size: 316.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439162379e48a71eb90cd146d7a4f24fff49915c57a87a1bfdf0a62d560e7f84`  
		Last Modified: Tue, 13 Aug 2024 13:15:12 GMT  
		Size: 726.3 KB (726341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36386b0de4fd815dac409fab815d91a08e92b4afbb57b4588cb8f3085eee623b`  
		Last Modified: Tue, 13 Aug 2024 13:15:12 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283063bcf8033bce90b85b7185fb373e6f5cac5a113ff9d94de272c2c7058f72`  
		Last Modified: Tue, 13 Aug 2024 13:15:13 GMT  
		Size: 19.2 MB (19223737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:706831eab2a9df18f5fdca4c340b99ea2d3446c46e9d33b3cb53771f5786f44c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6480846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cd006cf8779cda2d200b9b3acec0894e6cb180d2f4b6a79ccc84a36a0ec68e7`

```dockerfile
```

-	Layers:
	-	`sha256:595d9a0414bebfce0b40fe2567498cd8672df63806b68971813f912b776ebed8`  
		Last Modified: Tue, 13 Aug 2024 13:15:09 GMT  
		Size: 6.4 MB (6446579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8ad97af517e4d215a75b025fc071a23fd3904ed63d53639360744de5ecc9a31`  
		Last Modified: Tue, 13 Aug 2024 13:15:08 GMT  
		Size: 34.3 KB (34267 bytes)  
		MIME: application/vnd.in-toto+json

### `drupal:fpm-bullseye` - linux; s390x

```console
$ docker pull drupal@sha256:99bb17e3decc311fe2a5fdbf67dec8c6f83797799806b31a2c94fb542695a30e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.5 MB (161528057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99204fbf821fd84669dd1820280d223a40cb2dea30008ec774f693f7decfdea5`
-	Entrypoint: `["docker-php-entrypoint"]`
-	Default Command: `["php-fpm"]`

```dockerfile
# Thu, 08 Aug 2024 09:27:22 GMT
ADD file:a473fc09ddb0d1045f7f330f3a48b9cfe65ff9ea65cfa5c8262a8a5be9d4db75 in / 
# Thu, 08 Aug 2024 09:27:22 GMT
CMD ["bash"]
# Thu, 08 Aug 2024 09:27:22 GMT
RUN set -eux; 	{ 		echo 'Package: php*'; 		echo 'Pin: release *'; 		echo 'Pin-Priority: -1'; 	} > /etc/apt/preferences.d/no-debian-php
# Thu, 08 Aug 2024 09:27:22 GMT
ENV PHPIZE_DEPS=autoconf 		dpkg-dev 		file 		g++ 		gcc 		libc-dev 		make 		pkg-config 		re2c
# Thu, 08 Aug 2024 09:27:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		$PHPIZE_DEPS 		ca-certificates 		curl 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 08 Aug 2024 09:27:22 GMT
ENV PHP_INI_DIR=/usr/local/etc/php
# Thu, 08 Aug 2024 09:27:22 GMT
RUN set -eux; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	[ ! -d /var/www/html ]; 	mkdir -p /var/www/html; 	chown www-data:www-data /var/www/html; 	chmod 1777 /var/www/html
# Thu, 08 Aug 2024 09:27:22 GMT
ENV PHP_CFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 Aug 2024 09:27:22 GMT
ENV PHP_CPPFLAGS=-fstack-protector-strong -fpic -fpie -O2 -D_LARGEFILE_SOURCE -D_FILE_OFFSET_BITS=64
# Thu, 08 Aug 2024 09:27:22 GMT
ENV PHP_LDFLAGS=-Wl,-O1 -pie
# Thu, 08 Aug 2024 09:27:22 GMT
ENV GPG_KEYS=1198C0117593497A5EC5C199286AF1F9897469DC C28D937575603EB4ABB725861C0779DC5C0A9DE4 AFD8691FDAEDF03BDF6E460563F15A9B715376CA
# Thu, 08 Aug 2024 09:27:22 GMT
ENV PHP_VERSION=8.3.10
# Thu, 08 Aug 2024 09:27:22 GMT
ENV PHP_URL=https://www.php.net/distributions/php-8.3.10.tar.xz PHP_ASC_URL=https://www.php.net/distributions/php-8.3.10.tar.xz.asc
# Thu, 08 Aug 2024 09:27:22 GMT
ENV PHP_SHA256=a0f2179d00931fe7631a12cbc3428f898ca3d99fe564260c115af381d2a1978d
# Thu, 08 Aug 2024 09:27:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends gnupg; 	rm -rf /var/lib/apt/lists/*; 		mkdir -p /usr/src; 	cd /usr/src; 		curl -fsSL -o php.tar.xz "$PHP_URL"; 		if [ -n "$PHP_SHA256" ]; then 		echo "$PHP_SHA256 *php.tar.xz" | sha256sum -c -; 	fi; 		if [ -n "$PHP_ASC_URL" ]; then 		curl -fsSL -o php.tar.xz.asc "$PHP_ASC_URL"; 		export GNUPGHOME="$(mktemp -d)"; 		for key in $GPG_KEYS; do 			gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key"; 		done; 		gpg --batch --verify php.tar.xz.asc php.tar.xz; 		gpgconf --kill all; 		rm -rf "$GNUPGHOME"; 	fi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false
# Thu, 08 Aug 2024 09:27:22 GMT
COPY file:ce57c04b70896f77cc11eb2766417d8a1240fcffe5bba92179ec78c458844110 in /usr/local/bin/ 
# Thu, 08 Aug 2024 09:27:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libargon2-dev 		libcurl4-openssl-dev 		libonig-dev 		libreadline-dev 		libsodium-dev 		libsqlite3-dev 		libssl-dev 		libxml2-dev 		zlib1g-dev 	; 		export 		CFLAGS="$PHP_CFLAGS" 		CPPFLAGS="$PHP_CPPFLAGS" 		LDFLAGS="$PHP_LDFLAGS" 		PHP_BUILD_PROVIDER='https://github.com/docker-library/php' 		PHP_UNAME='Linux - Docker' 	; 	docker-php-source extract; 	cd /usr/src/php; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	debMultiarch="$(dpkg-architecture --query DEB_BUILD_MULTIARCH)"; 	if [ ! -d /usr/include/curl ]; then 		ln -sT "/usr/include/$debMultiarch/curl" /usr/local/include/curl; 	fi; 	./configure 		--build="$gnuArch" 		--with-config-file-path="$PHP_INI_DIR" 		--with-config-file-scan-dir="$PHP_INI_DIR/conf.d" 				--enable-option-checking=fatal 				--with-mhash 				--with-pic 				--enable-mbstring 		--enable-mysqlnd 		--with-password-argon2 		--with-sodium=shared 		--with-pdo-sqlite=/usr 		--with-sqlite3=/usr 				--with-curl 		--with-iconv 		--with-openssl 		--with-readline 		--with-zlib 				--disable-phpdbg 				--with-pear 				--with-libdir="lib/$debMultiarch" 				--disable-cgi 				--enable-fpm 		--with-fpm-user=www-data 		--with-fpm-group=www-data 	; 	make -j "$(nproc)"; 	find -type f -name '*.a' -delete; 	make install; 	find 		/usr/local 		-type f 		-perm '/0111' 		-exec sh -euxc ' 			strip --strip-all "$@" || : 		' -- '{}' + 	; 	make clean; 		cp -v php.ini-* "$PHP_INI_DIR/"; 		cd /; 	docker-php-source delete; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		pecl update-channels; 	rm -rf /tmp/pear ~/.pearrc; 		php --version
# Thu, 08 Aug 2024 09:27:22 GMT
COPY multi:869bde9dbeae74886a05c9e2107b3e3b4877116db8c6d9adbaff2719f9fb5262 in /usr/local/bin/ 
# Thu, 08 Aug 2024 09:27:22 GMT
RUN docker-php-ext-enable sodium
# Thu, 08 Aug 2024 09:27:22 GMT
ENTRYPOINT ["docker-php-entrypoint"]
# Thu, 08 Aug 2024 09:27:22 GMT
WORKDIR /var/www/html
# Thu, 08 Aug 2024 09:27:22 GMT
RUN set -eux; 	cd /usr/local/etc; 	if [ -d php-fpm.d ]; then 		sed 's!=NONE/!=!g' php-fpm.conf.default | tee php-fpm.conf > /dev/null; 		cp php-fpm.d/www.conf.default php-fpm.d/www.conf; 	else 		mkdir php-fpm.d; 		cp php-fpm.conf.default php-fpm.d/www.conf; 		{ 			echo '[global]'; 			echo 'include=etc/php-fpm.d/*.conf'; 		} | tee php-fpm.conf; 	fi; 	{ 		echo '[global]'; 		echo 'error_log = /proc/self/fd/2'; 		echo; echo '; https://github.com/docker-library/php/pull/725#issuecomment-443540114'; echo 'log_limit = 8192'; 		echo; 		echo '[www]'; 		echo '; php-fpm closes STDOUT on startup, so sending logs to /proc/self/fd/1 does not work.'; 		echo '; https://bugs.php.net/bug.php?id=73886'; 		echo 'access.log = /proc/self/fd/2'; 		echo; 		echo 'clear_env = no'; 		echo; 		echo '; Ensure worker stdout and stderr are sent to the main error log.'; 		echo 'catch_workers_output = yes'; 		echo 'decorate_workers_output = no'; 	} | tee php-fpm.d/docker.conf; 	{ 		echo '[global]'; 		echo 'daemonize = no'; 		echo; 		echo '[www]'; 		echo 'listen = 9000'; 	} | tee php-fpm.d/zz-docker.conf; 	mkdir -p "$PHP_INI_DIR/conf.d"; 	{ 		echo '; https://github.com/docker-library/php/issues/878#issuecomment-938595965'; 		echo 'fastcgi.logging = Off'; 	} > "$PHP_INI_DIR/conf.d/docker-fpm.ini"
# Thu, 08 Aug 2024 09:27:22 GMT
STOPSIGNAL SIGQUIT
# Thu, 08 Aug 2024 09:27:22 GMT
EXPOSE 9000
# Thu, 08 Aug 2024 09:27:22 GMT
CMD ["php-fpm"]
# Thu, 08 Aug 2024 09:27:22 GMT
RUN set -eux; 		if command -v a2enmod; then 		a2enmod expires rewrite; 	fi; 		savedAptMark="$(apt-mark showmanual)"; 		apt-get update; 	apt-get install -y --no-install-recommends 		libfreetype6-dev 		libjpeg-dev 		libpng-dev 		libpq-dev 		libwebp-dev 		libzip-dev 	; 		docker-php-ext-configure gd 		--with-freetype 		--with-jpeg=/usr 		--with-webp 	; 		docker-php-ext-install -j "$(nproc)" 		gd 		opcache 		pdo_mysql 		pdo_pgsql 		zip 	; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	ldd "$(php -r 'echo ini_get("extension_dir");')"/*.so 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query -S 		| cut -d: -f1 		| sort -u 		| xargs -rt apt-mark manual; 		apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 Aug 2024 09:27:22 GMT
RUN { 		echo 'opcache.memory_consumption=128'; 		echo 'opcache.interned_strings_buffer=8'; 		echo 'opcache.max_accelerated_files=4000'; 		echo 'opcache.revalidate_freq=60'; 	} > /usr/local/etc/php/conf.d/opcache-recommended.ini # buildkit
# Thu, 08 Aug 2024 09:27:22 GMT
COPY /usr/bin/composer /usr/local/bin/ # buildkit
# Thu, 08 Aug 2024 09:27:22 GMT
ENV DRUPAL_VERSION=11.0.1
# Thu, 08 Aug 2024 09:27:22 GMT
ENV COMPOSER_ALLOW_SUPERUSER=1
# Thu, 08 Aug 2024 09:27:22 GMT
WORKDIR /opt/drupal
# Thu, 08 Aug 2024 09:27:22 GMT
RUN set -eux; 	export COMPOSER_HOME="$(mktemp -d)"; 	composer create-project --no-interaction "drupal/recommended-project:$DRUPAL_VERSION" ./; 	composer check-platform-reqs; 	chown -R www-data:www-data web/sites web/modules web/themes; 	rmdir /var/www/html; 	ln -sf /opt/drupal/web /var/www/html; 	rm -rf "$COMPOSER_HOME" # buildkit
# Thu, 08 Aug 2024 09:27:22 GMT
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
	-	`sha256:a7c84ccfffd76a0e7beed19acb002b0d2d2043e5b2e7ed38528a885c950655a4`  
		Last Modified: Tue, 13 Aug 2024 03:17:46 GMT  
		Size: 12.8 MB (12802555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37cb616d30c2680dd1655af2fe6a8c0476acd184af059d6958fdfc2143227fa`  
		Last Modified: Tue, 13 Aug 2024 03:17:45 GMT  
		Size: 492.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ad74f454c8c82fd6f45eefd3910270e3ba29f4b0ef65685a38769049747a839`  
		Last Modified: Tue, 13 Aug 2024 03:18:17 GMT  
		Size: 26.0 MB (25955350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa339e04a93ee97b264d28638fe8cf657d6063b9a07766ae686186d4512c9cd2`  
		Last Modified: Tue, 13 Aug 2024 03:18:13 GMT  
		Size: 2.5 KB (2450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d42401fe2a0503c27f2746ed4265109d3f31144cf9004f26a767851480d3340`  
		Last Modified: Tue, 13 Aug 2024 03:18:13 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbf3b64a270b5ea8017de96460b5671c5335d14a2d02fed9a18242940af26875`  
		Last Modified: Tue, 13 Aug 2024 03:18:14 GMT  
		Size: 9.2 KB (9179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1c27100aa9268702ad85c76b2adfc58e81d95f2cfc5353f0b31dd993b161227`  
		Last Modified: Tue, 13 Aug 2024 10:45:56 GMT  
		Size: 1.5 MB (1497360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0a044c5545ed470061887cd1235aa2bb839adaf7da0601b4477e97b88f998f9`  
		Last Modified: Tue, 13 Aug 2024 10:45:56 GMT  
		Size: 315.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e6a7c348d0f52efde1abf6c8c715e4ff427f6916357557f28249ea55ad9213`  
		Last Modified: Tue, 13 Aug 2024 10:45:56 GMT  
		Size: 726.3 KB (726347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2fa59d56a9e60a8fca48a9e456e9532c4330a41435fc1c6d9b52c7b6c54fda`  
		Last Modified: Tue, 13 Aug 2024 10:45:56 GMT  
		Size: 115.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0621afabefed781f0f47b40cc63cefd469ab03ef96c882edb8cd11f0247b2970`  
		Last Modified: Tue, 13 Aug 2024 10:45:57 GMT  
		Size: 19.2 MB (19223643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `drupal:fpm-bullseye` - unknown; unknown

```console
$ docker pull drupal@sha256:54fc7deeb969d9b536dcb711d7ca63aa29d3dae63a0bfc406ce9fffb7a5efba8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6345446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:140af2234d2fc7ebbe96c9deac42f0af15dfd46fdeb89f1bf4074d70ed7f563d`

```dockerfile
```

-	Layers:
	-	`sha256:fb7380eb5b6a9ca3ef788dce31e560fba669105c8e874bca724cb9aa593b0f8b`  
		Last Modified: Tue, 13 Aug 2024 10:45:54 GMT  
		Size: 6.3 MB (6311254 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25bb6eaca681a34e3e615d021462e35502c866c326550db66d11bde0a522f5f0`  
		Last Modified: Tue, 13 Aug 2024 10:45:54 GMT  
		Size: 34.2 KB (34192 bytes)  
		MIME: application/vnd.in-toto+json
